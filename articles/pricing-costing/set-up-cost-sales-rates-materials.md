---
title: 设置材料的成本和销售费率
description: 本文提供有关如何设置项目所用材料的成本和销售费率的信息。
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911769"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>设置材料的成本和销售费率

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

您可以在 Dynamics 365 Project Operations 中设置产品的成本和销售价格。 产品的成本和销售价格只能以一种货币列出，该货币必须是价目表标题上的货币。

若要设置产品的成本和销售费率，请完成以下步骤。 

1. 转到 **销售** > **客户** > **价目表** 并选择 **新建** 以创建新的价目表。 
2. 在子网格菜单上的 **价目表项** 中，选择 **新建价目表项**。 
3. 在 **快速创建** 页上，输入创建新价格所针对的产品和单位。

有关如何为目录项定义价格的详细信息，请参阅[使用价目表和价目表项定义产品定价](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products)和[货币和定价的小数精度](/dynamics365/sales/decimal-precision-currency-pricing)。
> [!NOTE]
> Dynamics 365 Project Operations 不能为 Dynamics 365 Sales 这样的产品支持所有定价方式。 为项目中使用的产品支持的唯一定价方式是 *货币金额*。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
