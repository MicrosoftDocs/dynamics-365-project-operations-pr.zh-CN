---
title: 查看资源的应计费利用率
description: 此主题介绍资源利用率视图。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992823"
---
# <a name="view-chargeable-utilization-for-resources"></a>查看资源的应计费利用率

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Project Service 资源利用率** 页上的 **利用率视图** 显示每项可预订资源的应计费利用率。 因为此视图基于日程安排板，因此您将发现很多相同的功能。

> ![利用率视图的屏幕截图](media/FAQ-utilization-1.png)
 

应收费利用率计算如下：

   应收费利用率 =（可用实际时数）/（资源产能）

此单元格表示为所选期间计算的应收费利用率（天、周或月）。

每个单元格的颜色显示资源的应收费利用率（对比其目标应收费利用率）。 

目标利用率可以对资源的默认角色或单个资源本身设置。 计算首先将个人视为目标，然后是资源的默认角色。

## <a name="set-target-on-a-resource"></a>为资源设置目标

1. 转到 **资源**\>**资源**。 
2. 选择一项资源以打开记录。 
3. 在 **Project Service** 选项卡上，可以设置资源的目标利用率。

> ![使用 Project Service 选项卡设置目标利用率的屏幕截图](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>设置角色的目标利用率

1. 转到 **资源**\>**资源角色**。 
2. 选择一个角色，然后打开记录。 
3. 设置角色的目标利用率。

> ![使用“资源角色”设置目标利用率的屏幕截图](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>计算资源的应收费利用率

若要计算资源的应收费利用率，您需要满足一些先决条件。 

### <a name="set-default-role-for-individual-resource"></a>为单个资源设置默认角色

首先，目标利用率必须对单个资源或资源角色设置。 如果您使用资源角色作为目标，每个单个资源均必须具有默认角色。 

1. 若要进行此设置，转到 **资源** \> **资源**。 
2. 选择资源，打开记录，然后选择 **Project Service** 选项卡。 
3. 在 **资源角色** 网格中，确保资源有一个角色，并且 **为默认** 设置为 **是**。
 
### <a name="change-billing-type-for-resource-role"></a>更改资源角色的记帐类型

资源角色必须设置为 **应计费** 记帐类型。 

1. 转到 **资源**\>**资源角色**。 
2. 打开要更新的记录，然后将记帐类型默认值设置为 **应计费**。

### <a name="set-working-hours-for-resource-role"></a>为资源角色设置工时
 
资源必须有用于产能计算的工时。 

1. 转到 **资源**\>**资源**。 
2. 选择资源打开记录，然后选择 **显示工时**。 
3. 您可以通过从 **资源列表** 视图应用 **工时模板** 来批量更新资源列表。

## <a name="troubleshooting-chargeable-actual-hours"></a>应计费实际工时疑难解答

应计费实际工时源自 **实际值** 实体。 记帐类型为 **应计费** 的实际值包含在计算中，因此，您必须有应计费的实际值的项目。

如果看不到应收费利用率，您可以检查一些事项：

- 该资源是否有为产能定义的工时。
- 该资源是否有单独定义的利用率目标或是否有分派给它的默认角色。 该角色是否有为其定义的利用率目标。
- 实际值在您希望计算利用率的期间内是否有 **应计费** 记帐类型。 如果您看到实际值的记帐类型不是应计费，请检查以下事项：

  - 实际使用的角色是否有应收费以外的默认记帐类型。
  - 支持项目的项目合同子项中的角色是否已设置为非应收费。
  - 项目是否没有关联的合同子项。



[!INCLUDE[footer-include](../includes/footer-banner.md)]