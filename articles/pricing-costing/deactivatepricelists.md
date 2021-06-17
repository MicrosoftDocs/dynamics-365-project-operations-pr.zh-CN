---
title: 停用价目表
description: 此主题说明如何停用或删除未使用或旧的价目表。
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001325"
---
# <a name="deactivate-price-lists"></a>停用价目表 

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

若要从 Dynamics 365 Project Operations 中删除旧价目表或未使用的价目表，您必须完成两个步骤。 

1. 从特定页面移除或删除价目表。
2. 停用或删除 **价目表** 页上“可用价目表”中的价目表。

>[!IMPORTANT]
> 您必须完成这两个步骤，才能完整移除价目表。 仅执行步骤 2（直接从“可用价目表”视图中删除或停用价目表）是不够的。 还必须从步骤 1 中提及的所有位置删除此价目表的关联。

## <a name="delete-the-price-list-from-specific-pages"></a>从特定页面删除价目表
1. 若要从 Project Operations 中删除价目表，请转到以下页面：  

      - **项目参数** 页面 > **价目表** 选项卡
      - **部门** 页面 > **价目表** 网格
      - **客户** 页面 > **项目价目表** 网格
      - **项目报价单** 页面 > **项目价目表** 网格：这适用于所有可用的项目报价单。
      - **项目合同** 页面 > **项目价目表** 网格：这适用于所有可用的项目合同。

 2. 对于每个页面，您需要选择要删除的价目表，然后选择 **删除**。 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>删除或停用“价目表”页中的价目表
 
1. 若要从可用价目表中删除价目表，请转到 **销售** > **客户** > **价目表**。 
2. 选择要删除的价目表，然后选择 **删除**。 只要在任何现有交易中引用了价目表，则将无法删除该价目表。 如果出现这种情况，您可以停用价目表，以便价目表不会显示在任何视图中。 
3. 若要停用价目表，请再次选择价目表，然后选择 **停用**。   
