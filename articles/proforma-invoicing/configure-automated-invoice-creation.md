---
title: 配置发票自动创建
description: 此主题提供有关如何将系统配置为自动生成发票的信息。
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005330"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="5c1fe-103">配置发票自动创建</span><span class="sxs-lookup"><span data-stu-id="5c1fe-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="5c1fe-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5c1fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5c1fe-105">完成以下步骤以在 Dynamics 365 Project operations 中配置发票自动运行。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="5c1fe-106">转到 **设置** > **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="5c1fe-107">创建一个批处理作业，将其命名为 **Project operations 创建发票**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="5c1fe-108">此批处理作业的名称中必须包含词语“创建发票”。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="5c1fe-109">在 **作业类型** 字段中，选择 **无**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="5c1fe-110">默认情况下，**每天频率** 和 **可用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="5c1fe-111">选择 **运行工作流**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-111">Select **Run Workflow**.</span></span> <span data-ttu-id="5c1fe-112">在 **查找记录** 对话框中，您将看到三个工作流：</span><span class="sxs-lookup"><span data-stu-id="5c1fe-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="5c1fe-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="5c1fe-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="5c1fe-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="5c1fe-114">ProcessRunner</span></span>
    - <span data-ttu-id="5c1fe-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="5c1fe-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="5c1fe-116">选择 **ProcessRunCaller**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="5c1fe-117">在下一个对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="5c1fe-118">**Sleep** 工作流后是 **Process** 工作流。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5c1fe-119">可以选择步骤 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="5c1fe-120">然后，当您选择 **确定** 时，**Process** 工作流后是 **Sleep** 工作流。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="5c1fe-121">**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="5c1fe-122">**ProcessRunCaller** 调用 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="5c1fe-123">**ProcessRunner** 是真正创建发票的工作流。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="5c1fe-124">它浏览必须为其创建发票的所有合同子项，然后为这些子项创建发票。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="5c1fe-125">为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="5c1fe-126">如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="5c1fe-127">如果没有需要为其创建发票的交易，作业将跳过发票创建。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="5c1fe-128">**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="5c1fe-129">然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="5c1fe-130">此计时器结束时，将关闭 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="5c1fe-131">用于创建发票的批处理作业是周期性作业。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="5c1fe-132">如果多次运行此批处理流程，将创建多个作业实例，并导致出错。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="5c1fe-133">因此，仅应启动此批处理流程一次，并且仅当其停止运行时才应重新启动它。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="5c1fe-134">仅为按发票计划配置的项目合同子项运行批处理开票。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="5c1fe-135">必须为采用固定价格记帐方法的合同子项配置里程碑。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="5c1fe-136">将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="5c1fe-137">这同样适用于基于项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="5c1fe-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]