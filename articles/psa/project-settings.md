---
title: 项目设置
description: 此主题介绍项目管理设置。
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072767"
---
# <a name="project-settings"></a><span data-ttu-id="49cd8-103">项目设置</span><span class="sxs-lookup"><span data-stu-id="49cd8-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="49cd8-104">可使用以下设置访问项目规划功能。</span><span class="sxs-lookup"><span data-stu-id="49cd8-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="49cd8-105">工作模板</span><span class="sxs-lookup"><span data-stu-id="49cd8-105">Work template</span></span>

<span data-ttu-id="49cd8-106">若要创建项目计划，请创建一个项目日历模板，用于定义每天的工时数和节假日。</span><span class="sxs-lookup"><span data-stu-id="49cd8-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="49cd8-107">若要创建项目日历模板，请将工作模板与项目的 **日历模板** 字段关联。</span><span class="sxs-lookup"><span data-stu-id="49cd8-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="49cd8-108">执行以下步骤创建一个工作模板。</span><span class="sxs-lookup"><span data-stu-id="49cd8-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="49cd8-109">在 PSA 的左侧导航窗格，单击 **资源** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="49cd8-110">在 **资源** 列表页中，打开一条用户记录，然后选择 **显示工时** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="49cd8-111">确保浏览器页中允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="49cd8-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="49cd8-112">这样您就可以查看为资源设置的工时。</span><span class="sxs-lookup"><span data-stu-id="49cd8-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="49cd8-113">在 **月视图** 选项卡中，单击 **设置** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="49cd8-114">将显示三个选项的列表：</span><span class="sxs-lookup"><span data-stu-id="49cd8-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="49cd8-115">新建周计划</span><span class="sxs-lookup"><span data-stu-id="49cd8-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="49cd8-116">一天的工作计划</span><span class="sxs-lookup"><span data-stu-id="49cd8-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="49cd8-117">休息时间</span><span class="sxs-lookup"><span data-stu-id="49cd8-117">Time Off</span></span>

> ![设置选项](media/project-13.png)

4. <span data-ttu-id="49cd8-119">选择 **新建周计划** ，然后为此资源计划设置选项。</span><span class="sxs-lookup"><span data-stu-id="49cd8-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="49cd8-120">可设置定期周计划、日工时参数、节假日等。</span><span class="sxs-lookup"><span data-stu-id="49cd8-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="49cd8-121">设置日期范围，选择 **保存** ，然后单击 **关闭** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="49cd8-122">回到 **资源** 列表页，然后选择要为其设置工时的资源。</span><span class="sxs-lookup"><span data-stu-id="49cd8-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="49cd8-123">选择 **日历设置为** 以设置工作模板。</span><span class="sxs-lookup"><span data-stu-id="49cd8-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="49cd8-124">在 **工作模板** 对话框中，输入工作模板的名称，然后选择 **应用** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="49cd8-125">现在可将此工作模板与项目日历模板关联。</span><span class="sxs-lookup"><span data-stu-id="49cd8-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="49cd8-126">资源角色</span><span class="sxs-lookup"><span data-stu-id="49cd8-126">Resource roles</span></span>

<span data-ttu-id="49cd8-127">术语 *资源角色* 指的是要对项目执行一组特定任务的人员必须拥有的一组技能、资格和认证。</span><span class="sxs-lookup"><span data-stu-id="49cd8-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="49cd8-128">可使用 PSA 根据资源关联的角色设置资源时间的成本和记帐。</span><span class="sxs-lookup"><span data-stu-id="49cd8-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="49cd8-129">每个组织必须使用 **Project Service** 菜单左侧导航设置这些角色。</span><span class="sxs-lookup"><span data-stu-id="49cd8-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="49cd8-130">每个组织必须在 **可用的资源类别** 页中设置这些角色。</span><span class="sxs-lookup"><span data-stu-id="49cd8-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="49cd8-131">若要打开此页，请在左侧导航窗格中选择 **资源角色** 。</span><span class="sxs-lookup"><span data-stu-id="49cd8-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="49cd8-132">价目表</span><span class="sxs-lookup"><span data-stu-id="49cd8-132">Price lists</span></span>

<span data-ttu-id="49cd8-133">可通过价目表设置资源角色、支出类别、产品和组织中的其他元素的成本和销售价。</span><span class="sxs-lookup"><span data-stu-id="49cd8-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="49cd8-134">在为项目设置必须交付的工作的财务估算之前，应创建基础成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="49cd8-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="49cd8-135">还应在参数部分中设置应用于组织中创建的每个项目的默认成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="49cd8-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="49cd8-136">在 **可用的项目参数** 页中，务必设置默认成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="49cd8-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
