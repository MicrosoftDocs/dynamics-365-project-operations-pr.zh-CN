---
title: Project Service Automation 集成参数
description: 本主题介绍在将 Microsoft Dynamics 365 for Project Service Automation 与 Dynamics 365 Finance 集成时，如何配置默认数据的输入方式。
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749694"
---
# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="88b69-103">Project Service Automation 集成参数</span><span class="sxs-lookup"><span data-stu-id="88b69-103">Project Service Automation integration parameters</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="88b69-104">在将 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 集成时，可在 **Project Service Automation 集成参数**页面配置默认数据的输入方式。</span><span class="sxs-lookup"><span data-stu-id="88b69-104">On the **Project Service Automation integration parameters** page, you can configure how default data is entered when you integrate Dynamics 365 Project Service Automation with Dynamics 365 Finance.</span></span> <span data-ttu-id="88b69-105">必须设置以下字段，才能将项目从 Project Service Automation 成功同步到 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="88b69-105">For projects to be successfully synchronized from Project Service Automation to Finance, you must set up the following fields.</span></span>

<span data-ttu-id="88b69-106">若要打开 **Project Service Automation 集成参数**页，请转到**项目管理与核算** \> **设置** \> **Dynamics 365 for Project Service Automation 集成参数**。</span><span class="sxs-lookup"><span data-stu-id="88b69-106">To open the **Project Service Automation integration parameters** page, go to **Project management and accounting** \> **Setup** \> **Dynamics 365 for Project Service Automation integration parameters**.</span></span> 

> [!NOTE]
> - <span data-ttu-id="88b69-107">版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="88b69-107">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="88b69-108">版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="88b69-108">Actuals integration is available in version 8.0.1 or later.</span></span>


