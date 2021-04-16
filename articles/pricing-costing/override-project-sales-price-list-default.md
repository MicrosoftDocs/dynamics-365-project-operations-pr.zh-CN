---
title: 替代项目销售价目表
description: 此主题提供有关创建自定义销售价目表的信息。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275527"
---
# <a name="override-project-sales-price-lists"></a>替代项目销售价目表

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

## <a name="customer-specific-project-price-lists"></a>特定于客户的项目价目表

在 Dynamics 365 Project Operations 中，特定于客户的价格协议可以设置为客户记录中的项目价目表。

若要设置特定于客户的项目价目表，在 **销售** 区域，导航到客户记录。

1. 打开 **客户** 列表页。
2. 找到并双击客户记录打开 **客户** 详细信息页。
3. 在 **项目价目表** 选项卡上，选择 **+ 新建项目价目表**。
4. 在 **新建项目价目表** 页上，从下拉列表中选择一个价目表。 仅包含将上下文设置为 **销售** 且其货币与客户货币匹配的价目表。
5. 为关联命名，然后选择 **保存**。 特定于客户的项目价目表已创建。 此价目表将用于设定为此客户创建的报价单或项目合同的创建日期在价目表有效期内的项目报价单或合同上的默认项目价格。

## <a name="custom-pricing-on-project-quotes"></a>项目报价单上的自定义定价

在项目报价单上，您可以使用从默认值来自客户或项目参数的默认标准价目表开始的项目定价。

当您需要为特定报价单上的项目相关工作进行自定义定价时，可以从与项目价目表关联的实体获取自定义定价。

完成以下步骤，设置特定于报价单的项目定价。

1. 打开项目报价单，选择 **项目价目表** 选项卡。
2. 在子网格中，选择 **创建自定义定价**。

附加到报价单的所有项目价目表都将复制到新价目表中。 新价目表的名称将反映报价单的名称，其中包含创建这些价目表的日期时间戳。

您可以使用其中的每个价目表，并可以对人工（角色价格）和支出（类别价格）价格进行更新。 这些价格仅适用于此项目报价单。

## <a name="price-lists-on-a-project-contract"></a>项目合同上的价目表

在项目合同上，项目定价始终默认为具有合同名称并且创建日期时间戳附加到名称中的自定义价目表。 无论是在报价单赢单时创建合同，还是从头创建合同，都是如此。 如果需要，您可以删除与自定义价目表的这一关联，然后将标准价目表与项目合同关联。

当您将标准价目表与报价单或合同上的项目价目表关联时，对价目表中的价格所作的任何更改都将影响使用该价目表的所有报价单和合同。


[!INCLUDE[footer-include](../includes/footer-banner.md)]