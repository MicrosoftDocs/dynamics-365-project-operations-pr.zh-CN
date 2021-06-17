---
title: 管理基于产品的合同子项的复杂单位 - 精简
description: 此主题提供有关支持基于订阅的产品的销售的信息。
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003170"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>管理基于产品的合同子项的复杂单位 - 精简

_**适用于：** 精简部署 - 估价交易开票_

Dynamics 365 Project Operations 使用数量因子为基于订阅的产品的销售提供支持。 对于基于订阅的产品，合同或项目合同子项中的数量表示为用户的月数。

订阅软件的价格以每用户每月价格的形式存储在目录中。 在销售流程中，合同子项中的价格通常为与销售代表协商并达成折扣的每用户每月价格。 每笔交易的用户数量和订阅月数不同。 用于计算合同子项金额的数量是用户数与订阅月数的乘积。

为了支持这种销售，Project Operations 支持 *数量因子* 概念。 数量因子依赖于产品属性。 为产品配置特定属性时，您可以将这些属性中的一小部分或全部标记为数量因子。

Project Operations 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。 在将具有配置的数量因子的产品添加到合同子项时，**数量** 字段将变为只读。 为充当数量因子的产品属性输入值之后，Project Operations 将计算合同子项的数量。

例如，Dynamics 365 Sales 可能具有以下属性：

- **用户数**：用户的数量。
- **月数**：订阅的月数。
- **产品 SKU**：产品的库存单位 (SKU)。

可以通过编辑产品明细的属性，将 **用户数** 和 **月数** 属性标记为数量因子。

若要从产品属性创建数量因子，请完成以下步骤。

1. 在 **Project Operations** 中，选择 **销售-产品**。
2. 打开需要设置数量因子的产品。 确保该产品已设置属性。
3. 在 **项目信息** 页面上，选择 **数量因子** 选项卡。
4. 在子网格中，选择 **+ 新建字段计算**。
5. 输入 **数量因子** 的名称，然后选择要映射到字段计算的属性值。
6. 保存并关闭窗体。
7. 对将共同构成基于产品的合同子项的数量的所有属性重复步骤 2-6。

数量因子设置后，当用户为此产品创建合同子项时，合同子项的数量将锁定。 然后，会将此数量作为该合同子项的属性值的产品进行计算。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]