| <span data-ttu-id="88b69-109">Tab 键</span><span class="sxs-lookup"><span data-stu-id="88b69-109">Tab</span></span>                    | <span data-ttu-id="88b69-110">字段</span><span class="sxs-lookup"><span data-stu-id="88b69-110">Field</span></span>                | <span data-ttu-id="88b69-111">描述</span><span class="sxs-lookup"><span data-stu-id="88b69-111">Description</span></span> |
|------------------------|----------------------|-------------|
| <span data-ttu-id="88b69-112">常规</span><span class="sxs-lookup"><span data-stu-id="88b69-112">General</span></span>                | <span data-ttu-id="88b69-113">默认项目类型</span><span class="sxs-lookup"><span data-stu-id="88b69-113">Default project type</span></span> | <span data-ttu-id="88b69-114">选择默认项目类型。</span><span class="sxs-lookup"><span data-stu-id="88b69-114">Select the default project type.</span></span> <span data-ttu-id="88b69-115">从 Project Service Automation 同步项目时，如果在集成模板中不提供默认值，将使用该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-115">When projects are synchronized from Project Service Automation, this value is used if you didn't provide a default value in the integration template.</span></span> <span data-ttu-id="88b69-116">同步期间，将把新项目的**项目类型**字段设置为该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-116">During synchronization, the **Project type** field of new projects is set to this value.</span></span> <span data-ttu-id="88b69-117">但是，从 Project Service Automation 同步项目联系人行时，可能更新该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-117">However, the value might be updated when the project contract lines are synchronized from Project Service Automation.</span></span> |
|                        | <span data-ttu-id="88b69-118">时间类别</span><span class="sxs-lookup"><span data-stu-id="88b69-118">Time category</span></span>        | <span data-ttu-id="88b69-119">选择默认时间类别。</span><span class="sxs-lookup"><span data-stu-id="88b69-119">Select the default time category.</span></span> <span data-ttu-id="88b69-120">从 Project Service Automation 同步工时估计值时使用该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-120">This value is used when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="88b69-121">从 Project Service Automation 同步工时估计值和工时实际值时，Finance 中的新项目工时预测的**类别**字段将设置为该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-121">When the hour estimates and hour actuals are synchronized from Project Service Automation, the **Category** field of new project hour forecasts in Finance is set to this value.</span></span> |
|                        | <span data-ttu-id="88b69-122">费用类别</span><span class="sxs-lookup"><span data-stu-id="88b69-122">Fee category</span></span>         | <span data-ttu-id="88b69-123">选择默认费用类别。</span><span class="sxs-lookup"><span data-stu-id="88b69-123">Select the default fee category.</span></span> <span data-ttu-id="88b69-124">从 Project Service Automation 同步费用实际值时使用该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-124">This value is used when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="88b69-125">从 Project Service Automation 同步费用实际值时，Finance 中的新费用交易记录的**类别**字段将设置为该值。</span><span class="sxs-lookup"><span data-stu-id="88b69-125">When the fee actuals are synchronized from Project Service Automation, the **Category** field of new fee transactions in Finance is set to this value.</span></span> |
| <span data-ttu-id="88b69-126">项目组的默认值</span><span class="sxs-lookup"><span data-stu-id="88b69-126">Project group defaults</span></span> | <span data-ttu-id="88b69-127">项目类型</span><span class="sxs-lookup"><span data-stu-id="88b69-127">Project type</span></span>         | <span data-ttu-id="88b69-128">单击**新建**添加一行，可在该行中选择要为默认项目组设置的项目类型。</span><span class="sxs-lookup"><span data-stu-id="88b69-128">Click **New** to add a row where you can select the project type to set the default project group for.</span></span> <span data-ttu-id="88b69-129">在配置中，特定项目类型只能选择一次。</span><span class="sxs-lookup"><span data-stu-id="88b69-129">A specific project type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="88b69-130">项目组</span><span class="sxs-lookup"><span data-stu-id="88b69-130">Project group</span></span>        | <span data-ttu-id="88b69-131">为所选项目类型选择默认项目组。</span><span class="sxs-lookup"><span data-stu-id="88b69-131">Select the default project group for the selected project type.</span></span> <span data-ttu-id="88b69-132">从 Project Service Automation 同步新项目时，如果尚未在集成模板中提供默认值，**项目组**字段将设置为项目类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="88b69-132">When new projects are synchronized from Project Service Automation, the **Project group** field is set to the default value for the project type if you didn't provide a default value in the integration template.</span></span> |
| <span data-ttu-id="88b69-133">计费类型默认值</span><span class="sxs-lookup"><span data-stu-id="88b69-133">Billing type defaults</span></span>  | <span data-ttu-id="88b69-134">记帐类型</span><span class="sxs-lookup"><span data-stu-id="88b69-134">Billing type</span></span>         | <span data-ttu-id="88b69-135">单击**新建**添加一行，可在该行中选择要为默认行属性设置的计费类型。</span><span class="sxs-lookup"><span data-stu-id="88b69-135">Click **New** to add a row where you can select the billing type to set the default line property for.</span></span> <span data-ttu-id="88b69-136">在配置中，特定计费类型只能选择一次。</span><span class="sxs-lookup"><span data-stu-id="88b69-136">A specific billing type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="88b69-137">行属性</span><span class="sxs-lookup"><span data-stu-id="88b69-137">Line property</span></span>        | <span data-ttu-id="88b69-138">为所选计费类型选择默认行属性。</span><span class="sxs-lookup"><span data-stu-id="88b69-138">Select the default line property for the selected billing type.</span></span> <span data-ttu-id="88b69-139">从 Project Service Automation 同步新工时估计值、新费用估计值或新实际值时，**行属性**字段将设置为计费类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="88b69-139">When new hour estimates, new expense estimates, or new actuals are synchronized from Project Service Automation, the **Line property** field is set to the default value for the billing type.</span></span> |
| <span data-ttu-id="88b69-140">功能锁定</span><span class="sxs-lookup"><span data-stu-id="88b69-140">Functionality locking</span></span>  | <span data-ttu-id="88b69-141">不适用</span><span class="sxs-lookup"><span data-stu-id="88b69-141">Not applicable</span></span>       | <span data-ttu-id="88b69-142">为源自 Project Service Automation 的项目和合同选择要在 Finance 中禁用的功能。</span><span class="sxs-lookup"><span data-stu-id="88b69-142">Select the functionality to disable in Finance for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="88b69-143">例如，可关闭 Finance 中的编辑合同和项目，创建工作分解结构以及输入工时单功能。</span><span class="sxs-lookup"><span data-stu-id="88b69-143">For example, you can turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance.</span></span> <span data-ttu-id="88b69-144">将继续启用与核算有关的字段，即使根据参数设置这些字段不可用也不例外。</span><span class="sxs-lookup"><span data-stu-id="88b69-144">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="88b69-145">默认情况下，将启用所有功能。</span><span class="sxs-lookup"><span data-stu-id="88b69-145">By default, all functionality is enabled.</span></span> |