---
title: 将可预订资源用作定价维度
description: 此主题介绍如何将可预订资源用作定价维度。
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643072"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>将可预订资源用作定价维度

 _**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_ 

此主题介绍如何将可预订资源用作定价维度。 如果设置了您的定价策略，以便每个可预订资源都必须具有特定的价格或成本费率，请使用可预订资源作为定价维度。

## <a name="prerequisites"></a>先决条件
在完成本主题中的步骤之前，您必须为组织提供一个新的定价维度解决方案。 如果尚未创建，请参阅[创建自定义字段和实体](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md)。

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>向窗体和视图添加“可预订资源”字段
若要使 **可预订资源** 字段显示在定价维度解决方案中，您需要将此字段作为实体添加到所有窗体和视图中。

下表按实体列出了所有现成的窗体和视图。 您还需要将新字段添加到自定义实体中的任何其他窗体或视图。

|   Entity        | 表单   |视图        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色价格| 信息 | - 可用的资源类别价格<br> - 关联的资源类别价格 |
|  角色价格加价| 信息| - 可用角色价格加价<br>- 关联的角色价格加价 |
|  报价单明细详细信息| - 项目信息<br>- 项目快速创建| - 可用的报价单明细详细信息<br>- 合并的报价单明细详细信息<br>- 关联的报价单明细详细信息 |
|  项目合同子项详细信息| - 项目信息<br>- 项目快速创建| - 合并的合同子项详细信息<br>- 可用的合同子项详细信息<br>- 关联的合同子项详细信息 |
|  项目任务| - 信息<br>- 新窗体| &nbsp; |
|  项目团队成员| - 信息<br>- 新窗体| - 可用的项目团队成员<br>- 项目团队成员<br>- 关联的项目团队成员 |
|  时间条目| - 信息<br>- 创建时间条目| - 我的按日期列出的时间条目<br>- 我本周的时间条目<br>- 供审批的时间条目|
|  日记帐行| - 信息<br>- 快速创建| - 可用的日记帐行<br>- 关联的日记帐行 |
|  发票明细详细信息| - 信息<br>- 快速创建| - 可用的发票明细详细信息<br>- 应计费发票交易记录<br>- 免费发票交易<br>- 关联的发票明细详细信息 <br>- 非应计费发票交易|
|  实际| - 信息<br>- 可用的实际值| 关联的实际项 |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>将可预订资源设置为定价维度
要将可预订资源设置为定价维度，请执行以下步骤：

1. 转到 **设置** > **参数**。 
2. 在 **参数** 页上的 **基于金额的定价维度** 选项卡上，验证网格是否显示 **定价维度** 实体中的记录。 
2. 将 **可预订资源** 作为 **msdyn_bookableresource** 添加到此定价维度列表。 
3. 在 **适用于成本** 和 **适用于销售** 中，选择一个值。
4. 在 **维度类型** 中，选择 **基于金额**。 
5. 选择可预订资源的成本和销售优先级。 通常，如果作为定价维度包含了可预订资源，则可预订资源具有最高优先级。 将优先级设置为 **1**（或设置为 **0**，具体取决于您如何计算优先级），以确保此行为。

## <a name="set-up-pricing-dimension-field-names"></a>设置定价维度字段名

当 **角色价格** 表中的定价维度字段名称与其中使用了默认价格的其他任何实体的字段名称不同时，定价维度记录必须获得有关不同名称的通知。  

对于可预订资源，**项目团队成员** 实体的字段名与其在 **角色价格** 实体中的名称稍微不同。 

 - **项目团队成员** 实体 = **msdyn_bookableresourceid**
 - **角色价格** 实体 = **msdyn_bookableresource**

**msydn_bookableresource** 的定价维度记录必须获得有关此差异的通知。

1. 请在 **定价维度** 网格中双击行以打开 **msdyn_bookableresource** 的维度页。
2. 在维度页的 **相关** 选项卡上，选择 **定价维度字段名称**。

  ![“定价维度字段名称”选项卡](media/PD-fieldname.png)

3. 在打开的关联视图中，选择 **添加新定价维度字段名称**。

  ![添加新定价维度字段名称](media/Add-NewPD-fieldname.png)

  此选项用于打开 **msdyn_bookableresource** 的 **新定价维度字段名称** 页。 

4. 在 **新定价维度字段名称** 页上，将 **msdyn_projectteam** 添加到 **实体逻辑名称** 中。
5. 向 **字段名称** 中添加 **msdyn_bookableresourceid**。

 ![“新定价维度字段名称”窗体](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]