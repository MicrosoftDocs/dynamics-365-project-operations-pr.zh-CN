---
title: 时间条目 UI 行为
description: 此主题提供有关时间条目 UI 的行为的信息。
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961687"
---
# <a name="time-entry-ui-behavior"></a><span data-ttu-id="51ce9-103">时间条目 UI 行为</span><span class="sxs-lookup"><span data-stu-id="51ce9-103">Time entry UI behavior</span></span>

<span data-ttu-id="51ce9-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="51ce9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="51ce9-105">**周时间条目**网格是一个自定义控件，有两个主部分，即**维度**和**持续时间**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-105">The **Weekly time entry** grid is a custom control that has two main sections, **Dimensions** and **Duration**.</span></span>

## <a name="dimensions"></a><span data-ttu-id="51ce9-106">维度</span><span class="sxs-lookup"><span data-stu-id="51ce9-106">Dimensions</span></span>
<span data-ttu-id="51ce9-107">**维度**部分显示可用来输入时间的维度。</span><span class="sxs-lookup"><span data-stu-id="51ce9-107">The **Dimensions** section shows the dimensions that time can be entered against.</span></span> <span data-ttu-id="51ce9-108">下图为支持的自带维度：</span><span class="sxs-lookup"><span data-stu-id="51ce9-108">The following dimensions are supported out-of-the-box:</span></span>

  - <span data-ttu-id="51ce9-109">Project</span><span class="sxs-lookup"><span data-stu-id="51ce9-109">Project</span></span>
  - <span data-ttu-id="51ce9-110">项目任务</span><span class="sxs-lookup"><span data-stu-id="51ce9-110">Project Task</span></span>
  - <span data-ttu-id="51ce9-111">角色</span><span class="sxs-lookup"><span data-stu-id="51ce9-111">Role</span></span>
  - <span data-ttu-id="51ce9-112">Type</span><span class="sxs-lookup"><span data-stu-id="51ce9-112">Type</span></span>
  - <span data-ttu-id="51ce9-113">条目状态</span><span class="sxs-lookup"><span data-stu-id="51ce9-113">Entry Status</span></span>

<span data-ttu-id="51ce9-114">**维度**部分不允许直接编辑。</span><span class="sxs-lookup"><span data-stu-id="51ce9-114">The **Dimensions** section doesn't allow inline editing.</span></span> <span data-ttu-id="51ce9-115">此部分受一个视图支持，该视图支持向周时间条目网格添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="51ce9-115">This section is backed by a view that enables custom fields to be added to the weekly time entry grid.</span></span>

## <a name="duration"></a><span data-ttu-id="51ce9-116">持续时间</span><span class="sxs-lookup"><span data-stu-id="51ce9-116">Duration</span></span>
<span data-ttu-id="51ce9-117">“持续时间”部分将星期几显示为列标题。</span><span class="sxs-lookup"><span data-stu-id="51ce9-117">The Duration section shows the days of the week as column headers.</span></span> <span data-ttu-id="51ce9-118">此部分允许直接编辑。</span><span class="sxs-lookup"><span data-stu-id="51ce9-118">This section allows inline editing.</span></span> <span data-ttu-id="51ce9-119">创建了具有相应维度的时间条目行之后，用户可快速输入用在这些维度上的时间量。</span><span class="sxs-lookup"><span data-stu-id="51ce9-119">After a time entry row is created with the appropriate dimensions, users can quickly enter the amount of time that they spent on those dimensions.</span></span>

## <a name="create-a-new-time-entry"></a><span data-ttu-id="51ce9-120">创建新时间条目</span><span class="sxs-lookup"><span data-stu-id="51ce9-120">Create a new time entry</span></span>

