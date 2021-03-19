---
title: 重新打造支出报表
description: 本主题说明了重新设计和重新构想的支出报表条目体验。
author: suvaidya
manager: AnnBe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aaa7dd24915982cf137b5959f2f4c244b9c1e012
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499705"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="a1aa0-103">重新打造支出报表</span><span class="sxs-lookup"><span data-stu-id="a1aa0-103">Expense reports reimagined</span></span>

<span data-ttu-id="a1aa0-104">支出报表条目已重新设计，以简化流程并减少完成报表所需的时间。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-104">Expense report entry has been redesigned to simplify the process and reduce the time needed to complete a report.</span></span> <span data-ttu-id="a1aa0-105">以下是新支出体验的主要组成部分：</span><span class="sxs-lookup"><span data-stu-id="a1aa0-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="a1aa0-106">新支出管理工作区可让您访问代理的支出。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="a1aa0-107">新的收据匹配体验，可以更好地显示标题级收据并简化将收据附加到支出行的流程。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="a1aa0-108">新的只读网格，使您可以查看更多支出行和其他数据列。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="a1aa0-109">现在，您可以查看所有细化和拆分的行及其父级支出。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="a1aa0-110">用于编辑支出的简化窗格。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="a1aa0-111">重新设计了错误、警告和策略消息，以提供正确的上下文以及对问题及如何解决的理解。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-111">Redesigned error, warning, and policy messages to provide the correct context and understanding of the issue and how to resolve it.</span></span> <span data-ttu-id="a1aa0-112">我们删除了在用户完成任务并解决问题之前出现的一些消息。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-112">We have removed several of the messages that appeared before users could complete their tasks and address the issues.</span></span>
- <span data-ttu-id="a1aa0-113">一个新页面，用于指定必填字段、可选字段和不应包含的字段。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-113">A new page to specify required fields, optional fields, and the fields that should not be included.</span></span> <span data-ttu-id="a1aa0-114">此页帮助减少必须设置的字段的数量。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-114">This page helps to reduce the number of fields that must be set.</span></span>
- <span data-ttu-id="a1aa0-115">新的支出报表外观，使报表看起来不再像是为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="a1aa0-116">若要启用新体验，请使用 **功能管理** 工作区打开 **重新打造支出报表** 功能。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports reimagined** feature.</span></span> <span data-ttu-id="a1aa0-117">当您启用此功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="a1aa0-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="a1aa0-118">现有支出工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a1aa0-119">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a1aa0-120">支出报表（现有页面）或支出报表字段的现有菜单项未删除。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="a1aa0-121">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="a1aa0-122">为新用户提供的入门视频</span><span class="sxs-lookup"><span data-stu-id="a1aa0-122">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="a1aa0-123">[Dynamics 365 for Finance and Operations 中的支出体验](https://youtu.be/Ocy-MsTvEE0)视频（上方所示）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-123">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="a1aa0-124">新功能</span><span class="sxs-lookup"><span data-stu-id="a1aa0-124">New features</span></span>

