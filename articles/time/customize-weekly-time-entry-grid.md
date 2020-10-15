---
title: 扩展时间条目
description: 此主题提供有关开发人员如何扩展时间条目控件的信息。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930869"
---
# <a name="extending-time-entries"></a><span data-ttu-id="91612-103">扩展时间条目</span><span class="sxs-lookup"><span data-stu-id="91612-103">Extending time entries</span></span>

<span data-ttu-id="91612-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="91612-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91612-105">Dynamics 365 Project Operations 包含可扩展的时间条目自定义控件。</span><span class="sxs-lookup"><span data-stu-id="91612-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="91612-106">此控件包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="91612-106">This control includes the following features:</span></span>

- <span data-ttu-id="91612-107">在一周内横向输入时间</span><span class="sxs-lookup"><span data-stu-id="91612-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="91612-108">按日、行或周汇总</span><span class="sxs-lookup"><span data-stu-id="91612-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="91612-109">复制行或周</span><span class="sxs-lookup"><span data-stu-id="91612-109">Copy rows or weeks</span></span>
- <span data-ttu-id="91612-110">使用 HH:mm 或 HH.hh 的时间条目（自动转换为 HH.hh）</span><span class="sxs-lookup"><span data-stu-id="91612-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="91612-111">从工作、预订或约会导入</span><span class="sxs-lookup"><span data-stu-id="91612-111">Import from assignments, bookings or appointments</span></span>

<span data-ttu-id="91612-112">可以在两个方面扩展时间条目：</span><span class="sxs-lookup"><span data-stu-id="91612-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="91612-113">添加自定义时间条目供您自己使用</span><span class="sxs-lookup"><span data-stu-id="91612-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="91612-114">自定义每周时间条目控件</span><span class="sxs-lookup"><span data-stu-id="91612-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="91612-115">添加自定义时间条目供您自己使用。</span><span class="sxs-lookup"><span data-stu-id="91612-115">Add custom time entries for your own use.</span></span>

<span data-ttu-id="91612-116">时间条目是设计用于多个场景的核心实体。</span><span class="sxs-lookup"><span data-stu-id="91612-116">Time entries are a core entity that is designed to be used for multiple scenarios.</span></span> <span data-ttu-id="91612-117">在 2020 年 4 月第 1 波中，引入了 TESA 核心解决方案，其提供**设置**实体和新的**时间条目用户**安全角色。</span><span class="sxs-lookup"><span data-stu-id="91612-117">In April Wave 1 2020, the TESA core solution was introduced, which provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="91612-118">还提供了新字段 **msdyn_start** 和 **msdyn_end**，它们与 **msdyn_duration** 有直接关系。</span><span class="sxs-lookup"><span data-stu-id="91612-118">The new fields, **msdyn_start** and **msdyn_end** which have a direct relation to **msdyn_duration**, were also included.</span></span> <span data-ttu-id="91612-119">新实体、安全角色和字段使跨多个产品的时间分配方法更加统一。</span><span class="sxs-lookup"><span data-stu-id="91612-119">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="91612-120">时间源实体</span><span class="sxs-lookup"><span data-stu-id="91612-120">Time Source Entity</span></span>
| <span data-ttu-id="91612-121">字段</span><span class="sxs-lookup"><span data-stu-id="91612-121">Field</span></span> | <span data-ttu-id="91612-122">描述</span><span class="sxs-lookup"><span data-stu-id="91612-122">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="91612-123">客户</span><span class="sxs-lookup"><span data-stu-id="91612-123">Name</span></span>  | <span data-ttu-id="91612-124">时间条目创建期间用作选择值的时间源条目的名称。</span><span class="sxs-lookup"><span data-stu-id="91612-124">The name of the Time Source entry used as the selection value during time entry creation.</span></span> |
| <span data-ttu-id="91612-125">默认时间源 [时间源：isdefault]</span><span class="sxs-lookup"><span data-stu-id="91612-125">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="91612-126">默认情况下，默认时间源只能标记一个时间源。</span><span class="sxs-lookup"><span data-stu-id="91612-126">By default, only one Time Source may be marked at the default time source.</span></span> <span data-ttu-id="91612-127">此功能允许条目默认为时间源（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="91612-127">This capability allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="91612-128">时间源类型 [时间源：sourcetype]</span><span class="sxs-lookup"><span data-stu-id="91612-128">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="91612-129">源类型是一个选项（时间条目源类型），允许时间源与应用关联。</span><span class="sxs-lookup"><span data-stu-id="91612-129">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="91612-130">在添加其他应用程序时，其他值将添加到此选项集。</span><span class="sxs-lookup"><span data-stu-id="91612-130">Additional values will be added to this option set as additional applications are added.</span></span> <span data-ttu-id="91612-131">请注意，Microsoft 保留大于 190,000,000 的值。</span><span class="sxs-lookup"><span data-stu-id="91612-131">Note that Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="91612-132">时间条目和时间源实体</span><span class="sxs-lookup"><span data-stu-id="91612-132">Time entries and the Time Source Entity</span></span>
<span data-ttu-id="91612-133">每个时间条目都与一个时间源记录相关联。</span><span class="sxs-lookup"><span data-stu-id="91612-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="91612-134">此记录确定如何以及哪些应用程序应处理时间条目。</span><span class="sxs-lookup"><span data-stu-id="91612-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="91612-135">时间条目始终是一个连续的时段，连接了开始、结束和持续时间。</span><span class="sxs-lookup"><span data-stu-id="91612-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="91612-136">逻辑将在以下情况下自动更新时间条目记录：</span><span class="sxs-lookup"><span data-stu-id="91612-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="91612-137">如果提供了以下三个字段中的两个，将自动计算第三个</span><span class="sxs-lookup"><span data-stu-id="91612-137">If two of the three following fields are provided, the third is calculated automatically</span></span> 

    - <span data-ttu-id="91612-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="91612-138">**msdyn_start**</span></span>
    - <span data-ttu-id="91612-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="91612-139">**msdyn_end**</span></span>
    - <span data-ttu-id="91612-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="91612-140">**msdyn_duration**</span></span>

