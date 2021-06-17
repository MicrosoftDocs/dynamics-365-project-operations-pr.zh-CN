---
title: 重新打造支出报表
description: 本主题说明了重新设计和重新构想的支出报表条目体验。
author: suvaidya
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76073d5c58398b2c296fdca05ba7bdf7f01951bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995340"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="4d3d4-103">重新打造支出报表</span><span class="sxs-lookup"><span data-stu-id="4d3d4-103">Expense reports reimagined</span></span>

<span data-ttu-id="4d3d4-104">支出报表条目已重新设计，以简化流程并减少完成报表所需的时间。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="4d3d4-105">以下是新支出体验的主要组成部分：</span><span class="sxs-lookup"><span data-stu-id="4d3d4-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="4d3d4-106">新支出管理工作区可让您访问代理的支出。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="4d3d4-107">新的收据匹配体验，可以更好地显示标题级收据并简化将收据附加到支出行的流程。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="4d3d4-108">新的只读网格，使您可以查看更多支出行和其他数据列。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="4d3d4-109">现在，您可以查看所有细化和拆分的行及其父级支出。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="4d3d4-110">用于编辑支出的简化窗格。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="4d3d4-111">重新设计了错误、警告和策略消息，以提供正确的上下文以及对问题及如何解决的理解。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="4d3d4-112">我们删除了在用户完成任务并解决问题之前出现的一些消息。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="4d3d4-113">一个新页面，用于指定必填字段、可选字段和不应包含的字段。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="4d3d4-114">此页帮助减少必须设置的字段的数量。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="4d3d4-115">新的支出报表外观，使报表看起来不再像是为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="4d3d4-116">若要启用新体验，请使用 **功能管理** 工作区打开 **重新打造支出报表** 功能。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined** feature.</span></span> <span data-ttu-id="4d3d4-117">当您启用此功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="4d3d4-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="4d3d4-118">现有支出工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="4d3d4-119">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="4d3d4-120">支出报表（现有页面）或支出报表字段的现有菜单项未删除。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="4d3d4-121">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a><span data-ttu-id="4d3d4-122">新功能</span><span class="sxs-lookup"><span data-stu-id="4d3d4-122">New features</span></span>

