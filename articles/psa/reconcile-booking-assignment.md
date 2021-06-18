---
title: 协调预订和分派
description: 本主题提供有关实际值的信息。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73cbc89ae4350cbd568f1bb978825ff53da07afb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008885"
---
# <a name="reconcile-bookings-and-assignments"></a><span data-ttu-id="4d26f-103">协调预订和分派</span><span class="sxs-lookup"><span data-stu-id="4d26f-103">Reconcile bookings and assignments</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4d26f-104">项目团队成员的项目预订与项目任务分派之间关系松散。</span><span class="sxs-lookup"><span data-stu-id="4d26f-104">A project team member's project bookings and project task assignments are loosely coupled.</span></span> <span data-ttu-id="4d26f-105">因此，一个资源可以有不与预订对应的任务分派和不与任务分派对应的预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-105">Therefore, a resource can have task assignments that don't correspond to bookings and bookings that don't correspond to task assignments.</span></span> <span data-ttu-id="4d26f-106">理想情况下，项目预订和分派一致，这样资源就可以落实产能以执行其任务分派。</span><span class="sxs-lookup"><span data-stu-id="4d26f-106">Ideally, project bookings and assignments are aligned, so that resources have committed capacity to perform their task assignments.</span></span> <span data-ttu-id="4d26f-107">但是，现实却是预订可能基于可用性，而任务计时可能随着项目经历其生命周期而改变。</span><span class="sxs-lookup"><span data-stu-id="4d26f-107">However, the reality is that bookings can occur based on availability, and task timings can change as the project continues through its lifecycle.</span></span> <span data-ttu-id="4d26f-108">因此，松散耦合为灵活性留出了余地。</span><span class="sxs-lookup"><span data-stu-id="4d26f-108">Therefore, the loose coupling allows for flexibility.</span></span>

<span data-ttu-id="4d26f-109">由于项目预订与任务分派松散耦合，项目实体中有一个 **协调** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="4d26f-109">Because of the loose coupling of project bookings and task assignments, a **Reconciliation** tab is included on the Project entity.</span></span> <span data-ttu-id="4d26f-110">此选项卡可帮助项目经理协调其项目团队的团队成员预订及其分派。</span><span class="sxs-lookup"><span data-stu-id="4d26f-110">This tab helps project managers reconcile team members' bookings and their assignments for their project team.</span></span>

<span data-ttu-id="4d26f-111">对于每位指定团队成员，**协调** 选项卡显示深入到单个任务分派的预订和分派。</span><span class="sxs-lookup"><span data-stu-id="4d26f-111">For each named team member, the **Reconciliation** tab shows bookings and assignments down to the individual task assignment.</span></span> <span data-ttu-id="4d26f-112">它通过单元格显示可表示时间段（从数月到数天）的工时。</span><span class="sxs-lookup"><span data-stu-id="4d26f-112">It shows hours in cells that can represent periods from months down to days.</span></span>

<span data-ttu-id="4d26f-113">在 **时间刻度** 字段中，可以选择 **月**、**周** 或 **天**。</span><span class="sxs-lookup"><span data-stu-id="4d26f-113">In the **Timescale** field, you can select **Month**, **Week**, or **Day**.</span></span> <span data-ttu-id="4d26f-114">默认情况下选中 **周**。</span><span class="sxs-lookup"><span data-stu-id="4d26f-114">By default, **Week** is selected.</span></span> <span data-ttu-id="4d26f-115">但是，可以通过选择 **设置** 按钮更改默认值。</span><span class="sxs-lookup"><span data-stu-id="4d26f-115">However, you can change the default value by selecting the **Settings** button.</span></span> <span data-ttu-id="4d26f-116">打开 **协调** 选项卡后，将显示当前日期，但是可以使用日历控件在时间中前进或后退。</span><span class="sxs-lookup"><span data-stu-id="4d26f-116">When the **Reconciliation** tab is opened, it shows the current date, but you can use the calendar control to move forward or backward in time.</span></span> <span data-ttu-id="4d26f-117">如果项目的开始日期在将来，此选项卡将在项目打开时显示该日期。</span><span class="sxs-lookup"><span data-stu-id="4d26f-117">When a project has a start date that is in the future, the tab shows that date when it's opened.</span></span> <span data-ttu-id="4d26f-118">日历控件中还有用于移到项目开始日期和结束日期的选项。</span><span class="sxs-lookup"><span data-stu-id="4d26f-118">The calendar control also has options that let you move to the project start and end dates.</span></span>

