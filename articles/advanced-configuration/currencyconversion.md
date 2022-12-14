---
title: 设置货币换算以根据成本费率计算销售价格
description: 本文介绍如何配置根据成本交易生成销售交易时将在 Microsoft Dynamics 365 Project Operations 中使用的货币换算行为。
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816659"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>设置货币换算以根据成本费率计算销售价格

_**适用于：** 面向资源/非库存场景的 Project Operations_

在 Microsoft Dynamics 365 Project Operations 中，费用类别的销售价格可以设置为数值，也可以设置为根据产生的成本进行计算。

将它们设置为根据发生的成本计算时，以下选项可用：

- 按成本
- 成本加价百分比

在所发生支出费用的货币与项目合同的销售货币不同的情况下，需要进行货币换算以根据成本计算销售价格。

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>使用本地 Dataverse 汇率的货币换算行为

默认情况下，Project Operations 使用存储在 Dataverse 内的“货币”表中的货币汇率。 要将 Project Operations 配置为使用本地汇率根据成本计算销售价格，请执行以下步骤。

1. 转到 **Project Operations \> 设置 \> 参数**。
1. 打开 **项目参数** 详细信息页。
1. 将 **货币换算逻辑** 字段设置为空值。

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>使用财务和运营应用中的汇率的货币换算行为

Dataverse 中本地可用的“货币”表中的汇率没有时效性。 因此，它们可能并不总是按照您根据成本费率计算销售价格的要求进行缩放。

您可以使用财务和运营环境中的汇率，根据以成本货币为单位的成本费率计算以销售货币为单位的销售价格。 若要配置此货币换算行为，请执行以下步骤。

1. 在 **项目参数** 页上，添加 **货币换算逻辑** 字段。 然后保存并发布自定义。
1. 转到 **Project Operations \> 设置 \> 参数**。
1. 打开 **项目参数** 详细信息页。 
1. 将 **货币换算行为** 字段设置为 **通过恢复默认完成扩展**。
1. 向 **双重写入应用用户** 安全角色授予对下表的 **全局读取** 权限：

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. 在您的财务和运营环境中，使用初始同步运行以下双重写入映射：

    - 汇率类型 (msdyn\_exchangeratetypes)
    - 汇率币种对 (msdyn\_currencyexchangeratepairs)
    - CDS 汇率 (msdyn\_currencyexchangerates)

完成这些更改后，双重写入将使财务和运营环境的汇率在 Dataverse 中可用。 然后，Project Operations 将使用这些汇率将成本费率转换为合同的销售货币。

> [!NOTE]
> 此货币换算行为仅适用于根据成本费率计算销售价格。 它不会用于基础货币值常规计算。 基础货币值将始终使用本地 Dataverse 汇率，与是否完成此过程无关。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
