---
title: 创建自定义字段和实体，作为定价维度
description: 此主题提供有关如何创建自定义选项集或实体的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072642"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>创建自定义字段和实体，作为定价维度

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

任何时候要创建自定义选项集或实体，请完成以下步骤。

> [!IMPORTANT]
> 建议在单独的解决方案中进行所有自定义定价维度更改。 这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。 进行了所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>为定价维度创建自定义解决方案
1. 转到 **设置** > **解决方案** ，然后选择 **新建** 创建新的解决方案。 
2. 将该解决方案命名为 **\<your organization name> 定价维度** ，输入其余必需信息，然后选择 **保存** 。
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定价维度解决方案中创建自定义字段和选项集

定价维度可以是选项集或实体。 两种都必须在定价解决方案中创建。 此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。

### <a name="entity-based-dimensions"></a>基于实体的维度

1. 转到 **设置** > **解决方案** ，然后双击 **\<your organization name> 定价维度** 。
2. 在解决方案资源管理器中左侧导航窗格上，选择 **实体** 。
3. 选择 **新建** 创建一个IE名称为 **标准标题** 的新实体。 
4. 输入其余所需信息，然后选择 **保存** 。


### <a name="option-set-based-dimensions"></a>基于选项集的维度 
可创建两个基于选项集的维度。 **资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格，值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。


1. 转到 **设置** > **解决方案** ，双击 **\<your organization name> 定价维度** 。 
2. 在解决方案资源管理器中左侧导航窗格上，选择 **选项集** 。 
3. 选择 **新建** 创建一个新的选项集，输入其余必需信息，然后选择 **保存** 。

## <a name="create-data-for-entity-based-dimensions"></a>为基于实体的维度创建数据

可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。 使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题： **系统工程师** 和 **高级系统工程师** 。 如果要创建的数据很少（如在以下示例中），可以使用标准窗体。

1. 选择 **高级查找** ，选择实体 **标准标题** ，然后选择 **结果** 。 将显示 **标准标题** 实体中的所有行。
2. 选择 **新建** ，在 **名称** 字段中，输入“系统工程师”，然后选择 **保存** 。
3. 关闭此窗体。 
4. 重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>向定价维度解决方案添加所有必需实体和相关组件
您需要向定价解决方案添加以下实体。 请使用此过程中的步骤在定价解决方案中进行一些重要的架构更改，以便实体可以识别新的定价维度。

1. 选择 **设置** > **解决方案** ，双击 **\<your organization name> 定价维度** 。 
2. 在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体** 。
3. 在 **解决方案组件** 对话框中，选择以下实体：

  - 实际值
  - 可预订的资源
  - 估算明细
  - 发票明细详细信息
  - 日记帐行
  - 项目合同子项详细信息
  - 项目团队成员
  - 报价单明细详细信息
  - 角色价格加价
  - 角色价格 
  - 时间条目 


> [!NOTE]
> 务必包括所选每个实体的所有窗体和视图。

4. 当系统提示包括上面所选实体的任何依赖实体时，选择 **否** 。