<span data-ttu-id="4d26f-119">可使用每个资源的展开器控件显示资源的预订详细信息。</span><span class="sxs-lookup"><span data-stu-id="4d26f-119">You can use the expander controls on each resource to show the details of that resource's bookings.</span></span> <span data-ttu-id="4d26f-120">也可以将每项资源的分派展开至单个任务级别。</span><span class="sxs-lookup"><span data-stu-id="4d26f-120">You can also expand each resource's assignments to the level of the individual task.</span></span>

<span data-ttu-id="4d26f-121">**协调** 选项卡底部显示项目的整体净总额，而此选项卡中还包含一个总计列。</span><span class="sxs-lookup"><span data-stu-id="4d26f-121">The bottom of the **Reconciliation** tab shows an overall net total for the project, and the tab also includes a total column.</span></span> <span data-ttu-id="4d26f-122">对于每个资源，此选项卡采用团队成员的项目预订与该团队成员任务分派汇总之差。</span><span class="sxs-lookup"><span data-stu-id="4d26f-122">For each resource, the tab takes the difference between a team member's bookings on the project and rollup of that team member's task assignments.</span></span> <span data-ttu-id="4d26f-123">理想情况下，差应该为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="4d26f-123">Ideally, the difference should be 0 (zero).</span></span> <span data-ttu-id="4d26f-124">换句话说，资源的预订与其任务分派之间应该无差额。</span><span class="sxs-lookup"><span data-stu-id="4d26f-124">In other words, there should be no difference between the resource's bookings and its task assignments.</span></span> <span data-ttu-id="4d26f-125">将使用颜色和阴影来指示所有差额以指示两种情况：</span><span class="sxs-lookup"><span data-stu-id="4d26f-125">Any differences are indicated by color and shading to call out two conditions:</span></span>

- <span data-ttu-id="4d26f-126">**预订不足** – 资源的分派比预订的多时，会发生预订不足。</span><span class="sxs-lookup"><span data-stu-id="4d26f-126">**Booking shortage** – Booking shortages occur when a resource has more assignments than bookings.</span></span> <span data-ttu-id="4d26f-127">因为尚未保留此产能，所以项目经理可以解决这个问题，方法是扩展资源的预订以弥补不足。</span><span class="sxs-lookup"><span data-stu-id="4d26f-127">Because this capacity hasn't been reserved, a project manager can correct this condition by extending the resource's bookings to cover the shortage.</span></span>
- <span data-ttu-id="4d26f-128">**超出预订** – 当已经将某个资源预订给项目，但是尚未将其分派给任务时，发生超出预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-128">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="4d26f-129">可能可以接受这种情况，例如，资源在任务分派前预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-129">This condition might be acceptable if, for example, the resource has been booked before task assignment occurs.</span></span> <span data-ttu-id="4d26f-130">但是，如果是其他情况，可能不会计划分派资源。</span><span class="sxs-lookup"><span data-stu-id="4d26f-130">However, in other cases, the resource might not be planned to be assigned.</span></span> <span data-ttu-id="4d26f-131">在这些情况下，项目经理应该考虑取消资源的预订，以便将产能用于其他项目。</span><span class="sxs-lookup"><span data-stu-id="4d26f-131">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

> [!NOTE]
> <span data-ttu-id="4d26f-132">可能会隐藏这些情况的图例，以便为网格留出更多空间。</span><span class="sxs-lookup"><span data-stu-id="4d26f-132">The legend for these conditions might be hidden to leave more room for the grid.</span></span> <span data-ttu-id="4d26f-133">在此情况下，可以使用 **设置** 按钮显示此图例。</span><span class="sxs-lookup"><span data-stu-id="4d26f-133">In this case, you can make the legend visible by selecting the **Settings** button.</span></span>

