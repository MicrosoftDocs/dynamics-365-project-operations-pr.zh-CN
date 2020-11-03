---
title: 根据资源要求预订指定资源
description: 此部分介绍如何为通用资源要求预订指定资源。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072809"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="4a5a2-103">根据资源要求预订指定资源</span><span class="sxs-lookup"><span data-stu-id="4a5a2-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4a5a2-104">可以预订指定资源以替换具有资源要求的通用资源。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="4a5a2-105">在 Project Service Automation (PSA) 中的 **项目** 页中，单击 **团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="4a5a2-106">从列表中选择具有资源要求的通用资源，然后单击 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="4a5a2-107">或者，打开资源要求，然后单击 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-107">Or, open the resource requirement and then click **Book**.</span></span>


![预订通用团队成员](media/RM-how-to-14.png)


3. <span data-ttu-id="4a5a2-109">在 **日程安排助理** 页中，选择要为项目团队预订的指定资源，然后单击 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![使用日程安排助理预订通用团队成员](media/RM-how-to-15.png)

<span data-ttu-id="4a5a2-111">预订完成并由指定资源满足时，将把通用资源替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![指定团队成员替换通用团队成员](media/RM-how-to-16.png)

<span data-ttu-id="4a5a2-113">也将使用该指定资源更新计划的分派。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![分派给项目任务的指定团队成员](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="4a5a2-115">使用多项指定资源替代通用资源</span><span class="sxs-lookup"><span data-stu-id="4a5a2-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="4a5a2-116">使用多项指定资源满足通用资源的要求类似分派一项指定资源。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="4a5a2-117">例如，有一个持续时间为 5 天，工作量为 120 个小时的任务。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="4a5a2-118">此任务不能由一个每周工作五天，每天通常工作八小时的资源完成。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![一个需要为期五天的 120 小时工作量的任务](media/RM-how-to-21.png)

<span data-ttu-id="4a5a2-120">此要求适用于五天工作 120 小时的机器人，即每天工作 24 小时。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![按天要求](media/RM-how-to-22.png)

<span data-ttu-id="4a5a2-122">这个示例是需要多项指定资源来满足一项通用资源请求。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="4a5a2-123">您需要订阅多项资源以满足此要求。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![订阅多项资源以满足要求](media/RM-how-to-23.png)

<span data-ttu-id="4a5a2-125">此方案的主要区别是，分派给任务的团队中仍然保留通用资源，并且此位置中不分派预订的指定资源团队成员。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="4a5a2-126">项目经理可以根据需要将工作分派给指定资源。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="4a5a2-127">**协调** 视图可帮助项目经理将多项资源的预订分解为任务分派。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="4a5a2-128">不会自动执行此操作，因为比上面的简单示例更复杂的方案中（如您有大量任务构成要求），需要系统假设项目经理的分派方法意图。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="4a5a2-129">因为系统无法理解意图，所以假设可能与意图不同，并且可能会发生错误结果或不可预料的结果。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="4a5a2-130">可预测结果是项目经理在 **协调** 视图的协助下特意创建资源之前，一直使用分派的通用资源。</span><span class="sxs-lookup"><span data-stu-id="4a5a2-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


