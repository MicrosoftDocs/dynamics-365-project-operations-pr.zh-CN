---
title: 业务交易
description: 本文提供有关业务交易的信息。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 07002890e0474dbdaf979d9dcdf064e9c382a0f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926995"
---
# <a name="business-transactions"></a>业务交易

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 中，*业务交易* 是不能通过任何实体表示的抽象概念。 但是实体中的某些常用字段或流程应该采用业务交易概念。 以下实体使用此抽象概念：

- 报价单明细详细信息
- 合同子项详细信息
- 估算明细
- 日记帐行
- 实际

在这些实体中，报价单明细详细信息、合同子项详细信息和估算明细映射到项目生命周期中的估算阶段。 日记帐行和实际值实体映射到项目生命周期中的执行阶段。

PSA 将这五种实体中的记录视为业务交易。 唯一区别是实体中映射到估算阶段的记录被视为财务预测，而实体中映射到执行阶段的记录则被视为已发生的财务结果。

有关详细信息，请参阅[估算](estimates.md)和[实际值](actuals.md)。

## <a name="concepts-that-are-unique-to-business-transactions"></a>业务交易独有的概念
以下概念专属于业务交易：

- 交易类型
- 交易分类
- 交易来源
- 交易连接

### <a name="transaction-type"></a>交易类型

交易类型代表对项目的财务影响的时间安排和上下文。 其在 PSA 中通过具有以下支持值的选项集表示：
- 成本
- 项目合同
- 未记帐销售额
- 已记帐销售额
- 组织间销售额
- 资源单位成本

### <a name="transaction-class"></a>交易分类

交易分类代表项目中出现的不同类型的成本。 其在 PSA 中通过具有以下支持值的选项集表示：

- Time
- 费用
- 材料
- 费用
- 里程碑
- 税款

在 PSA 中，**里程碑** 值通常由固定价格记帐的业务逻辑使用。

### <a name="transaction-origin"></a>交易来源

交易来源是存储每个业务交易的来源的实体。 在执行项目的过程中，每个业务交易都将引起其他业务交易，而后者也将引起另一个业务交易，依此类推。 交易来源实体旨在存储有关每个交易的来源的数据，以帮助报告和跟踪。 

### <a name="transaction-connection"></a>交易连接

交易连接是一种实体，用于存储两个相似业务交易（如陈和关联的实际销售额）之间的关系，或记帐活动（如确认发票或更正发票）触发的交易冲销。

交易来源和交易连接实体可共同帮助您保持跟踪业务交易与导致创建特定业务交易的操作之间的关系。

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>示例：交易记录如何与交易连接配合工作

以下示例显示对 PSA 项目生命周期中的时间条目的典型处理。

> ![处理 Project Service 生命周期中的时间条目。](media/basic-guide-17.png)
 
1. 提交时间条目将导致创建两个日记帐行：一个针对成本，一个针对未记帐销售额。
2. 最终批准时间条目将导致创建两个实际值：一个针对成本，一个针对未记帐销售额。
3. 当用户创建项目发票时，将使用未记帐实际销售额的数据创建发票明细交易。 
4. 确认发票时，将创建两个新实际值：未记帐销售额冲销和已记帐实际销售额。

这些事件中的每一个都会在交易来源和交易连接实体中触发记录的创建，以帮助创建对在时间条目、日记帐行、实际值和发票明细详细信息中创建的这些记录之间的关系的跟踪。

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
| 更正发票 GUID      | 发票                  | 新的未记帐实际销售额 GUID    | 实际值                            |                          |

下表显示上一个工作流的交易连接实体中的记录。

| 事件                          | 交易 1                 | 交易 1 角色 | 交易 1 类型           | 交易 2                | 交易 2 角色 | 交易 2 类型 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| 时间条目提交          | 日记帐行（销售额）GUID     | 未记帐销售额     | msdyn_journalline            | 日记帐行（成本）GUID     | 成本               | msdyn_journalline  |
| 时间审批                  | 未记帐实际值（销售额）GUID  | 未记帐销售额     | msdyn_actual                 | 实际成本（成本）GUID       | 成本               | msdyn_actual       |
| 发票创建               | 发票明细详细信息 GUID      | 已记帐销售额       | msdyn_invoicelinetransaction | 未记帐实际销售额 GUID   | 未记帐销售额     | msdyn_actual       |
| 发票确认           | 冲销实际值 GUID         | 冲销          | msdyn_actual                 | 原始未记帐销售额 GUID | 原始           | msdyn_actual       |
| 已记帐销售额 GUID              | 已记帐销售额                  | msdyn_actual       | 未记帐实际销售额 GUID   | 未记帐销售额               | msdyn_actual       |                    |
| 草稿发票更正       | 发票明细交易 GUID | 替换          | msdyn_invoicelinetransaction | 已记帐销售额 GUID            | 原始           | msdyn_actual       |
| 确认发票更正     | 已记帐销售额冲销 GUID    | 冲销          | msdyn_actual                 | 已记帐销售额 GUID            | 原始           | msdyn_actual       |
| 新的未记帐实际销售额 GUID | 替换                     | msdyn_actual       | 已记帐销售额 GUID            | 原始                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
