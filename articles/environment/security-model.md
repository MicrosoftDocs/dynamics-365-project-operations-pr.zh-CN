---
title: 安全模型
description: 本主题提供有关 Dynamics 365 Project Operations 中安全模型的信息。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3f65d13809fef342be8bec682c11d95c4d9e9b19
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276787"
---
# <a name="security-model"></a><span data-ttu-id="94f2e-103">安全模型</span><span class="sxs-lookup"><span data-stu-id="94f2e-103">Security Model</span></span>

<span data-ttu-id="94f2e-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="94f2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="94f2e-105">Microsoft Dynamics 365 Project Operations 包含一个唯一的安全模型，此模型允许使用与 Microsoft Office 组协作的基于角色的业务安全模型。</span><span class="sxs-lookup"><span data-stu-id="94f2e-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="94f2e-106">安全角色</span><span class="sxs-lookup"><span data-stu-id="94f2e-106">Security roles</span></span>
<span data-ttu-id="94f2e-107">Project Operations 前端功能包括下列角色：</span><span class="sxs-lookup"><span data-stu-id="94f2e-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="94f2e-108">角色</span><span class="sxs-lookup"><span data-stu-id="94f2e-108">Role</span></span>                          | <span data-ttu-id="94f2e-109">描述</span><span class="sxs-lookup"><span data-stu-id="94f2e-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="94f2e-110">作用域</span><span class="sxs-lookup"><span data-stu-id="94f2e-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="94f2e-111">实践经理</span><span class="sxs-lookup"><span data-stu-id="94f2e-111">Practice manager</span></span>              | <span data-ttu-id="94f2e-112">支持跨项目报告。</span><span class="sxs-lookup"><span data-stu-id="94f2e-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="94f2e-113">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-113">Business unit</span></span>              |
| <span data-ttu-id="94f2e-114">项目审批者</span><span class="sxs-lookup"><span data-stu-id="94f2e-114">Project approver</span></span>              | <span data-ttu-id="94f2e-115">审批项目的时间和支出。</span><span class="sxs-lookup"><span data-stu-id="94f2e-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="94f2e-116">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-116">Business unit</span></span> |
| <span data-ttu-id="94f2e-117">项目计费管理员</span><span class="sxs-lookup"><span data-stu-id="94f2e-117">Project billing administrator</span></span> | <span data-ttu-id="94f2e-118">创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="94f2e-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="94f2e-119">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-119">Business unit</span></span> |
| <span data-ttu-id="94f2e-120">项目经理</span><span class="sxs-lookup"><span data-stu-id="94f2e-120">Project manager</span></span>               | <span data-ttu-id="94f2e-121">创建项目计划与请求资源。</span><span class="sxs-lookup"><span data-stu-id="94f2e-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="94f2e-122">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-122">Business unit</span></span> |
| <span data-ttu-id="94f2e-123">项目资源</span><span class="sxs-lookup"><span data-stu-id="94f2e-123">Project resource</span></span>              | <span data-ttu-id="94f2e-124">可以被预订和报告时间的团队成员。</span><span class="sxs-lookup"><span data-stu-id="94f2e-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="94f2e-125">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-125">Business unit</span></span>|
| <span data-ttu-id="94f2e-126">资源经理</span><span class="sxs-lookup"><span data-stu-id="94f2e-126">Resource manager</span></span>              | <span data-ttu-id="94f2e-127">所有资源管理功能（如实施资源请求和预订）分开，以支持混合项目经理 + 资源经理配置以及单个和集中式资源经理角色。</span><span class="sxs-lookup"><span data-stu-id="94f2e-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="94f2e-128">业务部门</span><span class="sxs-lookup"><span data-stu-id="94f2e-128">Business unit</span></span> |