- <span data-ttu-id="91612-141">**msdyn_start** 和 **msdyn_end** 字段可识别时区。</span><span class="sxs-lookup"><span data-stu-id="91612-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="91612-142">创建的时间条目在仅指定 **msdyn_date** 和 **msdyn_duration** 时会在午夜开始，**msdyn_start** 和 **msdyn_end** 会相应更新。</span><span class="sxs-lookup"><span data-stu-id="91612-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight, and **msdyn_start** and **msdyn_end** will be updated accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="91612-143">时间条目类型</span><span class="sxs-lookup"><span data-stu-id="91612-143">Time entry types</span></span>

<span data-ttu-id="91612-144">时间条目记录具有关联的类型，其定义关联的应用程序的提交流中的行为。</span><span class="sxs-lookup"><span data-stu-id="91612-144">Time entry records have an associated type that defines behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="91612-145">标签</span><span class="sxs-lookup"><span data-stu-id="91612-145">Label</span></span> | <span data-ttu-id="91612-146">值</span><span class="sxs-lookup"><span data-stu-id="91612-146">Value</span></span>|
|-----|-----|
|<span data-ttu-id="91612-147">在休息时</span><span class="sxs-lookup"><span data-stu-id="91612-147">On break</span></span>   |<span data-ttu-id="91612-148">192,355,000</span><span class="sxs-lookup"><span data-stu-id="91612-148">192,355,000</span></span>|
|<span data-ttu-id="91612-149">旅行</span><span class="sxs-lookup"><span data-stu-id="91612-149">Travel</span></span> | <span data-ttu-id="91612-150">192,355,001</span><span class="sxs-lookup"><span data-stu-id="91612-150">192,355,001</span></span>|
|<span data-ttu-id="91612-151">加班</span><span class="sxs-lookup"><span data-stu-id="91612-151">Overtime</span></span>   | <span data-ttu-id="91612-152">192,354,320</span><span class="sxs-lookup"><span data-stu-id="91612-152">192,354,320</span></span>|
|<span data-ttu-id="91612-153">工作</span><span class="sxs-lookup"><span data-stu-id="91612-153">Work</span></span>   | <span data-ttu-id="91612-154">192,350,000</span><span class="sxs-lookup"><span data-stu-id="91612-154">192,350,000</span></span>|
|<span data-ttu-id="91612-155">休假</span><span class="sxs-lookup"><span data-stu-id="91612-155">Absence</span></span>    | <span data-ttu-id="91612-156">192,350,001</span><span class="sxs-lookup"><span data-stu-id="91612-156">192,350,001</span></span>|
|<span data-ttu-id="91612-157">休假</span><span class="sxs-lookup"><span data-stu-id="91612-157">Vacation</span></span>   | <span data-ttu-id="91612-158">192,350,002</span><span class="sxs-lookup"><span data-stu-id="91612-158">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="91612-159">自定义每周时间条目控件</span><span class="sxs-lookup"><span data-stu-id="91612-159">Customize the weekly Time Entry control</span></span>
<span data-ttu-id="91612-160">开发人员可以向其他实体添加其他字段和查找，并实施自定义业务规则以支持其业务场景。</span><span class="sxs-lookup"><span data-stu-id="91612-160">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="91612-161">向其他实体添加具有查找的自定义字段</span><span class="sxs-lookup"><span data-stu-id="91612-161">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="91612-162">向周时间条目网格添加自定义字段主要分三步。</span><span class="sxs-lookup"><span data-stu-id="91612-162">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

