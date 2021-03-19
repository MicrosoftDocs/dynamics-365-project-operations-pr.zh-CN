---
title: 资源管理更改 (Project Service Automation 3.x)
description: 此主题介绍对资源管理区域的更改。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284752"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="036fa-103">资源管理更改 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="036fa-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="036fa-104">此主题介绍已经对 Dynamics 365 Project Service Automation 版本 3.x 的“资源管理”区域进行的更改。</span><span class="sxs-lookup"><span data-stu-id="036fa-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="036fa-105">项目估算</span><span class="sxs-lookup"><span data-stu-id="036fa-105">Project estimates</span></span>

<span data-ttu-id="036fa-106">项目估算基于 **msdyn\_resourceassignment** 实体（**资源分派**），而不是基于 **msdyn\_projecttask** 实体（**项目任务**）。</span><span class="sxs-lookup"><span data-stu-id="036fa-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="036fa-107">资源分派已成为任务计划和定价的“事实来源”。</span><span class="sxs-lookup"><span data-stu-id="036fa-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="036fa-108">明细任务</span><span class="sxs-lookup"><span data-stu-id="036fa-108">Line tasks</span></span>

<span data-ttu-id="036fa-109">在 PSA 3.x 中，明细任务已过时（已弃用）。</span><span class="sxs-lookup"><span data-stu-id="036fa-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="036fa-110">分派现在指向整个任务，而不是明细任务。</span><span class="sxs-lookup"><span data-stu-id="036fa-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="036fa-111">以下示例显示在 PSA 早期版本中和 PSA 3.x 中如何为团队成员 A 和 B 分派名称为“测试任务”的任务。</span><span class="sxs-lookup"><span data-stu-id="036fa-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="036fa-112">**PSA 3.x 之前版本：**</span><span class="sxs-lookup"><span data-stu-id="036fa-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="036fa-113">测试任务</span><span class="sxs-lookup"><span data-stu-id="036fa-113">Test task</span></span>

        - <span data-ttu-id="036fa-114">测试任务 – 明细任务 1</span><span class="sxs-lookup"><span data-stu-id="036fa-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="036fa-115">A 的分派</span><span class="sxs-lookup"><span data-stu-id="036fa-115">Assignment to A</span></span>

        - <span data-ttu-id="036fa-116">测试任务 – 明细任务 2</span><span class="sxs-lookup"><span data-stu-id="036fa-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="036fa-117">B 的分派</span><span class="sxs-lookup"><span data-stu-id="036fa-117">Assignment to B</span></span>

- <span data-ttu-id="036fa-118">**PSA 3.x：**</span><span class="sxs-lookup"><span data-stu-id="036fa-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="036fa-119">测试任务</span><span class="sxs-lookup"><span data-stu-id="036fa-119">Test task</span></span>

        - <span data-ttu-id="036fa-120">A 的分派</span><span class="sxs-lookup"><span data-stu-id="036fa-120">Assignment to A</span></span>
        - <span data-ttu-id="036fa-121">B 的分派</span><span class="sxs-lookup"><span data-stu-id="036fa-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="036fa-122">未分派的分派</span><span class="sxs-lookup"><span data-stu-id="036fa-122">Unassigned assignment</span></span>

