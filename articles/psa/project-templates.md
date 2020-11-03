---
title: 项目模板
description: 此主题介绍如何使用项目模板快速设置项目。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072766"
---
# <a name="project-templates"></a><span data-ttu-id="a6e96-103">项目模板</span><span class="sxs-lookup"><span data-stu-id="a6e96-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a6e96-104">项目模板是一种预定义的框架，可帮助您快速、轻松地启动项目。</span><span class="sxs-lookup"><span data-stu-id="a6e96-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="a6e96-105">单击一次，即可使用预定义的模板创建新项目。</span><span class="sxs-lookup"><span data-stu-id="a6e96-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="a6e96-106">至于项目，必须为项目模板定义先决条件。</span><span class="sxs-lookup"><span data-stu-id="a6e96-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="a6e96-107">必须为每个项目模板定义项目日历，并且必须在组织中预定义角色和价目表，因此模板的组件中包含有用的数据。</span><span class="sxs-lookup"><span data-stu-id="a6e96-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="a6e96-108">项目模板有三个组件组成：计划、项目估算和项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="a6e96-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="a6e96-109">Schedule</span><span class="sxs-lookup"><span data-stu-id="a6e96-109">Schedule</span></span>

<span data-ttu-id="a6e96-110">项目模板中的计划与项目中的计划拥有同一组元素。</span><span class="sxs-lookup"><span data-stu-id="a6e96-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="a6e96-111">您可以创建任务层次结构，将角色与任务关联，定义计划属性，以及设置依赖项。</span><span class="sxs-lookup"><span data-stu-id="a6e96-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="a6e96-112">项目模板中的计划也支持每个任务拥有任务模式。</span><span class="sxs-lookup"><span data-stu-id="a6e96-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="a6e96-113">因此，支持计划引擎。</span><span class="sxs-lookup"><span data-stu-id="a6e96-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="a6e96-114">必须将项目日历与项目关联。</span><span class="sxs-lookup"><span data-stu-id="a6e96-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="a6e96-115">创建工作计划时，项目模板和项目之间没有差异。</span><span class="sxs-lookup"><span data-stu-id="a6e96-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="a6e96-116">项目估算</span><span class="sxs-lookup"><span data-stu-id="a6e96-116">Project estimates</span></span>

<span data-ttu-id="a6e96-117">项目模板中的项目估算与项目中的项目估算的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="a6e96-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="a6e96-118">但是，将从参数中定义的默认成本和销售价目表提取成本和销售价。</span><span class="sxs-lookup"><span data-stu-id="a6e96-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="a6e96-119">从模板创建项目</span><span class="sxs-lookup"><span data-stu-id="a6e96-119">Creating a project from a template</span></span>
 
<span data-ttu-id="a6e96-120">可通过多种方法从项目模板创建项目：</span><span class="sxs-lookup"><span data-stu-id="a6e96-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="a6e96-121">在根据报价单创建项目时，您可以在 **快速创建: 项目** 窗体中选择项目模板。</span><span class="sxs-lookup"><span data-stu-id="a6e96-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![“快速创建: 项目”对话框](media/project-11.png)

- <span data-ttu-id="a6e96-123">通过选择 **新建项目** 创建项目时，保存记录之前将显示 **项目** 页。</span><span class="sxs-lookup"><span data-stu-id="a6e96-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="a6e96-124">在 **选取模板** 字段中，选择组织中的一个预定义项目模板。</span><span class="sxs-lookup"><span data-stu-id="a6e96-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="a6e96-125">使用 **模板实体** 页上的 **从模板创建项目** 。</span><span class="sxs-lookup"><span data-stu-id="a6e96-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="a6e96-126">将模板组件复制到项目</span><span class="sxs-lookup"><span data-stu-id="a6e96-126">Copying components of template to project</span></span>

<span data-ttu-id="a6e96-127">将项目模板的组件复制到项目时，可能进行一些替代，具体取决于项目中的设置。</span><span class="sxs-lookup"><span data-stu-id="a6e96-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="a6e96-128">复制计划</span><span class="sxs-lookup"><span data-stu-id="a6e96-128">Copying the schedule</span></span>

<span data-ttu-id="a6e96-129">在从项目模板复制计划时，如果项目的项目日历与模板不同，项目日历的工作时间将应用于任务计划。</span><span class="sxs-lookup"><span data-stu-id="a6e96-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="a6e96-130">这样，将调整计划以匹配基础项目日历。</span><span class="sxs-lookup"><span data-stu-id="a6e96-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="a6e96-131">同样，计划的第一项任务获取项目的开始日期，并基于在模板中指定的持续时间和依赖项更新层次结构其余部分的计划。</span><span class="sxs-lookup"><span data-stu-id="a6e96-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="a6e96-132">复制项目估算</span><span class="sxs-lookup"><span data-stu-id="a6e96-132">Copying project estimates</span></span> 

<span data-ttu-id="a6e96-133">在项目估算明细之间进行复制时，将更新价目表。</span><span class="sxs-lookup"><span data-stu-id="a6e96-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="a6e96-134">对于成本价目表，这些更新基于项目的负责单位。</span><span class="sxs-lookup"><span data-stu-id="a6e96-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="a6e96-135">对于销售价目表，则基于客户。</span><span class="sxs-lookup"><span data-stu-id="a6e96-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="a6e96-136">对于与销售实体关联的项目，单位成本和销售价根据这些价目表确定。</span><span class="sxs-lookup"><span data-stu-id="a6e96-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="a6e96-137">复制项目团队</span><span class="sxs-lookup"><span data-stu-id="a6e96-137">Copying a project team</span></span>

<span data-ttu-id="a6e96-138">在将项目团队从项目模板复制到项目时，通用资源与模板中定义的技能和专长一起复制。</span><span class="sxs-lookup"><span data-stu-id="a6e96-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="a6e96-139">通用资源分派也与项目模板中一样进行维护。</span><span class="sxs-lookup"><span data-stu-id="a6e96-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="a6e96-140">项目模板中不支持指定资源。</span><span class="sxs-lookup"><span data-stu-id="a6e96-140">Named resources aren't supported in project templates.</span></span>
