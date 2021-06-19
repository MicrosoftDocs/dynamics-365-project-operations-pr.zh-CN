---
title: 审批集
description: 本主题提供有关审批集、请求和这些操作的子集的信息。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116860"
---
# <a name="approval-sets"></a><span data-ttu-id="8518c-103">审批集</span><span class="sxs-lookup"><span data-stu-id="8518c-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8518c-104">审批集将审批请求一起组成一个较小的操作子集。</span><span class="sxs-lookup"><span data-stu-id="8518c-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="8518c-105">此分组允许按项目顺序处理审批，并允许重试和排序。</span><span class="sxs-lookup"><span data-stu-id="8518c-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="8518c-106">对于大量审批，分组提高了审批处理的可靠性和可追溯性。</span><span class="sxs-lookup"><span data-stu-id="8518c-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="8518c-107">审批集指示其相关记录的整体处理状态。</span><span class="sxs-lookup"><span data-stu-id="8518c-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="8518c-108">在使用审批集处理审批记录时，记录会从 **已提交** 转变为 **已审批**，并且与审批集不关联。</span><span class="sxs-lookup"><span data-stu-id="8518c-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="8518c-109">如果记录在提交审批后失败，则记录会保持 **已提交** 状态，并且审批集会标记为失败。</span><span class="sxs-lookup"><span data-stu-id="8518c-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="8518c-110">审批集会记录失败的错误消息。</span><span class="sxs-lookup"><span data-stu-id="8518c-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="8518c-111">处理审批和审批集</span><span class="sxs-lookup"><span data-stu-id="8518c-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="8518c-112">排队等待处理的审批在 **处理审批** 视图中可见。</span><span class="sxs-lookup"><span data-stu-id="8518c-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="8518c-113">系统尝试多次异步处理所有条目，包括在先前尝试失败时重试审批。</span><span class="sxs-lookup"><span data-stu-id="8518c-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="8518c-114">**审批集生存期** 字段记录了在将集标记为失败之前剩余的集处理尝试次数。</span><span class="sxs-lookup"><span data-stu-id="8518c-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="8518c-115">失败的审批和审批集</span><span class="sxs-lookup"><span data-stu-id="8518c-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="8518c-116">**失败的审批** 视图会列出需要用户干预的所有审批。</span><span class="sxs-lookup"><span data-stu-id="8518c-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="8518c-117">打开关联的审批集日志以确定失败的原因。</span><span class="sxs-lookup"><span data-stu-id="8518c-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="8518c-118">选择 **重试** 可添加到审批集生存期计数中，将审批集重新设置为 **正在处理** 状态，并尝试处理其余记录。</span><span class="sxs-lookup"><span data-stu-id="8518c-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="8518c-119">配置审批集</span><span class="sxs-lookup"><span data-stu-id="8518c-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="8518c-120">启用“审批集”功能</span><span class="sxs-lookup"><span data-stu-id="8518c-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="8518c-121">在启用“审批集”功能之前，确认当前没有正在处理审批。</span><span class="sxs-lookup"><span data-stu-id="8518c-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8518c-122">转到 **项目参数** 页并选择 **功能控制** > **启用现代审批**。</span><span class="sxs-lookup"><span data-stu-id="8518c-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="8518c-123">关闭“审批集”功能</span><span class="sxs-lookup"><span data-stu-id="8518c-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="8518c-124">在关闭“审批集”功能之前，确认当前没有正在处理审批。</span><span class="sxs-lookup"><span data-stu-id="8518c-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8518c-125">转到 **项目参数** 页并选择 **功能控制** > **禁用现代审批**。</span><span class="sxs-lookup"><span data-stu-id="8518c-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="8518c-126">配置异步阈值</span><span class="sxs-lookup"><span data-stu-id="8518c-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="8518c-127">创建审批集后，当选定的审批记录数超过指示的阈值时，处理会移到后台。</span><span class="sxs-lookup"><span data-stu-id="8518c-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="8518c-128">使用 **异步阈值** 字段配置应该同步或异步运行审批处理的时间。</span><span class="sxs-lookup"><span data-stu-id="8518c-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="8518c-129">有效值为：</span><span class="sxs-lookup"><span data-stu-id="8518c-129">Valid values are:</span></span>

  - <span data-ttu-id="8518c-130">零：应异步处理所有请求。</span><span class="sxs-lookup"><span data-stu-id="8518c-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="8518c-131">大于零的数字：仅在提交审批数超过此值时异步处理审批。</span><span class="sxs-lookup"><span data-stu-id="8518c-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
