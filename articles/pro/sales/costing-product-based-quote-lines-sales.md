---
title: 基于产品的报价单明细成本核算
description: 此主题提供有关将成本费应用于基于产品的报价单明细的信息。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003440"
---
# <a name="costing-product-based-quote-lines"></a>基于产品的报价单明细成本核算

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


Dynamics 365 Project Operations 中基于产品的报价单行也具有 **成本费** 字段。 此字段用于在报价单明细中跟踪产品的成本费，并用于下游利润率的计算。

为目录产品创建基于产品的报价单明细时，基于产品的报价单明细的成本默认为产品目录中 **标准成本** 字段的值。 产品目录中的“标准成本”字段以组织的基础货币设置。 基于产品的报价单明细上的默认单位成本将转换为报价单上的销售货币。

## <a name="unit-cost-on-a-product-based-quote-line"></a>基于产品的报价单明细中的单位成本

在基于产品的报价单明细中提供单位成本的目的是为了让每个销售的产品显示不同的成本。 这不是一个典型场景，但有时供应商可能根据最终销售的客户为产品成本提供折扣。

例如：

Fabrikam Robotics 正在 A Datum Corporation 的装配线上安装机械臂。 Fabrikam 提供安装服务，但机械臂需要从 Trey 机器人公司购买。 如果在 A Datum Corporation 安装机械臂为 Trey 的机械臂开辟了一个新的行业类别，那么 Trey 可能为这笔交易给予 Fabrikam 特殊折扣。

在这种情况下，Fabrikam 将为机械臂创建基于产品的报价单明细，并为此报价单输入特殊的每单位成本。 此成本与 Trey 机械臂的标准成本不同。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]