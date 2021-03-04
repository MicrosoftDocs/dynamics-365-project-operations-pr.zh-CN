---
title: 在 Office 365 日历中管理项目和预订
description: 如何在 Office 365 日历中管理项目和预订
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: c575bd3deba5bcde2526ccfc598327917bf91642
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144447"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="d211b-103">在日历中管理项目和预订 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d211b-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="d211b-104">已弃用：此功能已被弃用，无法再使用。</span><span class="sxs-lookup"><span data-stu-id="d211b-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="d211b-105">可使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历查看个人约会、项目工作预订以及现场服务工作订单分派情况。</span><span class="sxs-lookup"><span data-stu-id="d211b-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="d211b-106">由于所有内容汇集在一处，所以非常容易管理日常工作。</span><span class="sxs-lookup"><span data-stu-id="d211b-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="d211b-107">会议、约会、预订和任务全都在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历中。</span><span class="sxs-lookup"><span data-stu-id="d211b-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="d211b-108">如果在使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，还可以在 Project Service 时间条目视图中输入个人约会。</span><span class="sxs-lookup"><span data-stu-id="d211b-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="d211b-109">这样项目和资源经理就可以了解您对项目的可用性。</span><span class="sxs-lookup"><span data-stu-id="d211b-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="d211b-110">还可以解决时间，因为您不必输入有关个人约会的信息两次。</span><span class="sxs-lookup"><span data-stu-id="d211b-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="d211b-111">只需将个人约会从日历导入 Project Service 时间条目视图。</span><span class="sxs-lookup"><span data-stu-id="d211b-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="d211b-112">日历将同步当天到接下来四周的项目和工作订单预订情况。</span><span class="sxs-lookup"><span data-stu-id="d211b-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="d211b-113">不能更改此设置。</span><span class="sxs-lookup"><span data-stu-id="d211b-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="d211b-114">仅支持从 PSA 到 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历的单向同步。</span><span class="sxs-lookup"><span data-stu-id="d211b-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="d211b-115">您可以按相反的顺序进行同步。</span><span class="sxs-lookup"><span data-stu-id="d211b-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="d211b-116">若要了解如何使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历，请参阅 [Outlook 中的日历在网上的商用](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)。</span><span class="sxs-lookup"><span data-stu-id="d211b-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="d211b-117">设置</span><span class="sxs-lookup"><span data-stu-id="d211b-117">Setup</span></span>  
 <span data-ttu-id="d211b-118">需要先进行一些设置，才能在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历中查看和管理预订。</span><span class="sxs-lookup"><span data-stu-id="d211b-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="d211b-119">需要 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 全局管理员或系统管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="d211b-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="d211b-120">您的管理员需要配置电子邮件服务器配置文件，而每位用户则需要配置自己的邮箱。</span><span class="sxs-lookup"><span data-stu-id="d211b-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d211b-121">[通过服务器端同步设置电子邮件处理](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="d211b-121">[Set up email processing through server-side synchronization](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="d211b-122">为组织开启同步（管理员任务）</span><span class="sxs-lookup"><span data-stu-id="d211b-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="d211b-123">在主菜单中单击 **设置** > **管理**。</span><span class="sxs-lookup"><span data-stu-id="d211b-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="d211b-124">单击 **系统设置**。</span><span class="sxs-lookup"><span data-stu-id="d211b-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="d211b-125">单击 **同步** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d211b-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="d211b-126">在 **选择是否为资源预订启用同步** 下，选中 **与 Outlook 同步资源预订**。</span><span class="sxs-lookup"><span data-stu-id="d211b-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="d211b-127">为用户配置文件开启同步（用户任务）</span><span class="sxs-lookup"><span data-stu-id="d211b-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="d211b-128">单击屏幕右上角的 **设置** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d211b-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="d211b-129">单击 **选项**。</span><span class="sxs-lookup"><span data-stu-id="d211b-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="d211b-130">单击 **同步** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d211b-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="d211b-131">在 **与 Outlook 同步资源预订** 下，选中 **与 Outlook 同步资源预订**。</span><span class="sxs-lookup"><span data-stu-id="d211b-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="d211b-132">导入个人约会（用户任务）</span><span class="sxs-lookup"><span data-stu-id="d211b-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="d211b-133">可以将个人约会从日历导入 Project Service Automation 时间条目视图。</span><span class="sxs-lookup"><span data-stu-id="d211b-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="d211b-134">打开 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历并单击 **导入数据**。</span><span class="sxs-lookup"><span data-stu-id="d211b-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="d211b-135">在“筛选器”屏幕中，选择 **来自 Exchange 的约会**，然后单击 **应用**。</span><span class="sxs-lookup"><span data-stu-id="d211b-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="d211b-136">系统将把约会提取到时间条目视图，充当本周的建议条目。</span><span class="sxs-lookup"><span data-stu-id="d211b-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="d211b-137">若要添加另一周的条目，请单击 **上一周** 或 **下一周**。</span><span class="sxs-lookup"><span data-stu-id="d211b-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="d211b-138">选择要添加到 Project Service Automation 时间条目视图的约会。</span><span class="sxs-lookup"><span data-stu-id="d211b-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="d211b-139">在 **时间条目** 弹出框中，选择相应选项，以便将约会转换为 Project Service Automation 时间条目视图。</span><span class="sxs-lookup"><span data-stu-id="d211b-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="d211b-140">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d211b-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d211b-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d211b-141">See Also</span></span>  
 [<span data-ttu-id="d211b-142">时间、费用和协作指南</span><span class="sxs-lookup"><span data-stu-id="d211b-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
