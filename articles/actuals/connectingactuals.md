---
title: 交易连接 - 链接不同交易类型的实际值
description: 本文说明如何使用交易连接来链接不同类型的实际值，以帮助跟踪利润率、记帐积压以及记帐与未记帐收入计算。
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926075"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>交易连接 - 链接不同交易类型的实际值

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

随着时间、支出或材料使用在其生命周期中从报价单或售前阶段移动到合同阶段、审批和/或撤消、开票以及可能的贷记或纠正开票，将创建交易连接记录来链接不同类型的实际值。

以下示例显示对 Project Operations 项目生命周期中的时间条目的典型处理。

> ![在 Project Operations 中处理时间条目。](media/basic-guide-17.png)

Project Operations 项目生命周期中时间条目的处理采用以下步骤： 

1. 提交时间条目将创建两个日记帐行：一个针对成本，一个针对未记帐销售额。 
2. 最终批准时间条目将创建两个实际值：一个针对成本，一个针对未记帐销售额。 这 2 个实际值使用交易连接来链接。
3. 当用户创建项目发票时，将使用未记帐实际销售额的数据创建发票明细交易。
4. 确认发票时，将创建两个新实际值：未记帐销售额冲销和已记帐实际销售额。 未记帐销售冲销和原始未记帐实际销售额使用冲销交易连接来连接。 已记帐销售额与原始的未记帐实际销售额也会连接，以显示曾经的积压或在制品 (WIP) 收入与现在的已记帐收入之间的链接。   

处理工作流中的每个事件都会触发在 **交易连接** 表中创建记录。 这有助于在跨时间条目、日记帐行、实际值和发票明细详细信息创建的记录之间建立关系跟踪。

下表显示上一个工作流的 **交易连接** 实体中的记录。

|事件                   |交易 1                 |交易 1 角色 |交易 1 类型       |交易 2          |交易 2 角色 |交易 2 类型 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|时间条目提交   |日记帐行（销售额）GUID     |未记帐销售额 |msdyn_journalline            |日记帐行（成本）GUID     |成本            |msdyn_journalline  |
|时间审批           |未记帐实际值（销售额）GUID  |未记帐销售额 |msdyn_actual                 |实际成本（成本）GUID       |成本            |msdyn_actual       |
|发票创建        |发票明细详细信息 GUID      |已记帐销售额   |msdyn_invoicelinetransaction |未记帐实际销售额 GUID   |未记帐销售额  |msdyn_actual       |
|发票确认    |冲销实际值 GUID         |冲销      |msdyn_actual                 |原始未记帐销售额 GUID |原始        |msdyn_actual       |
|                        |已记帐销售额 GUID             |已记帐销售额   |msdyn_actual                 |未记帐实际销售额 GUID   |未记帐销售额  |msdyn_actual       |
|草稿发票更正 |发票明细交易 GUID|替换      |msdyn_invoicelinetransaction |已记帐销售额 GUID            |原始        |msdyn_actual       |
|确认发票更正|已记帐销售额冲销 GUID  |冲销      |msdyn_actual                 |已记帐销售额 GUID            |原始        |msdyn_actual       |
|                        |新未记帐销售额 GUID |替换            |msdyn_actual                 |已记帐销售额 GUID            |原始        |msdyn_actual       |


下图使用 Project Operations 中的时间条目示例显示了在各个事件中不同类型的实际值之间创建的链接。

> ![不同类型的实际值在 Project Operations 中如何相互链接。](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