<span data-ttu-id="036fa-123">在 PSA 3.x 中，未分派的分派是分派给 **空** 团队成员和 **空** 资源的分派。</span><span class="sxs-lookup"><span data-stu-id="036fa-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="036fa-124">下面的两种方案中可能出现未分派的分派：</span><span class="sxs-lookup"><span data-stu-id="036fa-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="036fa-125">如果已创建任务，但是尚未将其分派给任何团队成员，则始终创建未分派的分派。</span><span class="sxs-lookup"><span data-stu-id="036fa-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="036fa-126">如果删除了任务的所有被分派人，则为该任务重新创建未分派的分派。</span><span class="sxs-lookup"><span data-stu-id="036fa-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="036fa-127">项目任务实体中的计划字段</span><span class="sxs-lookup"><span data-stu-id="036fa-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="036fa-128">**msdyn\_projecttask** 实体中的字段已弃用或移到 **msdyn\_resourceassignment** 实体，或者现在从 **msdyn\_projectteam** 实体（**项目团队成员**）引用。</span><span class="sxs-lookup"><span data-stu-id="036fa-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="036fa-129">msdyn\_projecttask（项目任务）中已弃用的字段</span><span class="sxs-lookup"><span data-stu-id="036fa-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="036fa-130">msdyn\_resourceassignment（资源分派）中的新字段</span><span class="sxs-lookup"><span data-stu-id="036fa-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="036fa-131">注释</span><span class="sxs-lookup"><span data-stu-id="036fa-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="036fa-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="036fa-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="036fa-133">无</span><span class="sxs-lookup"><span data-stu-id="036fa-133">None</span></span> | |
| <span data-ttu-id="036fa-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="036fa-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="036fa-135">无</span><span class="sxs-lookup"><span data-stu-id="036fa-135">None</span></span> | |
| <span data-ttu-id="036fa-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="036fa-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="036fa-137">无</span><span class="sxs-lookup"><span data-stu-id="036fa-137">None</span></span> | |
| <span data-ttu-id="036fa-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="036fa-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="036fa-139">无</span><span class="sxs-lookup"><span data-stu-id="036fa-139">None</span></span> | |
| <span data-ttu-id="036fa-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="036fa-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="036fa-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="036fa-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="036fa-142">已更改了字段中存储的 JavaScript 对象表示法 (JSON) 数据结构格式。</span><span class="sxs-lookup"><span data-stu-id="036fa-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="036fa-143">计划分布</span><span class="sxs-lookup"><span data-stu-id="036fa-143">Schedule contour</span></span>

<span data-ttu-id="036fa-144">计划分布存储在每个 **资源分派** 实体 (**msdyn\_resourceassignment**) 的 **计划的工作** 字段 (**msdyn\_plannedwork**) 中。</span><span class="sxs-lookup"><span data-stu-id="036fa-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="036fa-145">结构</span><span class="sxs-lookup"><span data-stu-id="036fa-145">Structure</span></span>

<span data-ttu-id="036fa-146">新的计划分布结构由为计划的每一天定义的灵活时间片段构成。</span><span class="sxs-lookup"><span data-stu-id="036fa-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="036fa-147">每个时间片段具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="036fa-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="036fa-148">**开始** – 根据项目日历，工作日的开始工作时间。</span><span class="sxs-lookup"><span data-stu-id="036fa-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="036fa-149">**结束** – 根据项目日历，工作日的结束工作时间。</span><span class="sxs-lookup"><span data-stu-id="036fa-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="036fa-150">**工时** – 为当天分派的工时数量。</span><span class="sxs-lookup"><span data-stu-id="036fa-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="036fa-151">**示例**</span><span class="sxs-lookup"><span data-stu-id="036fa-151">**Example**</span></span>

<span data-ttu-id="036fa-152">在此示例使用的项目日历中，工作日为 UTC-8 时区上午 9 点到下午 5 点。</span><span class="sxs-lookup"><span data-stu-id="036fa-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="036fa-153">自动计划和手动计划</span><span class="sxs-lookup"><span data-stu-id="036fa-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="036fa-154">如果任务是自动计划的，则工时是前载型，可能会缩短任务持续时间。</span><span class="sxs-lookup"><span data-stu-id="036fa-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="036fa-155">**示例**</span><span class="sxs-lookup"><span data-stu-id="036fa-155">**Example**</span></span>

<span data-ttu-id="036fa-156">以下任务自动计划为三天内 18 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）。</span><span class="sxs-lookup"><span data-stu-id="036fa-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="036fa-157">如果任务是手动计划的，则将工时平均分配给所有日期。</span><span class="sxs-lookup"><span data-stu-id="036fa-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="036fa-158">**示例**</span><span class="sxs-lookup"><span data-stu-id="036fa-158">**Example**</span></span>