- <span data-ttu-id="91612-163">将自定义字段添加到快速创建对话框。</span><span class="sxs-lookup"><span data-stu-id="91612-163">Add the custom field to the quick create dialog box.</span></span>
- <span data-ttu-id="91612-164">配置网格以显示该自定义字段。</span><span class="sxs-lookup"><span data-stu-id="91612-164">Configure the grid to show the custom field.</span></span>
- <span data-ttu-id="91612-165">将该自定义字段添加到行编辑任务流或单元格编辑任务流。</span><span class="sxs-lookup"><span data-stu-id="91612-165">Add the custom field to either the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="91612-166">还必须确保新字段在行或单元格编辑任务流中进行必需的验证。</span><span class="sxs-lookup"><span data-stu-id="91612-166">You must also make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="91612-167">此步骤中，必须基于时间条目状态锁定字段。</span><span class="sxs-lookup"><span data-stu-id="91612-167">As part of this step, you must lock the field based on the time entry status.</span></span>

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="91612-168">将自定义字段添加到快速创建对话框</span><span class="sxs-lookup"><span data-stu-id="91612-168">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="91612-169">必须将自定义字段添加到**创建时间条目快速创建**对话框。</span><span class="sxs-lookup"><span data-stu-id="91612-169">You must add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="91612-170">然后，用户在通过选择**新建**添加时间条目时可以输入值。</span><span class="sxs-lookup"><span data-stu-id="91612-170">Users can then enter a value when they add time entries by selecting **New**.</span></span>

#### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="91612-171">配置网格以显示该自定义字段</span><span class="sxs-lookup"><span data-stu-id="91612-171">Configure the grid to show the custom field</span></span>
<span data-ttu-id="91612-172">可通过两种方法向周时间条目网格添加自定义字段：</span><span class="sxs-lookup"><span data-stu-id="91612-172">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="91612-173">自定义视图和添加自定义字段</span><span class="sxs-lookup"><span data-stu-id="91612-173">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="91612-174">创建新的默认自定义时间条目</span><span class="sxs-lookup"><span data-stu-id="91612-174">Create a new default custom time entry</span></span> 


<span data-ttu-id="91612-175">**自定义视图和添加自定义字段**</span><span class="sxs-lookup"><span data-stu-id="91612-175">**Customize a view and add a custom field**</span></span>

<span data-ttu-id="91612-176">您可以自定义**我的周时间条目**视图并向其添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="91612-176">You can customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="91612-177">可选择自定义字段在网格中的位置和大小，方法是在视图中编辑这些属性。</span><span class="sxs-lookup"><span data-stu-id="91612-177">You can choose the position and size of the custom field in the grid by editing those properties in the view.</span></span>

<span data-ttu-id="91612-178">**创建新的默认自定义时间条目**</span><span class="sxs-lookup"><span data-stu-id="91612-178">**Create a new default custom time entry**</span></span> 

