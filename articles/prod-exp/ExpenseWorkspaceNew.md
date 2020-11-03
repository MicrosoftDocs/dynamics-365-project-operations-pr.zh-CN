---
title: 重新设计的支出报表
description: 本主题介绍 Microsoft Dynamics 365 Finance 中经过重新设计和重构的支出报表录入体验。 新体验简化了填写支出报表的流程，并缩短了所需时间。
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ec8737d848ae5ad25219a43c68306d19b1c1fbce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072647"
---
# <a name="redesigned-expense-reports"></a><span data-ttu-id="b7a92-104">重新设计的支出报表</span><span class="sxs-lookup"><span data-stu-id="b7a92-104">Redesigned expense reports</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7a92-105">重新设计了支出报表录入，以便简化填写支出报表的流程和缩短所需时间。</span><span class="sxs-lookup"><span data-stu-id="b7a92-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="b7a92-106">以下是新支出体验的主要组成部分：</span><span class="sxs-lookup"><span data-stu-id="b7a92-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="b7a92-107">新支出管理工作区可让您访问代理的支出。</span><span class="sxs-lookup"><span data-stu-id="b7a92-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="b7a92-108">新的收据匹配体验，可以更好地显示标题级收据并简化将收据附加到支出行的流程。</span><span class="sxs-lookup"><span data-stu-id="b7a92-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="b7a92-109">新的只读网格，使您可以查看更多支出行和其他数据列。</span><span class="sxs-lookup"><span data-stu-id="b7a92-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="b7a92-110">现在，您可以查看所有细化和拆分的行及其父级支出。</span><span class="sxs-lookup"><span data-stu-id="b7a92-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="b7a92-111">用于编辑支出的简化窗格。</span><span class="sxs-lookup"><span data-stu-id="b7a92-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="b7a92-112">错误、警告和策略消息已经过重新设计，可以帮助确保为您提供正确的上下文来了解问题及其解决方法。</span><span class="sxs-lookup"><span data-stu-id="b7a92-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="b7a92-113">Microsoft 已删除了用户有机会完成任务之前显示的大量消息，并解决了明细化消息之类问题。</span><span class="sxs-lookup"><span data-stu-id="b7a92-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="b7a92-114">一个新页面，用于指定哪些字段是组织必需的，哪些字段可选和哪些字段不应捕获。</span><span class="sxs-lookup"><span data-stu-id="b7a92-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="b7a92-115">此页面将减少用户必须设置的字段数量。</span><span class="sxs-lookup"><span data-stu-id="b7a92-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="b7a92-116">新的支出报表外观，使报表看起来不再像是为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="b7a92-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="b7a92-117">若要开启新体验，请使用 **功能管理** 工作区开启 **已重构的支出报表** 功能。</span><span class="sxs-lookup"><span data-stu-id="b7a92-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="b7a92-118">当您启用此功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="b7a92-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="b7a92-119">现有支出工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="b7a92-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="b7a92-120">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="b7a92-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="b7a92-121">支出报表（现有页面）或支出报表字段的现有菜单项未删除。</span><span class="sxs-lookup"><span data-stu-id="b7a92-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="b7a92-122">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="b7a92-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="b7a92-123">为新用户提供的入门视频</span><span class="sxs-lookup"><span data-stu-id="b7a92-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="b7a92-124">[Dynamics 365 for Finance and Operations 中的支出体验](https://youtu.be/Ocy-MsTvEE0)视频（上方所示）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="b7a92-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="b7a92-125">新功能</span><span class="sxs-lookup"><span data-stu-id="b7a92-125">New features</span></span>

