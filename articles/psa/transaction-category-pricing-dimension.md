---
title: 将交易类别用作定价维度
description: 此主题介绍如何将交易类别用作定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072688"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>将交易类别用作定价维度
此主题显示如何将交易类别用作定价维度。 首先，如果尚未创建定价维度解决方案，需要新建一个。 如果已经有了定价维度解决方案，则可在该解决方案中进行更改。 如果尚未为组织新建定价维度解决方案，请完成[创建自定义字段和实体](create-custom-fields-entities.md)主题中的过程。

## <a name="add-transaction-category-to-forms-and-views"></a>向窗体和视图添加交易类别
若要在定价维度解决方案的 UI 中显示交易类别，需要浏览关键实体的所有窗体和视图，并将这些字段添加到这些实体的窗体和视图。
下表是需要更新的大量自带窗体和视图的列表（按实体排列），将使用新字段更新这些窗体和视图。 如果这些实体的自定义项中有任何其他视图或窗体，请将新字段也添加到这些视图或窗体。

|  实体        | 窗体     |视图        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色价格|• 信息 |• 可用的资源类别价格<br> • 资源类别价格关联视图|
|  角色价格加价|• 信息|• 可用角色价格加价<br>• 角色价格加价关联视图|
|  报价单明细详细信息|• 项目信息<br>• 项目快速创建|• 可用的报价单明细详细信息<br>• 合并的报价单明细详细信息<br>• 报价单明细详细信息关联视图|
|  项目合同子项详细信息|• 项目信息<br>• 项目快速创建|• 合并的合同子项详细信息<br>• 可用的合同子项详细信息<br>• 合同子项详细信息关联视图|
|  项目任务|• 信息<br>• 新窗体||
|  项目团队成员|• 信息<br>• 新窗体|• 可用的项目团队成员<br>• 项目团队成员<br>• 项目团队成员关联视图|
|  时间条目|• 信息<br>• 创建时间条目|• 我的按日期列出的时间条目<br>• 我本周的时间条目<br>• 供审批的时间条目|
|  日记帐行|• 信息<br>• 快速创建|• 可用的日记帐行<br>• 日记帐行关联视图|
|  发票明细详细信息|• 信息<br>• 快速创建|• 可用的发票明细详细信息<br>• 应计费发票交易记录<br>• 免费发票交易记录<br>• 发票明细详细信息关联视图<br>• 非应计费发票交易记录|
|  实际值|• 信息<br>• 可用的实际值|• 实际值关联视图|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>将交易类别设置为定价维度

1. 在 Web 界面中，转到 **Project Service** > **设置** > **参数** 。 
2. 请注意， **参数** 页 **基于金额的定价维度** 选项卡上的网格显示 **定价维度** 实体中的记录。
3. 向此列表添加 **交易类别** ，然后将 **适用于成本** 和 **适用于销售** 字段设置为 **是** 。
4. 在 **维度类型** 字段中，选择 **基于金额** ，然后选择与成本和销售有关的 **交易类别** 的优先级。
