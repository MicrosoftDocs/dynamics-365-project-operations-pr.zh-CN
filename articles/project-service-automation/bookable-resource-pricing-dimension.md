---
title: 将可预订资源用作定价维度
description: 此主题介绍如何将可预订资源用作定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749714"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>将可预订资源用作定价维度
此主题介绍如何将可预订资源用作定价维度。 首先，如果尚未创建定价维度解决方案，需要新建一个。 如果已经有了定价维度解决方案，则可在该解决方案中进行更改。 如果尚未为组织新建定价维度解决方案，请完成[创建自定义字段和实体](create-custom-fields-entities.md)主题中的过程。

## <a name="add-bookable-resource-to-forms-and-views"></a>向窗体和视图添加可预订资源
若要在定价维度解决方案的 UI 中显示这些字段，需要浏览关键 Project Service 实体的所有窗体和视图，并将这些字段添加到这些实体的窗体和视图。
下表是需要更新的大量自带窗体和视图的列表（按实体排列）。 如果这些实体的自定义项中有任何其他视图或窗体，请将新字段也添加到这些视图或窗体。
打开解决方案资源管理器以找到定价维度解决方案，然后单击**发布所有自定义项**。


|   实体        | 窗体   |视图        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色价格|• 信息 |• 可用的资源类别价格<br> • 资源类别价格关联视图|
|  角色价格加价|• 信息|• 可用角色价格加价<br>• 角色价格加价关联视图|
|  报价单明细详细信息|• 项目信息<br>• 项目快速创建|• 可用的报价单明细详细信息<br>• 合并的报价单明细详细信息<br>• 报价单明细详细信息关联视图|
|  项目合同子项详细信息|• 项目信息<br>• 项目快速创建|• 合并的合同子项详细信息<br>• 可用的合同子项详细信息<br>• 合同子项详细信息关联视图|
|  项目团队成员|• 信息<br>• 新窗体|• 可用的项目团队成员<br>• 项目团队成员<br>• 项目团队成员关联视图|
|  时间条目|• 信息<br>• 创建时间条目|• 我的按日期列出的时间条目<br>• 我本周的时间条目<br>• 供审批的时间条目|
|  日记帐行|• 信息<br>• 快速创建|• 可用的日记帐行<br>• 日记帐行关联视图|
|  发票明细详细信息|• 信息<br>• 快速创建|• 可用的发票明细详细信息<br>• 应计费发票交易记录<br>• 免费发票交易记录<br>• 发票明细详细信息关联视图<br>• 非应计费发票交易记录|
|  实际值|• 信息<br>• 可用的实际值|• 实际值关联视图|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>将可预订资源设置为定价维度

1. 在 Web 界面中，转到 **Project Service** > **设置** > **参数**。 请注意，**参数**页**基于金额的定价维度**选项卡上的网格显示定价维度实体中的记录。 
2. 将**可预订资源**作为 **msdyn_bookableresource** 添加到此定价维度列表。 
3. 指定充当定价维度的可预订资源的上下文，并设置**适用于成本**和**适用于销售**值。
4. 在**维度类型**字段中，选择**基于金额**。 
5. 选择可预订资源的成本和销售优先级。 通常，作为定价维度包含的可预订资源的优先级最高，所以将其设置为 **1**（或 **0**，具体取决于优先级的统计方法）将确保此行为。

## <a name="set-up-pricing-dimension-field-names"></a>设置定价维度字段名

当定价维度在**角色价格**表中的字段名与其在需要设置默认价格的其他任何实体中的字段名不同时，定价维度记录必须了解不同名称。    
对于可预订资源，**项目团队成员**实体的字段名 (**msdyn_bookableresourceid**) 与其在**角色价格**实体中的名称 (**msdyn_bookableresource**) 稍微不同。 **msydn_bookableresource** 的定价维度记录必须了解这一点。 
1. 为此，请在**定价维度**网格中单击行以打开 **msdyn_bookableresource** 的维度页。
2. 在维度页的**相关**选项卡上，单击**定价维度字段名称**。

 ![“定价维度字段名称”选项卡](media/PD-fieldname.png)

4. 在打开的关联视图中，单击**添加新定价维度字段名称**。

 ![添加新定价维度字段名称](media/Add-NewPD-fieldname.png)


此选项用于打开 **msdyn_bookableresource** 的**新定价维度字段名称**页。 

5. 将 **msdyn_projectteam** 添加到**实体逻辑名称**字段，将 **msdyn_bookableresourceid** 添加到**字段名称**字段。 保存记录。

 ![“新定价维度字段名称”窗体](media/PD-fieldname-Added.png)