<span data-ttu-id="94f2e-129">Web 版本的 Microsoft Project 包含以下角色：</span><span class="sxs-lookup"><span data-stu-id="94f2e-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="94f2e-130">角色</span><span class="sxs-lookup"><span data-stu-id="94f2e-130">Role</span></span>           | <span data-ttu-id="94f2e-131">描述</span><span class="sxs-lookup"><span data-stu-id="94f2e-131">Description</span></span>                                                                                                        | <span data-ttu-id="94f2e-132">作用域</span><span class="sxs-lookup"><span data-stu-id="94f2e-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="94f2e-133">项目用户</span><span class="sxs-lookup"><span data-stu-id="94f2e-133">Project user</span></span>   | <span data-ttu-id="94f2e-134">项目的协作用户，可以创建自己的项目并查看与其共享的任何项目。</span><span class="sxs-lookup"><span data-stu-id="94f2e-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="94f2e-135">用户</span><span class="sxs-lookup"><span data-stu-id="94f2e-135">User</span></span>   |
| <span data-ttu-id="94f2e-136">项目系统</span><span class="sxs-lookup"><span data-stu-id="94f2e-136">Project system</span></span> | <span data-ttu-id="94f2e-137">用于应用程序上下文的角色。</span><span class="sxs-lookup"><span data-stu-id="94f2e-137">Role used for application   context.</span></span> <span data-ttu-id="94f2e-138">客户应该不会使用此系统角色。</span><span class="sxs-lookup"><span data-stu-id="94f2e-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="94f2e-139">全局</span><span class="sxs-lookup"><span data-stu-id="94f2e-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="94f2e-140">安全执行</span><span class="sxs-lookup"><span data-stu-id="94f2e-140">Security enforcement</span></span>
<span data-ttu-id="94f2e-141">在项目级别执行的操作将在已登录用户的上下文中执行。</span><span class="sxs-lookup"><span data-stu-id="94f2e-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="94f2e-142">这意味着，为了创建、打开或删除项目，用户需要在 CD 中有访问权限。</span><span class="sxs-lookup"><span data-stu-id="94f2e-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="94f2e-143">可通过平台中包括的任何可能的机制授予 CDS 中的访问权限。</span><span class="sxs-lookup"><span data-stu-id="94f2e-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="94f2e-144">例如，范围较大的用户可以访问项目，或者执行了明确的项目共享操作以授予用户访问权限。</span><span class="sxs-lookup"><span data-stu-id="94f2e-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="94f2e-145">在 Project Operations 中创建项目时，务必考虑这一点。</span><span class="sxs-lookup"><span data-stu-id="94f2e-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="94f2e-146">使用 Project Operations 进行新式组协作</span><span class="sxs-lookup"><span data-stu-id="94f2e-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="94f2e-147">Web 项目和 Project Operations 项目支持新式组进行协作。</span><span class="sxs-lookup"><span data-stu-id="94f2e-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="94f2e-148">通过组添加到项目中的用户可以编辑项目计划。</span><span class="sxs-lookup"><span data-stu-id="94f2e-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="94f2e-149">Web 项目会在分配后自动将用户添加到组中。</span><span class="sxs-lookup"><span data-stu-id="94f2e-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="94f2e-150">组允许提供项目权限和支持协作项目的协作工作。</span><span class="sxs-lookup"><span data-stu-id="94f2e-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="94f2e-151">下图描述了在组分配流程中发生的事件和状态更改。</span><span class="sxs-lookup"><span data-stu-id="94f2e-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="94f2e-152">Project Operations 不会通过隐式操作创建组，只会通过推进组建立的显式操作来创建组。</span><span class="sxs-lookup"><span data-stu-id="94f2e-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="94f2e-153">**组管理** 对话中的组成员搜索仅限于那些被设置为环境安全组一部分的用户。</span><span class="sxs-lookup"><span data-stu-id="94f2e-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="94f2e-154">有关详细信息，请参阅[控制用户对环境的访问权限：安全组和许可证](https://docs.microsoft.com/power-platform/admin/control-user-access)。</span><span class="sxs-lookup"><span data-stu-id="94f2e-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

![组模式](./media/groupsmode.png)

1. <span data-ttu-id="94f2e-156">项目由创建用户创建和负责。</span><span class="sxs-lookup"><span data-stu-id="94f2e-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="94f2e-157">项目负责人将更新到团队。</span><span class="sxs-lookup"><span data-stu-id="94f2e-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="94f2e-158">负责人团队会映射到指定或创建的 Office 组。</span><span class="sxs-lookup"><span data-stu-id="94f2e-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="94f2e-159">项目的原始负责人将添加到 Office 组中。</span><span class="sxs-lookup"><span data-stu-id="94f2e-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="94f2e-160">部署建议</span><span class="sxs-lookup"><span data-stu-id="94f2e-160">Deployment recommendation</span></span>
<span data-ttu-id="94f2e-161">随着 Office 组协作模型的发展，以后会添加功能来提供更详细的控制。</span><span class="sxs-lookup"><span data-stu-id="94f2e-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="94f2e-162">鼓励今天部署 Project Operations 的客户专注于传统的 Microsoft Dynamics 365 安全模型。</span><span class="sxs-lookup"><span data-stu-id="94f2e-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="94f2e-163">有关详细信息，请参阅 [Common Data Service 中的安全性](https://docs.microsoft.com/power-platform/admin/wp-security)。</span><span class="sxs-lookup"><span data-stu-id="94f2e-163">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="94f2e-164">Project Operations 和 Microsoft Dynamics 365 Finance 的安全性</span><span class="sxs-lookup"><span data-stu-id="94f2e-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="94f2e-165">Project Operations 包括以下角色：：</span><span class="sxs-lookup"><span data-stu-id="94f2e-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="94f2e-166">项目经理</span><span class="sxs-lookup"><span data-stu-id="94f2e-166">Project manager</span></span>
- <span data-ttu-id="94f2e-167">项目会计</span><span class="sxs-lookup"><span data-stu-id="94f2e-167">Project accountant</span></span>

<span data-ttu-id="94f2e-168">有关 Finance 中的安全性的详细信息，请参阅[基于角色的安全性](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)。</span><span class="sxs-lookup"><span data-stu-id="94f2e-168">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]