---
title: 创建自定义字段和实体
description: 此主题介绍在 Power Apps 平台中如何在自己的解决方案内创建选项集和实体。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998940"
---
# <a name="create-custom-fields-and-entities"></a>创建自定义字段和实体 

[!include [banner](../includes/psa-now-project-operations.md)]

如果要在 Power Apps 平台中创建自定义选项集或实体，随时可完成以下步骤。  
此主题中的过程应使用 Project Service Automation (PSA) 的 Web 界面完成。

> [!IMPORTANT]
> 建议在单独的解决方案中进行所有自定义定价维度更改。 这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。 进行了所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定价维度解决方案中创建自定义字段和选项集

定价维度可以是选项集或实体。 两种都必须在定价解决方案中创建。 此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。

### <a name="entity-based-dimensions"></a>基于实体的维度

1. 在 PSA 中，单击 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。
2. 在解决方案资源管理器中左侧导航窗格上，选择 **实体**。
3. 单击 **新建** 创建一个IE名称为 **标准标题** 的新实体。 输入其余所需信息，然后单击 **保存**。

> ![标准标题实体定义](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>基于选项集的维度 
可创建两个基于选项集的维度。 **资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格，值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。


1. 在 PSA 中，单击 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。 
2. 在解决方案资源管理器中左侧导航窗格上，选择 **选项集**。 
3. 单击 **新建** 创建一个新的选项集，输入其余必需信息，然后单击 **保存**。

> ![称为“资源工作位置”且基于选项集的定价维度 ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![称为“资源工作时间”且基于选项集的定价维度 ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>为基于实体的维度创建数据

可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。 使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题：**系统工程师** 和 **高级系统工程师**。 如果要创建的数据很少（如在以下示例中），可以使用标准窗体。

1. 在 PSA 中，单击 **高级查找**。 选择实体 **标准标题**，然后单击 **结果**。 将显示 **标准标题** 实体中的所有行。
2. 单击 **新建**。 在 **名称** 字段中，输入“系统工程师”，然后单击 **保存**。
3. 关闭窗体。 
4. 重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。

> ![标准标题实体的示例数据 ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]