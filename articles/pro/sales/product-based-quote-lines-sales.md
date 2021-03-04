---
title: 基于产品的报价单明细概述 - 精简
description: 此主题提供有关处理基于产品的报价单明细的信息。
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178177"
---
# <a name="product-based-quote-lines-overview---lite"></a>基于产品的报价单明细概述 - 精简

_**适用于：** 精简部署 - 估价交易开票_

可在 Dynamics 365 Project Operations 中创建基于产品的报价单明细。 基于产品的报价单明细可以手动添加，也可以是产品目录中的项。

## <a name="product-catalog"></a>产品目录

产品目录中的每个产品都有默认计价单位和计价单位组。 如果多个产品共享同一组属性，可以创建共享这些属性的产品系列。 

例如，一家公司销售不同类型软件的订阅许可证。 所有订阅软件都有下面的两个属性：

- 用户数
- 订阅持续时间（以月为单位）

要维护这类目录，创建一个名称为 **订阅软件** 的产品系列，然后将用户数目和订阅持续时间添加为属性。 接下来，您可以将各个产品添加到 **订阅软件** 产品系列中。

## <a name="add-product-catalog-items-to-a-project-quote"></a>向项目报价单添加产品目录项

**项目报价单** 和 **项目合同** 页有两个部分：基于项目的明细和基于产品的明细。 对于基于产品的明细，报价单明细或项目合同子项的下拉列表中包含产品价目表中的所有产品和单位。 您还可以添加不属于产品价目表的产品。

此外，还可以从其他价目表或直接从产品目录选择产品。 直接从产品目录选择产品时，产品的默认价目表用于获取产品的销售价。 如果未设置默认价目表，则该价格设置为零 (0)。

当报价单明细基于产品目录时，可直接在报价单明细中替代售价。 有两个可用值的 **定价** 字段中的报价单明细：

- **替代定价**
- **系统价格**

如果选择 **替代定价**，将不设置默认价格。 而是必须为报价单中的产品输入价格。 如果您选择 **系统价格**，将使用默认售价，此字段将被锁定，无法进行编辑。

将在报价单的基于产品的明细中输入默认售价。 然后将 **定价** 字段设置为 **替代定价**，以便您编辑报价单明细中的默认价格。 这是对 Dynamics 365 Sales 中基于产品的明细行为的 Project Operations 特定替代。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]