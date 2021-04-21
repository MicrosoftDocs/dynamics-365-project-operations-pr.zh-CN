---
title: 审批概述
description: 本主题提供有关在 Project Operations 中使用审批的信息。
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852488"
---
# <a name="approvals-overview"></a><span data-ttu-id="6a9a6-103">审批概述</span><span class="sxs-lookup"><span data-stu-id="6a9a6-103">Approvals overview</span></span>

<span data-ttu-id="6a9a6-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="6a9a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a9a6-105">时间、支出和材料使用提交将经历审批工作流。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="6a9a6-106">条目被批准后，将在实际值中记录交易或在计划中预订时间。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="6a9a6-107">审批工作流</span><span class="sxs-lookup"><span data-stu-id="6a9a6-107">Approvals workflow</span></span>
<span data-ttu-id="6a9a6-108">创建并提交时间、支出或材料使用条目时，将创建审批记录。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="6a9a6-109">项目审批者或经理将审核并批准该条目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="6a9a6-110">如果此条目与项目相关，则将在审批后创建实际值。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="6a9a6-111">这样可以跟踪成本和计费。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="6a9a6-112">审批条目</span><span class="sxs-lookup"><span data-stu-id="6a9a6-112">Approve an entry</span></span>
<span data-ttu-id="6a9a6-113"> **审批** 页使您能够在不同的视图之间切换，以便可以查看不同类型的审批。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="6a9a6-114">转到 **审批** 页并选择 **支出**、**时间**、**材料使用** 或 **撤消**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="6a9a6-115">查看每个审批，选择您要执行的审批。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="6a9a6-116">选择 **批准** 将批准选定的条目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="6a9a6-117">系统将处理这些条目并创建实际值。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="6a9a6-118">拒绝条目</span><span class="sxs-lookup"><span data-stu-id="6a9a6-118">Reject an entry</span></span>
<span data-ttu-id="6a9a6-119">作为项目审批者，您可能必须将条目发送回用户以进行更正。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="6a9a6-120">转到 **审批** 页面，选择要拒绝的条目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="6a9a6-121">选择 **拒绝**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-121">Select **Reject**.</span></span>
3. <span data-ttu-id="6a9a6-122">（可选）请在 **拒绝注释** 对话框中添加注释，以通知用户拒绝该条目的原因。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="6a9a6-123">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-123">Select **OK**.</span></span> <span data-ttu-id="6a9a6-124">此条目将返回给用户。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="6a9a6-125">取消审批</span><span class="sxs-lookup"><span data-stu-id="6a9a6-125">Cancel approval</span></span>
<span data-ttu-id="6a9a6-126">在某些情况下，您可能需要取消以前批准的条目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="6a9a6-127">取消之前批准的条目将影响财务。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="6a9a6-128">审批撤消请求</span><span class="sxs-lookup"><span data-stu-id="6a9a6-128">Approving recall requests</span></span>
<span data-ttu-id="6a9a6-129">在某些情况下，顾问可能需要撤消之前批准的条目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="6a9a6-130">取消之前批准的条目将影响财务。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="6a9a6-131">项目审批者需要批准撤消以撤消实际值中的交易。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="6a9a6-132">指定项目审批者</span><span class="sxs-lookup"><span data-stu-id="6a9a6-132">Specify Project approvers</span></span>
<span data-ttu-id="6a9a6-133">每个项目有很多项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-133">Each project has a number of project team members.</span></span> <span data-ttu-id="6a9a6-134">您还可以指定哪些团队成员同时也是项目审批者。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="6a9a6-135">转到 **项目** 页，并从列表中打开项目。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="6a9a6-136">在 **团队** 选项卡上，选择将成为项目审批者的团队成员，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="6a9a6-137">将 **项目审批者** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="6a9a6-138">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-138">Select **Save**.</span></span>
5. <span data-ttu-id="6a9a6-139">重复步骤 2-4 添加其他项目审批者。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="6a9a6-140">配置用户的经理</span><span class="sxs-lookup"><span data-stu-id="6a9a6-140">Configure the user's manager</span></span>

1. <span data-ttu-id="6a9a6-141">转到 **设置** > **安全** > **用户**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="6a9a6-142">选择要向其分派经理的用户，然后在 **组织信息** 区域中，从列表中选择经理。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="6a9a6-143">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6a9a6-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
