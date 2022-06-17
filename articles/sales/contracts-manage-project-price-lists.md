---
title: 管理项目合同上的项目价目表
description: 本文提供有关在项目合同中管理项目价目表的信息。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926167"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>管理项目合同上的项目价目表

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 中的项目合同设计为支持合同上的多个有时效的销售价目表。 在 Project Operations 中，有一个名为 **项目价目表** 的新的关联实体。 此实体与项目合同之间具有一对多关系。

项目价目表用于为项目的时间、材料和支出交易定价。 当合同具有一个或多个项目价目表时，这些价目表用于通过合同子项对与该合同关联的项目的时间、材料、支出估计和实际值进行定价。

如果项目合同上没有项目价目表，将显示一条警告消息，指出不存在项目价目表，并且将不会对您的估计值、实际项目工作、材料和记录的支出进行定价。 销售值不会有价格。

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>关联或取消关联项目合同中的项目价目表

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>为基于项目的工作、材料和支出创建或关联特定的价目表

1. 在项目合同上，选择 **项目价目表** 选项卡。
2. 在子网格中，选择 **+ 添加新项目价目表**。
3. 在 **快速创建** 滑块上，选择一个价目表。 

  下拉列表显示将上下文设置为 **销售** 的所有价目表，价目表中的货币与合同中的货币匹配。
  
4. 为项目价目表关联输入说明，请选择 **保存**，然后关闭 **快速创建** 滑块。

   将创建项目价目表关联。
   
5. 重复步骤 1-4，将多个项目价目表与项目合同关联。 如果您在每个关联项目价目表上有不同时效，这种情况下才会创建多个项目价目表。

> [!NOTE]
> Project Operations 不支持重叠项目价目表的时效。 如果交易有给定日期的多个项目价目表，该交易中的价格将默认为零。

### <a name="remove-a-project-price-list-association"></a>删除项目价目表关联

- 选择项目价目表，然后在子网格中选择 **删除合同项目价目表**。 

  价目表将被从合同上的项目价目表中删除。 价目表本身不会被删除。 只会删除与合同的关联。

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>设置合同上的项目价格表的自动默认设置

可以将项目价目表设置为默认项目价目表。 此安装程序可确保贵组织的所有合同始终从该价格期间的标准项目价目表开始。

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>设置项目价目表的组织默认值

1. 转到 **设置** > **常规**，然后选择 **参数**。
2. 在 **可用参数** 列表页上，选择并双击记录将其打开。 双击时，请确保没有单击超链接字段值。 
3. 在 **可用参数** 页上，选择 **价目表** 选项卡。一个子网格将显示默认价目表的列表。 这是包含标准成本和销售价目表的列表。 在此处为您销售所使用的每种货币关联一个 **销售** 价目表，确保此销售价目表是您为以此货币进行交易的客户创建的任何合同上的默认价目表。

### <a name="set-up-a-customer-specific-project-price-list"></a>设置特定于客户的项目价目表

在与客户商定了主定价协议后，您还可以设置特定于客户的项目价目表。

1. 转到 **销售** > **客户**。
2. 从可用客户列表中，选择有特殊价目表的客户。
3. 选择客户记录将其打开，然后选择 **项目价目表** 选项卡。一个子网格将显示特定于此客户的项目价目表的列表。 
4. 在此处创建新的价目表关联，以获得特定于此客户的项目价目表。

## <a name="custom-pricing-on-a-project-contract"></a>项目合同上的自定义定价

在您有了组织的特定于客户的默认项目价目表之后，您的项目合同将自动创建，并具有这些项目价目表关联。 但是，项目合同上的项目价目表复制时始终带有向其追加的日期和合同名称。 客户和项目经理随后可以开始对这些副本上的价格进行编辑。 这些更改的价格仅适用于此项目合同。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
