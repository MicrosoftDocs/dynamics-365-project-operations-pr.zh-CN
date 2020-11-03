---
title: 创建项目模板
description: 如何在 Project Service 中创建项目模板
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072617"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="dba16-103">创建项目模板 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dba16-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dba16-104">如果您的公司是对类似的项目类型定期投标，项目模板将节约您的时间。</span><span class="sxs-lookup"><span data-stu-id="dba16-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="dba16-105">它们提供项目类型的一组标准角色和估计时间。</span><span class="sxs-lookup"><span data-stu-id="dba16-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="dba16-106">客户经理和项目经理可以基于项目模板创建项目，也可以复制模板和制作一个他们自己的模板。</span><span class="sxs-lookup"><span data-stu-id="dba16-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="dba16-107">项目模板组件</span><span class="sxs-lookup"><span data-stu-id="dba16-107">Components of project template</span></span>
 <span data-ttu-id="dba16-108">项目模板具有三个组件：</span><span class="sxs-lookup"><span data-stu-id="dba16-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="dba16-109">**工作分解结构** ：项目模板中的工作分解结构具有与项目相同的一组元素。</span><span class="sxs-lookup"><span data-stu-id="dba16-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="dba16-110">您可以创建任务层次结构，将角色关联到任务，定义计划属性，设置依赖项并在甘特图中查看所有数据。</span><span class="sxs-lookup"><span data-stu-id="dba16-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="dba16-111">项目模板中的工作分解结构还支持各项任务的任务模式。</span><span class="sxs-lookup"><span data-stu-id="dba16-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="dba16-112">在创建工作计划时，项目模板和项目之间没有差异。</span><span class="sxs-lookup"><span data-stu-id="dba16-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="dba16-113">**项目估算** ：除默认的价目表外，模板中的项目估算方式与项目中的方式相同，成本价和销售价始终是在[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]参数中定义的默认成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="dba16-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="dba16-114">此功能的其他部分与项目中的功能相同。</span><span class="sxs-lookup"><span data-stu-id="dba16-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="dba16-115">**项目团队建立** ：在为项目模板建立项目团队时，您不能在模板中预订指定的资源。</span><span class="sxs-lookup"><span data-stu-id="dba16-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="dba16-116">您在工作分解结构中可以使用 **生成项目团队** 来生成一套通用资源。</span><span class="sxs-lookup"><span data-stu-id="dba16-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="dba16-117">您还可以为通用资源指定所需的技能和专长。</span><span class="sxs-lookup"><span data-stu-id="dba16-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="dba16-118">您不能在项目模板中使用可预订资源替代通用资源。</span><span class="sxs-lookup"><span data-stu-id="dba16-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="dba16-119">从模板创建项目</span><span class="sxs-lookup"><span data-stu-id="dba16-119">Create a project from a template</span></span>  
 <span data-ttu-id="dba16-120">您可以按照以下方法从模板创建项目：</span><span class="sxs-lookup"><span data-stu-id="dba16-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="dba16-121">在根据报价单创建一个项目时，您可以在项目快速创建窗体中选择项目模板。</span><span class="sxs-lookup"><span data-stu-id="dba16-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="dba16-122">在通过单击 **新建项目** 创建项目时，项目窗体将在您保存记录前显示。</span><span class="sxs-lookup"><span data-stu-id="dba16-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="dba16-123">在此，您可以单击 **选取模板** 字段从您组织的预定义项目模板列表中选择模板。</span><span class="sxs-lookup"><span data-stu-id="dba16-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="dba16-124">单击 **项目模板** 页上的 **从模板创建项目** 来从模板创建项目。</span><span class="sxs-lookup"><span data-stu-id="dba16-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="dba16-125">将模板组件复制到项目</span><span class="sxs-lookup"><span data-stu-id="dba16-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="dba16-126">在将模板组件复制到项目时，您应当了解一些事项。</span><span class="sxs-lookup"><span data-stu-id="dba16-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="dba16-127">**复制工作分解结构** ：在从项目模板复制工作分解结构时，如果项目的项目日历与模板不同，项目日历的上班时间将应用于任务计划。</span><span class="sxs-lookup"><span data-stu-id="dba16-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="dba16-128">这会将计划调整为支持项目日历。</span><span class="sxs-lookup"><span data-stu-id="dba16-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="dba16-129">同样，工作分解结构的第一项任务获取项目的开始日期，这样任务层次结构计划的其余部分基于在模板的工作分解结构中指定的持续时间和依赖项更新。</span><span class="sxs-lookup"><span data-stu-id="dba16-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="dba16-130">**复制项目估算** ：当您跨项目估算复制时，价目表基于成本价目表的项目和销售价目表的客户的负责部门更新。</span><span class="sxs-lookup"><span data-stu-id="dba16-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="dba16-131">单位成本和销售价格从与销售实体关联的项目中的这些价目表确定。</span><span class="sxs-lookup"><span data-stu-id="dba16-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="dba16-132">**复制项目团队** ：在将项目团队从模板复制到项目时，通用资源跨在模板中定义的技能和专长并与其一起复制。</span><span class="sxs-lookup"><span data-stu-id="dba16-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="dba16-133">通用资源分派也与项目模板中一样进行维护。</span><span class="sxs-lookup"><span data-stu-id="dba16-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dba16-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dba16-134">See Also</span></span>  
 [<span data-ttu-id="dba16-135">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="dba16-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
