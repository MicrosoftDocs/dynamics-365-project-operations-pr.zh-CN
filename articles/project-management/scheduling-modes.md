---
title: 计划模式
description: 本主题介绍计划模式。
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116696"
---
# <a name="scheduling-modes"></a><span data-ttu-id="c25e4-103">计划模式</span><span class="sxs-lookup"><span data-stu-id="c25e4-103">Scheduling modes</span></span>

<span data-ttu-id="c25e4-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="c25e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c25e4-105">Dynamics 365 Project Operations 让组织能够定义他们如何管理工作分解结构内任务中关键变量的更改。</span><span class="sxs-lookup"><span data-stu-id="c25e4-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="c25e4-106">根据组织的特定需求，项目经理可以在创建项目时更改计划模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="c25e4-107">Project Operations 中有三个计划模式：</span><span class="sxs-lookup"><span data-stu-id="c25e4-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="c25e4-108">固定持续时间（这是默认模式）</span><span class="sxs-lookup"><span data-stu-id="c25e4-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="c25e4-109">固定工作量（*工作*）</span><span class="sxs-lookup"><span data-stu-id="c25e4-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="c25e4-110">固定的单位</span><span class="sxs-lookup"><span data-stu-id="c25e4-110">Fixed units</span></span>

<span data-ttu-id="c25e4-111">受特定计划模式的定义影响的值由以下公式确定：</span><span class="sxs-lookup"><span data-stu-id="c25e4-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="c25e4-112">工作量 = 持续时间 x 单位</span><span class="sxs-lookup"><span data-stu-id="c25e4-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="c25e4-113">定义项目的计划模式时，您将设置以下值之一，之后此值将无法更改。</span><span class="sxs-lookup"><span data-stu-id="c25e4-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="c25e4-114">将此值保持为常数会对其赋予优先级，这会通知系统在其他两个值更改时不要更改它。</span><span class="sxs-lookup"><span data-stu-id="c25e4-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="c25e4-115">下表提供了有关选择特定模式的影响的信息。</span><span class="sxs-lookup"><span data-stu-id="c25e4-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="c25e4-116">**在此任务中**</span><span class="sxs-lookup"><span data-stu-id="c25e4-116">**In this task**</span></span>             | <span data-ttu-id="c25e4-117">**如果您修订单位**</span><span class="sxs-lookup"><span data-stu-id="c25e4-117">**If you revise units**</span></span>   | <span data-ttu-id="c25e4-118">**如果您修订持续时间**</span><span class="sxs-lookup"><span data-stu-id="c25e4-118">**If you revise duration**</span></span> | <span data-ttu-id="c25e4-119">**如果您修订工作量**</span><span class="sxs-lookup"><span data-stu-id="c25e4-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="c25e4-120">固定单位任务</span><span class="sxs-lookup"><span data-stu-id="c25e4-120">Fixed units task</span></span>     | <span data-ttu-id="c25e4-121">将重新计算持续时间。</span><span class="sxs-lookup"><span data-stu-id="c25e4-121">Duration is recalculated.</span></span> | <span data-ttu-id="c25e4-122">将重新计算工作量。</span><span class="sxs-lookup"><span data-stu-id="c25e4-122">Effort is recalculated.</span></span>    | <span data-ttu-id="c25e4-123">将重新计算持续时间。</span><span class="sxs-lookup"><span data-stu-id="c25e4-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="c25e4-124">固定工作量任务</span><span class="sxs-lookup"><span data-stu-id="c25e4-124">Fixed effort task</span></span>    | <span data-ttu-id="c25e4-125">将重新计算持续时间。</span><span class="sxs-lookup"><span data-stu-id="c25e4-125">Duration is recalculated.</span></span> | <span data-ttu-id="c25e4-126">将重新计算单位。</span><span class="sxs-lookup"><span data-stu-id="c25e4-126">Units are recalculated.</span></span>    | <span data-ttu-id="c25e4-127">将重新计算持续时间。</span><span class="sxs-lookup"><span data-stu-id="c25e4-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="c25e4-128">固定持续时间任务</span><span class="sxs-lookup"><span data-stu-id="c25e4-128">Fixed duration task</span></span>  | <span data-ttu-id="c25e4-129">将重新计算工作量。</span><span class="sxs-lookup"><span data-stu-id="c25e4-129">Effort is recalculated.</span></span>   | <span data-ttu-id="c25e4-130">将重新计算工作量。</span><span class="sxs-lookup"><span data-stu-id="c25e4-130">Effort is recalculated.</span></span>    | <span data-ttu-id="c25e4-131">将重新计算单位。</span><span class="sxs-lookup"><span data-stu-id="c25e4-131">Units are recalculated.</span></span>   |

<span data-ttu-id="c25e4-132">有关给定模式的影响的详细信息，请参阅[更改任务类型以进行更准确地计划](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)。</span><span class="sxs-lookup"><span data-stu-id="c25e4-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="c25e4-133">在该主题中，使用的是 **工作** 一词，而不是 **工作量**。</span><span class="sxs-lookup"><span data-stu-id="c25e4-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="c25e4-134">更改组织的计划模式</span><span class="sxs-lookup"><span data-stu-id="c25e4-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="c25e4-135">完成以下步骤来定义组织的计划模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="c25e4-136">转到 **设置**\>**常规**\>**参数**，然后选择项目参数。</span><span class="sxs-lookup"><span data-stu-id="c25e4-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="c25e4-137">在 **项目参数** 页上，为组织选择默认的计划模式，然后为项目经理定义在创建新项目时替代设置的能力。</span><span class="sxs-lookup"><span data-stu-id="c25e4-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="c25e4-138">更改项目上的计划模式设置</span><span class="sxs-lookup"><span data-stu-id="c25e4-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="c25e4-139">如果组织允许项目经理替代默认计划模式，项目经理可以在创建新项目时进行更改。</span><span class="sxs-lookup"><span data-stu-id="c25e4-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="c25e4-140">但是，保存项目后，将无法更改计划模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="c25e4-141">复制的项目</span><span class="sxs-lookup"><span data-stu-id="c25e4-141">Copied projects</span></span>

<span data-ttu-id="c25e4-142">由于在执行复制项目操作时创建了项目，因此项目经理无法设置计划模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="c25e4-143">目标项目将始终默认为在组织级别定义的模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="c25e4-144">复制的任务</span><span class="sxs-lookup"><span data-stu-id="c25e4-144">Copied tasks</span></span>

<span data-ttu-id="c25e4-145">将任务从一个项目复制到另一个项目时，该任务将继承目标项目的计划模式。</span><span class="sxs-lookup"><span data-stu-id="c25e4-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