1. <span data-ttu-id="51ce9-121">在时间条目网格中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-121">In the time entry grid, select **New**.</span></span> 
2. <span data-ttu-id="51ce9-122">在**时间条目快速创建**对话框中，选择时间条目日期。</span><span class="sxs-lookup"><span data-stu-id="51ce9-122">In the **Time Entry Quick Create** dialog box, select the time entry date.</span></span>
3. <span data-ttu-id="51ce9-123">为**项目**、**项目任务**、**角色**和**持续时间**维度输入数据。</span><span class="sxs-lookup"><span data-stu-id="51ce9-123">Enter data for the **Project**, **Project Task**, **Role**, and **Duration** dimensions.</span></span> <span data-ttu-id="51ce9-124">此信息应以分钟、小时或天添加，方法是键入 **h**、**m** 或 **d** 加数字。</span><span class="sxs-lookup"><span data-stu-id="51ce9-124">This information should be added in minutes, hours, or days by typing **h**, **m**, or **d**, together with the number.</span></span> 
4. <span data-ttu-id="51ce9-125">为条目输入说明，以及可以在外部共享的有关时间条目的任何注释。</span><span class="sxs-lookup"><span data-stu-id="51ce9-125">Enter a description for the entry and any comments that can be shared externally regarding time entry.</span></span> 

<span data-ttu-id="51ce9-126">当您保存条目时，输入的值将显示在**维度**部分。</span><span class="sxs-lookup"><span data-stu-id="51ce9-126">When you save the entry, the entered values appear in the **Dimensions** section.</span></span> <span data-ttu-id="51ce9-127">在**持续时间**字段中输入的信息在为其创建时间条目的日期上显示。</span><span class="sxs-lookup"><span data-stu-id="51ce9-127">The information entered in the **Duration** field appears on the date that the time entry was created for.</span></span>

<span data-ttu-id="51ce9-128">查找字段受系统视图支持。</span><span class="sxs-lookup"><span data-stu-id="51ce9-128">Lookup fields are backed by system views.</span></span> <span data-ttu-id="51ce9-129">例如，用户进入项目后，**项目任务**字段默认设置为**复制**视图。</span><span class="sxs-lookup"><span data-stu-id="51ce9-129">For example, after a user enters a project, the **Project Task** field is set to the **Copy** view by default.</span></span> <span data-ttu-id="51ce9-130">若要为尚未分派给用户的任务创建时间条目，请在查找对话框中选择**更改视图**，然后选择**所有可用的项目任务**视图。</span><span class="sxs-lookup"><span data-stu-id="51ce9-130">To create time entries for tasks that aren't assigned to a user, select **Change View** in the lookup dialog box, and then select the **All Active Project Tasks** view.</span></span>

## <a name="edit-a-time-entry"></a><span data-ttu-id="51ce9-131">编辑时间条目</span><span class="sxs-lookup"><span data-stu-id="51ce9-131">Edit a time entry</span></span> 
<span data-ttu-id="51ce9-132">周时间条目网格中不显示时间条目页中某些字段（如**描述**和**外部注释**）内的详细信息。</span><span class="sxs-lookup"><span data-stu-id="51ce9-132">Details from some fields on the time entry page, such as **Description** and **External Comments**, aren't shown in the weekly time entry grid.</span></span> <span data-ttu-id="51ce9-133">而是在具有这些额外详细信息的**持续时间**单元格中显示一个小三角指示器。</span><span class="sxs-lookup"><span data-stu-id="51ce9-133">Instead, a small triangular indicator appears in the **Duration** cells that have these additional details.</span></span> 

1. <span data-ttu-id="51ce9-134">若要编辑时间条目，在时间条目中选择要更新的单元格。</span><span class="sxs-lookup"><span data-stu-id="51ce9-134">To edit a time entry, select the cell you want to update in the time entry.</span></span>
2. <span data-ttu-id="51ce9-135">选择**编辑详细信息**更新**时间条目主窗体**窗格中的数据。</span><span class="sxs-lookup"><span data-stu-id="51ce9-135">Select **Edit Details** to update the data in the **Time Entry Mainform** pane.</span></span> 

