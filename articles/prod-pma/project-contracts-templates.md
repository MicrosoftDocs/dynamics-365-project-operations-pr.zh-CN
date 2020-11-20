---
title: 将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations
description: 此主题介绍用于将项目合同和项目直接从 Microsoft  Dynamics 365 Project Service Automation 同步到 Dynamics 365 Finance 的模板和基础任务。
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e4f11ec0bb88ed0971a3d082e7ca7823fcf8453
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072738"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a94e0-103">将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a94e0-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a94e0-104">此主题介绍用于直接同步 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 的项目合同和项目的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="a94e0-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="a94e0-105">如果在使用 Enterprise edition 7.3.0，则必须安装 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="a94e0-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a94e0-106">Project Service Automation 到 Finance 的数据传输</span><span class="sxs-lookup"><span data-stu-id="a94e0-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="a94e0-107">应先熟悉 Dynamics 365 Data integration 功能，才能使用 Project Service Automation 到 Finance 集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="a94e0-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="a94e0-108">Project Service Automation 到 Finance 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="a94e0-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a94e0-109">可通过数据集成功能提供的集成模板将有关项目合同、项目、项目合同行和项目合同行里程碑的数据从 Project Service Automation 传输到 Finance。</span><span class="sxs-lookup"><span data-stu-id="a94e0-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a94e0-110">下图显示 Project Service Automation 与 Finance 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="a94e0-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a94e0-111">[![Project Service Automation 与 Finance 集成的数据传输](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="a94e0-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a94e0-112">模板和任务</span><span class="sxs-lookup"><span data-stu-id="a94e0-112">Templates and tasks</span></span>

<span data-ttu-id="a94e0-113">若要访问可用模板，请在 Microsoft Power Apps 管理员中心中选择 **项目** ，然后在右上角中选择 **新建项目** 以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="a94e0-113">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a94e0-114">以下模板和基础任务用于将项目合同和项目从 Project Service Automation 同步到 Finance：</span><span class="sxs-lookup"><span data-stu-id="a94e0-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="a94e0-115">与 Dynamics 365 Project Service Automation v2.x 集成</span><span class="sxs-lookup"><span data-stu-id="a94e0-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="a94e0-116">**数据集成中的模板名称：** 项目和合同（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-116">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a94e0-117">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="a94e0-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a94e0-118">项目合同（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-118">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-119">项目（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-119">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-120">项目合同行（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-120">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-121">项目合同行里程碑（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-121">Project contract line milestones PSA to Fin and Ops</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="a94e0-122">与 Dynamics 365 Project Service Automation v3.x 集成</span><span class="sxs-lookup"><span data-stu-id="a94e0-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="a94e0-123">Project Service Automation 中有一项会影响项目合同行里程碑模板的架构更改，需要使用此模板的 v2 版才能将 Project Service Automation v3.x 与 Dynamics 365 集成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="a94e0-124">**数据集成中的模板名称：** 项目和合同（PSA 3.x 到 Fin and Ops）- v2</span><span class="sxs-lookup"><span data-stu-id="a94e0-124">**Name of the template in Data integration:** Projects and Contracts (PSA 3.x to Fin and Ops) - v2</span></span>
- <span data-ttu-id="a94e0-125">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="a94e0-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a94e0-126">项目合同（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-126">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-127">项目（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-127">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-128">项目合同行（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-128">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="a94e0-129">项目合同行里程碑（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="a94e0-129">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="a94e0-130">必须先同步科目，才能同步项目合同和项目。</span><span class="sxs-lookup"><span data-stu-id="a94e0-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a94e0-131">实体集</span><span class="sxs-lookup"><span data-stu-id="a94e0-131">Entity set</span></span>

| <span data-ttu-id="a94e0-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a94e0-132">Project Service Automation</span></span>       | <span data-ttu-id="a94e0-133">财经</span><span class="sxs-lookup"><span data-stu-id="a94e0-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="a94e0-134">订单</span><span class="sxs-lookup"><span data-stu-id="a94e0-134">Orders</span></span>                           | <span data-ttu-id="a94e0-135">项目合同集成实体</span><span class="sxs-lookup"><span data-stu-id="a94e0-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="a94e0-136">项目</span><span class="sxs-lookup"><span data-stu-id="a94e0-136">Projects</span></span>                         | <span data-ttu-id="a94e0-137">项目的集成实体</span><span class="sxs-lookup"><span data-stu-id="a94e0-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="a94e0-138">订单明细</span><span class="sxs-lookup"><span data-stu-id="a94e0-138">Order lines</span></span>                      | <span data-ttu-id="a94e0-139">项目合同行集成实体</span><span class="sxs-lookup"><span data-stu-id="a94e0-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="a94e0-140">项目合同行里程碑</span><span class="sxs-lookup"><span data-stu-id="a94e0-140">Project contract line milestones</span></span> | <span data-ttu-id="a94e0-141">项目合同行里程碑集成实体</span><span class="sxs-lookup"><span data-stu-id="a94e0-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a94e0-142">实体流</span><span class="sxs-lookup"><span data-stu-id="a94e0-142">Entity flow</span></span>

<span data-ttu-id="a94e0-143">项目合同在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同。</span><span class="sxs-lookup"><span data-stu-id="a94e0-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="a94e0-144">在集成模板中，可在 Finance 中为项目合同设置集成源。</span><span class="sxs-lookup"><span data-stu-id="a94e0-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="a94e0-145">时间和物料项目和固定价格项目在 Project Service Automation 中管理，并同步到 Finance 中充当项目。</span><span class="sxs-lookup"><span data-stu-id="a94e0-145">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance as projects.</span></span> <span data-ttu-id="a94e0-146">在模板集成中，可在 Finance 中为项目设置集成源。</span><span class="sxs-lookup"><span data-stu-id="a94e0-146">As part of the template integration, you can set the integration source in Finance for the project.</span></span>

<span data-ttu-id="a94e0-147">项目合同行在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同计费规则。</span><span class="sxs-lookup"><span data-stu-id="a94e0-147">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="a94e0-148">如果交付方法与默认项目类型不同，同步将更新合同行项目和项目组的项目类型。</span><span class="sxs-lookup"><span data-stu-id="a94e0-148">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="a94e0-149">项目合同行里程碑在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同计费规则里程碑。</span><span class="sxs-lookup"><span data-stu-id="a94e0-149">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="a94e0-150">Project Service Automation 到 Finance 集成解决方案</span><span class="sxs-lookup"><span data-stu-id="a94e0-150">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="a94e0-151">**项目合同** 页上有 **项目合同 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="a94e0-151">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="a94e0-152">该字段由一个自然唯一密钥组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-152">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="a94e0-153">新建项目合同时，如果 **项目合同 ID** 值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-153">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a94e0-154">该值由 **ORD** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-154">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a94e0-155">下面是一个示例： **ORD-01022-Z4M9Q0** 。</span><span class="sxs-lookup"><span data-stu-id="a94e0-155">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="a94e0-156">**项目编号** 字段在 **项目** 页提供。</span><span class="sxs-lookup"><span data-stu-id="a94e0-156">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="a94e0-157">该字段由一个自然唯一密钥组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-157">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="a94e0-158">新建项目时，如果 **项目编号** 值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-158">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a94e0-159">该值由 **PRJ** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="a94e0-159">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a94e0-160">下面是一个示例： **PRJ-01049-CCNID0** 。</span><span class="sxs-lookup"><span data-stu-id="a94e0-160">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="a94e0-161">应用 Project Service Automation 到 Finance 集成解决方案时，升级脚本将在 Project Service Automation 为现有项目合同设置 **项目合同 ID** 字段，为现有项目设置 **项目编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="a94e0-161">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a94e0-162">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="a94e0-162">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="a94e0-163">必须先同步科目，才能同步项目合同和项目。</span><span class="sxs-lookup"><span data-stu-id="a94e0-163">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="a94e0-164">在连接集中，向 **msdyn\_name \[Name\]** 添加 **msdyn\_organizationalunits** 的集成密钥字段映射。</span><span class="sxs-lookup"><span data-stu-id="a94e0-164">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="a94e0-165">可能首先需要向连接集添加一个项目。</span><span class="sxs-lookup"><span data-stu-id="a94e0-165">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="a94e0-166">有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="a94e0-166">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="a94e0-167">在连接集中，向 **msdynce\_projectnumber \[Project Number\]** 添加 **msdyn\_projects** 的集成密钥字段映射。</span><span class="sxs-lookup"><span data-stu-id="a94e0-167">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="a94e0-168">可能首先需要向连接集添加一个项目。</span><span class="sxs-lookup"><span data-stu-id="a94e0-168">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="a94e0-169">有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="a94e0-169">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="a94e0-170">可将项目合同和项目的 **SourceDataID** 更新为其他值，也可以将其从映射中移除。</span><span class="sxs-lookup"><span data-stu-id="a94e0-170">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="a94e0-171">默认模板值为 **Project Service Automation** 。</span><span class="sxs-lookup"><span data-stu-id="a94e0-171">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="a94e0-172">必须更新 **PaymentTerms** 映射，才能在 Finance 中体现有效的付款期限。</span><span class="sxs-lookup"><span data-stu-id="a94e0-172">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="a94e0-173">也可以从项目任务中移除映射。</span><span class="sxs-lookup"><span data-stu-id="a94e0-173">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="a94e0-174">默认值映射具有演示数据的默认值。</span><span class="sxs-lookup"><span data-stu-id="a94e0-174">The default value map has default values for demo data.</span></span> <span data-ttu-id="a94e0-175">下表显示 Project Service Automation 中的值。</span><span class="sxs-lookup"><span data-stu-id="a94e0-175">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="a94e0-176">Value</span><span class="sxs-lookup"><span data-stu-id="a94e0-176">Value</span></span> | <span data-ttu-id="a94e0-177">描述</span><span class="sxs-lookup"><span data-stu-id="a94e0-177">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="a94e0-178">7</span><span class="sxs-lookup"><span data-stu-id="a94e0-178">1</span></span>     | <span data-ttu-id="a94e0-179">N30</span><span class="sxs-lookup"><span data-stu-id="a94e0-179">Net 30</span></span>        |
    | <span data-ttu-id="a94e0-180">2</span><span class="sxs-lookup"><span data-stu-id="a94e0-180">2</span></span>     | <span data-ttu-id="a94e0-181">2/10 N30</span><span class="sxs-lookup"><span data-stu-id="a94e0-181">2% 10, Net 30</span></span> |
    | <span data-ttu-id="a94e0-182">3</span><span class="sxs-lookup"><span data-stu-id="a94e0-182">3</span></span>     | <span data-ttu-id="a94e0-183">N45</span><span class="sxs-lookup"><span data-stu-id="a94e0-183">Net 45</span></span>        |
    | <span data-ttu-id="a94e0-184">4</span><span class="sxs-lookup"><span data-stu-id="a94e0-184">4</span></span>     | <span data-ttu-id="a94e0-185">N60</span><span class="sxs-lookup"><span data-stu-id="a94e0-185">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="a94e0-186">Power Query</span><span class="sxs-lookup"><span data-stu-id="a94e0-186">Power Query</span></span>

<span data-ttu-id="a94e0-187">如果满足以下条件，则必须使用 Microsoft Power Query for Excel：</span><span class="sxs-lookup"><span data-stu-id="a94e0-187">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="a94e0-188">您在 Dynamics 365 Sales 中有销售订单。</span><span class="sxs-lookup"><span data-stu-id="a94e0-188">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="a94e0-189">您在 Project Service Automation 中有多个组织单位，并且这些组织单位将映射到 Finance 中的多个法人。</span><span class="sxs-lookup"><span data-stu-id="a94e0-189">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="a94e0-190">如果必须使用 Power Query，请遵守以下准则：</span><span class="sxs-lookup"><span data-stu-id="a94e0-190">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="a94e0-191">项目和合同（PSA 到 Fin and Ops）模板有一个默认筛选器，其中仅包含类型为 **工作项 (msdyn\_ordertype = 192350001)** 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a94e0-191">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="a94e0-192">此筛选器有助于确保不在 Finance 中为销售订单创建项目合同。</span><span class="sxs-lookup"><span data-stu-id="a94e0-192">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="a94e0-193">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="a94e0-193">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="a94e0-194">创建的 Power Query 筛选器必须仅包含应同步到集成连接集的法人的合同组织。</span><span class="sxs-lookup"><span data-stu-id="a94e0-194">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="a94e0-195">例如，应将您的包含合同组织单位 Contoso US 的项目合同同步到 USSI 法人，但您的包含合同组织单位 Contoso Global 的项目合同则应同步到 USMF 法人。</span><span class="sxs-lookup"><span data-stu-id="a94e0-195">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="a94e0-196">如果不向任务映射添加此筛选器，则将把所有项目合同同步到为连接集定义的法人，而不考虑合同组织单位。</span><span class="sxs-lookup"><span data-stu-id="a94e0-196">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a94e0-197">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="a94e0-197">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="a94e0-198">项目合同的默认映射中不包含 **CustomerReference** 、 **AddressCity** 、 **AddressCountryRegionID** 、 **AddressDescription** 、 **AddressLine1** 、 **AddressLine2** 、 **AddressState** 和 **AddressZipCode** 字段。</span><span class="sxs-lookup"><span data-stu-id="a94e0-198">The **CustomerReference** , **AddressCity** , **AddressCountryRegionID** , **AddressDescription** , **AddressLine1** , **AddressLine2** , **AddressState** , and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="a94e0-199">如果需要为项目合同同步此数据，可添加这些映射。</span><span class="sxs-lookup"><span data-stu-id="a94e0-199">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="a94e0-200">项目的默认映射中不包含 **Description** 、 **ParentID** 、 **ProjectGroup** 、 **ProjectManagerPersonnelNumber** 和 **ProjectType** 字段。</span><span class="sxs-lookup"><span data-stu-id="a94e0-200">The **Description** , **ParentID** , **ProjectGroup** , **ProjectManagerPersonnelNumber** , and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="a94e0-201">如果需要为项目同步此数据，可添加这些映射。</span><span class="sxs-lookup"><span data-stu-id="a94e0-201">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="a94e0-202">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="a94e0-202">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="a94e0-203">此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="a94e0-203">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a94e0-204">[![项目合同模板映射](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="a94e0-204">[![Project contract template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="a94e0-205">[![项目模板映射](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="a94e0-205">[![Project template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="a94e0-206">[![项目合同子项模板映射](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="a94e0-206">[![Project contract lines template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="a94e0-207">[![项目合同子项里程碑模板映射](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="a94e0-207">[![Project contract line milestone template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="a94e0-208">项目和合同中的项目合同行里程碑映射（PSA 3.x 到 Dynamics）- v2 模板：</span><span class="sxs-lookup"><span data-stu-id="a94e0-208">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="a94e0-209">[![使用第二版模板的项目合同子项里程碑映射](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="a94e0-209">[![Project contract line milestone mapping with version two template](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>