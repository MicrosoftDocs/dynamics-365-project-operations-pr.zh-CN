---
title: 撤消以前批准的时间或支出条目
description: 此主题介绍如何撤消以前批准的时间或支出交易。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147822"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="b2100-103">撤消以前批准的时间或支出条目</span><span class="sxs-lookup"><span data-stu-id="b2100-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b2100-104">提交时间或支出条目的项目团队成员或其他人可以在该条目已被批准后将其撤消。</span><span class="sxs-lookup"><span data-stu-id="b2100-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="b2100-105">撤消已批准时间或支出条目的流程分两步：</span><span class="sxs-lookup"><span data-stu-id="b2100-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="b2100-106">提交者请求撤消。</span><span class="sxs-lookup"><span data-stu-id="b2100-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="b2100-107">审批者批准撤消。</span><span class="sxs-lookup"><span data-stu-id="b2100-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="b2100-108">请求撤消</span><span class="sxs-lookup"><span data-stu-id="b2100-108">Request a recall</span></span>

<span data-ttu-id="b2100-109">执行以下步骤请求撤消已批准的时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="b2100-110">对于时间条目，请转到 **项目** \> **我的工作** \> **时间条目**。</span><span class="sxs-lookup"><span data-stu-id="b2100-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="b2100-111">–或–</span><span class="sxs-lookup"><span data-stu-id="b2100-111">–or–</span></span>

    <span data-ttu-id="b2100-112">对于支出条目，请转到 **项目** \> **我的工作** \> **支出条目**。</span><span class="sxs-lookup"><span data-stu-id="b2100-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="b2100-113">对于时间条目，选择项目和任务特定组合的所有时间条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="b2100-114">也可以在网格中选择特定项目特定日期的时间的单个单元格。</span><span class="sxs-lookup"><span data-stu-id="b2100-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="b2100-115">–或–</span><span class="sxs-lookup"><span data-stu-id="b2100-115">–or–</span></span>

    <span data-ttu-id="b2100-116">对于支出条目，选择要撤消的支出条目的行。</span><span class="sxs-lookup"><span data-stu-id="b2100-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="b2100-117">选择 **撤消**。</span><span class="sxs-lookup"><span data-stu-id="b2100-117">Select **Recall**.</span></span> <span data-ttu-id="b2100-118">出现确认对话框。</span><span class="sxs-lookup"><span data-stu-id="b2100-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="b2100-119">如果已批准了所选时间和支出条目，系统将提示您输入撤消原因。</span><span class="sxs-lookup"><span data-stu-id="b2100-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="b2100-120">输入撤消原因，然后选择 **确定** 确认操作。</span><span class="sxs-lookup"><span data-stu-id="b2100-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="b2100-121">系统将向条目的审批者发送有关批准撤消的请求。</span><span class="sxs-lookup"><span data-stu-id="b2100-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="b2100-122">虽然可以撤消已批准的时间和支出条目，如果已经对客户为批准的时间或支出条目条目开票，则不能创建撤消请求。</span><span class="sxs-lookup"><span data-stu-id="b2100-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="b2100-123">尝试创建撤消请求的用户将收到消息，说明不能撤消时间或支出，因为已为其开票。</span><span class="sxs-lookup"><span data-stu-id="b2100-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="b2100-124">批准或拒绝撤消请求</span><span class="sxs-lookup"><span data-stu-id="b2100-124">Approve or reject a recall request</span></span>

