---
title: 将项目评估直接从 Project Service Automation 同步到 Finance and Operations
description: 此主题介绍用于将项目工时估计和项目费用估计直接从 Microsoft Dynamics 365 Project Service Automation 同步到 Dynamics 365 Finance 的模板和基础任务。
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072732"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="d6ef8-103">将项目评估直接从 Project Service Automation 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d6ef8-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d6ef8-104">此主题介绍用于直接同步 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 的项目工时估计和项目费用估计的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="d6ef8-105">版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="d6ef8-106">版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="d6ef8-107">Project Service Automation 到 Finance 的数据传输</span><span class="sxs-lookup"><span data-stu-id="d6ef8-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="d6ef8-108">Project Service Automation 到 Finance 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="d6ef8-109">可通过数据集成功能提供的集成模板将有关项目工时估计值和项目支出估计值的数据从 Project Service Automation 传输到 Finance。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="d6ef8-110">下图显示 Project Service Automation 与 Finance 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="d6ef8-111">[![Project Service Automation 与 Finance 集成的数据传输](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="d6ef8-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="d6ef8-112">项目工时估计值</span><span class="sxs-lookup"><span data-stu-id="d6ef8-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="d6ef8-113">模板和任务</span><span class="sxs-lookup"><span data-stu-id="d6ef8-113">Template and tasks</span></span>

<span data-ttu-id="d6ef8-114">若要访问可用模板，请在 Microsoft Power Apps 管理员中心中选择 **项目** ，然后在右上角中选择 **新建项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d6ef8-115">以下模板和基础任务用于将项目工时估计值从 Project Service Automation 同步到 Finance：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="d6ef8-116">**数据集成中的模板名称：** 项目工时估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="d6ef8-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="d6ef8-117">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="d6ef8-118">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="d6ef8-118">Transaction relationships</span></span>
    - <span data-ttu-id="d6ef8-119">费用估算</span><span class="sxs-lookup"><span data-stu-id="d6ef8-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="d6ef8-120">实体集</span><span class="sxs-lookup"><span data-stu-id="d6ef8-120">Entity set</span></span>

| <span data-ttu-id="d6ef8-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d6ef8-121">Project Service Automation</span></span> | <span data-ttu-id="d6ef8-122">财经</span><span class="sxs-lookup"><span data-stu-id="d6ef8-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d6ef8-123">项目任务</span><span class="sxs-lookup"><span data-stu-id="d6ef8-123">Project tasks</span></span>              | <span data-ttu-id="d6ef8-124">项目工时估计集成实体</span><span class="sxs-lookup"><span data-stu-id="d6ef8-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="d6ef8-125">实体流</span><span class="sxs-lookup"><span data-stu-id="d6ef8-125">Entity flow</span></span>

<span data-ttu-id="d6ef8-126">项目工时估计值在 Project Service Automation 中管理，并同步到 Finance 中充当项目工时预测。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d6ef8-127">先决条件</span><span class="sxs-lookup"><span data-stu-id="d6ef8-127">Prerequisites</span></span>

<span data-ttu-id="d6ef8-128">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目工时估计值。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="d6ef8-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="d6ef8-129">Power Query</span></span>

<span data-ttu-id="d6ef8-130">在项目工时估计值模板中，必须使用 Microsoft Power Query for Excel 才能完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="d6ef8-131">设置将在集成新建工时预测时使用的默认预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="d6ef8-132">筛选掉任务中所有资源特定的且将导致与工时预测集成失败的记录。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="d6ef8-133">筛选掉所有空交易记录类别行。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="d6ef8-134">如果未能完成此任务，可能导致工时预测不正确。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="d6ef8-135">设置默认预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="d6ef8-135">Set the default forecast model ID</span></span>

