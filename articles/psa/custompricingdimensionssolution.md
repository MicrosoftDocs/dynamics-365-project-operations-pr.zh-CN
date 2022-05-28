---
title: 为定价维度创建自定义解决方案
description: 此主题说明如何在创建自定义定价维度时创建自定义解决方案。
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7a15c5fc45ada4394dcb8e3dc2b477cb2a0bb8c6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592267"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>为定价维度创建自定义解决方案

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> 所有自定义定价维度的更改都应在单独的解决方案中进行。 这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。 进行所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。

1. 选择 **设置** > **解决方案**，然后选择 **新建**。 
2. 将该解决方案命名为 **\<your organization name> 定价维度**，输入其余必需信息，然后选择 **保存**。

> ![为定价维度创建自定义解决方案。](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>向定价维度解决方案添加所有必需实体和相关组件
您需要向定价解决方案添加以下 Project Service 实体。 完成此过程中的步骤在定价解决方案中进行一些重要的架构更改，以便实体可以识别新的定价维度。

1. 选择 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。 
2. 在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体**。
3. 在 **解决方案组件** 对话框中，选择以下实体：

- 实际
- 可预订资源
- 估计值明细
- 项目任务
- 发票明细详细信息
- 日记帐行
- 项目合同子项详细信息
- 项目团队成员
- 报价单行明细
- 角色价格加价
- 角色价格 
- 时间条目 

> ![向定价维度解决方案添加现有实体。](media/Existing-entities-to-PD-solution.png)

> ![选择解决方案组件。](media/Dimension-Components.png)

> [!NOTE]
> 务必包括所选每个实体的所有窗体和视图。

4. 当系统提示包括所选实体的任何依赖实体时，选择 **否**。

> ![请勿包含全部相关组件。](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
