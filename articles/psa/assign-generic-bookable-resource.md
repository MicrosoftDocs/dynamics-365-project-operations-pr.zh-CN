---
title: 为任务和项目团队分派通用可预订资源
description: 本主题提供有关为任务和项目团队预订通用资源的信息。
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072619"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="19666-103">为任务分派通用可预订资源和生成资源要求</span><span class="sxs-lookup"><span data-stu-id="19666-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="19666-104">除了为项目预订和分派指定资源或实际资源，还可以为项目任务分派通用资源。</span><span class="sxs-lookup"><span data-stu-id="19666-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="19666-105">在您准备好使用指定资源为项目安排人员之前，这些资源可充当指定资源的替身。</span><span class="sxs-lookup"><span data-stu-id="19666-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="19666-106">在 Project Service Automation (PSA) 中，打开 **项目** 页面，然后在 **计划** 选项卡上计划的 **资源** 单元格中，输入通用资源的位置名称。</span><span class="sxs-lookup"><span data-stu-id="19666-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="19666-107">或单击单元格中的 **资源** 图标打开资源选取器，然后输入要创建的通用资源的名称。</span><span class="sxs-lookup"><span data-stu-id="19666-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![创建和分派通用团队成员](media/RM-how-to-9.png)

<span data-ttu-id="19666-109">这将打开 **快速创建: 项目团队成员** 面板。</span><span class="sxs-lookup"><span data-stu-id="19666-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="19666-110">输入通用资源团队成员的角色和部门，然后单击 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="19666-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![快速创建通用团队成员](media/RM-how-to-10.png)

3. <span data-ttu-id="19666-112">创建新的通用资源团队成员之后，将把其分派给任务。</span><span class="sxs-lookup"><span data-stu-id="19666-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="19666-113">您可以继续把该通用资源分派给任务计划中的其他任务。</span><span class="sxs-lookup"><span data-stu-id="19666-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![将现有通用团队成员分派给任务](media/RM-how-to-11.png)

4. <span data-ttu-id="19666-115">分派通用资源之后，可以通过直接预订或向资源经理提交资源请求来生成资源要求并满足。</span><span class="sxs-lookup"><span data-stu-id="19666-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![为通用团队成员生成要求](media/RM-how-to-12.png)

<span data-ttu-id="19666-117">在团队成员网格中，除了可以按照上面的介绍使用资源选取器，还可以直接生成通用资源。</span><span class="sxs-lookup"><span data-stu-id="19666-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="19666-118">将添加资源和基于 **快速创建: 项目团队成员** 面板中指定的开始/结束日期和分配方法的资源要求。</span><span class="sxs-lookup"><span data-stu-id="19666-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="19666-119">如果您直接添加通用团队成员，然后向通用资源添加比它们要求工时内所需更多的任务，可能会发现差异。</span><span class="sxs-lookup"><span data-stu-id="19666-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="19666-120">请单击 **生成要求** 再次生成要求以平衡所需工时与分派。</span><span class="sxs-lookup"><span data-stu-id="19666-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="19666-121">还可以单击团队网格中的 **资源要求** 链接打开要求并添加技能、首选资源等。</span><span class="sxs-lookup"><span data-stu-id="19666-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![资源要求](media/RM-how-to-13.png)