| <span data-ttu-id="4d3d4-123">新功能</span><span class="sxs-lookup"><span data-stu-id="4d3d4-123">New feature</span></span> | <span data-ttu-id="4d3d4-124">描述</span><span class="sxs-lookup"><span data-stu-id="4d3d4-124">Description</span></span> |
|---|----|
| <span data-ttu-id="4d3d4-125">支出字段可见性</span><span class="sxs-lookup"><span data-stu-id="4d3d4-125">Expense field visibility</span></span> | <span data-ttu-id="4d3d4-126">新设置页面使您可以指定应对组织禁用的字段，应该必填的字段以及建议的字段。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-126">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="4d3d4-127">必填字段</span><span class="sxs-lookup"><span data-stu-id="4d3d4-127">Required fields</span></span> | <span data-ttu-id="4d3d4-128">新的简单配置使您无需使用策略框架即可让一些字段成为必填字段。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-128">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="4d3d4-129">可选字段</span><span class="sxs-lookup"><span data-stu-id="4d3d4-129">Optional fields</span></span> | <span data-ttu-id="4d3d4-130">添加了第二个可选字段页面。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-130">A second page for optional fields is added.</span></span> <span data-ttu-id="4d3d4-131">这样，员工不会觉得自己必须设置这些字段，但这些字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-131">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="4d3d4-132">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="4d3d4-132">Add unattached receipts</span></span> | <span data-ttu-id="4d3d4-133">从工作区和支出报表上可以更清楚地看到将未附加的收据添加到支出报表的功能。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-133">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="4d3d4-134">改进的消息</span><span class="sxs-lookup"><span data-stu-id="4d3d4-134">Improved messaging</span></span> | <span data-ttu-id="4d3d4-135">可以更好地查看有警告或错误的支出行。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-135">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="4d3d4-136">减少消息栏中的消息</span><span class="sxs-lookup"><span data-stu-id="4d3d4-136">Reduction in messages in the message bar</span></span>| <span data-ttu-id="4d3d4-137">减少了信息日志消息的数量，并努力使在多数情况下不会出现重复消息。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-137">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="4d3d4-138">将常用操作分组在一起</span><span class="sxs-lookup"><span data-stu-id="4d3d4-138">Grouped together common actions</span></span> | <span data-ttu-id="4d3d4-139">对界面进行了清理，为大多数常用的行级操作添加了新操作按钮，为标题和其他使用频率较低的操作添加了省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-139">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="4d3d4-140">提高可见性的新工作区</span><span class="sxs-lookup"><span data-stu-id="4d3d4-140">New workspace to increase visibility</span></span> | <span data-ttu-id="4d3d4-141">新工作区统一了让用户能够转到不同区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-141">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="4d3d4-142">在支出创建过程中添加现有支出和收据</span><span class="sxs-lookup"><span data-stu-id="4d3d4-142">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="4d3d4-143">创建支出报表时，可以添加所有支出，也可以选择未附加的支出。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-143">When you create expense reports, you can add all expenses, or select unattached expenses.</span></span> <span data-ttu-id="4d3d4-144">未附加的支出是从公司信用卡源导入的支出，或用户手动创建但却没有附加到支出报表的支出。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-144">Unattached expenses are expenses that were imported from the corporate credit card feed or expenses that were manually created by the user but haven't been attached to an expense report.</span></span>|
| <span data-ttu-id="4d3d4-145">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="4d3d4-145">Exchange rate calculator</span></span> | <span data-ttu-id="4d3d4-146">添加了汇率计算器，可让您计算现金支付多货币交易的汇率。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-146">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="4d3d4-147">保存和添加新支出行</span><span class="sxs-lookup"><span data-stu-id="4d3d4-147">Save and add new expense lines</span></span> | <span data-ttu-id="4d3d4-148">输入新支出时，**保存** 和 **新建** 按钮可用，帮助您快速输入支出行。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-148">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="4d3d4-149">更清晰地查看拆分和细化行</span><span class="sxs-lookup"><span data-stu-id="4d3d4-149">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="4d3d4-150">细化和拆分行直接添加到支出列表中，以增加可见性，帮助您轻松确定是否有错误。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-150">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="4d3d4-151">在细化时显示收据</span><span class="sxs-lookup"><span data-stu-id="4d3d4-151">Show receipts during itemization</span></span> | <span data-ttu-id="4d3d4-152">收据可以在细化时显示。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-152">Receipts can be shown during itemization.</span></span> |
| <span data-ttu-id="4d3d4-153">预付现金选择</span><span class="sxs-lookup"><span data-stu-id="4d3d4-153">Cash advance selection</span></span> | <span data-ttu-id="4d3d4-154">选择一个或多个预付现金以完成单个支出交易。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-154">Select one or more cash advances for fulfilling a single expense transaction.</span></span> |
| <span data-ttu-id="4d3d4-155">预付现金余额</span><span class="sxs-lookup"><span data-stu-id="4d3d4-155">Cash advance balance</span></span> | <span data-ttu-id="4d3d4-156">在针对批准和付款的预付现金创建支出条目时，实时查看预付现金余额。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-156">Review the cash advance balance in real time when you create an expense entry against approved and paid cash advances.</span></span> |

<span data-ttu-id="4d3d4-157">初始版本关注的是支出输入场景。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-157">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="4d3d4-158">任何支出报表的检查或审批场景都将继续使用现有的支出输入页面。</span><span class="sxs-lookup"><span data-stu-id="4d3d4-158">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="4d3d4-159">以下功能在重新构想的支出工作区中不受支持：</span><span class="sxs-lookup"><span data-stu-id="4d3d4-159">The following features aren't supported on the Reimagined Expense Workspace:</span></span>

- <span data-ttu-id="4d3d4-160">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="4d3d4-160">Travel requisition integration</span></span>
- <span data-ttu-id="4d3d4-161">每日支出条目</span><span class="sxs-lookup"><span data-stu-id="4d3d4-161">Per diem expense entry</span></span>
- <span data-ttu-id="4d3d4-162">临时审批者支持</span><span class="sxs-lookup"><span data-stu-id="4d3d4-162">Interim approver support</span></span>
- <span data-ttu-id="4d3d4-163">能够查看工作流历史记录</span><span class="sxs-lookup"><span data-stu-id="4d3d4-163">Ability to view workflow history</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
