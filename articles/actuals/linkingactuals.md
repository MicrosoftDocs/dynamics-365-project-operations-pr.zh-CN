---
title: 交易起源 - 将实际值链接到源
description: 本文解释了如何使用交易起源概念将实际值链接到原始源记录，如时间条目、支出条目或材料使用日志。
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921291"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>交易起源 - 将实际值链接到源

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

创建交易起源记录来将实际值链接到源，如时间条目、支出条目、材料使用日志和项目发票。

以下示例显示对 Project Operations 项目生命周期中的时间条目的典型处理。

> ![在 Project Operations 中处理时间条目。](media/basic-guide-17.png)
 
1. 提交时间条目将创建两个日记帐行：一个针对成本，一个针对未记帐销售额。
2. 最终批准时间条目将创建两个实际值：一个针对成本，一个针对未记帐销售额。
3. 当用户创建项目发票时，将使用未记帐实际销售额的数据创建发票明细交易。
4. 确认发票时，将创建两个新实际值：未记帐销售额冲销和已记帐实际销售额。

此处理工作流中的每个事件都会在交易起源实体中触发记录的创建，以帮助创建对在时间条目、日记帐行、实际值和发票明细详细信息中创建的这些记录之间的关系的跟踪。

下表显示上一个工作流的交易来源实体中的记录。

| 事件                        | 来源                   | 来源类型                       | 交易                       | 交易类型         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| 时间条目提交        | 时间条目记录 GUID   | 时间条目                        | 日记帐行记录 GUID（成本）   | 日记帐行             |
| 时间条目记录 GUID       | 时间条目               | 日记帐行记录 GUID（销售额）  | 日记帐行                      |                          |
| 时间审批                | 日记帐行记录 GUID | 日记帐行                      | 未记帐销售额记录 GUID        | 实际值                   |
| 时间条目记录 GUID       | 时间条目               | 未记帐销售额记录 GUID        | 实际值                            |                          |
| 日记帐行记录 GUID     | 日记帐行             | 实际成本记录 GUID           | 实际值                            |                          |
| 时间条目记录 GUID       | 时间条目               | 实际成本记录 GUID           | 实际值                            |                          |
| 发票创建             | 时间条目记录 GUID   | 时间条目                        | 发票明细交易 GUID     | 发票明细交易 |
| 日记帐行记录 GUID     | 日记帐行             | 发票明细交易 GUID     | 发票明细交易          |                          |
| 发票确认         | 发票明细 GUID        | 发票行                      | 已记帐销售额记录 GUID          | 实际值                   |
| 发票 GUID                 | 发票                  | 已记帐销售额记录 GUID          | 实际值                            |                          |
| 发票明细详细信息 GUID     | 发票明细详细信息      | 已记帐销售额记录 GUID          | 实际值                            |                          |
| 时间条目记录 GUID       | 时间条目               | 已记帐销售额记录 GUID          | 实际值                            |                          |
| 日记帐行记录 GUID     | 日记帐行             | 已记帐销售额记录 GUID          | 实际值                            |                          |
| 时间条目记录 GUID       | 时间条目               | 未记帐销售额冲销 GUID      | 实际值                            |                          |
| 日记帐行记录 GUID     | 日记帐行             | 未记帐销售额冲销 GUID      | 实际值                            |                          |
| 草稿发票更正     | 旧 ILD GUID             | 发票明细交易          | 更正 ILD GUID               | 发票明细交易 |
| 旧 IL GUID                  | 发票行             | 更正 ILD GUID               | 发票明细交易          |                          |
| 旧发票 GUID             | 发票                  | 更正 ILD GUID               | 发票明细交易          |                          |
| 时间条目记录 GUID       | 时间条目               | 更正 ILD GUID               | 发票明细交易          |                          |
| 日记帐行记录 GUID     | 日记帐行             | 更正 ILD GUID               | 发票明细交易          |                          |
| 已确认发票更正 | 旧 ILD GUID             | 发票明细交易          | 保留的已记帐实际销售额 GUID | 实际值                   |
| 旧 IL GUID                  | 发票行             | 保留的已记帐实际销售额 GUID | 实际值                            |                          |
| 旧发票 GUID             | 发票                  | 保留的已记帐实际销售额 GUID | 实际值                            |                          |
| 时间条目记录 GUID       | 时间条目               | 保留的已记帐实际销售额 GUID | 实际值                            |                          |
| 日记帐行记录 GUID     | 日记帐行             | 保留的已记帐实际销售额 GUID | 实际值                            |                          |
| 旧 ILD GUID                 | 发票明细交易 | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 旧 IL GUID                  | 发票行             | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 旧发票 GUID             | 发票                  | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 时间条目记录 GUID       | 时间条目               | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 日记帐行记录 GUID     | 日记帐行             | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 更正 ILD GUID          | 发票明细交易 | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 更正 IL GUID           | 发票行             | 新的未记帐实际销售额 GUID    | 实际值                            |                          |
| 更正发票 GUID      | 账单                  | 新的未记帐实际销售额 GUID    | 实际                            |                          |


下图使用 Project Operations 中的时间条目示例显示了在各个事件中的实际值及其源之间创建的链接。

> ![实际值如何链接到 Project Operations 中的源记录。](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
