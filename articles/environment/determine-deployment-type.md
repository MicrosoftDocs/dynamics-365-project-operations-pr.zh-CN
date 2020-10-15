---
title: 部署类型
description: 此主题提供的信息可帮助您确定您公司的 Project operations 的正确部署类型。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948768"
---
# <a name="deployment-types"></a><span data-ttu-id="6d139-103">部署类型</span><span class="sxs-lookup"><span data-stu-id="6d139-103">Deployment types</span></span>

<span data-ttu-id="6d139-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="6d139-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d139-105">购买许可证后，请从此处开始，使用[引导式安装流](https://aka.ms/provisionprojectoperations)确定 Dynamics 365 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="6d139-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6d139-106">完成引导式安装流后，您将被定向到正确的管理门户来完成安装。</span><span class="sxs-lookup"><span data-stu-id="6d139-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6d139-107">请参阅下面的部署详细信息完成安装。</span><span class="sxs-lookup"><span data-stu-id="6d139-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6d139-108">使用 Dynamics 365 Project Service Automation 的现有 Dynamics 客户</span><span class="sxs-lookup"><span data-stu-id="6d139-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6d139-109">Project Operations 包含 Project Service Automation 随附的功能。</span><span class="sxs-lookup"><span data-stu-id="6d139-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6d139-110">将来将为这些客户发布升级路径。</span><span class="sxs-lookup"><span data-stu-id="6d139-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6d139-111">使用“项目管理和会计”的现有 Dynamics 365 Finance 客户</span><span class="sxs-lookup"><span data-stu-id="6d139-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6d139-112">使用“项目管理和会计”功能的现有 Finance 客户可以继续像以前一样使用此功能。</span><span class="sxs-lookup"><span data-stu-id="6d139-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="6d139-113">请参阅[面向库存/生产订单场景的 Project Operations](#pma)。</span><span class="sxs-lookup"><span data-stu-id="6d139-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="6d139-114">Project Operations 支持多个部署选项以满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="6d139-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6d139-115">无论您是 Dynamics 365 的新客户还是现有客户，Project Operations 都可以满足您的需求。</span><span class="sxs-lookup"><span data-stu-id="6d139-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6d139-116">我们的[部署调查表](https://aka.ms/provisionprojectoperations)将帮助您确定正确的部署。</span><span class="sxs-lookup"><span data-stu-id="6d139-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6d139-117">结果将指导您执行以下一种部署类型：</span><span class="sxs-lookup"><span data-stu-id="6d139-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6d139-118">精简部署 - 估价交易开票</span><span class="sxs-lookup"><span data-stu-id="6d139-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6d139-119">面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="6d139-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6d139-120">面向库存/生产订单场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="6d139-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6d139-121">Project Operations 通过法人级别的配置在同一环境中支持库存/生产订单场景和非库存/资源场景。</span><span class="sxs-lookup"><span data-stu-id="6d139-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6d139-122">例如，Contoso 可以在其美国制造工厂（法人 = Contoso Manufacturing United States）中利用库存/生产订单功能，在其英国的 Contoso Robotics Arms 维修厂利用非库存/资源功能（法人 = Contoso Robotics United Kingdom）。</span><span class="sxs-lookup"><span data-stu-id="6d139-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="6d139-123"><a name="lite"><a/>精简部署 - 估价交易开票</span><span class="sxs-lookup"><span data-stu-id="6d139-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="6d139-124">精简部署包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="6d139-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6d139-125">使用 Web 版本的 Microsoft Project 进行项目规划</span><span class="sxs-lookup"><span data-stu-id="6d139-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6d139-126">多维定价</span><span class="sxs-lookup"><span data-stu-id="6d139-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6d139-127">统一资源管理</span><span class="sxs-lookup"><span data-stu-id="6d139-127">Unified Resource Management</span></span>
- <span data-ttu-id="6d139-128">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="6d139-128">Time Tracking</span></span>
- <span data-ttu-id="6d139-129">基本支出</span><span class="sxs-lookup"><span data-stu-id="6d139-129">Basic Expense</span></span>
- <span data-ttu-id="6d139-130">发票方案</span><span class="sxs-lookup"><span data-stu-id="6d139-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6d139-131">部署步骤：</span><span class="sxs-lookup"><span data-stu-id="6d139-131">Deployment steps:</span></span>
<span data-ttu-id="6d139-132">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="6d139-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6d139-133">对于此部署，请参阅[注册获取预览订阅](lite-preview-subscription-sign-up.md)和[设置新环境](lite-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="6d139-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6d139-134"><a name="integrated"><a/>面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="6d139-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6d139-135">面向资源/非库存场景的 Project Operations 包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="6d139-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6d139-136">使用 Web 版本的 Microsoft Project 进行项目规划</span><span class="sxs-lookup"><span data-stu-id="6d139-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6d139-137">多维定价</span><span class="sxs-lookup"><span data-stu-id="6d139-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6d139-138">统一资源管理</span><span class="sxs-lookup"><span data-stu-id="6d139-138">Unified Resource Management</span></span>
- <span data-ttu-id="6d139-139">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="6d139-139">Time Tracking</span></span>
- <span data-ttu-id="6d139-140">基本支出</span><span class="sxs-lookup"><span data-stu-id="6d139-140">Basic Expense</span></span>
- <span data-ttu-id="6d139-141">全部支出</span><span class="sxs-lookup"><span data-stu-id="6d139-141">Full Expense</span></span>
- <span data-ttu-id="6d139-142">收据 OCR</span><span class="sxs-lookup"><span data-stu-id="6d139-142">Receipt OCR</span></span>
- <span data-ttu-id="6d139-143">完整开票</span><span class="sxs-lookup"><span data-stu-id="6d139-143">Full Invoicing</span></span>
- <span data-ttu-id="6d139-144">收入确认</span><span class="sxs-lookup"><span data-stu-id="6d139-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6d139-145">部署步骤：</span><span class="sxs-lookup"><span data-stu-id="6d139-145">Deployment steps:</span></span>
<span data-ttu-id="6d139-146">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="6d139-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6d139-147">对于此部署，请参阅[注册获取预览订阅](resource-sign-up-preview-subscription.md)和[设置新环境](resource-provision-new-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="6d139-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6d139-148">面向库存/生产订单场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="6d139-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6d139-149">使用 WBS 进行项目计划</span><span class="sxs-lookup"><span data-stu-id="6d139-149">Project planning using WBS</span></span>
- <span data-ttu-id="6d139-150">资源管理</span><span class="sxs-lookup"><span data-stu-id="6d139-150">Resource Management</span></span>
- <span data-ttu-id="6d139-151">时间跟踪</span><span class="sxs-lookup"><span data-stu-id="6d139-151">Time Tracking</span></span>
- <span data-ttu-id="6d139-152">全部支出</span><span class="sxs-lookup"><span data-stu-id="6d139-152">Full Expense</span></span>
- <span data-ttu-id="6d139-153">收据 OCR</span><span class="sxs-lookup"><span data-stu-id="6d139-153">Receipt OCR</span></span>
- <span data-ttu-id="6d139-154">完整开票</span><span class="sxs-lookup"><span data-stu-id="6d139-154">Full Invoicing</span></span>
- <span data-ttu-id="6d139-155">收入确认</span><span class="sxs-lookup"><span data-stu-id="6d139-155">Revenue Recognition</span></span>
- <span data-ttu-id="6d139-156">生产订单</span><span class="sxs-lookup"><span data-stu-id="6d139-156">Production Orders</span></span>
- <span data-ttu-id="6d139-157">材料支持</span><span class="sxs-lookup"><span data-stu-id="6d139-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6d139-158">部署步骤：</span><span class="sxs-lookup"><span data-stu-id="6d139-158">Deployment steps:</span></span>
<span data-ttu-id="6d139-159">使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="6d139-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6d139-160">对于此部署，请参阅[注册获取预览订阅](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[设置新环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="6d139-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



