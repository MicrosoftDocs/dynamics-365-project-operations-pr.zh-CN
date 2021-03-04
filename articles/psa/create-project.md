---
title: 创建项目
description: 如何在 Project Service 中创建项目
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 93958f8e7654ebc4cb038ba7ca0c5e4e02f39937
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148857"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="75ea7-103">创建项目 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="75ea7-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="75ea7-104">如果要为基于项目的服务创建商机、报价单或合同，请使用 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能创建项目。</span><span class="sxs-lookup"><span data-stu-id="75ea7-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="75ea7-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能可帮助您管理从商机到完成的一应项目事务。</span><span class="sxs-lookup"><span data-stu-id="75ea7-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="75ea7-106">创建项目时，还将创建工作分解结构，该结构可影响报价单、成本预计和资源管理。</span><span class="sxs-lookup"><span data-stu-id="75ea7-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="75ea7-107">转到 **Project Service > 项目**。</span><span class="sxs-lookup"><span data-stu-id="75ea7-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="75ea7-108">单击 **新建项目**。</span><span class="sxs-lookup"><span data-stu-id="75ea7-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="75ea7-109">在 **摘要** 区域中，输入项目的名称，然后尽量填写详细信息。</span><span class="sxs-lookup"><span data-stu-id="75ea7-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="75ea7-110">标有红色星号 (\*) 的项为必填项。</span><span class="sxs-lookup"><span data-stu-id="75ea7-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="75ea7-111">单击 **保存** 创建项目，以便继续编辑。</span><span class="sxs-lookup"><span data-stu-id="75ea7-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="75ea7-112">接下来将为项目创建工作分解结构，以便定义项目所需的任务、时间安排和资源角色。</span><span class="sxs-lookup"><span data-stu-id="75ea7-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="75ea7-113">在进行计划时，Project Service Automation 将采用所应用的 **工作时间** 模板的时区。</span><span class="sxs-lookup"><span data-stu-id="75ea7-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="75ea7-114">但是，在查看计划任务时，任务的开始和结束日期将以用户的时区显示。</span><span class="sxs-lookup"><span data-stu-id="75ea7-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="75ea7-115">这适用于 **项目** 窗体中的其他分时段视图。</span><span class="sxs-lookup"><span data-stu-id="75ea7-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="75ea7-116">如果用户的时区与应用于项目的工作时间模板的时区不匹配，将出现警告，说明存在差异。</span><span class="sxs-lookup"><span data-stu-id="75ea7-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="75ea7-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75ea7-117">See Also</span></span>  
 [<span data-ttu-id="75ea7-118">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="75ea7-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