<span data-ttu-id="b2100-125">可执行以下步骤批准或拒绝撤消请求。</span><span class="sxs-lookup"><span data-stu-id="b2100-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="b2100-126">转到 **项目** \> **我的工作** \> **审批**。</span><span class="sxs-lookup"><span data-stu-id="b2100-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="b2100-127">在 **审批** 列表页中，将视图更改为 **撤消待审批的请求**。</span><span class="sxs-lookup"><span data-stu-id="b2100-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="b2100-128">将显示提交的撤消请求的列表。</span><span class="sxs-lookup"><span data-stu-id="b2100-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="b2100-129">选择一个或多个条目，然后选择 **批准** 或 **拒绝**。</span><span class="sxs-lookup"><span data-stu-id="b2100-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="b2100-130">如果选择的是 **批准**，将收到警告消息，介绍批准的影响。</span><span class="sxs-lookup"><span data-stu-id="b2100-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="b2100-131">选择 **确定** 确认操作。</span><span class="sxs-lookup"><span data-stu-id="b2100-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="b2100-132">将批准撤消请求。</span><span class="sxs-lookup"><span data-stu-id="b2100-132">The recall request is approved.</span></span>

    <span data-ttu-id="b2100-133">–或–</span><span class="sxs-lookup"><span data-stu-id="b2100-133">–or–</span></span>

    <span data-ttu-id="b2100-134">如果选择的是 **拒绝**，将拒绝撤消请求。</span><span class="sxs-lookup"><span data-stu-id="b2100-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="b2100-135">请求撤消时，如果批准了撤消，系统将检查时间或支出条目的任何开票活动。</span><span class="sxs-lookup"><span data-stu-id="b2100-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="b2100-136">如果已经为条目开票，或者已经属于草稿发票，审批者将收到错误消息，说明不能批准撤消该时间或支持，因为已为其开票。</span><span class="sxs-lookup"><span data-stu-id="b2100-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="b2100-137">撤消请求的影响</span><span class="sxs-lookup"><span data-stu-id="b2100-137">Impact of a recall request</span></span>

<span data-ttu-id="b2100-138">撤消审批时，同时会产生运营影响和财务影响。</span><span class="sxs-lookup"><span data-stu-id="b2100-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="b2100-139">运营影响</span><span class="sxs-lookup"><span data-stu-id="b2100-139">Operational impact</span></span>

<span data-ttu-id="b2100-140">如果批准了撤消请求，将把审批记录标记为 **已拒绝**。</span><span class="sxs-lookup"><span data-stu-id="b2100-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="b2100-141">条目的状态将更改为 **已返回** 或 **已拒绝**，具体取决于是时间条目还是支出条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="b2100-142">项目团队成员可以查看条目，编辑条目再重新提交，或完全删除条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="b2100-143">如果拒绝了撤消请求，条目的状态仍然为 **已批准**，并且项目团队成员或项目审批者不能编辑该条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="b2100-144">财务影响</span><span class="sxs-lookup"><span data-stu-id="b2100-144">Financial impact</span></span>

<span data-ttu-id="b2100-145">如果批准了撤消请求，将按照以下方式更新成本和销售额的相应实际值：</span><span class="sxs-lookup"><span data-stu-id="b2100-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="b2100-146">**调整状态** 字段更新为 **已调整**。</span><span class="sxs-lookup"><span data-stu-id="b2100-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="b2100-147">**记帐状态** 字段更新为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="b2100-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="b2100-148">接下来，在实际值表中创建冲销条目。</span><span class="sxs-lookup"><span data-stu-id="b2100-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="b2100-149">为了创建冲销条目，系统将复制并覆盖原始实际值的字段值。</span><span class="sxs-lookup"><span data-stu-id="b2100-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="b2100-150">唯一不复制覆盖的值为数量值。</span><span class="sxs-lookup"><span data-stu-id="b2100-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="b2100-151">而是冲销这些值。</span><span class="sxs-lookup"><span data-stu-id="b2100-151">These values are reversed instead.</span></span> <span data-ttu-id="b2100-152">将为实际 **成本** 和 **未记帐销售额** 创建冲销实际值。</span><span class="sxs-lookup"><span data-stu-id="b2100-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="b2100-153">已冲销实际值的 **调整状态** 字段设置为 **不可调整**，而 **记帐状态** 字段设置为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="b2100-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="b2100-154">由于这些更改，记录的项目开销和收入积压不再计入这些实际值表示的金额。</span><span class="sxs-lookup"><span data-stu-id="b2100-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="b2100-155">如果拒绝了撤消请求，则不存在对项目的财务影响。</span><span class="sxs-lookup"><span data-stu-id="b2100-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="b2100-156">对时间条目记录的更改</span><span class="sxs-lookup"><span data-stu-id="b2100-156">Changes to time entry records</span></span>

<span data-ttu-id="b2100-157">下图显示撤销了已批准时间条目时发生的更改。</span><span class="sxs-lookup"><span data-stu-id="b2100-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![时间条目状态转换](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="b2100-159">对支出条目记录的更改</span><span class="sxs-lookup"><span data-stu-id="b2100-159">Changes to expense entry records</span></span>

<span data-ttu-id="b2100-160">下图显示撤销了已批准支出条目时发生的更改。</span><span class="sxs-lookup"><span data-stu-id="b2100-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![支出条目状态转换](media/ExpenseEntryStateTransitions.png)
