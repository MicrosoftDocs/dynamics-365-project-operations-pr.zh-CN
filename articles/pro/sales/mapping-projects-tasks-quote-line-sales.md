---
title: 将项目和任务映射到基于项目的报价单明细
description: 此主题提供有关如何将项目和任务映射到基于项目的任务明细的信息。
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964896"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>将项目和任务映射到基于项目的报价单明细

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

在基于项目的报价单明细上，可以映射已经与报价单明细关联的项目的特定任务。

当您将任务映射到报价单明细时，您在报价单明细上定义的以下项目将仅应用于这些任务：

- 计费方法
- 应计费选项
- 上限
- 客户

例如，您可能有一个项目，其中一个阶段是固定价格，所有其他阶段是时间和材料。 在这种情况下，您可以使用固定价格计费方法将第一阶段及其所有子任务与该阶段的报价单明细相关联。 然后，您可以将所有其他阶段与基于时间和材料的报价单明细关联起来。

## <a name="associate-tasks-to-project-based-quote-lines"></a>将任务与基于项目的报价单明细相关联

您可以从以下位置将任务与报价单明细相关联：

- **项目**页 > **任务记帐**选项卡（最佳）
- **报价单明细**页 > **应计费任务**选项卡 

### <a name="from-the-project-page"></a>从“项目”页

**项目**页提供将任务与报价单明细关联的最佳体验。 您可以使用此页面选择多个任务，然后将所有任务及其子任务关联到选定的报价单明细。

1. 在基于项目的报价单明细的**常规**选项卡上，确认**项目**字段已填写。
2. 在**包含的任务**字段中，选择**仅所选任务**。
3. 保存基于项目的报价单明细。 当窗体刷新时，**应计费任务**选项卡将显示。
4. 在**常规**选项卡上，从**项目**字段中选择项目的链接。
5. 在**项目**页上，选择**任务记帐**选项卡。
6. 在第二个网格（适用于特定于任务的计费设置）中，选择一个或多个任务，然后选择**关联报价单明细**。
7. 在出现的对话页面中，选择一个在报价单上显示基于项目的报价单明细的报价单明细。
8. 在**计费类型**字段中，指明这些任务是应计费还是非应计费。
9. 选中复选框以指示关联是否应包括所选任务的子任务。 选中复选框会将所选任务的子任务与报价单明细相关联。
10. 选择**确定**以关闭对话框。

### <a name="from-the-quote-line-page"></a>从“报价单明细”页

您可以从**报价单明细**页的**应计费任务**选项卡将项目任务与报价单明细相关联。

>[!NOTE]
>将项目任务与报价单明细相关联的最佳位置是在**项目**页的**任务记帐**选项卡上。 如果您从**报价单明细**页的**应计费任务**选项卡关联任务，则必须手动关联每个项目。

1. 在基于项目的报价单明细的**常规**选项卡上，确认在**项目**字段中选择了一个项目。
2. 在**包含的任务**字段中，选择**仅所选任务**。
3. 保存基于项目的报价单明细。 当窗体刷新时，**应计费任务**选项卡将显示。
4. 在**应计费任务**选项卡上，选择**添加报价单明细任务**。
5. 在**报价单明细任务**页上的**任务**字段中，选择任务，然后在**计费类型**字段中选择**保存**。 
6. 关闭该页面。 所选任务现已与报价单明细关联。

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>取消任务与基于项目的报价单明细的关联

### <a name="from-the-project-page"></a>从“项目”页

此方法提供取消任务与报价单明细的关联的最佳体验。 您可以选择多个任务，然后取消所有任务及其子任务与选定的报价单明细的关联。

1. 在基于项目的报价单明细的**常规**选项卡上，在**项目**字段中，选择项目链接。
2. 在**项目**页上，选择**任务记帐**选项卡。
3. 在第二个网格（适用于特定于任务的计费设置）中，选择一个或多个任务，然后选择**取消关联报价单明细**。
4. 在显示的对话页面中，选择报价单明细。
5. 选中复选框以指示是否还应从所选任务的子任务中删除此关联。 选中复选框还将取消所选任务的子任务与报价单明细的关联。
6. 选择**确定**。 警告消息将通知您，如果删除此关联，以前记录在任务中的所有实际值都可能取消。 
7. 选择**确定**继续删除任务与基于项目的报价单明细之间的关联。

### <a name="from-the-quote-line-page"></a>从“报价单明细”页

您还可以从**报价单明细**页的**应计费任务**选项卡取消项目任务与报价单明细的关联。

1. 在**应计费任务**选项卡上，选择**删除报价单明细任务**。
2. 选择**确定**。 警告消息将通知您，如果删除此关联，以前记录在任务中的所有实际值都可能取消。 
3. 选择**确定**继续删除任务与基于项目的报价单明细之间的关联。

>[!NOTE]
> 此过程不会从项目中删除任务。 只是从基于项目的报价单明细中删除任务关联。
