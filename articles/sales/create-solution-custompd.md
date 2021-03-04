---
title: 为自定义定价维度创建解决方案
description: 本主题提供了有关如何为自定义定价维度创建解决方案的信息。
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513963"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>为自定义定价维度创建解决方案

 _**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_ 

>[!IMPORTANT]
>所有自定义定价维度的更改都应在单独的解决方案中进行。 这项重要的最佳实践让您可以灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。 进行了所有必需更改之后，将此解决方案作为 **托管** 解决方案导出，然后导入到其他实例中，以便重复利用。

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>为自定义定价维度创建解决方案

1.  选择 **设置** > **解决方案**，然后选择 **新建**。
2.  将此解决方案命名为 *<your organization name> 定价维度*。
3. 输入其余所需信息，然后选择 **保存**。

  ![创建自定义定价维度解决方案](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>向定价维度解决方案添加所有必需实体和相关组件

将以下 Project Service 实体添加到定价解决方案中，以在定价解决方案中进行重要的架构更改。 完成此过程后，实体将识别新的定价维度。

1.  选择 **设置** > **解决方案**，然后双击 **<*您的组织名称*> 定价维度**。
2.  在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体**。
3.  在 **解决方案组件** 对话框中，选择以下实体：
 
   - **实际**
   - **可预订资源**
   - **估计值明细**
   - **项目任务**
   - **发票明细详细信息**
   - **日记帐行**
   - **项目合同子项详细信息**
   - **项目团队成员**
   - **报价单行明细**
   - **角色价格加价**
   - **角色价格**
   - **时间条目**
 
   ![添加现有实体的自定义定价维度解决方案](./media/Existing-entities-to-PD-solution.png)
 
 4. 对于每个实体，查看要添加的组件以及每个实体的实体资产最终列表。 

   >[!NOTE]
   > 包括所选每个实体的所有窗体和视图。

  ![已添加实体](./media/solution-component-selection.png)


5.  当提示包括所选实体的任何相关实体时，选择 **否，不包含必需组件。**

    ![包括相关实体](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]