<span data-ttu-id="4d26f-134">在某些情况下，当 **时间刻度** 字段设置为比 **天** 更高的级别，计算出的差额可能为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="4d26f-134">In some cases, when the **Timescale** field is set to a level that is higher than **Day**, differences might be calculated as 0 (zero).</span></span> <span data-ttu-id="4d26f-135">例如，在 **月** 级别，某个资源的净差额可能为 0（零），说明预订等于分派。</span><span class="sxs-lookup"><span data-stu-id="4d26f-135">For example, at the **Month** level, the net difference for a resource might be 0 (zero) to indicate that bookings equal assignments.</span></span> <span data-ttu-id="4d26f-136">但是，如果查看 **周** 级别，可能会发现当月第一周的分派为 0（零）小时，预订为 40 小时，但是当月第二周的分派为 40 小时，预订为 0（零）小时。</span><span class="sxs-lookup"><span data-stu-id="4d26f-136">However, if you look at the **Week** level, you might see that there are assignments of 0 (zero) hours and bookings of 40 hours in the first week of the month, and assignments of 40 hours and bookings of 0 (zero) hours in the second week of the month.</span></span> <span data-ttu-id="4d26f-137">尽管当月的总预订和分派相等，但按周时则不相等。</span><span class="sxs-lookup"><span data-stu-id="4d26f-137">Although the total bookings and assignments for the month are equal, they differ by week.</span></span>

<span data-ttu-id="4d26f-138">查看更高级别时，**协调** 选项卡显示一个单元格指示器，用于通知您较低时间级别存在差额。</span><span class="sxs-lookup"><span data-stu-id="4d26f-138">When you view higher time levels, the **Reconciliation** tab shows a cell indicator to notify you that there are differences at lower time levels.</span></span> <span data-ttu-id="4d26f-139">例如，在下图中，名称为龚莲的资源的 2018 年 10 月的单元格中显示了一个单元格指示器。</span><span class="sxs-lookup"><span data-stu-id="4d26f-139">For example, in the following illustration, a cell indicator appears in the cell for the month of October 2018 for the resource that is named Katelyn Merritt.</span></span> <span data-ttu-id="4d26f-140">因此您可以看到，即使该资源的预订和分派在 **月** 级别聚合时相等，在更低级别则不匹配。</span><span class="sxs-lookup"><span data-stu-id="4d26f-140">Therefore, you can see that, even though the resource's bookings and assignments are equal when they are aggregated at the **Month** level, they don't match at lower levels.</span></span>

![每月级别的预订和分配不匹配](media/reconcile-assignments-01.JPG)

<span data-ttu-id="4d26f-142">双击单元格放大到下一个更低级别并查看差额。</span><span class="sxs-lookup"><span data-stu-id="4d26f-142">Double-click a cell to zoom in to the next lower level and view the difference.</span></span> <span data-ttu-id="4d26f-143">例如，如果双击龚莲的 2018 年 10 月差额，将向下钻取到 **周** 级别。</span><span class="sxs-lookup"><span data-stu-id="4d26f-143">For example, if you double-click the October 2018 difference for Katelyn Merritt, you drill down to the **Week** level.</span></span> <span data-ttu-id="4d26f-144">然后可以看到 10 月前两周该资源的预订为 16 个工时，但是没有任何分派，10 月第三周有 16 个工时的分派，但是没有任何预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-144">You can then see that the resource has bookings of 16 hours but no assignments in the first two weeks of October, and 16 hours of assignments but no bookings in the third week of October.</span></span>

![每周级别的预订和分配不匹配](media/reconcile-assignments-02.JPG)

<span data-ttu-id="4d26f-146">可以右键单击单元格缩小到下一个更高级别。</span><span class="sxs-lookup"><span data-stu-id="4d26f-146">You can right-click a cell to zoom out the next higher level.</span></span> <span data-ttu-id="4d26f-147">也可以通过选择 **设置** 按钮关闭单元格指示器。</span><span class="sxs-lookup"><span data-stu-id="4d26f-147">You can also turn off the cell indicator by selecting the **Settings** button.</span></span> 

