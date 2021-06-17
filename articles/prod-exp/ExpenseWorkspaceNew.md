---
title: 重新设计的支出报表
description: 本主题提供有关重新设计和重新打造的支出报表输入体验的信息。
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: bd334d3404e9baae4f8314173834d9fbb708d574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993676"
---
# <a name="redesigned-expense-reports"></a><span data-ttu-id="039f3-103">重新设计的支出报表</span><span class="sxs-lookup"><span data-stu-id="039f3-103">Redesigned expense reports</span></span>

<span data-ttu-id="039f3-104">重新设计了支出报表录入，以便简化填写支出报表的流程和缩短所需时间。</span><span class="sxs-lookup"><span data-stu-id="039f3-104">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="039f3-105">以下是新支出体验的主要组成部分：</span><span class="sxs-lookup"><span data-stu-id="039f3-105">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="039f3-106">新支出管理工作区可让您访问代理的支出。</span><span class="sxs-lookup"><span data-stu-id="039f3-106">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="039f3-107">新的收据匹配体验，可以更好地显示标题级收据并简化将收据附加到支出行的流程。</span><span class="sxs-lookup"><span data-stu-id="039f3-107">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="039f3-108">新的只读网格，使您可以查看更多支出行和其他数据列。</span><span class="sxs-lookup"><span data-stu-id="039f3-108">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="039f3-109">现在，您可以查看所有细化和拆分的行及其父级支出。</span><span class="sxs-lookup"><span data-stu-id="039f3-109">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="039f3-110">用于编辑支出的简化窗格。</span><span class="sxs-lookup"><span data-stu-id="039f3-110">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="039f3-111">错误、警告和策略消息已经过重新设计，可以帮助确保为您提供正确的上下文来了解问题及其解决方法。</span><span class="sxs-lookup"><span data-stu-id="039f3-111">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="039f3-112">Microsoft 已删除了用户有机会完成任务之前显示的大量消息，并解决了明细化消息之类问题。</span><span class="sxs-lookup"><span data-stu-id="039f3-112">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="039f3-113">一个新页面，用于指定哪些字段是组织必需的，哪些字段可选和哪些字段不应捕获。</span><span class="sxs-lookup"><span data-stu-id="039f3-113">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="039f3-114">此页面将减少用户必须设置的字段数量。</span><span class="sxs-lookup"><span data-stu-id="039f3-114">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="039f3-115">新的支出报表外观，使报表看起来不再像是为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="039f3-115">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="039f3-116">若要开启新体验，请使用 **功能管理** 工作区开启 **已重构的支出报表** 功能。</span><span class="sxs-lookup"><span data-stu-id="039f3-116">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="039f3-117">当您启用此功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="039f3-117">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="039f3-118">现有支出工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="039f3-118">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="039f3-119">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="039f3-119">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="039f3-120">支出报表（现有页面）或支出报表字段的现有菜单项未删除。</span><span class="sxs-lookup"><span data-stu-id="039f3-120">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="039f3-121">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="039f3-121">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="new-features"></a><span data-ttu-id="039f3-122">新功能</span><span class="sxs-lookup"><span data-stu-id="039f3-122">New features</span></span>