## <a name="copy-a-time-entry-row"></a><span data-ttu-id="51ce9-136">复制时间条目行</span><span class="sxs-lookup"><span data-stu-id="51ce9-136">Copy a time entry row</span></span>
<span data-ttu-id="51ce9-137">创建行后，您可选择**复制行**将整行复制到新行。</span><span class="sxs-lookup"><span data-stu-id="51ce9-137">After the row has been created, you can select **Copy Row** to copy the whole row to a new row.</span></span> <span data-ttu-id="51ce9-138">如果按照这种方法复制行，也将复制维度和持续时间。</span><span class="sxs-lookup"><span data-stu-id="51ce9-138">When a row is copied in this way, dimensions and durations are also copied.</span></span> <span data-ttu-id="51ce9-139">您还可以选择**编辑行**以在**持续时间**部分中更新维度值和持续时间。</span><span class="sxs-lookup"><span data-stu-id="51ce9-139">You can also select **Edit Row** to update dimension values and durations in the **Duration** section.</span></span>

## <a name="open-a-time-entry-behavior"></a><span data-ttu-id="51ce9-140">打开时间条目行为</span><span class="sxs-lookup"><span data-stu-id="51ce9-140">Open a time entry behavior</span></span>
<span data-ttu-id="51ce9-141">为了支持最醒目字段中的最佳快速条目，周时间条目网格显示一小组选定维度和持续时间。</span><span class="sxs-lookup"><span data-stu-id="51ce9-141">To support optimal and quick entry in the most prominent fields, the weekly time entry grid shows a subset of selected dimensions and time durations.</span></span> <span data-ttu-id="51ce9-142">若要查看一个时间条目的所有详细信息，请在**编辑条目**下选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-142">To view all the details of a single time entry, under **Edit Entry**, select **Open**.</span></span>

## <a name="submit-a-time-entry"></a><span data-ttu-id="51ce9-143">提交时间条目</span><span class="sxs-lookup"><span data-stu-id="51ce9-143">Submit a time entry</span></span>
<span data-ttu-id="51ce9-144">您可以提交一个或一组时间条目，方法是选择单元格区域或整个时间条目行，然后选择**提交**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-144">You can submit a single time entry or a group of time entries by selecting a block of cells or a whole time entry row, and then selecting **Submit**.</span></span> <span data-ttu-id="51ce9-145">提交的时间条目在审批者的**审批**页中显示为待审批条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-145">Submitted time entries appear as entries that are pending approval on the approvers' **Approval** page.</span></span> <span data-ttu-id="51ce9-146">时间条目在成功提交后不可编辑。</span><span class="sxs-lookup"><span data-stu-id="51ce9-146">After time entries are successfully submitted, they can't be edited.</span></span>

## <a name="recall-a-time-entry"></a><span data-ttu-id="51ce9-147">撤消时间条目</span><span class="sxs-lookup"><span data-stu-id="51ce9-147">Recall a time entry</span></span>
<span data-ttu-id="51ce9-148">可撤销已提交的时间条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-148">You can recall time entries that you've submitted.</span></span> <span data-ttu-id="51ce9-149">可撤销一个、一部分或整行时间条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-149">You can recall a single time entry, a block of time entries, or a whole row of time entries.</span></span> <span data-ttu-id="51ce9-150">撤销的时间条目可以编辑。</span><span class="sxs-lookup"><span data-stu-id="51ce9-150">Recalled time entries can be edited.</span></span>

## <a name="time-entry-status"></a><span data-ttu-id="51ce9-151">时间条目状态</span><span class="sxs-lookup"><span data-stu-id="51ce9-151">Time entry status</span></span>

- <span data-ttu-id="51ce9-152">**草稿**：将为新时间条目自动分派**草稿**状态。</span><span class="sxs-lookup"><span data-stu-id="51ce9-152">**Draft**: New time entries are automatically assigned a status of **Draft**.</span></span> <span data-ttu-id="51ce9-153">只能删除状态为**草稿**的时间条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-153">Only time entries that have a status of **Draft** can be deleted.</span></span>
- <span data-ttu-id="51ce9-154">**已提交**：提交时间条目时，其状态更新为**已提交**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-154">**Submitted**: When a time entry is submitted, the status is updated to **Submitted**.</span></span> 
- <span data-ttu-id="51ce9-155">**已批准**：批准已提交的时间条目时，其状态更新为**已批准**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-155">**Approved**: When a submitted time entry is approved, the status is updated to **Approved**.</span></span> 
- <span data-ttu-id="51ce9-156">**已返回**：如果拒绝了时间条目，其状态将更新为**已返回**，并且可更正和重新提交该条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-156">**Returned**: If a time entry is rejected, the status is updated to **Returned**, and the entry becomes available for correction and resubmission.</span></span> 

