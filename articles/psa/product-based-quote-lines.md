---
title: 基于产品的报价单明细
description: 此主题介绍基于产品的报价单明细。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998490"
---
# <a name="product-based-quote-lines"></a>基于产品的报价单明细

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


可在 Dynamics 365 Project Service Automation 中创建基于产品的报价单明细。 基于产品的报价单明细可以是“目录外”明细，也可以是产品目录中的项。

## <a name="product-catalog"></a>产品目录

Dynamics 365 产品目录中的产品具有默认计价单位和计价单位组。 如果多个产品共享同一组属性，可以创建也具有这些属性的产品系列。 同一个产品系列中的所有产品继承同一组属性。

例如，一家公司销售大量软件的订阅许可证。 所有订阅软件都有下面的两个属性：

- 用户数目 
- 订阅持续时间（以月为单位）

维护这种目录的一个好办法是创建一个名称为 **订阅软件** 的产品系列，并且该产品系列的属性为 **用户数目** 和 **订阅持续时间**。 然后可以向 **订阅软件** 产品系列添加单个产品，如 **Dynamics 365 Sales** 或 **Dynamics 365 Field Service**。

## <a name="adding-product-catalog-items-to-a-project-quote"></a>向项目报价单添加产品目录项

项目报价单和项目合同页有两种明细的部分：基于项目的明细和基于产品的明细。 对于基于产品的明细，Dynamics 365 用于将产品目录中的项添加到报价单。 报价单明细或项目合同子项的下拉列表中包含附加到该报价单或项目合同的产品价目表中的所有产品和单位。 也可以添加不属于报价单产品价目表的产品。

此外，还可以从其他价目表选择产品，或者直接从产品目录选择产品。 直接从产品目录选择产品时，产品的默认价目表用于获取产品的销售价。 如果未设置默认价目表，则该价格设置为 0（零）。

如果报价单明细基于产品目录，则可直接在报价单明细中替代销售价。 请注意，Dynamics 365 中的报价单明细有一个 **定价** 字段。 有两个值：

- 替代定价  
- 使用默认值

如果将此字段设置为 **替代定价**，Dynamics 365 将不设置默认价格。 必须为报价单中的产品输入价格。 如果将此字段设置为 **使用默认值**，Dynamics 365 将使用默认销售价，并锁定字段，以免被编辑。

安装 PSA 之后，将在报价单中基于产品的明细内输入默认销售价。 然后将 **定价** 字段设置为 **替代定价**，以便您编辑报价单明细中的默认价格。

> ![设置替代定价](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>产品的数量因子

PSA 使用数量因子为基于订阅的产品的销售提供支持。 对于基于订阅的产品，报价单或项目合同子项中的数量表示为用户的月数。

通常，订阅软件的价格以每用户每月价格的形式存储在目录中。 但是，可改用其他时间描述。 销售阶段中，报价单明细中的价格通常为与 IT 销售代表协商并达成折扣的每用户每月价格。 每笔交易的用户数量和订阅月数不同。 用于计算报价单明细金额的数量是用户数与订阅月数的乘积。

为了支持这种销售，PSA 引入了数量因子这一概念。 在 Dynamics 365 中，数量因子依赖于产品属性。 为产品配置特定属性时，PSA 将请您把这些属性中的一小部分或全部标记为数量因子。

PSA 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。 将为其配置了数量因子的产品添加到报价单明细时，报价单明细中的 **数量** 字段将成为只读字段。 为充当数量因子的产品属性输入值之后，PSA 将计算报价单明细的数量。

例如，Dynamics 365 可能具有以下属性： 

- **用户数目** - 用户的数量 
- **月数** - 订阅的月数
- **产品 SKU** 

可以通过编辑产品明细的属性，将 **用户数目** 和 **月数** 属性标记为数量因子。 

> ![将“用户数目”和“月数”标记为数量因子](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]