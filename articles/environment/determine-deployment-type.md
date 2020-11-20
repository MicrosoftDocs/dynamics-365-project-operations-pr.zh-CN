---
title: 确定部署类型
description: 此主题提供的信息可帮助您确定您公司的 Project operations 的正确部署类型。
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401207"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="65efe-103">确定部署类型</span><span class="sxs-lookup"><span data-stu-id="65efe-103">Determine your deployment type</span></span>

<span data-ttu-id="65efe-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="65efe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65efe-105">购买许可证后，请从此处开始，使用[引导式安装流](https://aka.ms/provisionprojectoperations)确定 Dynamics 365 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="65efe-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="65efe-106">完成引导式安装流后，您将被定向到正确的管理门户来完成安装。</span><span class="sxs-lookup"><span data-stu-id="65efe-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="65efe-107">请参阅部署详细信息完成安装。</span><span class="sxs-lookup"><span data-stu-id="65efe-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="65efe-108">使用 Dynamics 365 Project Service Automation 的现有 Dynamics 客户</span><span class="sxs-lookup"><span data-stu-id="65efe-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="65efe-109">Project Operations 包含 Project Service Automation 随附的功能。</span><span class="sxs-lookup"><span data-stu-id="65efe-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="65efe-110">升级路径将在 2021 年发行版本第 1 波中为这些客户发布。</span><span class="sxs-lookup"><span data-stu-id="65efe-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="65efe-111">使用“项目管理和会计”的现有 Dynamics 365 Finance 客户</span><span class="sxs-lookup"><span data-stu-id="65efe-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="65efe-112">使用项目管理和会计功能的 Finance 的现有客户可以继续像以往一样使用它。</span><span class="sxs-lookup"><span data-stu-id="65efe-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="65efe-113">请参阅[面向库存/生产订单场景的 Project Operations](#pma)。</span><span class="sxs-lookup"><span data-stu-id="65efe-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="65efe-114">部署类型</span><span class="sxs-lookup"><span data-stu-id="65efe-114">Deployment types</span></span>
<span data-ttu-id="65efe-115">Project Operations 支持多个部署选项以满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="65efe-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="65efe-116">无论您是 Dynamics 365 的新客户还是现有客户，Project Operations 都可以满足您的需求。</span><span class="sxs-lookup"><span data-stu-id="65efe-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="65efe-117">我们的[部署调查表](https://aka.ms/provisionprojectoperations)将帮助您确定正确的部署。</span><span class="sxs-lookup"><span data-stu-id="65efe-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="65efe-118">结果将指导您执行以下一种部署类型：</span><span class="sxs-lookup"><span data-stu-id="65efe-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="65efe-119">精简部署 - 估价交易开票</span><span class="sxs-lookup"><span data-stu-id="65efe-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="65efe-120">面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="65efe-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="65efe-121">面向库存/生产订单场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="65efe-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="65efe-122">Project Operations 通过法人级别的配置在同一环境中支持库存/生产订单场景和非库存/资源场景。</span><span class="sxs-lookup"><span data-stu-id="65efe-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="65efe-123">例如，Contoso 可以在他们的美国生产设施中使用库存/生产订单功能（法人 = Contoso Manufacturing United States）。</span><span class="sxs-lookup"><span data-stu-id="65efe-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="65efe-124">Contoso 可以在他们位于英国的 Contoso 机械臂维修设施中使用非库存/资源功能（法人 = Contoso Robotics United Kingdom）。</span><span class="sxs-lookup"><span data-stu-id="65efe-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="65efe-125">精简部署 - 估价交易开票</span><span class="sxs-lookup"><span data-stu-id="65efe-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="65efe-126">精简部署包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="65efe-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="65efe-127">扩展 Dynamics 365 Sales 应用程序体验的项目的销售流程</span><span class="sxs-lookup"><span data-stu-id="65efe-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="65efe-128">使用 Web 版本的 Microsoft Project 进行项目规划</span><span class="sxs-lookup"><span data-stu-id="65efe-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="65efe-129">多维定价</span><span class="sxs-lookup"><span data-stu-id="65efe-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="65efe-130">统一资源管理</span><span class="sxs-lookup"><span data-stu-id="65efe-130">Unified resource management</span></span>
- <span data-ttu-id="65efe-131">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="65efe-131">Time tracking</span></span>
- <span data-ttu-id="65efe-132">基本支出</span><span class="sxs-lookup"><span data-stu-id="65efe-132">Basic expense</span></span>
- <span data-ttu-id="65efe-133">估价和面向客户的开票</span><span class="sxs-lookup"><span data-stu-id="65efe-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="65efe-134">部署步骤</span><span class="sxs-lookup"><span data-stu-id="65efe-134">Deployment steps</span></span>
<span data-ttu-id="65efe-135">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="65efe-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="65efe-136">对于此部署，请参阅[注册获取预览订阅](lite-preview-subscription-sign-up.md)和[设置新环境](lite-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="65efe-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="65efe-137">面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="65efe-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="65efe-138">面向资源/非库存场景的 Project Operations 包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="65efe-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="65efe-139">扩展 Dynamics 365 Sales 应用程序的项目的销售流程</span><span class="sxs-lookup"><span data-stu-id="65efe-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="65efe-140">使用 Web 版本的 Microsoft Project 进行项目规划</span><span class="sxs-lookup"><span data-stu-id="65efe-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="65efe-141">多维定价</span><span class="sxs-lookup"><span data-stu-id="65efe-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="65efe-142">统一资源管理</span><span class="sxs-lookup"><span data-stu-id="65efe-142">Unified resource management</span></span>
- <span data-ttu-id="65efe-143">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="65efe-143">Time tracking</span></span>
- <span data-ttu-id="65efe-144">基本支出</span><span class="sxs-lookup"><span data-stu-id="65efe-144">Basic expense</span></span>
- <span data-ttu-id="65efe-145">全部支出</span><span class="sxs-lookup"><span data-stu-id="65efe-145">Full expense</span></span>
- <span data-ttu-id="65efe-146">收据 OCR</span><span class="sxs-lookup"><span data-stu-id="65efe-146">Receipt OCR</span></span>
- <span data-ttu-id="65efe-147">估价和面向客户的开票</span><span class="sxs-lookup"><span data-stu-id="65efe-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="65efe-148">项目收入确认</span><span class="sxs-lookup"><span data-stu-id="65efe-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="65efe-149">部署步骤</span><span class="sxs-lookup"><span data-stu-id="65efe-149">Deployment steps</span></span>
<span data-ttu-id="65efe-150">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="65efe-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="65efe-151">对于此部署，请参阅[注册获取预览订阅](resource-sign-up-preview-subscription.md)和[设置新环境](resource-provision-new-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="65efe-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="65efe-152">面向库存/生产订单场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="65efe-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="65efe-153">使用 WBS 进行项目计划</span><span class="sxs-lookup"><span data-stu-id="65efe-153">Project planning using WBS</span></span>
- <span data-ttu-id="65efe-154">资源管理</span><span class="sxs-lookup"><span data-stu-id="65efe-154">Resource Management</span></span>
- <span data-ttu-id="65efe-155">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="65efe-155">Time Tracking</span></span>
- <span data-ttu-id="65efe-156">全部支出</span><span class="sxs-lookup"><span data-stu-id="65efe-156">Full Expense</span></span>
- <span data-ttu-id="65efe-157">收据 OCR</span><span class="sxs-lookup"><span data-stu-id="65efe-157">Receipt OCR</span></span>
- <span data-ttu-id="65efe-158">完整开票</span><span class="sxs-lookup"><span data-stu-id="65efe-158">Full Invoicing</span></span>
- <span data-ttu-id="65efe-159">收入确认</span><span class="sxs-lookup"><span data-stu-id="65efe-159">Revenue Recognition</span></span>
- <span data-ttu-id="65efe-160">生产订单</span><span class="sxs-lookup"><span data-stu-id="65efe-160">Production Orders</span></span>
- <span data-ttu-id="65efe-161">材料支持</span><span class="sxs-lookup"><span data-stu-id="65efe-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="65efe-162">部署步骤</span><span class="sxs-lookup"><span data-stu-id="65efe-162">Deployment steps</span></span>
<span data-ttu-id="65efe-163">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="65efe-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="65efe-164">对于此部署，请参阅[注册获取预览订阅](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[设置新环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="65efe-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

