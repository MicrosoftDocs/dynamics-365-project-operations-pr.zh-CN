---
title: 为项目安排资源
description: 如何在 Project Service 中为项目安排资源
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150432"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="9d703-103">为项目安排资源 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9d703-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9d703-104">可以检查资源可用性以概览资源的预订情况，也可以按技能、团队、位置和其他选项筛选视图。</span><span class="sxs-lookup"><span data-stu-id="9d703-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="9d703-105">日程安排板显示资源列表及资源可用性。</span><span class="sxs-lookup"><span data-stu-id="9d703-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="9d703-106">选择视图模式将按 **小时**、**日**、**周** 或 **月** 显示可用性。</span><span class="sxs-lookup"><span data-stu-id="9d703-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="9d703-107">使用日程安排板之前，请务必设置该板。</span><span class="sxs-lookup"><span data-stu-id="9d703-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="9d703-108">有关详细信息，请参阅[配置日程安排板（Field Service 或 Project Service Automation）](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board)。</span><span class="sxs-lookup"><span data-stu-id="9d703-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="9d703-109">如果在使用早期版本，并且需要了解资源可用性，请参阅[查看资源可用性](../psa/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="9d703-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="9d703-110">若要使用日程安排板的预订功能、地理编码和位置服务，需要开启地图。</span><span class="sxs-lookup"><span data-stu-id="9d703-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="9d703-111">在主菜单中，选择 **资源计划** > **管理**。</span><span class="sxs-lookup"><span data-stu-id="9d703-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="9d703-112">单击 **计划参数**。</span><span class="sxs-lookup"><span data-stu-id="9d703-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="9d703-113">打开记录，向下滚动到 **Resource Scheduling Optimization** 部分。</span><span class="sxs-lookup"><span data-stu-id="9d703-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="9d703-114">在 **连接到地图** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9d703-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="9d703-115">接受条款并保存记录。</span><span class="sxs-lookup"><span data-stu-id="9d703-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="9d703-116">在主菜单中，选择 **Project Service** > **日程安排板**。</span><span class="sxs-lookup"><span data-stu-id="9d703-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="9d703-117">可在此处通过多种方法手动安排预订要求。</span><span class="sxs-lookup"><span data-stu-id="9d703-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="9d703-118">选择适合您的方法。</span><span class="sxs-lookup"><span data-stu-id="9d703-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="9d703-119">查找可用资源</span><span class="sxs-lookup"><span data-stu-id="9d703-119">Find available resources</span></span>

1.  <span data-ttu-id="9d703-120">在 **预订要求** 列表中右键单击未安排的预订并选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="9d703-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="9d703-121">选择 **查找可用性 - 当前资源**，以便从日程安排板中的资源列表查找可用资源。</span><span class="sxs-lookup"><span data-stu-id="9d703-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="9d703-122">选择 **查找可用性 - 所有资源**，以便从系统中的资源查找可用资源</span><span class="sxs-lookup"><span data-stu-id="9d703-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="9d703-123">执行此操作时，筛选器将显示所选预订要求的选项。</span><span class="sxs-lookup"><span data-stu-id="9d703-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="9d703-124">看到可用时隙时，在日程安排板中右键单击该时隙，然后选择 **在此处预订**。</span><span class="sxs-lookup"><span data-stu-id="9d703-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="9d703-125">或者将预订要求拖放到可用时隙。</span><span class="sxs-lookup"><span data-stu-id="9d703-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="9d703-126">使用日视图预订资源并查找已预订人员</span><span class="sxs-lookup"><span data-stu-id="9d703-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="9d703-127">在日程安排板中，选择 **视图模式**，然后选择 **日**。</span><span class="sxs-lookup"><span data-stu-id="9d703-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="9d703-128">下面显示一个网格视图，该视图中是某个资源按天预订了多少小时，哪些天有空。</span><span class="sxs-lookup"><span data-stu-id="9d703-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="9d703-129">单击要预订的资源的名称，然后选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="9d703-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="9d703-130">在 **资源预订（创建）** 对话框中，选择要为其预订资源的项目，以及预订方法和开始及结束时间。</span><span class="sxs-lookup"><span data-stu-id="9d703-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="9d703-131">完成后，选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="9d703-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="9d703-132">查看日程安排板</span><span class="sxs-lookup"><span data-stu-id="9d703-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="9d703-133">从底部的列表中选择未安排的预订要求。</span><span class="sxs-lookup"><span data-stu-id="9d703-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="9d703-134">将预订要求拖到日程安排板中的可用资源/时隙。</span><span class="sxs-lookup"><span data-stu-id="9d703-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="9d703-135">完成后，选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="9d703-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="9d703-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="9d703-136">Additional resources</span></span>  
 [<span data-ttu-id="9d703-137">资源经理指南</span><span class="sxs-lookup"><span data-stu-id="9d703-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
