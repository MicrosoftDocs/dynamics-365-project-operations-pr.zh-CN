---
title: 多货币方案（版本 3.x）
description: 此主题介绍多货币方案。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 33e44297dc80801c3e4416cd9fc3bedae5f3c4ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291698"
---
# <a name="multiple-currency-scenarios"></a>多货币方案

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 有两种货币概念：

- **交易货币** - 进行交易时使用的货币。 
- **基础货币** - Dynamics 365 实例的货币。 此货币是在设置 Dynamics 365 实例时设置的。 不能更改。

例如，Contoso US 以每件 15 英镑 (GBP) 的价格向英国的一位客户销售了 100 件 T 恤衫。 下表显示订单产品实体中如何记录这笔交易。

| 产品 | 数量 | 单价 | 货币 | 金额 | 汇率 | 单价（基础货币）| 金额（基础货币）|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T 恤杉 | 100      | 15             | GBP      | 1500   | 0.94          | 17.25 美元               | 1,725 美元       |

**货币** 列显示交易货币，这是进行销售时使用的货币。 **汇率** 列显示交易货币与基础货币之间的汇率。 基础货币为美元 (USD)。 此基础货币是在设置 Dynamics 365 实例时设置的。
表中显示，每笔交易同时使用交易货币和基础货币记录。 Dynamics 365 使用货币汇率计算基础货币金额。

## <a name="project-service-automation-extensions"></a>Project Service Automation 扩展

Dynamics 365 Project Service Automation 会影响交易货币，因为业务交易通常有两方面：成本和销售额。

以下实体被视为业务交易：

- 报价单明细详细信息
- 项目合同子项详细信息
- 估算明细
- 日记帐行
- 发票明细详细信息
- 实际值

在这些实体的每一个中，有一个记录表示成本额或销售额。 就像具有 **金额** 字段的任何 Dynamics 365 实体，每个记录中都包含交易货币和基础货币的金额。 

PSA 在以下方面扩展了成本和销售额的交易货币概念：

- 时间交易的成本交易货币始终来自负责或管理项目的部门的货币。 此部门称为合同签订部门。
- 时间和支出交易的销售额交易货币始终来自项目合同的货币。
- 支出的成本交易货币来自创建支出条目时使用的货币。

## <a name="multiple-currency-scenario"></a>多货币方案

此部分介绍英国 Contoso 为日本客户 Fabrikam 交付的项目的示例。 下面介绍此方案是如何设置的：

1. 在 **设置** \> **业务管理** \> **货币** 下设置 GBP 和日元 (JPY)。 
2. 设置名称为 **Fabrikam - 日本** 的客户帐户，并选择 JPY 作为此帐户的货币。
3. 设置名称为 **Contoso 英国** 的部门，并选择 GBP 作为货币。
4. 创建一个项目合同，其中将 **Contoso 英国** 指定为合同签订部门，将 **Fabrikam – 日本** 指定为客户。
5. 根据项目各交易分类的记帐安排（如时间的记帐与支出的记帐）创建项目合同子项。
6. 创建一个项目，其中 **Contoso 英国** 指定为合同签订部门。 将创建此项目并映射到项目合同子项。


在使用报价单明细详细信息、项目合同子项详细信息或计划中的估算明细的估算期间，始终创建两条记录。 一条记录针对成本，另一条记录针对销售额。

- 默认情况下，成本记录中的交易货币设置为项目的合同签订部门的货币。 在此示例中，货币为 GBP。
- 默认情况下，销售额记录中的交易货币设置为项目合同的货币。 在此示例中，货币为 JPY。

使用时间条目或日记帐行为时间创建实际值时，将发生以下行为：

- 默认情况下，成本记录中的交易货币设置为项目的合同签订部门的货币。
- 默认情况下，销售额记录中的交易货币设置为项目合同的货币。

按支出条目或日记帐行为支出创建实际值时，将发生以下行为：

- 可以使用任何货币记录支出金额。 使用 **支出条目** 页或 **日记帐行** 页中的货币选取器选择货币。 默认情况下，成本记录的交易货币设置为支出条目中的货币。 
- 默认情况下，销售额记录的交易货币为项目合同的货币。 为了设置此货币，系统首先将用户输入的货币的交易金额转换为基础货币的金额。 然后将金额转换为项目合同的货币的金额。 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>将使用多种交易货币记录创建项目实际值时的计算汇总。

Dynamics 365 自动处理不同货币的金额汇总。 下面是一个示例。

| 交易分类 | 交易类型| Date   | 资源 | 交易类别 | 数量 | 单价 | 金额      | 汇率 | 基础货币金额 |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | 未记帐销售额   | 6 月 14 日 | 建  |                      | 8 小时    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Time              | 未记帐销售额   | 6 月 15 日 | 建  |                      | 8 小时    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| 费用           | 未记帐销售额   | 6 月 16 日 | 建  | 酒店                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265.95 USD     |
| 费用           | 未记帐销售额   | 6 月 17 日 | 建  | 汽车租赁           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159.57 USD     |

若要计算项目的总未记帐销售值，可以为所有相关未记帐实际销售额的 **金额** 字段创建一个汇总字段。 汇总字段是 Dynamics 365 的一项构造，用于快速创建相关记录的公式。


[!INCLUDE[footer-include](../includes/footer-banner.md)]