## <a name="view-rejection-comments"></a><span data-ttu-id="51ce9-157">查看拒绝注释</span><span class="sxs-lookup"><span data-stu-id="51ce9-157">View rejection comments</span></span>
<span data-ttu-id="51ce9-158">审批者在拒绝时间条目时，可能会添加注释来帮助资源了解拒绝原因。</span><span class="sxs-lookup"><span data-stu-id="51ce9-158">When a time entry is rejected by an approver, the approver might add comments to help the resource understand the reason for the rejection.</span></span> <span data-ttu-id="51ce9-159">若要查看时间条目的拒绝注释，请选择**打开条目**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-159">To view the rejection comments for a time entry, select **Open entry**.</span></span> <span data-ttu-id="51ce9-160">将在时间线中显示拒绝注释。</span><span class="sxs-lookup"><span data-stu-id="51ce9-160">The rejection comments will be shown in the timeline.</span></span> <span data-ttu-id="51ce9-161">用户可以在重新提交条目之前响应拒绝注释。</span><span class="sxs-lookup"><span data-stu-id="51ce9-161">The user can respond to the rejection comments before they resubmit the entry.</span></span>

## <a name="copy-week"></a><span data-ttu-id="51ce9-162">复制周</span><span class="sxs-lookup"><span data-stu-id="51ce9-162">Copy week</span></span>
<span data-ttu-id="51ce9-163">在创建了几个时间条目后，用户可以同时创建多个时间条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-163">After a few time entries have been created, users can create multiple time entries at the same time.</span></span>

1. <span data-ttu-id="51ce9-164">在**时间条目**窗体中，选择**复制周**来批量创建更多时间条目。</span><span class="sxs-lookup"><span data-stu-id="51ce9-164">In the **Time Entries** form, select **Copy Week** to bulk-create additional time entries.</span></span> 
2. <span data-ttu-id="51ce9-165">在**复制**对话框中，在**开始期间**部分，使用**开始日期**和**结束日期**字段定义要复制的时间条目所属日期范围。</span><span class="sxs-lookup"><span data-stu-id="51ce9-165">In the **Copy** dialog box, in the **From period** section, use the **Start Date** and **End Date** fields to define the date range to copy time entries from.</span></span> 
3. <span data-ttu-id="51ce9-166">在**目标期间**部分中**开始日期**字段内，指定要为其创建时间条目的日期。</span><span class="sxs-lookup"><span data-stu-id="51ce9-166">In the **To Period** section, in the **Start Date** field, specify the date to create time entries for.</span></span> 
4. <span data-ttu-id="51ce9-167">选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="51ce9-167">Select **Copy**.</span></span> <span data-ttu-id="51ce9-168">对于**目标期间**内的指定日期，将为**开始期间**中相应星期几的时间条目创建一个副本。</span><span class="sxs-lookup"><span data-stu-id="51ce9-168">For the specified date in the **To period**, a copy of the time entries for the corresponding day of the week in the **From period** is created.</span></span> <span data-ttu-id="51ce9-169">例如，将把上周星期一的时间条目复制到指定为**目标期间**的周的星期一。</span><span class="sxs-lookup"><span data-stu-id="51ce9-169">For example, Monday's time entry from last week is copied into Monday of the week that is specified as the **To period**.</span></span>

## <a name="import"></a><span data-ttu-id="51ce9-170">导入</span><span class="sxs-lookup"><span data-stu-id="51ce9-170">Import</span></span>
<span data-ttu-id="51ce9-171">同样的基本流程用于从预订、分派和交换导入。</span><span class="sxs-lookup"><span data-stu-id="51ce9-171">The same basic process is used to import from bookings, assignments, and exchanges.</span></span> <span data-ttu-id="51ce9-172">您可以指定要从中导入预订的日期范围，然后明确选择应该复制到草稿时间条目的预订。</span><span class="sxs-lookup"><span data-stu-id="51ce9-172">You can specify the date range that bookings are imported from and then explicitly select the bookings that should be copied into draft time entries.</span></span> 