<span data-ttu-id="036fa-159">以下任务手动计划为三天内 18 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）。</span><span class="sxs-lookup"><span data-stu-id="036fa-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="036fa-160">分派单位</span><span class="sxs-lookup"><span data-stu-id="036fa-160">Assignment unit</span></span>

<span data-ttu-id="036fa-161">PSA 3.x 中已弃用分派单位。</span><span class="sxs-lookup"><span data-stu-id="036fa-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="036fa-162">现在按天为所有分派的资源平均分配任务工作量小时数。</span><span class="sxs-lookup"><span data-stu-id="036fa-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="036fa-163">**示例**</span><span class="sxs-lookup"><span data-stu-id="036fa-163">**Example**</span></span>

<span data-ttu-id="036fa-164">在此示例中，任务分派给两项资源，并自动计划为三天内 36 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）</span><span class="sxs-lookup"><span data-stu-id="036fa-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="036fa-165">分派 1：</span><span class="sxs-lookup"><span data-stu-id="036fa-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="036fa-166">分派 2：</span><span class="sxs-lookup"><span data-stu-id="036fa-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="036fa-167">定价维度</span><span class="sxs-lookup"><span data-stu-id="036fa-167">Pricing dimensions</span></span>

<span data-ttu-id="036fa-168">在 PSA 3.x 中，已从 **msdyn\_projecttask** 实体删除了资源特定的定价维度字段（如 **角色** 和 **部门**）。</span><span class="sxs-lookup"><span data-stu-id="036fa-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="036fa-169">现在可以在生成项目估算时，从资源分派 (**msdyn\_resourceassignment**) 的相应项目团队成员 (**msdyn\_projectteam**) 检索这些字段。</span><span class="sxs-lookup"><span data-stu-id="036fa-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="036fa-170">已经为 **msdyn\_projectteam** 实体新增了字段 **msdyn\_organizationalunit**。</span><span class="sxs-lookup"><span data-stu-id="036fa-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="036fa-171">msdyn\_projecttask（项目任务）中已弃用的字段</span><span class="sxs-lookup"><span data-stu-id="036fa-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="036fa-172">改用了来自 msdyn\_projectteam（项目团队成员）的字段</span><span class="sxs-lookup"><span data-stu-id="036fa-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="036fa-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="036fa-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="036fa-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="036fa-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="036fa-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="036fa-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="036fa-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="036fa-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="036fa-177">分布</span><span class="sxs-lookup"><span data-stu-id="036fa-177">Contours</span></span>

<span data-ttu-id="036fa-178">**msdyn\_projecttask** 实体中已弃用了定价和估算分布字段。</span><span class="sxs-lookup"><span data-stu-id="036fa-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="036fa-179">已将其移到 **msdyn\_resourceassignment** 实体。</span><span class="sxs-lookup"><span data-stu-id="036fa-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="036fa-180">msdyn\_projecttask（项目任务）中已弃用的字段</span><span class="sxs-lookup"><span data-stu-id="036fa-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="036fa-181">msdyn\_resourceassignment（资源分派）中的新字段</span><span class="sxs-lookup"><span data-stu-id="036fa-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="036fa-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="036fa-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="036fa-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="036fa-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="036fa-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="036fa-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="036fa-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="036fa-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="036fa-186">已为 **msdyn\_resourceassignment** 实体增加了以下字段：</span><span class="sxs-lookup"><span data-stu-id="036fa-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="036fa-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="036fa-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="036fa-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="036fa-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="036fa-189">**msdyn\_projecttask** 实体中计划的成本、实际成本和剩余成本的以下字段未变：</span><span class="sxs-lookup"><span data-stu-id="036fa-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="036fa-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="036fa-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="036fa-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="036fa-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="036fa-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="036fa-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="036fa-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="036fa-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="036fa-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="036fa-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="036fa-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="036fa-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]