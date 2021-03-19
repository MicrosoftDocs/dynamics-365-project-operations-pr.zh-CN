---
title: 在 Finance and Operations 和 Project Service Automation 之间同步项目支出类别
description: 此主题介绍用于将项目费用类别直接从 Microsoft Dynamics 365 Finance 同步到 Dynamics 365 Project Service Automation 的模板和基础任务。
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289628"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="572f0-103">在 Finance and Operations 和 Project Service Automation 之间同步项目支出类别</span><span class="sxs-lookup"><span data-stu-id="572f0-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="572f0-104">此主题介绍用于直接同步 Dynamics 365 Finance 与 Dynamics 365 Project Service Automation 之间的项目费用类别的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="572f0-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="572f0-105">版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="572f0-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="572f0-106">版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="572f0-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="572f0-107">如果您正在使用 Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="572f0-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="572f0-108">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="572f0-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="572f0-109">Project Service Automation 与 Finance 之间的数据传输</span><span class="sxs-lookup"><span data-stu-id="572f0-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="572f0-110">Project Service Automation 与 Finance 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="572f0-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="572f0-111">可通过数据集成功能提供的集成模板在 Finance 与 Project Service Automation 之间传输有关项目支出交易记录类别的数据。</span><span class="sxs-lookup"><span data-stu-id="572f0-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="572f0-112">如果项目支出类别掌握在 Finance 中，则集成流首先从 Finance 到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="572f0-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="572f0-113">然后，通过从 Project Service Automation 到 Finance 的同步更新项目支出类别的集成 ID。</span><span class="sxs-lookup"><span data-stu-id="572f0-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="572f0-114">如果项目支出类别掌握在 Project Service Automation 中，则集成流首先从 Project Service Automation 到 Finance。</span><span class="sxs-lookup"><span data-stu-id="572f0-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="572f0-115">从 Project Service Automation 同步之前，必须已在 Finance 中配置了项目类别。</span><span class="sxs-lookup"><span data-stu-id="572f0-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="572f0-116">然后从 Finance 同步回 Project Service Automation，然后再次从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="572f0-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="572f0-117">这样就可以帮助确保链接类别，并且不创建重复项。</span><span class="sxs-lookup"><span data-stu-id="572f0-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="572f0-118">项目支出类别通常掌握在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="572f0-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="572f0-119">但是，如果不是，或者如果已在 Project Service Automation 中创建了支出类别，则必须首先通过使用支出交易记录类别（PSA 到 Fin and Ops）模板进行同步。</span><span class="sxs-lookup"><span data-stu-id="572f0-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="572f0-120">然后通过使用项目支出交易记录类别（Fin and Ops 到 PSA）模板进行同步。</span><span class="sxs-lookup"><span data-stu-id="572f0-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="572f0-121">然后应再次运行从 Project Service Automation 到 Finance 的同步。</span><span class="sxs-lookup"><span data-stu-id="572f0-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="572f0-122">如果首先从 Project Service Automation 同步，则必须先在 Finance 中满足以下要求，才能运行同步：</span><span class="sxs-lookup"><span data-stu-id="572f0-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="572f0-123">必须有与 Project Service Automation 中设置的项目类别匹配的共享类别，并且必须同时为 **项目** 和 **支出** 启用该共享类别。</span><span class="sxs-lookup"><span data-stu-id="572f0-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="572f0-124">对于必须集成的每个 Finance 法人，必须有以下项目类别：</span><span class="sxs-lookup"><span data-stu-id="572f0-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="572f0-125">有 **项目类别**。</span><span class="sxs-lookup"><span data-stu-id="572f0-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="572f0-126">已启用 **在支出使用**。</span><span class="sxs-lookup"><span data-stu-id="572f0-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="572f0-127">已启用 **在日记帐中有效**。</span><span class="sxs-lookup"><span data-stu-id="572f0-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="572f0-128">**交易记录类型** 设置为 **支出**。</span><span class="sxs-lookup"><span data-stu-id="572f0-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="572f0-129">下图显示 Project Service Automation 与 Finance 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="572f0-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="572f0-130">[![Project Service Automation 与 Finance 集成的数据传输](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="572f0-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="572f0-131">从 Finance 到 Project Service Automation 的项目支出类别同步</span><span class="sxs-lookup"><span data-stu-id="572f0-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="572f0-132">模板和任务</span><span class="sxs-lookup"><span data-stu-id="572f0-132">Template and task</span></span>

<span data-ttu-id="572f0-133">若要访问此模板，请在 Microsoft Power Apps 管理员中心中选择 **项目**，然后在右上角中选择 **新建项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="572f0-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="572f0-134">以下模板和基础任务用于将项目支出类别从 Finance 同步到 Project Service Automation：</span><span class="sxs-lookup"><span data-stu-id="572f0-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="572f0-135">**数据集成中的模板名称：** 项目支出交易记录类别（Fin and Ops 到 PSA）</span><span class="sxs-lookup"><span data-stu-id="572f0-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="572f0-136">**项目中任务的名称：** 将类别同步到 PSA</span><span class="sxs-lookup"><span data-stu-id="572f0-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="572f0-137">实体集</span><span class="sxs-lookup"><span data-stu-id="572f0-137">Entity set</span></span>

| <span data-ttu-id="572f0-138">财经</span><span class="sxs-lookup"><span data-stu-id="572f0-138">Finance</span></span>                           | <span data-ttu-id="572f0-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="572f0-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="572f0-140">类别的集成实体</span><span class="sxs-lookup"><span data-stu-id="572f0-140">Integration entity for categories</span></span> | <span data-ttu-id="572f0-141">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="572f0-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="572f0-142">实体流</span><span class="sxs-lookup"><span data-stu-id="572f0-142">Entity flow</span></span>

<span data-ttu-id="572f0-143">项目支出类别掌握在 Finance 中，并且作为交易记录类别同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="572f0-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="572f0-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="572f0-144">Power Query</span></span>

<span data-ttu-id="572f0-145">同步到 Project Service Automation 时，必须使用 Microsoft Power Query for Excel 为交易记录类别设置计费类型。</span><span class="sxs-lookup"><span data-stu-id="572f0-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="572f0-146">项目支出交易记录类别（Fin and Ops 到 PSA）提供默认列和映射。</span><span class="sxs-lookup"><span data-stu-id="572f0-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="572f0-147">如果创建自己的模板，则必须在 Power Query 中添加一个条件列。</span><span class="sxs-lookup"><span data-stu-id="572f0-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="572f0-148">请按照以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="572f0-148">Follow these steps.</span></span>

1. <span data-ttu-id="572f0-149">单击箭头在项目支出交易记录类别（Fin and Ops 到 PSA）模板中打开项目支出类别任务的映射。</span><span class="sxs-lookup"><span data-stu-id="572f0-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="572f0-150">单击 **高级查询和筛选** 链接以打开 Power Query。</span><span class="sxs-lookup"><span data-stu-id="572f0-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="572f0-151">选择 **添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="572f0-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="572f0-152">为新列输入名称，如 **BillingType**。</span><span class="sxs-lookup"><span data-stu-id="572f0-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="572f0-153">输入以下条件：**if CATEGORYID not equal to null then 19235001, Otherwise null**。</span><span class="sxs-lookup"><span data-stu-id="572f0-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="572f0-154">在列中单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="572f0-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="572f0-155">请务必在映射页上映射这个新列。</span><span class="sxs-lookup"><span data-stu-id="572f0-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="572f0-156">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="572f0-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="572f0-157">此映射显示将从 Finance 同步到 Project Service Automation 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="572f0-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="572f0-158">[![项目支出类别到 Project Service Automation 的模板映射](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="572f0-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="572f0-159">从 Project Service Automation 到 Finance 的项目支出类别同步</span><span class="sxs-lookup"><span data-stu-id="572f0-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="572f0-160">模板和任务</span><span class="sxs-lookup"><span data-stu-id="572f0-160">Template and task</span></span>

<span data-ttu-id="572f0-161">以下模板和基础任务用于将项目支出类别从 Project Service Automation 同步到 Finance：</span><span class="sxs-lookup"><span data-stu-id="572f0-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="572f0-162">**数据集成中的模板名称：** 项目支出交易记录类别（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="572f0-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="572f0-163">**项目中任务的名称：** 将类别同步到 Fin Ops</span><span class="sxs-lookup"><span data-stu-id="572f0-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="572f0-164">实体集</span><span class="sxs-lookup"><span data-stu-id="572f0-164">Entity set</span></span>

| <span data-ttu-id="572f0-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="572f0-165">Project Service Automation</span></span> | <span data-ttu-id="572f0-166">财经</span><span class="sxs-lookup"><span data-stu-id="572f0-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="572f0-167">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="572f0-167">Transaction categories</span></span>     | <span data-ttu-id="572f0-168">类别的集成实体</span><span class="sxs-lookup"><span data-stu-id="572f0-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="572f0-169">实体流</span><span class="sxs-lookup"><span data-stu-id="572f0-169">Entity flow</span></span>

<span data-ttu-id="572f0-170">项目支出类别掌握在 Finance 中，并且作为交易记录类别同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="572f0-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="572f0-171">同步回 Finance 将更新 Finance 项目类别中来自 Project Service Automation 的项目类别。</span><span class="sxs-lookup"><span data-stu-id="572f0-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="572f0-172">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="572f0-172">Template mapping in Data integration</span></span>

<span data-ttu-id="572f0-173">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="572f0-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="572f0-174">此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="572f0-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="572f0-175">[![Project Service Automation 到 Finance 的模板映射](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="572f0-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]