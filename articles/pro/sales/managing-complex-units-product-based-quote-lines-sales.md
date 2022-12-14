---
title: 管理基于产品的报价单明细的复杂单位（如每用户、每月）
description: 本文提供有关管理基于产品的报价单明细的复杂单位的信息。
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50151e9a34e8608c98e406a30131c1efc4bf2f11
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825460"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>管理基于产品的报价单明细的复杂单位（如每用户、每月）

_**适用于：** 精简部署 - 估价交易开票_

Dynamics 365 Project Operations 使用数量因子为基于订阅的产品的销售提供支持。 对于基于订阅的产品，报价单或项目合同子项中的数量表示为用户的月数。

通常，订阅软件的价格以每用户每月价格的形式存储在目录中。 销售阶段中，报价单明细中的价格通常为与 IT 销售代表协商并达成折扣的每用户每月价格。 每笔交易的用户数量和订阅月数不同。 用于计算报价单明细的数量是用户数与订阅月数的乘积。

为了支持这种销售，Project Operations 引入了数量因子这一概念。 在 Dynamics 365 中，数量因子依赖于产品属性。 为产品配置特定属性时，Project Operations 会让您将部分或全部属性标记为数量因子。

Project Operations 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。 当您将具有数量因子的产品添加到报价单明细时，**数量** 字段将变为只读。 为充当数量因子的产品属性输入值之后，Project Operations 将计算报价单明细的数量。

例如，Dynamics 365 Sales 可能具有以下属性：

- **用户数**：用户的数量
- **月数**：订阅的月数
- **产品 SKU**

您可以通过编辑产品明细的属性，将 **用户数** 和 **月数** 属性标记为数量因子。

若要从产品属性创建数量因子，请执行以下步骤：

1. 在 Project Operations 的左侧导航窗格中，转到 **销售** > **产品**。
2. 打开需要为其配置数量因子的产品。 确保产品已配置属性。
3. 在产品的 **项目信息** 页上，选择 **数量因子** 选项卡。
4. 在子网格中，选择 **+ 新建字段计算**。
5. 输入数量因子的名称，然后选择要映射到字段计算的属性值。
6. 保存并关闭窗体。 对所有用于计算基于产品的报价单明细的数量的属性重复这些步骤。

在您为产品创建基于产品的报价单明细时，报价单明细的数量将被锁定。 此数量将计算为您为该报价单明细输入的属性值的乘积。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
