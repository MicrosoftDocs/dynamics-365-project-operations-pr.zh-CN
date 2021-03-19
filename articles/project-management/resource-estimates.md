---
title: 资源预估
description: 此主题提供有关在 Project Operations 中如何计算资源预估的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286507"
---
# <a name="resource-estimates"></a>资源预估

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

资源预估来自工作分解结构中定义的分时段工作量以及适用的定价维度。 通常，计算方式是 **每个角色的费率/小时 x 时数**。 每个资源的分时段工作量存储在资源分配记录中。 定价存储在预定义的价目表中。 单位转换基于适用的价目表应用。

![资源预估](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>默认成本费和成本货币

成本费默认为部门中的值。

## <a name="default-bill-rate-and-sales-currency"></a>默认帐单费率和销售货币

每笔交易应用一次售价。 销售价目表的默认层次结构如下：

1. 组织
2. 客户
3. 报价单/合同


[!INCLUDE[footer-include](../includes/footer-banner.md)]