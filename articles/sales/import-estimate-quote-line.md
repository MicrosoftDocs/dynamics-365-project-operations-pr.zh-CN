---
title: 将项目预估导入基于项目的报价单明细
description: 此主题提供有关将预估从项目导入报价单明细的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c0fe18b33207f73848709b99334f64aadc7867a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072520"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a><span data-ttu-id="97979-103">将项目预估导入基于项目的报价单明细</span><span class="sxs-lookup"><span data-stu-id="97979-103">Import estimates for a project to a project-based quote line</span></span>

<span data-ttu-id="97979-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="97979-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="97979-105">如果在预售阶段创建了项目，您可以选择将财务预估从项目导入到基于项目的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="97979-105">If a project is created during the pre-sales stage, you can select to import the financial estimate from the project to the project-based quote line.</span></span>

1. <span data-ttu-id="97979-106">确保基于项目的报价单明细在 **项目** 字段中有项目信息。</span><span class="sxs-lookup"><span data-stu-id="97979-106">Make sure that the project-based quote line has the project information in the **Project** field.</span></span>
2. <span data-ttu-id="97979-107">在 **报价单明细详细信息** 选项卡上，选择 **从项目预估导入** 。</span><span class="sxs-lookup"><span data-stu-id="97979-107">On the **Quote line details** tab, select **Import from Project Estimation**.</span></span>
3. <span data-ttu-id="97979-108">在打开的对话页面上，选择以下摘要选项之一：</span><span class="sxs-lookup"><span data-stu-id="97979-108">On the dialog page opens, select one of the following summarization options:</span></span>

  - <span data-ttu-id="97979-109">**交易分类**</span><span class="sxs-lookup"><span data-stu-id="97979-109">**Transaction class**</span></span>
  - <span data-ttu-id="97979-110">**类别**</span><span class="sxs-lookup"><span data-stu-id="97979-110">**Category**</span></span>
  - <span data-ttu-id="97979-111">**角色**</span><span class="sxs-lookup"><span data-stu-id="97979-111">**Role**</span></span> 
  - <span data-ttu-id="97979-112">**项目任务**</span><span class="sxs-lookup"><span data-stu-id="97979-112">**Project task**</span></span>

<span data-ttu-id="97979-113">根据您的选择，将复制此报价单明细中包括的所有交易类的项目预估。</span><span class="sxs-lookup"><span data-stu-id="97979-113">Based on your selection, the estimate from the project for all transaction classes included on this quote line are copied over.</span></span> <span data-ttu-id="97979-114">要检查包括哪些交易类，选择基于项目的报价单明细上的 **常规** 选项卡，并检查 **包括时间** 、 **包括支出** 和 **包括费用** 。</span><span class="sxs-lookup"><span data-stu-id="97979-114">To check what transaction classes are included, select the **General** tab on the project-based quote line, and check the values for **Include Time** , **Include Expenses** , and **Include Fees**.</span></span>

<span data-ttu-id="97979-115">导入预估时，系统将基于报价单所附的项目价目表和在基于项目的报价单明细上设置的计费类型默认选择定价。</span><span class="sxs-lookup"><span data-stu-id="97979-115">When you import estimates, the system will default pricing based on the project price lists attached to the quote and the billing type set up on the project-based quote line.</span></span> <span data-ttu-id="97979-116">如果在基于项目的报价单明细上将角色或类别设置为非应计费，导入的预估明细将设置为非应计费，不会加总报价单明细的报价值。</span><span class="sxs-lookup"><span data-stu-id="97979-116">If a role or category is set up on the project-based quote line as non-chargeable, the imported estimate line will set as non-chargeable and won't add up to the quoted value of quote line.</span></span>

<span data-ttu-id="97979-117">当报价单明细包含明细详细信息时，报价单明细上的 **报价单值** 和 **预计税款** 字段将汇总，无法进行编辑。</span><span class="sxs-lookup"><span data-stu-id="97979-117">When a quote line has line details, the **Quote Value** and the **Estimated Tax** fields on the quote line are summarized and can't be edited.</span></span>

<span data-ttu-id="97979-118">选择多个汇总选项时，系统会尝试按所有选择的选项汇总。</span><span class="sxs-lookup"><span data-stu-id="97979-118">When multiple summarization options are selected, the system attempts to summarize by all selected options.</span></span> <span data-ttu-id="97979-119">结果是如果与仅选择一个汇总选项相比，导入的报价单明细的输出会更多。</span><span class="sxs-lookup"><span data-stu-id="97979-119">The result is that the output of imported quote lines will be more than if you selected only one summarization option.</span></span>

<span data-ttu-id="97979-120">例如，如果项目具有以下支出估算明细。</span><span class="sxs-lookup"><span data-stu-id="97979-120">For example, if the project has the following estimate lines for expenses.</span></span>

