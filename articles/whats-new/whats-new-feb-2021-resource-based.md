---
title: 2021 年 2 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 此主题提供有关 2021 年 2 月版本的面向资源/非库存场景的 Project Operations 中推出的质量更新的信息。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8270214d47f712cdb0942991b0ffb5baff64cbfb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948003"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="c251e-103">2021 年 2 月新增功能 - 面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="c251e-103">What's new February 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="c251e-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c251e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c251e-105">此主题适用于以下 Dynamics 365 Project Operations 组件和版本：</span><span class="sxs-lookup"><span data-stu-id="c251e-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="c251e-106">Dataverse 环境中的 Project Operations 4.7.0.95</span><span class="sxs-lookup"><span data-stu-id="c251e-106">Project Operations on Dataverse environment 4.7.0.95</span></span>
- <span data-ttu-id="c251e-107">Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.16</span><span class="sxs-lookup"><span data-stu-id="c251e-107">Project management and accounting in Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="c251e-108">质量更新</span><span class="sxs-lookup"><span data-stu-id="c251e-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="c251e-109">Dataverse 上的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="c251e-109">Project Operations on Dataverse</span></span>

| <span data-ttu-id="c251e-110">**功能区域**</span><span class="sxs-lookup"><span data-stu-id="c251e-110">**Feature Area**</span></span> | <span data-ttu-id="c251e-111">**参考编号**</span><span class="sxs-lookup"><span data-stu-id="c251e-111">**Reference number**</span></span> | <span data-ttu-id="c251e-112">**质量更新**</span><span class="sxs-lookup"><span data-stu-id="c251e-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c251e-113">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="c251e-113">**Billing and Pricing**</span></span> | <span data-ttu-id="c251e-114">2053736</span><span class="sxs-lookup"><span data-stu-id="c251e-114">2053736</span></span> | <span data-ttu-id="c251e-115">现在可以通过转到 **发票** > **相关信息** 来访问发票明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="c251e-115">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="c251e-116">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="c251e-116">**Billing and Pricing**</span></span> | <span data-ttu-id="c251e-117">2122613</span><span class="sxs-lookup"><span data-stu-id="c251e-117">2122613</span></span> | <span data-ttu-id="c251e-118">**激活** 和 **停用** 操作已从 **价目表** 关联实体中删除。</span><span class="sxs-lookup"><span data-stu-id="c251e-118">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="c251e-119">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="c251e-119">**Billing and Pricing**</span></span> | <span data-ttu-id="c251e-120">2128606</span><span class="sxs-lookup"><span data-stu-id="c251e-120">2128606</span></span> | <span data-ttu-id="c251e-121">解决了 **GetEstimatesForProject** 插件中 **ullReferenceException** 存在的问题。</span><span class="sxs-lookup"><span data-stu-id="c251e-121">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="c251e-122">**部署和配置**</span><span class="sxs-lookup"><span data-stu-id="c251e-122">**Deployment and configuration**</span></span> | <span data-ttu-id="c251e-123">2139346</span><span class="sxs-lookup"><span data-stu-id="c251e-123">2139346</span></span> | <span data-ttu-id="c251e-124">解决了导入非托管 **Dynamics365ProjectOperationsDualWrite** 解决方案存在的问题。</span><span class="sxs-lookup"><span data-stu-id="c251e-124">Resolved the issue with importing unmanaged **Dynamics365ProjectOperationsDualWrite** solution.</span></span> |
| <span data-ttu-id="c251e-125">**部署和配置**</span><span class="sxs-lookup"><span data-stu-id="c251e-125">**Deployment and configuration**</span></span> | <span data-ttu-id="c251e-126">2140569</span><span class="sxs-lookup"><span data-stu-id="c251e-126">2140569</span></span> | <span data-ttu-id="c251e-127">不能在 Dataverse Teams 环境中安装项目解决方案。</span><span class="sxs-lookup"><span data-stu-id="c251e-127">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="c251e-128">**部署和配置**</span><span class="sxs-lookup"><span data-stu-id="c251e-128">**Deployment and configuration**</span></span> | <span data-ttu-id="c251e-129">2086991</span><span class="sxs-lookup"><span data-stu-id="c251e-129">2086991</span></span> | <span data-ttu-id="c251e-130">限制自定义 Web 资源的本地化。</span><span class="sxs-lookup"><span data-stu-id="c251e-130">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="c251e-131">**商机管理**</span><span class="sxs-lookup"><span data-stu-id="c251e-131">**Opportunity Management**</span></span> | <span data-ttu-id="c251e-132">2136794</span><span class="sxs-lookup"><span data-stu-id="c251e-132">2136794</span></span> | <span data-ttu-id="c251e-133">当 **确认发票** 或 **发票标记为已支付** 流程失败时，显示正确的错误消息。</span><span class="sxs-lookup"><span data-stu-id="c251e-133">Display the correct error message when the **Confirm invoice** or **Mark invoice as paid** processes fail.</span></span> |
| <span data-ttu-id="c251e-134">**商机管理**</span><span class="sxs-lookup"><span data-stu-id="c251e-134">**Opportunity Management**</span></span> | <span data-ttu-id="c251e-135">2139330</span><span class="sxs-lookup"><span data-stu-id="c251e-135">2139330</span></span> | <span data-ttu-id="c251e-136">更改项目的项目经理不能将负责公司重置为默认值。</span><span class="sxs-lookup"><span data-stu-id="c251e-136">Changing the Project manager on a project must not reset the owning company back to the default value.</span></span> |
| <span data-ttu-id="c251e-137">**商机管理**</span><span class="sxs-lookup"><span data-stu-id="c251e-137">**Opportunity Management**</span></span> | <span data-ttu-id="c251e-138">2146376</span><span class="sxs-lookup"><span data-stu-id="c251e-138">2146376</span></span> | <span data-ttu-id="c251e-139">非应计费实际值中的更正税金额从发票确认创建。</span><span class="sxs-lookup"><span data-stu-id="c251e-139">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="c251e-140">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="c251e-140">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c251e-141">2099879</span><span class="sxs-lookup"><span data-stu-id="c251e-141">2099879</span></span> | <span data-ttu-id="c251e-142">Dataverse 环境部署必须创建具有静态 ID 的默认交易类别，而不能在每个环境中随机生成。</span><span class="sxs-lookup"><span data-stu-id="c251e-142">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="c251e-143">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="c251e-143">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c251e-144">2128577</span><span class="sxs-lookup"><span data-stu-id="c251e-144">2128577</span></span> | <span data-ttu-id="c251e-145">修复了更新资源分配上的交易类别的 Project Service 用户特权。</span><span class="sxs-lookup"><span data-stu-id="c251e-145">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="c251e-146">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="c251e-146">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c251e-147">2164035</span><span class="sxs-lookup"><span data-stu-id="c251e-147">2164035</span></span> | <span data-ttu-id="c251e-148">修复了 **复制项目** 功能存在的问题。</span><span class="sxs-lookup"><span data-stu-id="c251e-148">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="c251e-149">**时间条目**</span><span class="sxs-lookup"><span data-stu-id="c251e-149">**Time entry**</span></span> | <span data-ttu-id="c251e-150">2129161</span><span class="sxs-lookup"><span data-stu-id="c251e-150">2129161</span></span> | <span data-ttu-id="c251e-151">应用了更严格的限制，以确保用户不能更改和更新已提交或批准的时间条目。</span><span class="sxs-lookup"><span data-stu-id="c251e-151">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="c251e-152">**时间条目**</span><span class="sxs-lookup"><span data-stu-id="c251e-152">**Time entry**</span></span> | <span data-ttu-id="c251e-153">2103572</span><span class="sxs-lookup"><span data-stu-id="c251e-153">2103572</span></span> | <span data-ttu-id="c251e-154">非项目时间条目的时间审批不能查找项目审批者角色。</span><span class="sxs-lookup"><span data-stu-id="c251e-154">Time approval for non-project time entries must not be looking for project approver role.</span></span> |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a><span data-ttu-id="c251e-155">Dynamics 365 Finance 中的项目管理和会计</span><span class="sxs-lookup"><span data-stu-id="c251e-155">Project management and accounting in Dynamics 365 Finance</span></span> 

<span data-ttu-id="c251e-156">有关 Dynamics 365 Finance 中的项目管理和会计的详细信息，请参阅 [2021 年 1 月新增功能 - 面向资源/非库存场景的 Project Operations](whats-new-jan-2021-resource-based.md)。</span><span class="sxs-lookup"><span data-stu-id="c251e-156">For more information about Project management and accounting in Dynamics 365 Finance, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>


## <a name="regulatory-updates"></a><span data-ttu-id="c251e-157">法规更新</span><span class="sxs-lookup"><span data-stu-id="c251e-157">Regulatory updates</span></span>

<span data-ttu-id="c251e-158">有关 Finance and Operations 应用的法规更新的信息，请参阅[法规更新](/dynamics365/finance/localizations/regulatory-updates)。</span><span class="sxs-lookup"><span data-stu-id="c251e-158">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="c251e-159">了解法规更新的另一种方法是登录 Lifecycle Services(LCS)，然后使用问题搜索工具查看计划的法规更新。</span><span class="sxs-lookup"><span data-stu-id="c251e-159">Another way to learn about regulatory updates is to sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="c251e-160">通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。</span><span class="sxs-lookup"><span data-stu-id="c251e-160">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]