| <span data-ttu-id="a1aa0-125">新功能</span><span class="sxs-lookup"><span data-stu-id="a1aa0-125">New feature</span></span> | <span data-ttu-id="a1aa0-126">描述</span><span class="sxs-lookup"><span data-stu-id="a1aa0-126">Description</span></span> |
|---|----|
| <span data-ttu-id="a1aa0-127">支出字段可见性</span><span class="sxs-lookup"><span data-stu-id="a1aa0-127">Expense field visibility</span></span> | <span data-ttu-id="a1aa0-128">新设置页面使您可以指定应对组织禁用的字段，应该必填的字段以及建议的字段。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-128">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="a1aa0-129">必填字段</span><span class="sxs-lookup"><span data-stu-id="a1aa0-129">Required fields</span></span> | <span data-ttu-id="a1aa0-130">新的简单配置使您无需使用策略框架即可让一些字段成为必填字段。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-130">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="a1aa0-131">可选字段</span><span class="sxs-lookup"><span data-stu-id="a1aa0-131">Optional fields</span></span> | <span data-ttu-id="a1aa0-132">添加了第二个可选字段页面。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-132">A second page for optional fields is added.</span></span> <span data-ttu-id="a1aa0-133">这样，员工不会觉得自己必须设置这些字段，但这些字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-133">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="a1aa0-134">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="a1aa0-134">Add unattached receipts</span></span> | <span data-ttu-id="a1aa0-135">从工作区和支出报表上可以更清楚地看到将未附加的收据添加到支出报表的功能。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-135">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="a1aa0-136">改进的消息</span><span class="sxs-lookup"><span data-stu-id="a1aa0-136">Improved messaging</span></span> | <span data-ttu-id="a1aa0-137">可以更好地查看有警告或错误的支出行。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-137">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="a1aa0-138">减少消息栏中的消息</span><span class="sxs-lookup"><span data-stu-id="a1aa0-138">Reduction in messages in the message bar</span></span>| <span data-ttu-id="a1aa0-139">减少了信息日志消息的数量，并努力使在多数情况下不会出现重复消息。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-139">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="a1aa0-140">将常用操作分组在一起</span><span class="sxs-lookup"><span data-stu-id="a1aa0-140">Grouped together common actions</span></span> | <span data-ttu-id="a1aa0-141">对界面进行了清理，为大多数常用的行级操作添加了新操作按钮，为标题和其他使用频率较低的操作添加了省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-141">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="a1aa0-142">提高可见性的新工作区</span><span class="sxs-lookup"><span data-stu-id="a1aa0-142">New workspace to increase visibility</span></span> | <span data-ttu-id="a1aa0-143">新工作区统一了让用户能够转到不同区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-143">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="a1aa0-144">在支出创建过程中添加现有支出和收据</span><span class="sxs-lookup"><span data-stu-id="a1aa0-144">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="a1aa0-145">创建支出报表时，可以添加所有支出，也可以选择未附加的支出。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-145">When you create expense reports, you can add all expenses, or select unattached expenses.</span></span> <span data-ttu-id="a1aa0-146">未附加的支出是从公司信用卡源导入的支出，或用户手动创建但却没有附加到支出报表的支出。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-146">Unattached expenses are expenses that were imported from the corporate credit card feed or expenses that were manually created by the user but haven't been attached to an expense report.</span></span>|
| <span data-ttu-id="a1aa0-147">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="a1aa0-147">Exchange rate calculator</span></span> | <span data-ttu-id="a1aa0-148">添加了汇率计算器，可让您计算现金支付多货币交易的汇率。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="a1aa0-149">保存和添加新支出行</span><span class="sxs-lookup"><span data-stu-id="a1aa0-149">Save and add new expense lines</span></span> | <span data-ttu-id="a1aa0-150">输入新支出时，**保存** 和 **新建** 按钮可用，帮助您快速输入支出行。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="a1aa0-151">更清晰地查看拆分和细化行</span><span class="sxs-lookup"><span data-stu-id="a1aa0-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="a1aa0-152">细化和拆分行直接添加到支出列表中，以增加可见性，帮助您轻松确定是否有错误。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-152">Itemized and split lines are added directly to the list of expenses to increase visibility and help you easily determine whether there are any errors.</span></span> |
| <span data-ttu-id="a1aa0-153">在细化时显示收据</span><span class="sxs-lookup"><span data-stu-id="a1aa0-153">Show receipts during itemization</span></span> | <span data-ttu-id="a1aa0-154">收据可以在细化时显示。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-154">Receipts can be shown during itemization.</span></span> |
| <span data-ttu-id="a1aa0-155">预付现金选择</span><span class="sxs-lookup"><span data-stu-id="a1aa0-155">Cash advance selection</span></span> | <span data-ttu-id="a1aa0-156">选择一个或多个预付现金以完成单个支出交易。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-156">Select one or more cash advances for fulfilling a single expense transaction.</span></span> |
| <span data-ttu-id="a1aa0-157">预付现金余额</span><span class="sxs-lookup"><span data-stu-id="a1aa0-157">Cash advance balance</span></span> | <span data-ttu-id="a1aa0-158">在针对批准和付款的预付现金创建支出条目时，实时查看预付现金余额。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-158">Review the cash advance balance in real time when you create an expense entry against approved and paid cash advances.</span></span> |

<span data-ttu-id="a1aa0-159">初始版本关注的是支出输入场景。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-159">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="a1aa0-160">任何支出报表的检查或审批场景都将继续使用现有的支出输入页面。</span><span class="sxs-lookup"><span data-stu-id="a1aa0-160">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="a1aa0-161">以下功能在重新构想的支出工作区中不受支持：</span><span class="sxs-lookup"><span data-stu-id="a1aa0-161">The following features aren't supported on the Reimagined Expense Workspace:</span></span>

- <span data-ttu-id="a1aa0-162">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="a1aa0-162">Travel requisition integration</span></span>
- <span data-ttu-id="a1aa0-163">每日支出条目</span><span class="sxs-lookup"><span data-stu-id="a1aa0-163">Per diem expense entry</span></span>
- <span data-ttu-id="a1aa0-164">临时审批者支持</span><span class="sxs-lookup"><span data-stu-id="a1aa0-164">Interim approver support</span></span>
- <span data-ttu-id="a1aa0-165">能够查看工作流历史记录</span><span class="sxs-lookup"><span data-stu-id="a1aa0-165">Ability to view workflow history</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
