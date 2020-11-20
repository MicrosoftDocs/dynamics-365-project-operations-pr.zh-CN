---
title: 跟踪项目状态
description: 如何在 Project Service 中跟踪项目状态
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072690"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="2f6ec-103">跟踪项目状态 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2f6ec-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2f6ec-104">使用 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]来跟踪客户端项目的进度。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="2f6ec-105">作为执行进度，项目阶段更新以反映执行的阶段：</span><span class="sxs-lookup"><span data-stu-id="2f6ec-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="2f6ec-106">**新建**</span><span class="sxs-lookup"><span data-stu-id="2f6ec-106">**New**</span></span>    | <span data-ttu-id="2f6ec-107">创建项目时，该阶段设置为 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="2f6ec-108">如果您已从模板创建项目，则在此阶段，项目可能具有计划、估算和团队数据。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="2f6ec-109">否则，它将是项目的概述，您需要手动输入剩余的项目组成部分。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="2f6ec-110">**报价单**</span><span class="sxs-lookup"><span data-stu-id="2f6ec-110">**Quote**</span></span>   |      <span data-ttu-id="2f6ec-111">当您将项目关联至报价单或从报价单创建项目时，项目阶段设置为 **报价单** ，并且估算的开始和结束日期也会更新。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="2f6ec-112">当项目处于报价单阶段时，有关报价单的详细信息显示在 **项目** 页面上的 **销售** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="2f6ec-113">**规划**</span><span class="sxs-lookup"><span data-stu-id="2f6ec-113">**Plan**</span></span>   |                                     <span data-ttu-id="2f6ec-114">当您获得与项目相关的报价单时，并且当执行进度为合同阶段时，项目阶段更新为 **规划** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="2f6ec-115">合同详细信息显示在 **项目** 页面上的 **销售** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="2f6ec-116">**完成**</span><span class="sxs-lookup"><span data-stu-id="2f6ec-116">**Complete**</span></span> |                    <span data-ttu-id="2f6ec-117">项目工作完成后，可将阶段切换为 **完工** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="2f6ec-118">当项目阶段设置为完工时，可理解工作 100% 完成，但项目保持打开，便于记录任何待定时间或费用条目。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="2f6ec-119">**关闭**</span><span class="sxs-lookup"><span data-stu-id="2f6ec-119">**Close**</span></span>   |           <span data-ttu-id="2f6ec-120">当所有事务已记录在项目上且不希望再记录任何事务时，可手动将阶段设置为 **关闭** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="2f6ec-121">当将项目设置为 **结束** 时，将无法在项目上记录任何事务，并且项目是只读的。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="2f6ec-122">跟踪项目状态</span><span class="sxs-lookup"><span data-stu-id="2f6ec-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="2f6ec-123">转到 **Project Service > 项目** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="2f6ec-124">单击要处理的项目。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="2f6ec-125">在屏幕顶部横栏中，选择项目名称旁边的向下箭头，然后单击 **项目跟踪** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="2f6ec-126">在任务列表上方的下拉列表中选择 **工作量跟踪** 或 **成本跟踪** 。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="2f6ec-127">双击任何任务以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-127">Double-click any task to edit it.</span></span> <span data-ttu-id="2f6ec-128">您还可移动甘特图中的条形或调整其大小，以更改任务的时间和进度。</span><span class="sxs-lookup"><span data-stu-id="2f6ec-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="2f6ec-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f6ec-129">See Also</span></span>  
 [<span data-ttu-id="2f6ec-130">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="2f6ec-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)