| <span data-ttu-id="97979-121">任务</span><span class="sxs-lookup"><span data-stu-id="97979-121">Task</span></span> | <span data-ttu-id="97979-122">类别</span><span class="sxs-lookup"><span data-stu-id="97979-122">Category</span></span> | <span data-ttu-id="97979-123">日期</span><span class="sxs-lookup"><span data-stu-id="97979-123">Date</span></span> | <span data-ttu-id="97979-124">数量</span><span class="sxs-lookup"><span data-stu-id="97979-124">Quantity</span></span> | <span data-ttu-id="97979-125">单价</span><span class="sxs-lookup"><span data-stu-id="97979-125">Unit price</span></span> | <span data-ttu-id="97979-126">应收总额</span><span class="sxs-lookup"><span data-stu-id="97979-126">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="97979-127">任务 A</span><span class="sxs-lookup"><span data-stu-id="97979-127">Task A</span></span> | <span data-ttu-id="97979-128">机票</span><span class="sxs-lookup"><span data-stu-id="97979-128">Airfare</span></span> | <span data-ttu-id="97979-129">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-129">10/1/2020</span></span> | <span data-ttu-id="97979-130">4</span><span class="sxs-lookup"><span data-stu-id="97979-130">4</span></span> | <span data-ttu-id="97979-131">400</span><span class="sxs-lookup"><span data-stu-id="97979-131">400</span></span> | <span data-ttu-id="97979-132">1600</span><span class="sxs-lookup"><span data-stu-id="97979-132">1600</span></span> |
| <span data-ttu-id="97979-133">任务 B</span><span class="sxs-lookup"><span data-stu-id="97979-133">Task B</span></span> | <span data-ttu-id="97979-134">酒店</span><span class="sxs-lookup"><span data-stu-id="97979-134">Hotel</span></span> | <span data-ttu-id="97979-135">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-135">10/1/2020</span></span> | <span data-ttu-id="97979-136">4</span><span class="sxs-lookup"><span data-stu-id="97979-136">4</span></span> | <span data-ttu-id="97979-137">200</span><span class="sxs-lookup"><span data-stu-id="97979-137">200</span></span> | <span data-ttu-id="97979-138">800</span><span class="sxs-lookup"><span data-stu-id="97979-138">800</span></span> |
| <span data-ttu-id="97979-139">任务 C</span><span class="sxs-lookup"><span data-stu-id="97979-139">Task C</span></span> | <span data-ttu-id="97979-140">酒店</span><span class="sxs-lookup"><span data-stu-id="97979-140">Hotel</span></span> | <span data-ttu-id="97979-141">11/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-141">11/1/2020</span></span> | <span data-ttu-id="97979-142">2</span><span class="sxs-lookup"><span data-stu-id="97979-142">2</span></span> | <span data-ttu-id="97979-143">200</span><span class="sxs-lookup"><span data-stu-id="97979-143">200</span></span> | <span data-ttu-id="97979-144">400</span><span class="sxs-lookup"><span data-stu-id="97979-144">400</span></span> |

<span data-ttu-id="97979-145">当用户选择按交易类进行汇总时，将导入以下信息。</span><span class="sxs-lookup"><span data-stu-id="97979-145">When the user selects to summarize by Transaction class, the following information will be imported.</span></span>

| <span data-ttu-id="97979-146">任务</span><span class="sxs-lookup"><span data-stu-id="97979-146">Task</span></span> | <span data-ttu-id="97979-147">类别</span><span class="sxs-lookup"><span data-stu-id="97979-147">Category</span></span> | <span data-ttu-id="97979-148">日期</span><span class="sxs-lookup"><span data-stu-id="97979-148">Date</span></span> | <span data-ttu-id="97979-149">数量</span><span class="sxs-lookup"><span data-stu-id="97979-149">Quantity</span></span> | <span data-ttu-id="97979-150">单价</span><span class="sxs-lookup"><span data-stu-id="97979-150">Unit price</span></span> | <span data-ttu-id="97979-151">应收总额</span><span class="sxs-lookup"><span data-stu-id="97979-151">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| | | <span data-ttu-id="97979-152">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-152">10/1/2020</span></span> | <span data-ttu-id="97979-153">3.34</span><span class="sxs-lookup"><span data-stu-id="97979-153">3.34</span></span> | <span data-ttu-id="97979-154">840</span><span class="sxs-lookup"><span data-stu-id="97979-154">840</span></span> | <span data-ttu-id="97979-155">2800</span><span class="sxs-lookup"><span data-stu-id="97979-155">2800</span></span> |

<span data-ttu-id="97979-156">当用户选择按交易类和类别进行汇总时，将导入以下信息。</span><span class="sxs-lookup"><span data-stu-id="97979-156">When the user selects to summarize by Transaction class and Category, the following information will be imported.</span></span>