<span data-ttu-id="91612-179">除了网格中需要的列，此视图中还应包含**描述**和**外部注释**字段。</span><span class="sxs-lookup"><span data-stu-id="91612-179">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="91612-180">选择网格的位置、大小和默认排序顺序，方法是在视图中编辑这些属性。</span><span class="sxs-lookup"><span data-stu-id="91612-180">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="91612-181">配置此视图的自定义控件，使其成为**时间条目网格**控件。</span><span class="sxs-lookup"><span data-stu-id="91612-181">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="91612-182">将此控件添加到视图，然后选择将其用于 Web、手机和平板电脑。</span><span class="sxs-lookup"><span data-stu-id="91612-182">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="91612-183">配置周时间条目网格的参数。</span><span class="sxs-lookup"><span data-stu-id="91612-183">Configure the parameters for the weekly time entry grid.</span></span> <span data-ttu-id="91612-184">将**开始日期**字段设置为 **msdyn_date**，将**持续时间**字段设置为 **msdyn_duration**，将**状态**字段设置为 **msdyn_entrystatus**。</span><span class="sxs-lookup"><span data-stu-id="91612-184">Set the **Start Date** field to **msdyn_date**, set the **Duration** field to **msdyn_duration**, and set the **Status** field to **msdyn_entrystatus**.</span></span> 
5. <span data-ttu-id="91612-185">对于默认视图，**只读状态列表**字段设置为 **192350002,192350003,192350004**，**行编辑任务流**字段设置为 **msdyn_timeentryrowedit**，**单元格编辑任务流**字段设置为 **msdyn_timeentryedit**。</span><span class="sxs-lookup"><span data-stu-id="91612-185">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**, the **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**, and the **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
6. <span data-ttu-id="91612-186">可自定义这些字段以添加或删除只读状态，或使用其他基于任务的体验 (TBX) 编辑行或单元格。</span><span class="sxs-lookup"><span data-stu-id="91612-186">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="91612-187">应将这些字段绑定到静态值。</span><span class="sxs-lookup"><span data-stu-id="91612-187">These fields should be bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="91612-188">两种选项都会移除对**项目**和**项目任务**实体的一些自带筛选，因此将显示这些实体的所有查找视图。</span><span class="sxs-lookup"><span data-stu-id="91612-188">Both options will remove some out-of-box filtering on **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="91612-189">只有相关查找视图才会默认显示。</span><span class="sxs-lookup"><span data-stu-id="91612-189">Out-of-the-box, only the relevant lookup views are visible.</span></span>
<span data-ttu-id="91612-190">必须确定自定义字段的相应任务流。</span><span class="sxs-lookup"><span data-stu-id="91612-190">You must determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="91612-191">最可能的是，如果将字段添加到了网格，则应进入对适用于整行时间条目的字段使用的行编辑任务流。</span><span class="sxs-lookup"><span data-stu-id="91612-191">Most likely, if you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="91612-192">如果自定义字段每天有唯一值（如**结束时间**的自定义字段），则应进入单元格编辑任务流。</span><span class="sxs-lookup"><span data-stu-id="91612-192">If the custom field has a unique value every day, such as a custom field for **End time**, it should go in the cell edit task flow.</span></span>