<span data-ttu-id="4d26f-148">还可以使用网格上方的 **上一个** 和 **下一个** 按钮在项目中的任何差额之间切换。</span><span class="sxs-lookup"><span data-stu-id="4d26f-148">You can also use the **Previous** and **Next** buttons above the grid to move through any differences in your project.</span></span> <span data-ttu-id="4d26f-149">若要使用这些按钮，必须先选择资源。</span><span class="sxs-lookup"><span data-stu-id="4d26f-149">To use these buttons, you must first select a resource.</span></span> <span data-ttu-id="4d26f-150">选择 **下一个** 将转到该资源的预订与分派之间的下一个差额。</span><span class="sxs-lookup"><span data-stu-id="4d26f-150">Select **Next** to go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="4d26f-151">选择 **上一个** 则转到上一个差额。</span><span class="sxs-lookup"><span data-stu-id="4d26f-151">Select **Previous** to go to the previous difference.</span></span>

<span data-ttu-id="4d26f-152">如果资源有任务分派，但是没有预订，可以选择预订不足，然后选择 **扩展预订**。</span><span class="sxs-lookup"><span data-stu-id="4d26f-152">In situations where you have task assignments for a resource but no bookings, you can select the booking shortage and then select **Extend Booking**.</span></span> <span data-ttu-id="4d26f-153">然后可以查看需要来解决资源不足的预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-153">You can then see the booking that is required in order to address the resource's shortage.</span></span> <span data-ttu-id="4d26f-154">也可以查看该资源在当前项目和其他项目中的预订。</span><span class="sxs-lookup"><span data-stu-id="4d26f-154">You can also view the resource's bookings on the current project and other projects.</span></span> <span data-ttu-id="4d26f-155">选择 **确定** 为资源创建预订，并且不考虑当前可用性。</span><span class="sxs-lookup"><span data-stu-id="4d26f-155">Select **OK** to create the booking for the resource without regard to current availability.</span></span> <span data-ttu-id="4d26f-156">然后，项目经理或资源经理可使用日程安排板管理资源的预订已扩展，所以其超额预订已超过产能的情况。</span><span class="sxs-lookup"><span data-stu-id="4d26f-156">The project manager or resource manager can then use Schedule Board to manage situations where a resource has become overbooked beyond capacity because its bookings were extended.</span></span>