| <span data-ttu-id="97979-157">任务</span><span class="sxs-lookup"><span data-stu-id="97979-157">Task</span></span> | <span data-ttu-id="97979-158">类别</span><span class="sxs-lookup"><span data-stu-id="97979-158">Category</span></span> | <span data-ttu-id="97979-159">日期</span><span class="sxs-lookup"><span data-stu-id="97979-159">Date</span></span> | <span data-ttu-id="97979-160">数量</span><span class="sxs-lookup"><span data-stu-id="97979-160">Quantity</span></span> | <span data-ttu-id="97979-161">单价</span><span class="sxs-lookup"><span data-stu-id="97979-161">Unit price</span></span> | <span data-ttu-id="97979-162">应收总额</span><span class="sxs-lookup"><span data-stu-id="97979-162">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="97979-163">任务 A</span><span class="sxs-lookup"><span data-stu-id="97979-163">Task A</span></span> | <span data-ttu-id="97979-164">机票</span><span class="sxs-lookup"><span data-stu-id="97979-164">Airfare</span></span> | <span data-ttu-id="97979-165">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-165">10/1/2020</span></span> | <span data-ttu-id="97979-166">4</span><span class="sxs-lookup"><span data-stu-id="97979-166">4</span></span> | <span data-ttu-id="97979-167">400</span><span class="sxs-lookup"><span data-stu-id="97979-167">400</span></span> | <span data-ttu-id="97979-168">1600</span><span class="sxs-lookup"><span data-stu-id="97979-168">1600</span></span> |
| | <span data-ttu-id="97979-169">酒店</span><span class="sxs-lookup"><span data-stu-id="97979-169">Hotel</span></span> | <span data-ttu-id="97979-170">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-170">10/1/2020</span></span> | <span data-ttu-id="97979-171">6</span><span class="sxs-lookup"><span data-stu-id="97979-171">6</span></span> | <span data-ttu-id="97979-172">200</span><span class="sxs-lookup"><span data-stu-id="97979-172">200</span></span> | <span data-ttu-id="97979-173">1200</span><span class="sxs-lookup"><span data-stu-id="97979-173">1200</span></span> |

<span data-ttu-id="97979-174">当用户选择按交易类、类别和叶节点任务进行汇总时，将导入以下信息。</span><span class="sxs-lookup"><span data-stu-id="97979-174">When the user selects to summarize by Transaction class, Category, and Leaf Node Task, the following information will be imported.</span></span> <span data-ttu-id="97979-175">请注意，此结果与项目上的结果相同。</span><span class="sxs-lookup"><span data-stu-id="97979-175">Notice that this result is the same as what was on the project.</span></span>

| <span data-ttu-id="97979-176">任务</span><span class="sxs-lookup"><span data-stu-id="97979-176">Task</span></span> | <span data-ttu-id="97979-177">类别</span><span class="sxs-lookup"><span data-stu-id="97979-177">Category</span></span> | <span data-ttu-id="97979-178">日期</span><span class="sxs-lookup"><span data-stu-id="97979-178">Date</span></span> | <span data-ttu-id="97979-179">数量</span><span class="sxs-lookup"><span data-stu-id="97979-179">Quantity</span></span> | <span data-ttu-id="97979-180">单价</span><span class="sxs-lookup"><span data-stu-id="97979-180">Unit price</span></span> | <span data-ttu-id="97979-181">应收总额</span><span class="sxs-lookup"><span data-stu-id="97979-181">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="97979-182">任务 A</span><span class="sxs-lookup"><span data-stu-id="97979-182">Task A</span></span> | <span data-ttu-id="97979-183">机票</span><span class="sxs-lookup"><span data-stu-id="97979-183">Airfare</span></span> | <span data-ttu-id="97979-184">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-184">10/1/2020</span></span> | <span data-ttu-id="97979-185">4</span><span class="sxs-lookup"><span data-stu-id="97979-185">4</span></span> | <span data-ttu-id="97979-186">400</span><span class="sxs-lookup"><span data-stu-id="97979-186">400</span></span> | <span data-ttu-id="97979-187">1600</span><span class="sxs-lookup"><span data-stu-id="97979-187">1600</span></span> |
| <span data-ttu-id="97979-188">任务 B</span><span class="sxs-lookup"><span data-stu-id="97979-188">Task B</span></span> | <span data-ttu-id="97979-189">酒店</span><span class="sxs-lookup"><span data-stu-id="97979-189">Hotel</span></span> | <span data-ttu-id="97979-190">10/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-190">10/1/2020</span></span> | <span data-ttu-id="97979-191">4</span><span class="sxs-lookup"><span data-stu-id="97979-191">4</span></span> | <span data-ttu-id="97979-192">200</span><span class="sxs-lookup"><span data-stu-id="97979-192">200</span></span> | <span data-ttu-id="97979-193">800</span><span class="sxs-lookup"><span data-stu-id="97979-193">800</span></span> |
| <span data-ttu-id="97979-194">任务 C</span><span class="sxs-lookup"><span data-stu-id="97979-194">Task C</span></span> | <span data-ttu-id="97979-195">酒店</span><span class="sxs-lookup"><span data-stu-id="97979-195">Hotel</span></span> | <span data-ttu-id="97979-196">11/1/2020</span><span class="sxs-lookup"><span data-stu-id="97979-196">11/1/2020</span></span> | <span data-ttu-id="97979-197">2</span><span class="sxs-lookup"><span data-stu-id="97979-197">2</span></span> | <span data-ttu-id="97979-198">200</span><span class="sxs-lookup"><span data-stu-id="97979-198">200</span></span> | <span data-ttu-id="97979-199">400</span><span class="sxs-lookup"><span data-stu-id="97979-199">400</span></span> |