<span data-ttu-id="d6ef8-136">若要更新模板中的默认预测模型 ID，请单击 **映射** 箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="d6ef8-137">选择 **高级查询和筛选** 链接。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="d6ef8-138">如果在使用默认项目工时估计值（PSA 到 Fin and Ops）模板，请在 **应用的步骤** 列表中选择 **插入的条件** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="d6ef8-139">在 **函数** 条目中，将 **O\_forecast** 替换为集成应使用的预测模型 ID 的名称。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="d6ef8-140">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="d6ef8-141">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="d6ef8-142">在 Power Query 中，选择 **添加条件列** ，然后为新列输入名称，如 **ModelID** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="d6ef8-143">输入列的条件：where, if Project task is not null, then \<enter the forecast model ID\>; else null。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="d6ef8-144">筛选掉资源特定的记录</span><span class="sxs-lookup"><span data-stu-id="d6ef8-144">Filter out resource-specific records</span></span>

<span data-ttu-id="d6ef8-145">项目工时估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于去除资源特定的所有记录。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="d6ef8-146">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="d6ef8-147">选择 **高级查询和筛选** 链接以筛选 **msdyn\_islinetask** 列，以便仅包含 **False** 记录。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="d6ef8-148">筛选掉空交易记录类别行</span><span class="sxs-lookup"><span data-stu-id="d6ef8-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="d6ef8-149">必须添加筛选器以移除包含空交易记录类别的所有行。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="d6ef8-150">无论使用默认模板还是创建自己的模板，都需要执行此任务。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="d6ef8-151">此筛选器移除来自 Project Service Automation 且可能导致 Finance 中的工时预测不正确的所有汇总行。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="d6ef8-152">选择 **高级查询和筛选** 链接以筛选掉 **msdyn\_transactioncategory\_value** 列中的空记录。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d6ef8-153">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="d6ef8-153">Template mapping in Data integration</span></span>