<span data-ttu-id="91612-193">若要将自定义字段添加到任务流，请将一个**字段**元素拖到页中的相应位置，然后设置字段属性。</span><span class="sxs-lookup"><span data-stu-id="91612-193">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="91612-194">将**来源**属性设置为**时间条目**，将**数据字段**属性设置为自定义字段。</span><span class="sxs-lookup"><span data-stu-id="91612-194">Set the **Source** property to **Time Entry**, and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="91612-195">**字段**属性指定在 TBX 页上的显示名称。</span><span class="sxs-lookup"><span data-stu-id="91612-195">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="91612-196">选择**应用**将更改保存到字段，然后选择**更新**将更改保存到页面。</span><span class="sxs-lookup"><span data-stu-id="91612-196">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="91612-197">若要改用新的自定义 TBX 页，请创建一个新流程。</span><span class="sxs-lookup"><span data-stu-id="91612-197">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="91612-198">将类别设置为**业务流程**，将实体设置为**时间条目**，将业务流程类型设置为**将流程作为任务流运行**。</span><span class="sxs-lookup"><span data-stu-id="91612-198">Set the category to **Business Process Flow**, set the entity to **Time Entry**, and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="91612-199">应将**属性**下的**页面名称**属性设置为页面的显示名称。</span><span class="sxs-lookup"><span data-stu-id="91612-199">Under **Properties**, the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="91612-200">将所有相关字段添加到 TBX 页。</span><span class="sxs-lookup"><span data-stu-id="91612-200">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="91612-201">保存并激活流程，然后将相关任务流的自定义控件属性更新为流程中的**名称**的值。</span><span class="sxs-lookup"><span data-stu-id="91612-201">Save and activate the process, and then update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="91612-202">添加新选项集值</span><span class="sxs-lookup"><span data-stu-id="91612-202">Add new option set values</span></span>
<span data-ttu-id="91612-203">若要向自带字段添加选项集值，请打开该字段的编辑页，然后在**类型**下选择该选项集旁边的**编辑**。</span><span class="sxs-lookup"><span data-stu-id="91612-203">To add option set values to an out-of-box field, open the editing page for the field, and then, under **Type**, select **Edit** next to the option set.</span></span> <span data-ttu-id="91612-204">接下来，添加一个采用自定义标签和颜色的选项。</span><span class="sxs-lookup"><span data-stu-id="91612-204">Next, add a new option that has a custom label and color.</span></span> <span data-ttu-id="91612-205">如果要添加新的时间条目状态，则自带字段将命名为**条目状态**，而不是**状态**。</span><span class="sxs-lookup"><span data-stu-id="91612-205">If you want to add a new time entry status, the out-of-box field is named **Entry Status**, not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="91612-206">将新时间条目状态指定为只读</span><span class="sxs-lookup"><span data-stu-id="91612-206">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="91612-207">若要将新时间条目状态指定为只读，请将新时间条目值添加到**只读状态列表**属性中。</span><span class="sxs-lookup"><span data-stu-id="91612-207">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="91612-208">将对具有新状态的行锁定时间条目的可编辑部分。</span><span class="sxs-lookup"><span data-stu-id="91612-208">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="91612-209">接下来，添加业务规则以锁定**时间条目行编辑**和**时间条目编辑** TBX 页中的所有字段。</span><span class="sxs-lookup"><span data-stu-id="91612-209">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="91612-210">可以访问这些页的业务规则，方法是打开页的业务流程编辑器，然后选择**业务规则**。</span><span class="sxs-lookup"><span data-stu-id="91612-210">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="91612-211">可向现有规则中的条件添加新状态，也可以为新状态添加新业务规则。</span><span class="sxs-lookup"><span data-stu-id="91612-211">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="91612-212">添加自定义验证规则</span><span class="sxs-lookup"><span data-stu-id="91612-212">Add custom validation rules</span></span>
<span data-ttu-id="91612-213">您可以为每周时间条目网格体验添加两种类型的验证规则：</span><span class="sxs-lookup"><span data-stu-id="91612-213">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="91612-214">在快速创建对话框和 TBX 页面上起作用的客户端业务规则。</span><span class="sxs-lookup"><span data-stu-id="91612-214">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="91612-215">应用于所有时间条目更新的服务器端插件验证。</span><span class="sxs-lookup"><span data-stu-id="91612-215">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="91612-216">业务规则</span><span class="sxs-lookup"><span data-stu-id="91612-216">Business rules</span></span>
<span data-ttu-id="91612-217">可使用业务规则锁定和解锁字段，在字段中输入默认值，以及定义仅需要来自当前时间条目记录的信息的验证。</span><span class="sxs-lookup"><span data-stu-id="91612-217">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="91612-218">可以访问 TBX 页的业务规则，方法是打开页的业务流程编辑器，然后选择**业务规则**。</span><span class="sxs-lookup"><span data-stu-id="91612-218">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="91612-219">然后可以编辑现有业务规则或添加新的业务规则。</span><span class="sxs-lookup"><span data-stu-id="91612-219">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="91612-220">对于自定义程度甚至更高的验证，可以使用业务规则运行 JavaScript。</span><span class="sxs-lookup"><span data-stu-id="91612-220">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="91612-221">插件验证</span><span class="sxs-lookup"><span data-stu-id="91612-221">Plug-in validations</span></span>
<span data-ttu-id="91612-222">应该将插件验证用于需要的上下文比单个时间条目记录中的可用上下文多的任何验证，或用于要对网格中的内联更新运行的任何验证。</span><span class="sxs-lookup"><span data-stu-id="91612-222">You should use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="91612-223">若要完成验证，请在**时间条目**实体中创建一个自定义插件。</span><span class="sxs-lookup"><span data-stu-id="91612-223">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>
