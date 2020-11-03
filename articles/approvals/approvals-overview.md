---
title: 审批概述
description: 本主题提供有关在 Project Operations 中使用审批的信息。
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072464"
---
# <a name="approvals-overview"></a><span data-ttu-id="7529f-103">审批概述</span><span class="sxs-lookup"><span data-stu-id="7529f-103">Approvals overview</span></span>

<span data-ttu-id="7529f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="7529f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7529f-105">时间和支出提交通过审批工作流移动。</span><span class="sxs-lookup"><span data-stu-id="7529f-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="7529f-106">条目被批准后，将在实际值中记录交易或在计划中预订时间。</span><span class="sxs-lookup"><span data-stu-id="7529f-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="7529f-107">审批工作流</span><span class="sxs-lookup"><span data-stu-id="7529f-107">Approvals workflow</span></span>
<span data-ttu-id="7529f-108">当您创建和提交时间或支出条目时，会创建一个审批条目。</span><span class="sxs-lookup"><span data-stu-id="7529f-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="7529f-109">项目审批者或您的经理将审核和审批您的条目。</span><span class="sxs-lookup"><span data-stu-id="7529f-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="7529f-110">如果条目与项目相关，在批准后，将创建实际值。</span><span class="sxs-lookup"><span data-stu-id="7529f-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="7529f-111">这样可以跟踪成本和计费。</span><span class="sxs-lookup"><span data-stu-id="7529f-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="7529f-112">审批条目</span><span class="sxs-lookup"><span data-stu-id="7529f-112">Approve an entry</span></span>
<span data-ttu-id="7529f-113">通过 **审批** 窗体，您可以在不同的视图之间切换，查看不同类型的审批。</span><span class="sxs-lookup"><span data-stu-id="7529f-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="7529f-114">转到 **审批** 窗体，选择 **支出** 、 **时间** 或 **撤消** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="7529f-115">查看每个审批，选择您要执行的审批。</span><span class="sxs-lookup"><span data-stu-id="7529f-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="7529f-116">选择 **批准** 将批准选定的条目。</span><span class="sxs-lookup"><span data-stu-id="7529f-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="7529f-117">系统将处理这些条目并创建实际值或预订。</span><span class="sxs-lookup"><span data-stu-id="7529f-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="7529f-118">拒绝条目</span><span class="sxs-lookup"><span data-stu-id="7529f-118">Reject an entry</span></span>
<span data-ttu-id="7529f-119">作为项目审批者，您可能必须将条目发送回用户以进行更正。</span><span class="sxs-lookup"><span data-stu-id="7529f-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="7529f-120">转到 **审批** 窗体，选择要拒绝的条目。</span><span class="sxs-lookup"><span data-stu-id="7529f-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="7529f-121">选择 **拒绝** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-121">Select **Reject**.</span></span>
3. <span data-ttu-id="7529f-122">可选 - 在 **拒绝注释** 对话框中添加注释，以告知用户条目为何被拒绝。</span><span class="sxs-lookup"><span data-stu-id="7529f-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="7529f-123">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-123">Select **OK**.</span></span> <span data-ttu-id="7529f-124">此条目将返回给用户。</span><span class="sxs-lookup"><span data-stu-id="7529f-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="7529f-125">撤消条目</span><span class="sxs-lookup"><span data-stu-id="7529f-125">Recall entries</span></span>
<span data-ttu-id="7529f-126">在某些时候，您可能需要撤消已提交的条目。</span><span class="sxs-lookup"><span data-stu-id="7529f-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="7529f-127">如果条目尚未被批准，将会立即退回。</span><span class="sxs-lookup"><span data-stu-id="7529f-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="7529f-128">但是，已批准的条目可能会影响材料。</span><span class="sxs-lookup"><span data-stu-id="7529f-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="7529f-129">为了撤消实际值中的交易，需要项目审批者批准撤消。</span><span class="sxs-lookup"><span data-stu-id="7529f-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="7529f-130">指定项目审批者</span><span class="sxs-lookup"><span data-stu-id="7529f-130">Specify Project approvers</span></span>
<span data-ttu-id="7529f-131">每个项目有很多项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="7529f-131">Each project has a number of project team members.</span></span> <span data-ttu-id="7529f-132">您还可以指定哪些团队成员同时也是项目审批者。</span><span class="sxs-lookup"><span data-stu-id="7529f-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="7529f-133">转到 **项目** 窗体，从列表中打开项目。</span><span class="sxs-lookup"><span data-stu-id="7529f-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="7529f-134">在 **团队** 选项卡上，选择将成为项目审批者的团队成员，然后选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="7529f-135">将 **项目审批者** 字段设置为 **是** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="7529f-136">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-136">Select **Save**.</span></span>
5. <span data-ttu-id="7529f-137">重复步骤 2-4 添加其他项目审批者。</span><span class="sxs-lookup"><span data-stu-id="7529f-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="7529f-138">配置用户的经理</span><span class="sxs-lookup"><span data-stu-id="7529f-138">Configure the user's manager</span></span>

1. <span data-ttu-id="7529f-139">转到 **设置** > **安全** > **用户** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="7529f-140">选择要向其分派经理的用户，然后在 **组织信息** 区域中，从列表中选择经理。</span><span class="sxs-lookup"><span data-stu-id="7529f-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="7529f-141">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="7529f-141">Select **Save**.</span></span>