| <span data-ttu-id="b7a92-126">新功能</span><span class="sxs-lookup"><span data-stu-id="b7a92-126">New feature</span></span> | <span data-ttu-id="b7a92-127">描述</span><span class="sxs-lookup"><span data-stu-id="b7a92-127">Description</span></span> |
|---|----|
| <span data-ttu-id="b7a92-128">支出字段可见性</span><span class="sxs-lookup"><span data-stu-id="b7a92-128">Expense field visibility</span></span> | <span data-ttu-id="b7a92-129">新设置页面使您可以指定应对组织禁用的字段，应该必填的字段以及建议的字段。</span><span class="sxs-lookup"><span data-stu-id="b7a92-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="b7a92-130">必填字段</span><span class="sxs-lookup"><span data-stu-id="b7a92-130">Required fields</span></span> | <span data-ttu-id="b7a92-131">新的简单配置使您无需使用策略框架即可让一些字段成为必填字段。</span><span class="sxs-lookup"><span data-stu-id="b7a92-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="b7a92-132">可选字段</span><span class="sxs-lookup"><span data-stu-id="b7a92-132">Optional fields</span></span> | <span data-ttu-id="b7a92-133">添加了第二个可选字段页面。</span><span class="sxs-lookup"><span data-stu-id="b7a92-133">A second page for optional fields is added.</span></span> <span data-ttu-id="b7a92-134">这样，员工不会觉得自己必须设置这些字段，但这些字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="b7a92-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="b7a92-135">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="b7a92-135">Add unattached receipts</span></span> | <span data-ttu-id="b7a92-136">从工作区和支出报表上可以更清楚地看到将未附加的收据添加到支出报表的功能。</span><span class="sxs-lookup"><span data-stu-id="b7a92-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="b7a92-137">改进的消息</span><span class="sxs-lookup"><span data-stu-id="b7a92-137">Improved messaging</span></span> | <span data-ttu-id="b7a92-138">可以更好地查看有警告或错误的支出行。</span><span class="sxs-lookup"><span data-stu-id="b7a92-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="b7a92-139">减少消息栏中的消息</span><span class="sxs-lookup"><span data-stu-id="b7a92-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="b7a92-140">减少了信息日志消息的数量，并努力使在多数情况下不会出现重复消息。</span><span class="sxs-lookup"><span data-stu-id="b7a92-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="b7a92-141">将常用操作分组在一起</span><span class="sxs-lookup"><span data-stu-id="b7a92-141">Grouped together common actions</span></span> | <span data-ttu-id="b7a92-142">对界面进行了清理，为大多数常用的行级操作添加了新操作按钮，为标题和其他使用频率较低的操作添加了省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="b7a92-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="b7a92-143">提高可见性的新工作区</span><span class="sxs-lookup"><span data-stu-id="b7a92-143">New workspace to increase visibility</span></span> | <span data-ttu-id="b7a92-144">新工作区统一了让用户能够转到不同区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="b7a92-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="b7a92-145">在支出创建过程中添加现有支出和收据</span><span class="sxs-lookup"><span data-stu-id="b7a92-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="b7a92-146">在您创建支出报表时，可以添加所有或所选的支出和收据。</span><span class="sxs-lookup"><span data-stu-id="b7a92-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="b7a92-147">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="b7a92-147">Exchange rate calculator</span></span> | <span data-ttu-id="b7a92-148">添加了汇率计算器，可让您计算现金支付多货币交易的汇率。</span><span class="sxs-lookup"><span data-stu-id="b7a92-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="b7a92-149">保存和添加新支出行</span><span class="sxs-lookup"><span data-stu-id="b7a92-149">Save and add new expense lines</span></span> | <span data-ttu-id="b7a92-150">输入新支出时， **保存** 和 **新建** 按钮可用，帮助您快速输入支出行。</span><span class="sxs-lookup"><span data-stu-id="b7a92-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="b7a92-151">更清晰地查看拆分和细化行</span><span class="sxs-lookup"><span data-stu-id="b7a92-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="b7a92-152">明细化行和拆分行直接添加到支出列表，从而可以提高可见性和帮助您轻松确定是否发生了策略错误或其他错误。</span><span class="sxs-lookup"><span data-stu-id="b7a92-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="b7a92-153">在细化时显示收据</span><span class="sxs-lookup"><span data-stu-id="b7a92-153">Show receipts during itemization</span></span> | <span data-ttu-id="b7a92-154">收据可以在细化时显示。</span><span class="sxs-lookup"><span data-stu-id="b7a92-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="b7a92-155">初始版本关注的是支出输入场景。</span><span class="sxs-lookup"><span data-stu-id="b7a92-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="b7a92-156">任何支出报表的检查或审批场景都将继续使用现有的支出输入页面。</span><span class="sxs-lookup"><span data-stu-id="b7a92-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="b7a92-157">以下功能在现有页面上，但尚未在新页面提供。</span><span class="sxs-lookup"><span data-stu-id="b7a92-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="b7a92-158">这些功能将在接下来的几个版本中重新引入：</span><span class="sxs-lookup"><span data-stu-id="b7a92-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="b7a92-159">审批</span><span class="sxs-lookup"><span data-stu-id="b7a92-159">Approvals</span></span>
- <span data-ttu-id="b7a92-160">应付帐款审批和编辑会计的功能</span><span class="sxs-lookup"><span data-stu-id="b7a92-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="b7a92-161">多个进入点</span><span class="sxs-lookup"><span data-stu-id="b7a92-161">Multiple entry points</span></span>
- <span data-ttu-id="b7a92-162">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="b7a92-162">Travel requisition integration</span></span>
- <span data-ttu-id="b7a92-163">用于显示支出字段的数据实体</span><span class="sxs-lookup"><span data-stu-id="b7a92-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="b7a92-164">出差津贴支出条目</span><span class="sxs-lookup"><span data-stu-id="b7a92-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="b7a92-165">行级工作流</span><span class="sxs-lookup"><span data-stu-id="b7a92-165">Line-level workflow</span></span>
- <span data-ttu-id="b7a92-166">临时审批者支持</span><span class="sxs-lookup"><span data-stu-id="b7a92-166">Interim approver support</span></span>
- <span data-ttu-id="b7a92-167">高级细化</span><span class="sxs-lookup"><span data-stu-id="b7a92-167">Advanced itemization</span></span>
