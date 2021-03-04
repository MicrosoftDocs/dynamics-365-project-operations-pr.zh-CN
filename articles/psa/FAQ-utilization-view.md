---
title: 查看资源的应计费利用率
description: 此主题介绍资源利用率视图。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146382"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="47621-103">查看资源的应计费利用率</span><span class="sxs-lookup"><span data-stu-id="47621-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="47621-104">**Project Service 资源利用率** 页上的 **利用率视图** 显示每项可预订资源的应计费利用率。</span><span class="sxs-lookup"><span data-stu-id="47621-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="47621-105">因为此视图基于日程安排板，因此您将发现很多相同的功能。</span><span class="sxs-lookup"><span data-stu-id="47621-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![利用率视图的屏幕截图](media/FAQ-utilization-1.png)
 

<span data-ttu-id="47621-107">应收费利用率计算如下：</span><span class="sxs-lookup"><span data-stu-id="47621-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="47621-108">应收费利用率 =（可用实际时数）/（资源产能）</span><span class="sxs-lookup"><span data-stu-id="47621-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="47621-109">此单元格表示为所选期间计算的应收费利用率（天、周或月）。</span><span class="sxs-lookup"><span data-stu-id="47621-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="47621-110">每个单元格的颜色显示资源的应收费利用率（对比其目标应收费利用率）。</span><span class="sxs-lookup"><span data-stu-id="47621-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="47621-111">目标利用率可以对资源的默认角色或单个资源本身设置。</span><span class="sxs-lookup"><span data-stu-id="47621-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="47621-112">计算首先将个人视为目标，然后是资源的默认角色。</span><span class="sxs-lookup"><span data-stu-id="47621-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="47621-113">为资源设置目标</span><span class="sxs-lookup"><span data-stu-id="47621-113">Set target on a resource</span></span>

1. <span data-ttu-id="47621-114">转到 **资源**\>**资源**。</span><span class="sxs-lookup"><span data-stu-id="47621-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="47621-115">选择一项资源以打开记录。</span><span class="sxs-lookup"><span data-stu-id="47621-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="47621-116">在 **Project Service** 选项卡上，可以设置资源的目标利用率。</span><span class="sxs-lookup"><span data-stu-id="47621-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![使用 Project Service 选项卡设置目标利用率的屏幕截图](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="47621-118">设置角色的目标利用率</span><span class="sxs-lookup"><span data-stu-id="47621-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="47621-119">转到 **资源**\>**资源角色**。</span><span class="sxs-lookup"><span data-stu-id="47621-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="47621-120">选择一个角色，然后打开记录。</span><span class="sxs-lookup"><span data-stu-id="47621-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="47621-121">设置角色的目标利用率。</span><span class="sxs-lookup"><span data-stu-id="47621-121">Set the target utilization for the role.</span></span>

> ![使用“资源角色”设置目标利用率的屏幕截图](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="47621-123">计算资源的应收费利用率</span><span class="sxs-lookup"><span data-stu-id="47621-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="47621-124">若要计算资源的应收费利用率，您需要满足一些先决条件。</span><span class="sxs-lookup"><span data-stu-id="47621-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="47621-125">为单个资源设置默认角色</span><span class="sxs-lookup"><span data-stu-id="47621-125">Set default role for individual resource</span></span>

<span data-ttu-id="47621-126">首先，目标利用率必须对单个资源或资源角色设置。</span><span class="sxs-lookup"><span data-stu-id="47621-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="47621-127">如果您使用资源角色作为目标，每个单个资源均必须具有默认角色。</span><span class="sxs-lookup"><span data-stu-id="47621-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="47621-128">若要进行此设置，转到 **资源** \> **资源**。</span><span class="sxs-lookup"><span data-stu-id="47621-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="47621-129">选择资源，打开记录，然后选择 **Project Service** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="47621-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="47621-130">在 **资源角色** 网格中，确保资源有一个角色，并且 **为默认** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="47621-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="47621-131">更改资源角色的记帐类型</span><span class="sxs-lookup"><span data-stu-id="47621-131">Change billing type for resource role</span></span>

<span data-ttu-id="47621-132">资源角色必须设置为 **应计费** 记帐类型。</span><span class="sxs-lookup"><span data-stu-id="47621-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="47621-133">转到 **资源**\>**资源角色**。</span><span class="sxs-lookup"><span data-stu-id="47621-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="47621-134">打开要更新的记录，然后将记帐类型默认值设置为 **应计费**。</span><span class="sxs-lookup"><span data-stu-id="47621-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="47621-135">为资源角色设置工时</span><span class="sxs-lookup"><span data-stu-id="47621-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="47621-136">资源必须有用于产能计算的工时。</span><span class="sxs-lookup"><span data-stu-id="47621-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="47621-137">转到 **资源**\>**资源**。</span><span class="sxs-lookup"><span data-stu-id="47621-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="47621-138">选择资源打开记录，然后选择 **显示工时**。</span><span class="sxs-lookup"><span data-stu-id="47621-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="47621-139">您可以通过从 **资源列表** 视图应用 **工时模板** 来批量更新资源列表。</span><span class="sxs-lookup"><span data-stu-id="47621-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="47621-140">应计费实际工时疑难解答</span><span class="sxs-lookup"><span data-stu-id="47621-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="47621-141">应计费实际工时源自 **实际值** 实体。</span><span class="sxs-lookup"><span data-stu-id="47621-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="47621-142">记帐类型为 **应计费** 的实际值包含在计算中，因此，您必须有应计费的实际值的项目。</span><span class="sxs-lookup"><span data-stu-id="47621-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="47621-143">如果看不到应收费利用率，您可以检查一些事项：</span><span class="sxs-lookup"><span data-stu-id="47621-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="47621-144">该资源是否有为产能定义的工时。</span><span class="sxs-lookup"><span data-stu-id="47621-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="47621-145">该资源是否有单独定义的利用率目标或是否有分派给它的默认角色。</span><span class="sxs-lookup"><span data-stu-id="47621-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="47621-146">该角色是否有为其定义的利用率目标。</span><span class="sxs-lookup"><span data-stu-id="47621-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="47621-147">实际值在您希望计算利用率的期间内是否有 **应计费** 记帐类型。</span><span class="sxs-lookup"><span data-stu-id="47621-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="47621-148">如果您看到实际值的记帐类型不是应计费，请检查以下事项：</span><span class="sxs-lookup"><span data-stu-id="47621-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="47621-149">实际使用的角色是否有应收费以外的默认记帐类型。</span><span class="sxs-lookup"><span data-stu-id="47621-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="47621-150">支持项目的项目合同子项中的角色是否已设置为非应收费。</span><span class="sxs-lookup"><span data-stu-id="47621-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="47621-151">项目是否没有关联的合同子项。</span><span class="sxs-lookup"><span data-stu-id="47621-151">The project does not have an associated contract line.</span></span>

