---
title: 创建自定义字段和实体，作为定价维度
description: 此主题提供有关如何创建自定义选项集或实体的信息。
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275617"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>创建自定义字段和实体，作为定价维度

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

要创建自定义选项集或实体以将其用作定价维度时，请完成以下步骤。 有关详细信息，请参阅[定价维度概述](pricing-dimensions-overview.md)。  

> [!IMPORTANT]
> 建议在单独的解决方案中进行所有自定义定价维度更改。 此重要的最佳实践为将来根据需要更新或删除更改提供了灵活性。 这还将有助于重复使用您的工作，并且在完成所有必需的更改后更便于将这些更改加载到其他实例中，请将此解决方案导出为 **托管解决方案**，并将其导入到其他实例中，以重复使用定价设置。

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定价维度解决方案中创建自定义字段和选项集

定价维度可以是选项集或实体。 两种都必须在定价解决方案中创建。 此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。

### <a name="entity-based-dimensions"></a>基于实体的维度
若要创建基于实体的维度，请执行以下步骤：

1. 转到 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。
2. 在解决方案资源管理器内的左侧导航窗格中，选择 **实体**。
3. 选择 **新建** 创建一个IE名称为 **标准标题** 的新实体。 
4. 输入其余所需信息，然后选择 **保存**。

> ![标准标题实体定义](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>基于选项集的维度 
可创建两个基于选项集的维度。 

- **资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格。 
- 值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。

下图提供了 **资源工作位置** 维度的视图。 

> ![称为“资源工作位置”且基于选项集的定价维度](media/Option-set-PD-called-Resource-Work-Location.png)

下图提供了 **资源工作时间** 维度的视图。 

> ![称为“资源工作时间”且基于选项集的定价维度](media/Option-set-PD-called-Resource-Work-Hours.png)

1. 转到 **设置** > **解决方案**，双击 **\<your organization name> 定价维度**。 
2. 在解决方案资源管理器内的左侧导航窗格中，选择 **选项集**。 
3. 选择 **新建** 创建一个新的选项集，输入其余必需信息，然后选择 **保存**。

## <a name="create-data-for-entity-based-dimensions"></a>为基于实体的维度创建数据

可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。 使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题：**系统工程师** 和 **高级系统工程师**。 如果要创建的数据很少（如在以下示例中），可以使用标准窗体。

1. 选择 **高级查找**。
2. 选择实体 **标准标题**，然后选择 **结果**。 将显示 **标准标题** 实体中的所有行。
3. 选择 **新建**，在 **名称** 字段中，输入“系统工程师”，然后选择 **保存**。
4. 关闭该页面。 
5. 重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。

> ![标准标题实体的示例数据](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]