## <a name="managing-with-time-zones"></a><span data-ttu-id="4d26f-157">使用时区管理</span><span class="sxs-lookup"><span data-stu-id="4d26f-157">Managing with time zones</span></span>
<span data-ttu-id="4d26f-158">若要在使用扩展预订时确保获得准确且可预测的结果，必须满足以下两个主要先决条件：</span><span class="sxs-lookup"><span data-stu-id="4d26f-158">To ensure accurate and predictable results when using Extend Booking, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="4d26f-159">用户必须配置其设备时区，以与您的“系统个性化设置”中定义的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="4d26f-159">The user must configure their device's time zone to match the time zone defined in your system's Personalization Settings.</span></span>
 
  ![Windows 10 中的时区设置](media/reconcile-assignments-03.png)

  ![个性化设置中的时区设置](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="4d26f-162">可预订资源必须至少有一分钟的工作时间与用于定义所请求扩展的分布重叠。</span><span class="sxs-lookup"><span data-stu-id="4d26f-162">The Bookable Resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="4d26f-163">例如，以下示例显示了工作时间介于上午 9:00 和下午 7:00 之间的审阅资源。</span><span class="sxs-lookup"><span data-stu-id="4d26f-163">For instance, the following example shows review resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![资源分布比较](media/reconcile-assignments-05.png)

<span data-ttu-id="4d26f-165">下表显示了：</span><span class="sxs-lookup"><span data-stu-id="4d26f-165">The following table shows:</span></span>

- <span data-ttu-id="4d26f-166">项目日历模板。</span><span class="sxs-lookup"><span data-stu-id="4d26f-166">A project calendar template.</span></span>
- <span data-ttu-id="4d26f-167">资源 A：该资源具有相同的日历，并与项目位于同一时区中。</span><span class="sxs-lookup"><span data-stu-id="4d26f-167">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="4d26f-168">预订的开始时间将为上午 9:00。</span><span class="sxs-lookup"><span data-stu-id="4d26f-168">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="4d26f-169">资源 B：此资源与项目位于不同的时区中，因此开始时间为其时区中的上午 7:00。</span><span class="sxs-lookup"><span data-stu-id="4d26f-169">Resources B: This resource is located in a different time zone than the project and therefore starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="4d26f-170">但是，预订将在上午 9:00 开始，因为这是工作分布的最早开始时间。</span><span class="sxs-lookup"><span data-stu-id="4d26f-170">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="4d26f-171">资源 C 和 D：资源也位于不同的时区中，两个相互不同并且与项目也不同，且其预订开始时间不早于各自的可用开始时间。</span><span class="sxs-lookup"><span data-stu-id="4d26f-171">Resources C and D: The resources are also located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="4d26f-172">实体</span><span class="sxs-lookup"><span data-stu-id="4d26f-172">Entity</span></span>  |<span data-ttu-id="4d26f-173">日历</span><span class="sxs-lookup"><span data-stu-id="4d26f-173">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="4d26f-174">项目日历模板</span><span class="sxs-lookup"><span data-stu-id="4d26f-174">Project calendar template</span></span>   | ![项目日历](media/reconcile-assignments-06.png) |
|<span data-ttu-id="4d26f-176">资源 A</span><span class="sxs-lookup"><span data-stu-id="4d26f-176">Resource A</span></span>  | ![资源 A 日历](media/reconcile-assignments-06.png) |
|<span data-ttu-id="4d26f-178">资源 B</span><span class="sxs-lookup"><span data-stu-id="4d26f-178">Resource B</span></span>  |  ![资源 B 日历](media/reconcile-assignments-07.png) |
|<span data-ttu-id="4d26f-180">资源 C</span><span class="sxs-lookup"><span data-stu-id="4d26f-180">Resource C</span></span>  |  ![资源 C 日历](media/reconcile-assignments-08.png) |
|<span data-ttu-id="4d26f-182">资源 D</span><span class="sxs-lookup"><span data-stu-id="4d26f-182">Resource D</span></span>  | ![资源 D 日历](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="4d26f-184">当您导航到协调视图时，将显示资源分配和关联的预订不足。</span><span class="sxs-lookup"><span data-stu-id="4d26f-184">When you navigate to the reconciliation view, the resource assignments and the associated booking shortages will be displayed.</span></span>
 <span data-ttu-id="4d26f-185">![扩展前的协调视图](media/reconcile-assignments-10.png)</span><span class="sxs-lookup"><span data-stu-id="4d26f-185">![Reconciliation view before extension](media/reconcile-assignments-10.png)</span></span>

<span data-ttu-id="4d26f-186">对每个资源执行完扩展预订功能之后，每个资源的预订都将被成功扩展。</span><span class="sxs-lookup"><span data-stu-id="4d26f-186">After the Extend Booking functionality has been executed on each resource, bookings are successfully extended for each resource.</span></span> <span data-ttu-id="4d26f-187">这是因为每个资源的工作时间都与不足的分布重叠。</span><span class="sxs-lookup"><span data-stu-id="4d26f-187">This is because each resource’s working hours overlapped with the contours of the shortage.</span></span>
 <span data-ttu-id="4d26f-188">![预订扩展后的协调视图](media/reconcile-assignments-11.png)</span><span class="sxs-lookup"><span data-stu-id="4d26f-188">![Reconciliation view after booking extension](media/reconcile-assignments-11.png)</span></span> 

<span data-ttu-id="4d26f-189">但是，仔细查看预订的详细信息会发现预订开始时间有所不同。</span><span class="sxs-lookup"><span data-stu-id="4d26f-189">However, a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="4d26f-190">预订的开始时间将不早于工作分布的开始时间，也不会早于资源的可用开始时间。</span><span class="sxs-lookup"><span data-stu-id="4d26f-190">The bookings will start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>
 <span data-ttu-id="4d26f-191">![日程安排板中的新资源预订](media/reconcile-assignments-12.png)</span><span class="sxs-lookup"><span data-stu-id="4d26f-191">![New bookings of the resources in the schedule board](media/reconcile-assignments-12.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]