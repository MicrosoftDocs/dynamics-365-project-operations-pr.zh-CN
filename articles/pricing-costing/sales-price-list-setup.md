---
title: 设置销售价目表
description: 本文提供有关项目定价的销售价目表的信息。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1892607ac121e23a05cd45bc05d4e23ea84690b4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923039"
---
# <a name="set-up-a-sales-price-list"></a>设置销售价目表

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

对于项目报价单和合同，项目价目表采用的价格替代模式与产品价目表采用的不同。 在基于产品目录的报价单明细中，可以直接替代报价单明细中角色和类别的价格，因为每项报价单明细都正好指向一个目录项。 但是，在基于项目的报价单明细中，不能直接替代报价单明细中的角色和类别的价格。 您可以使用项目价目表来使用两种不同的替代模式。

> [!NOTE]
> 建议您为项目资源和目录项设置单独的价目表，因为在您替代定价时，这两者的行为不同。

对于项目定价，下面的每个实体可以有一个或多个关联的销售价目表：

- 客户（帐户） 
- 商机 
- 报价单 
- 项目合同

这些实体与价目表之间的关联通过项目价目表指示。 可以将一个或多个价目表与客户、商机、报价单和项目合同销售实体关联。

不会在客户记录中自动输入默认项目价目表。 但是，可以手动向客户记录附加项目价目表。 尽管如此，还是仅当与客户之间存在自定义定价协议时，才应手动附加项目价目表。 

如果向销售实体附加项目价目表，将验证以下信息：

- 价目表有 **销售** 上下文。 
- 价目表货币与客户货币匹配。 

在项目合同中，以下优先顺序用于自动设置相关项目价目表：

1. 报价单
2. 商机​​
3. 客户 
4. 全局设置 

默认输入项目价目表时，系统将验证货币是否匹配客户的货币，以及已输入的默认价目表是否有 **销售** 上下文。

可以将多个项目价目表与客户、商机、报价单和项目合同实体关联。 此功能支持为长期开展的项目合同设置特定于日期的默认价格，在此情况下，可能需要多个价目表来纳入通货膨胀导致的价格更新。 但是，如果与客户、商机、报价单或项目合同实体关联的价目表存在重合时效，默认价格可能不正确。 因此，应确保不将具有重合时效的项目价目表与这些实体关联。


[!INCLUDE[footer-include](../includes/footer-banner.md)]