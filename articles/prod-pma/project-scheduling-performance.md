---
title: 项目资源计划性能
description: 此主题介绍如何提高大量项目的资源计划性能。
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010010"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="d64b6-103">项目资源计划性能</span><span class="sxs-lookup"><span data-stu-id="d64b6-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="d64b6-104">当项目数量上千时，可能发生与资源计划有关的性能问题。</span><span class="sxs-lookup"><span data-stu-id="d64b6-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="d64b6-105">为了提高资源计划性能，提供了一项功能，供用户减少启动资源可用性窗体所用时间。</span><span class="sxs-lookup"><span data-stu-id="d64b6-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="d64b6-106">特别是，其去除了资源产能汇总同步流程，而是使用 **ResProjectResource** 表加快资源查找速度。</span><span class="sxs-lookup"><span data-stu-id="d64b6-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="d64b6-107">请注意，将不再使用 **ResRollup** 表。</span><span class="sxs-lookup"><span data-stu-id="d64b6-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d64b6-108">如果需要依赖资源产能汇总同步流程或 **ResProjectResource** 表，请勿使用此功能。</span><span class="sxs-lookup"><span data-stu-id="d64b6-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d64b6-109">启用资源计划性能增强</span><span class="sxs-lookup"><span data-stu-id="d64b6-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="d64b6-110">若要启用资源计划性能增强，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d64b6-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="d64b6-111">转到 **功能管理** > **所有**，然后在功能列表中找到 **启用项目资源计划性能增强功能**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d64b6-112">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="d64b6-113">如果在此列表中找不到该功能，请选择 **检查更新** 刷新列表。</span><span class="sxs-lookup"><span data-stu-id="d64b6-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="d64b6-114">刷新浏览器，然后转到 **项目管理和会计** > **定期** > **项目资源** > **同步所有公司的资源日历产能**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="d64b6-115">将 **删除现有产能记录** 设置为 **是** 以删除之前的数据。</span><span class="sxs-lookup"><span data-stu-id="d64b6-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d64b6-116">如果要生成增量数据，请将其设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="d64b6-117">在 **期间代码** 字段中，选择应生成数据的期间。</span><span class="sxs-lookup"><span data-stu-id="d64b6-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d64b6-118">如果选择期间代码，则无需定义开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="d64b6-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="d64b6-119">如果让 **期间代码** 字段保留为空，请选择特定的开始日期和结束日期以生成数据。</span><span class="sxs-lookup"><span data-stu-id="d64b6-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="d64b6-120">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d64b6-121">这将在您的环境中所有公司内把常规数据分发给 **ResCalendarCapacity** 表，以便只需在一个法人中运行批处理作业。</span><span class="sxs-lookup"><span data-stu-id="d64b6-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d64b6-122">需要此批处理作业中的数据，才能通过关联的日历计算资源产能。</span><span class="sxs-lookup"><span data-stu-id="d64b6-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="d64b6-123">转到 **项目管理和会计** > **定期** > **项目资源** > **填充所有公司的项目资源**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="d64b6-124">这是 **ResProjectResource**、**ResCalendarDateTimeRange** 和 **ResEffectiveDateTimeRange** 表中常规数据的数据更新脚本。</span><span class="sxs-lookup"><span data-stu-id="d64b6-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="d64b6-125">还将更新 **PSAPRojSchedRole.RootActivity** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="d64b6-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="d64b6-126">如果不运行，在尝试执行资源计划操作时，将收到警告。</span><span class="sxs-lookup"><span data-stu-id="d64b6-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d64b6-127">关闭资源计划性能增强</span><span class="sxs-lookup"><span data-stu-id="d64b6-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="d64b6-128">转到 **功能管理** > **所有**，然后搜索 **启用项目资源计划性能增强功能**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d64b6-129">选择功能，然后选择 **禁用** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d64b6-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="d64b6-130">刷新浏览器。</span><span class="sxs-lookup"><span data-stu-id="d64b6-130">Refresh your browser.</span></span>
4. <span data-ttu-id="d64b6-131">转到 **目管理与核算** > **定期** > **产能同步** > **同步资源产能汇总**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="d64b6-132">在 **产能汇总同步** 页面中，将 **删除现有产能记录** 设置为 **是** 以删除之前的数据。</span><span class="sxs-lookup"><span data-stu-id="d64b6-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d64b6-133">如果要生成增量数据，请将其设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="d64b6-134">在 **期间代码** 字段中，选择应生成数据的期间。</span><span class="sxs-lookup"><span data-stu-id="d64b6-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d64b6-135">如果选择期间代码，则无需定义开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="d64b6-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="d64b6-136">如果让 **期间代码** 字段保留为空，请选择特定的开始日期和结束日期以生成数据。</span><span class="sxs-lookup"><span data-stu-id="d64b6-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="d64b6-137">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d64b6-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d64b6-138">这将在您的环境中所有公司内把常规数据分发给 **ResRollup** 表，以便只需在一个法人中运行批处理作业。</span><span class="sxs-lookup"><span data-stu-id="d64b6-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d64b6-139">所有 **资源可用性** 视图都需要此批处理作业。</span><span class="sxs-lookup"><span data-stu-id="d64b6-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="d64b6-140">如果未运行此批处理作业，将即时生成 **ResRollup** 数据，这可能需要一些时间。</span><span class="sxs-lookup"><span data-stu-id="d64b6-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]