| <span data-ttu-id="039f3-123">新功能</span><span class="sxs-lookup"><span data-stu-id="039f3-123">New feature</span></span> | <span data-ttu-id="039f3-124">描述</span><span class="sxs-lookup"><span data-stu-id="039f3-124">Description</span></span> |
|---|----|
| <span data-ttu-id="039f3-125">支出字段可见性</span><span class="sxs-lookup"><span data-stu-id="039f3-125">Expense field visibility</span></span> | <span data-ttu-id="039f3-126">新设置页面使您可以指定应对组织禁用的字段，应该必填的字段以及建议的字段。</span><span class="sxs-lookup"><span data-stu-id="039f3-126">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="039f3-127">必填字段</span><span class="sxs-lookup"><span data-stu-id="039f3-127">Required fields</span></span> | <span data-ttu-id="039f3-128">新的简单配置使您无需使用策略框架即可让一些字段成为必填字段。</span><span class="sxs-lookup"><span data-stu-id="039f3-128">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="039f3-129">可选字段</span><span class="sxs-lookup"><span data-stu-id="039f3-129">Optional fields</span></span> | <span data-ttu-id="039f3-130">添加了第二个可选字段页面。</span><span class="sxs-lookup"><span data-stu-id="039f3-130">A second page for optional fields is added.</span></span> <span data-ttu-id="039f3-131">这样，员工不会觉得自己必须设置这些字段，但这些字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="039f3-131">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="039f3-132">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="039f3-132">Add unattached receipts</span></span> | <span data-ttu-id="039f3-133">从工作区和支出报表上可以更清楚地看到将未附加的收据添加到支出报表的功能。</span><span class="sxs-lookup"><span data-stu-id="039f3-133">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="039f3-134">改进的消息</span><span class="sxs-lookup"><span data-stu-id="039f3-134">Improved messaging</span></span> | <span data-ttu-id="039f3-135">可以更好地查看有警告或错误的支出行。</span><span class="sxs-lookup"><span data-stu-id="039f3-135">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="039f3-136">减少消息栏中的消息</span><span class="sxs-lookup"><span data-stu-id="039f3-136">Reduction in messages in the message bar</span></span>| <span data-ttu-id="039f3-137">减少了信息日志消息的数量，并努力使在多数情况下不会出现重复消息。</span><span class="sxs-lookup"><span data-stu-id="039f3-137">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="039f3-138">将常用操作分组在一起</span><span class="sxs-lookup"><span data-stu-id="039f3-138">Grouped together common actions</span></span> | <span data-ttu-id="039f3-139">对界面进行了清理，为大多数常用的行级操作添加了新操作按钮，为标题和其他使用频率较低的操作添加了省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="039f3-139">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="039f3-140">提高可见性的新工作区</span><span class="sxs-lookup"><span data-stu-id="039f3-140">New workspace to increase visibility</span></span> | <span data-ttu-id="039f3-141">新工作区统一了让用户能够转到不同区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="039f3-141">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="039f3-142">在支出创建过程中添加现有支出和收据</span><span class="sxs-lookup"><span data-stu-id="039f3-142">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="039f3-143">在您创建支出报表时，可以添加所有或所选的支出和收据。</span><span class="sxs-lookup"><span data-stu-id="039f3-143">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="039f3-144">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="039f3-144">Exchange rate calculator</span></span> | <span data-ttu-id="039f3-145">添加了汇率计算器，可让您计算现金支付多货币交易的汇率。</span><span class="sxs-lookup"><span data-stu-id="039f3-145">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="039f3-146">保存和添加新支出行</span><span class="sxs-lookup"><span data-stu-id="039f3-146">Save and add new expense lines</span></span> | <span data-ttu-id="039f3-147">输入新支出时，**保存** 和 **新建** 按钮可用，帮助您快速输入支出行。</span><span class="sxs-lookup"><span data-stu-id="039f3-147">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="039f3-148">更清晰地查看拆分和细化行</span><span class="sxs-lookup"><span data-stu-id="039f3-148">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="039f3-149">明细化行和拆分行直接添加到支出列表，从而可以提高可见性和帮助您轻松确定是否发生了策略错误或其他错误。</span><span class="sxs-lookup"><span data-stu-id="039f3-149">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="039f3-150">在细化时显示收据</span><span class="sxs-lookup"><span data-stu-id="039f3-150">Show receipts during itemization</span></span> | <span data-ttu-id="039f3-151">收据可以在细化时显示。</span><span class="sxs-lookup"><span data-stu-id="039f3-151">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="039f3-152">初始版本关注的是支出输入场景。</span><span class="sxs-lookup"><span data-stu-id="039f3-152">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="039f3-153">任何支出报表的检查或审批场景都将继续使用现有的支出输入页面。</span><span class="sxs-lookup"><span data-stu-id="039f3-153">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="039f3-154">以下功能在现有页面上，但尚未在新页面提供。</span><span class="sxs-lookup"><span data-stu-id="039f3-154">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="039f3-155">这些功能将在接下来的几个版本中重新引入：</span><span class="sxs-lookup"><span data-stu-id="039f3-155">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="039f3-156">审批</span><span class="sxs-lookup"><span data-stu-id="039f3-156">Approvals</span></span>
- <span data-ttu-id="039f3-157">应付帐款审批和编辑会计的功能</span><span class="sxs-lookup"><span data-stu-id="039f3-157">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="039f3-158">多个进入点</span><span class="sxs-lookup"><span data-stu-id="039f3-158">Multiple entry points</span></span>
- <span data-ttu-id="039f3-159">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="039f3-159">Travel requisition integration</span></span>
- <span data-ttu-id="039f3-160">用于显示支出字段的数据实体</span><span class="sxs-lookup"><span data-stu-id="039f3-160">Data entity for expense field visibility</span></span>
- <span data-ttu-id="039f3-161">出差津贴支出条目</span><span class="sxs-lookup"><span data-stu-id="039f3-161">Entry for per-diem expenses</span></span>
- <span data-ttu-id="039f3-162">行级工作流</span><span class="sxs-lookup"><span data-stu-id="039f3-162">Line-level workflow</span></span>
- <span data-ttu-id="039f3-163">临时审批者支持</span><span class="sxs-lookup"><span data-stu-id="039f3-163">Interim approver support</span></span>
- <span data-ttu-id="039f3-164">高级细化</span><span class="sxs-lookup"><span data-stu-id="039f3-164">Advanced itemization</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]