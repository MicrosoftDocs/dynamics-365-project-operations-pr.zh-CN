---
title: 创建工作时间模板
description: 如何在 Project Service 中创建工作时间模板
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072614"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="8f11e-103">创建工作时间模板 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8f11e-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8f11e-104">在创建项目时间表之前，您需要设置用于定义工作时间数量的项目日历，该日历可容纳时间表中的每一天和任何节假日。</span><span class="sxs-lookup"><span data-stu-id="8f11e-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="8f11e-105">您可使用工作时间模板执行此操作，该模板包含有关每天工作时间、休息日和任何其他节假日的详细信息。</span><span class="sxs-lookup"><span data-stu-id="8f11e-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="8f11e-106">当您在创建项目时，可将工作模板关联至项目日历，以应用项目的时间表。</span><span class="sxs-lookup"><span data-stu-id="8f11e-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="8f11e-107">创建工作时间模板可采用以下两种方法：</span><span class="sxs-lookup"><span data-stu-id="8f11e-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="8f11e-108">创建基于资源日历的工作时间模板。</span><span class="sxs-lookup"><span data-stu-id="8f11e-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="8f11e-109">创建新的工作时间模板。</span><span class="sxs-lookup"><span data-stu-id="8f11e-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="8f11e-110">创建基于资源日历的工作时间模板</span><span class="sxs-lookup"><span data-stu-id="8f11e-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="8f11e-111">转到 **Project Service > 资源** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="8f11e-112">选择要基于您工作时间的资源。</span><span class="sxs-lookup"><span data-stu-id="8f11e-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="8f11e-113">单击 **将日历另存为** ，输入工作时间模板的名称，然后单击 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="8f11e-114">完成更改选项后，单击 **保存并关闭** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="8f11e-115">在屏幕右下角，单击 **保存** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8f11e-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="8f11e-116">创建新的工作时间模板</span><span class="sxs-lookup"><span data-stu-id="8f11e-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="8f11e-117">转至 **Project Service > 工作时间模板** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="8f11e-118">单击 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="8f11e-119">输入工作时间模板的名称。</span><span class="sxs-lookup"><span data-stu-id="8f11e-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="8f11e-120">选择要基于工作时间的资源，然后单击 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="8f11e-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8f11e-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f11e-121">See Also</span></span>  
 [<span data-ttu-id="8f11e-122">设置资源</span><span class="sxs-lookup"><span data-stu-id="8f11e-122">Set up resources</span></span>](../psa/set-up-resources.md)
