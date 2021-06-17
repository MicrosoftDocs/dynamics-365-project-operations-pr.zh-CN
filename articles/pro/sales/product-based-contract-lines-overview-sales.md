---
title: 基于产品的合同子项概述 - 精简
description: 此主题介绍基于产品的合同子项。
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994530"
---
# <a name="product-based-contract-lines-overview---lite"></a>基于产品的合同子项概述 - 精简

_**适用于：** 精简部署 - 估价交易开票_

可在 Dynamics 365 Project Operations 中创建基于产品的合同子项。 基于产品的合同子项可以是手动创建的明细，也可以是产品目录中的项。

## <a name="product-catalog"></a>产品目录

产品目录中的产品具有默认计价单位和计价单位组。 如果多个产品共享同一组属性，可以创建也具有这些属性的产品系列。 同一个产品系列中的所有产品继承同一组属性。

例如，一家公司销售不同类型软件的订阅许可证。 所有订阅软件都有下面的两个属性：

- 用户数
- 订阅持续时间（以月为单位）

若要维护此类目录，请创建一个名为 **订阅软件** 的产品系列。 将属性、**用户数** 和 **订阅持续时间** 添加到产品系列中。 然后，将各个产品添加到 **订阅软件** 产品系列中。

## <a name="add-product-catalog-items-to-a-project-contract"></a>向项目合同添加产品目录项

项目合同针对两种明细划分部分：基于项目和基于产品。 基于产品的明细在合同中包含产品价目表中的所有产品和计价单位。 可以添加不属于合同的产品价目表的产品。

您可以从其他价目表中选择产品，也可以直接从产品目录中选择产品。 直接从产品目录选择产品时，该产品的默认价目表将用于产品的售价。 如果未设置默认价目表，则该价格设置为 0（零）。

如果合同子项基于产品目录，则可直接在合同子项中替代售价。 合同子项具有 **定价** 字段，此字段有两个值：

- **替代定价**
- **使用默认值**

如果将 **定价** 字段设置为 **替代定价**，将不设置默认价格。 为合同子项中的产品输入价格。 如果将此字段设置为 **使用默认值**，将使用默认售价，并且无法编辑此字段。

安装 Project Operations 之后，将在合同中基于产品的明细内输入默认售价。 **定价** 字段将设置为 **替代定价**，以便您编辑合同子项中的默认价格。 这是对 Dynamics 365 Sales 中基于产品的明细行为的 Project Operations 特定替代。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]