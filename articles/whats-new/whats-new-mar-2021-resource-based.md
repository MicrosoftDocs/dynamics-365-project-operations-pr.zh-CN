---
title: 2021 年 3 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 此主题提供有关 2021 年 3 月版本的面向资源/非库存场景的 Project Operations 中推出的质量更新的信息。
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d114ee64bd26d3271a1c72a7404c0f7035c2b61
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948048"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="51854-103">2021 年 3 月新增功能 - 面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="51854-103">What's new March 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="51854-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="51854-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="51854-105">此主题适用于以下 Dynamics 365 Project Operations 组件和版本：</span><span class="sxs-lookup"><span data-stu-id="51854-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="51854-106">Dataverse 环境中的 Project Operations 版本 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="51854-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 
- <span data-ttu-id="51854-107">Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.16</span><span class="sxs-lookup"><span data-stu-id="51854-107">Project management and accounting on Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="51854-108">质量更新</span><span class="sxs-lookup"><span data-stu-id="51854-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="51854-109">Dataverse 上的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="51854-109">Project Operations on Dataverse</span></span>


| <span data-ttu-id="51854-110">**功能区域**</span><span class="sxs-lookup"><span data-stu-id="51854-110">**Feature area**</span></span> | <span data-ttu-id="51854-111">**参考编号**</span><span class="sxs-lookup"><span data-stu-id="51854-111">**Reference number**</span></span> | <span data-ttu-id="51854-112">**质量更新**</span><span class="sxs-lookup"><span data-stu-id="51854-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="51854-113">计费和定价</span><span class="sxs-lookup"><span data-stu-id="51854-113">Billing and pricing</span></span> | <span data-ttu-id="51854-114">2133873</span><span class="sxs-lookup"><span data-stu-id="51854-114">2133873</span></span> | <span data-ttu-id="51854-115">修复了 **费用估计值** 网格中 **销售单价** 货币符号的显示问题。</span><span class="sxs-lookup"><span data-stu-id="51854-115">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="51854-116">计费和定价</span><span class="sxs-lookup"><span data-stu-id="51854-116">Billing and pricing</span></span> | <span data-ttu-id="51854-117">2174616</span><span class="sxs-lookup"><span data-stu-id="51854-117">2174616</span></span> | <span data-ttu-id="51854-118">赢得报价单时，会在从该报价单复制的合同子项详细信息中引用合同自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="51854-118">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="51854-119">商机管理</span><span class="sxs-lookup"><span data-stu-id="51854-119">Opportunity Management</span></span> | <span data-ttu-id="51854-120">2167475</span><span class="sxs-lookup"><span data-stu-id="51854-120">2167475</span></span> | <span data-ttu-id="51854-121">产生未记帐实际条目的更正发票中的固定税额。</span><span class="sxs-lookup"><span data-stu-id="51854-121">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="51854-122">商机管理</span><span class="sxs-lookup"><span data-stu-id="51854-122">Opportunity Management</span></span> | <span data-ttu-id="51854-123">2176285</span><span class="sxs-lookup"><span data-stu-id="51854-123">2176285</span></span> | <span data-ttu-id="51854-124">不能将税额从销售合同/报价单明细详细信息复制到成本合同/报价单明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="51854-124">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="51854-125">商机管理</span><span class="sxs-lookup"><span data-stu-id="51854-125">Opportunity Management</span></span> | <span data-ttu-id="51854-126">2188079</span><span class="sxs-lookup"><span data-stu-id="51854-126">2188079</span></span> | <span data-ttu-id="51854-127">不得为不基于工作的合同创建拆分记帐规则。</span><span class="sxs-lookup"><span data-stu-id="51854-127">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="51854-128">规划和跟踪</span><span class="sxs-lookup"><span data-stu-id="51854-128">Planning and Tracking</span></span> | <span data-ttu-id="51854-129">2125274</span><span class="sxs-lookup"><span data-stu-id="51854-129">2125274</span></span> | <span data-ttu-id="51854-130">**项目开始日期映射** 的 **项目双重写入映射** 属性已从 **msdyn\_taskearlieststart** 更新为 **msdyn\_actualstart**。</span><span class="sxs-lookup"><span data-stu-id="51854-130">**Project Dual Write Map** attribute for **Project Start Date Mapping** updated from **msdyn\_taskearlieststart** to **msdyn\_actualstart**.</span></span> |
| <span data-ttu-id="51854-131">规划和跟踪</span><span class="sxs-lookup"><span data-stu-id="51854-131">Planning and Tracking</span></span> | <span data-ttu-id="51854-132">2138853</span><span class="sxs-lookup"><span data-stu-id="51854-132">2138853</span></span> | <span data-ttu-id="51854-133">更新了项目复制功能，以确保将引用任务的支出估计行复制到目标项目。</span><span class="sxs-lookup"><span data-stu-id="51854-133">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="51854-134">规划和跟踪</span><span class="sxs-lookup"><span data-stu-id="51854-134">Planning and Tracking</span></span> | <span data-ttu-id="51854-135">2154306</span><span class="sxs-lookup"><span data-stu-id="51854-135">2154306</span></span> | <span data-ttu-id="51854-136">针对基于资源的方案修正了在 Project Operations 中删除费用估计值的问题。</span><span class="sxs-lookup"><span data-stu-id="51854-136">Fixed issues with deleting expense estimates in Project Operations for resource-based scenarios.</span></span> |
| <span data-ttu-id="51854-137">规划和跟踪</span><span class="sxs-lookup"><span data-stu-id="51854-137">Planning and Tracking</span></span> | <span data-ttu-id="51854-138">2173259</span><span class="sxs-lookup"><span data-stu-id="51854-138">2173259</span></span> | <span data-ttu-id="51854-139">项目复制功能已更新，以确保其在特定情况下不显示 **正在复制 WBS** 错误消息。</span><span class="sxs-lookup"><span data-stu-id="51854-139">Project copy function updated to ensure it doesn't display **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="51854-140">时间和支出</span><span class="sxs-lookup"><span data-stu-id="51854-140">Time and Expense</span></span> | <span data-ttu-id="51854-141">2148910</span><span class="sxs-lookup"><span data-stu-id="51854-141">2148910</span></span> | <span data-ttu-id="51854-142">修复了 **时间条目** 网格中的 **编辑条目** 页的显示问题。</span><span class="sxs-lookup"><span data-stu-id="51854-142">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="51854-143">时间和支出</span><span class="sxs-lookup"><span data-stu-id="51854-143">Time and Expense</span></span> | <span data-ttu-id="51854-144">2159798</span><span class="sxs-lookup"><span data-stu-id="51854-144">2159798</span></span> | <span data-ttu-id="51854-145">加强了控件，以确保无法编辑已批准的费用条目。</span><span class="sxs-lookup"><span data-stu-id="51854-145">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="51854-146">Dynamics 365 Finance 中的项目管理和会计</span><span class="sxs-lookup"><span data-stu-id="51854-146">Project management and accounting on Dynamics 365 Finance</span></span>

<span data-ttu-id="51854-147">有关详细信息，请参阅 [2021 年 1 月新增功能 - 面向资源/非库存场景的 Project Operations](whats-new-jan-2021-resource-based.md)。</span><span class="sxs-lookup"><span data-stu-id="51854-147">For more information, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="51854-148">法规更新</span><span class="sxs-lookup"><span data-stu-id="51854-148">Regulatory updates</span></span>

<span data-ttu-id="51854-149">有关 Finance and Operations 应用的法规更新的信息，请参阅[法规更新](/dynamics365/finance/localizations/regulatory-updates)。</span><span class="sxs-lookup"><span data-stu-id="51854-149">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="51854-150">了解法规更新的另一种方法是登录 LCS，然后使用问题搜索工具查看计划的法规更新。</span><span class="sxs-lookup"><span data-stu-id="51854-150">Another way to learn about regulatory updates is to sign in to LCS and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="51854-151">通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。</span><span class="sxs-lookup"><span data-stu-id="51854-151">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]