<span data-ttu-id="d6ef8-154">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="d6ef8-155">此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="d6ef8-156">[![数据集成中的模板任务映射](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="d6ef8-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="d6ef8-157">项目支出估计值</span><span class="sxs-lookup"><span data-stu-id="d6ef8-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="d6ef8-158">模板和任务</span><span class="sxs-lookup"><span data-stu-id="d6ef8-158">Template and tasks</span></span>

<span data-ttu-id="d6ef8-159">以下模板和基础任务用于将项目费用估计值从 Project Service Automation 同步到 Finance：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="d6ef8-160">**数据集成中的模板名称：** 项目支出估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="d6ef8-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="d6ef8-161">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="d6ef8-162">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="d6ef8-162">Transaction relationships</span></span> 
    - <span data-ttu-id="d6ef8-163">费用估算</span><span class="sxs-lookup"><span data-stu-id="d6ef8-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="d6ef8-164">实体集</span><span class="sxs-lookup"><span data-stu-id="d6ef8-164">Entity set</span></span>

| <span data-ttu-id="d6ef8-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d6ef8-165">Project Service Automation</span></span> | <span data-ttu-id="d6ef8-166">财经</span><span class="sxs-lookup"><span data-stu-id="d6ef8-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="d6ef8-167">交易连接</span><span class="sxs-lookup"><span data-stu-id="d6ef8-167">Transaction Connections</span></span>    | <span data-ttu-id="d6ef8-168">项目交易记录关系的集成实体</span><span class="sxs-lookup"><span data-stu-id="d6ef8-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="d6ef8-169">估计行</span><span class="sxs-lookup"><span data-stu-id="d6ef8-169">Estimate Lines</span></span>             | <span data-ttu-id="d6ef8-170">项目费用估计值的集成实体</span><span class="sxs-lookup"><span data-stu-id="d6ef8-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="d6ef8-171">实体流</span><span class="sxs-lookup"><span data-stu-id="d6ef8-171">Entity flow</span></span>

<span data-ttu-id="d6ef8-172">项目支出估计值在 Project Service Automation 中管理，并同步到 Finance 中充当项目支出预测。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d6ef8-173">先决条件</span><span class="sxs-lookup"><span data-stu-id="d6ef8-173">Prerequisites</span></span>

<span data-ttu-id="d6ef8-174">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目支出估计值。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="d6ef8-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="d6ef8-175">Power Query</span></span>

<span data-ttu-id="d6ef8-176">在项目支出估计值模板中，必须使用 Power Query 才能完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="d6ef8-177">筛选为仅包含支出估计值行记录。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="d6ef8-178">设置将在集成新建工时预测时使用的默认预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="d6ef8-179">转换计费类型。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-179">Transform the billing types.</span></span>
- <span data-ttu-id="d6ef8-180">转换交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="d6ef8-181">筛选为仅包含支出估计值行</span><span class="sxs-lookup"><span data-stu-id="d6ef8-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="d6ef8-182">项目支出估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于筛选为集成中仅包含支出行。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="d6ef8-183">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="d6ef8-184">选择 **交易记录关系** 任务，然后单击 **映射** 箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="d6ef8-185">选择 **高级查询和筛选** 链接。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="d6ef8-186">筛选 **msdyn\_transactiontype1** 列，以便其中仅包含 **msdyn\_estimateline** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="d6ef8-187">设置默认预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="d6ef8-187">Set the default forecast model ID</span></span>

<span data-ttu-id="d6ef8-188">若要更新模板中的默认预测模型 ID，请选择 **支出估计值** 任务，然后单击 **映射** 箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="d6ef8-189">选择 **高级查询和筛选** 链接。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="d6ef8-190">如果在使用默认的项目支出类别（PSA 到 Fin and Ops）模板，请在 Power Query, 中从 **应用的步骤** 部分选择第一个 **插入的条件** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="d6ef8-191">在 **函数** 条目中，将 **O\_forecast** 替换为集成应使用的预测模型 ID 的名称。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="d6ef8-192">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="d6ef8-193">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="d6ef8-194">在 Power Query 中，选择 **添加条件列** ，然后为新列输入名称，如 **ModelID** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="d6ef8-195">输入列的条件：where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="d6ef8-196">转换计费类型</span><span class="sxs-lookup"><span data-stu-id="d6ef8-196">Transform the billing types</span></span>

<span data-ttu-id="d6ef8-197">项目支出估计值（PSA 到 Fin and Ops）模板包含一个条件列，用于转换集成期间从 Project Service Automation 收到的计费类型。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="d6ef8-198">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="d6ef8-199">选择 **高级查询和筛选** 链接，然后选择 **添加条件列** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="d6ef8-200">为新列输入名称，如 **BillingType** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="d6ef8-201">然后输入以下条件：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-201">Then enter the following condition:</span></span>

<span data-ttu-id="d6ef8-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="d6ef8-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="d6ef8-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="d6ef8-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="d6ef8-206">转换交易记录类型</span><span class="sxs-lookup"><span data-stu-id="d6ef8-206">Transform the transaction types</span></span>

<span data-ttu-id="d6ef8-207">项目支出估计值（PSA 到 Fin and Ops）模板包含一个条件列，用于转换集成期间从 Project Service Automation 收到的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="d6ef8-208">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="d6ef8-209">选择 **高级查询和筛选** 链接，然后选择 **添加条件列** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="d6ef8-210">为新列输入名称，如 **TransactionType** 。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="d6ef8-211">然后输入以下条件：</span><span class="sxs-lookup"><span data-stu-id="d6ef8-211">Then enter the following condition:</span></span>

<span data-ttu-id="d6ef8-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="d6ef8-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="d6ef8-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="d6ef8-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d6ef8-215">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="d6ef8-215">Template mapping in Data integration</span></span>

<span data-ttu-id="d6ef8-216">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="d6ef8-217">此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="d6ef8-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="d6ef8-218">[![支出估算交易的模板映射](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="d6ef8-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="d6ef8-219">[![支出估算的模板映射](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="d6ef8-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>