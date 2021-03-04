---
title: 取消以前批准的时间和支出条目
description: 此主题介绍如何取消已批准的项目时间和支出交易。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150567"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="8cbc5-103">取消以前批准的时间或支出条目</span><span class="sxs-lookup"><span data-stu-id="8cbc5-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8cbc5-104">在 Dynamics 365 Project Service Automation 最新版本中，审批者可取消自己以前批准的时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="8cbc5-105">取消以前批准的时间或支出条目</span><span class="sxs-lookup"><span data-stu-id="8cbc5-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="8cbc5-106">执行以下步骤取消以前批准的时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="8cbc5-107">转到 **项目** \> **我的工作** \> **审批**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="8cbc5-108">在 **审批** 列表页中，将视图更改为 **我过去的审批**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="8cbc5-109">将显示您以前批准的时间和支出条目的列表。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="8cbc5-110">选择一个或多个条目，然后选择 **取消审批**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="8cbc5-111">您将收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-111">You receive a warning message.</span></span>
4. <span data-ttu-id="8cbc5-112">选择 **确定** 取消审批。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="8cbc5-113">了解取消时间和支出条目审批的影响</span><span class="sxs-lookup"><span data-stu-id="8cbc5-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="8cbc5-114">取消审批时，同时会产生运营影响和财务影响。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="8cbc5-115">运营影响</span><span class="sxs-lookup"><span data-stu-id="8cbc5-115">Operational impact</span></span>

<span data-ttu-id="8cbc5-116">在运营端，取消了一项审批时，记录的状态重置为 **草稿**，**我过去的审批** 视图中不再显示这项审批。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="8cbc5-117">而是在 **供审批的时间条目** 视图或 **供审批的支出条目** 视图中显示已取消的审批，具体取决于是时间条目还是支出条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="8cbc5-118">此外，相关时间或支出条目的状态更改为 **已提交**，以便让关联的条目与状态为 **草稿** 的审批一致。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="8cbc5-119">作为审批者，您可以编辑状态为 **草稿** 的审批的一些字段。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="8cbc5-120">这些字段包括 **记帐类型** 和 **时间条目的可记帐工时**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="8cbc5-121">进行更改之后，可再次审批记录。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="8cbc5-122">也可以拒绝此条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="8cbc5-123">如果拒绝时间条目的审批，该条目的状态将更改为 **已返回**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="8cbc5-124">如果拒绝支出条目的审批，该状态将更改为 **已拒绝**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="8cbc5-125">在功能方面，已返回条目和已拒绝条目与状态为 **草稿** 的条目具有相同行为。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="8cbc5-126">项目团队成员可以对条目进行所需的任何更改，然后重新提交进行审批，或完全删除条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="8cbc5-127">财务影响</span><span class="sxs-lookup"><span data-stu-id="8cbc5-127">Financial impact</span></span>

<span data-ttu-id="8cbc5-128">取消审批时，也会对项目造成财务影响。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="8cbc5-129">首先，按照以下方式更新成本和销售额的相应实际值。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="8cbc5-130">调整状态设置为 **已调整**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="8cbc5-131">记帐状态设置为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="8cbc5-132">接下来，在实际值表中创建冲销条目。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="8cbc5-133">为了创建冲销条目，系统将复制并覆盖原始实际值的字段值。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="8cbc5-134">唯一不复制覆盖的值为数量值。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="8cbc5-135">而是冲销这些值。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-135">These values are reversed instead.</span></span> <span data-ttu-id="8cbc5-136">将为实际 **成本** 和 **未记帐销售额** 创建冲销实际值。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="8cbc5-137">已冲销实际值的 **调整状态** 字段设置为 **不可调整**，而记帐状态设置为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="8cbc5-138">进行这些更改之后，记录为已对项目使用的金额和项目的收入积压不再计入这些实际值表示的金额。</span><span class="sxs-lookup"><span data-stu-id="8cbc5-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
