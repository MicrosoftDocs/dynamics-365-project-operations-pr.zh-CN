---
title: 启用 Project Finder Mobile 应用程序功能
description: 如何启用 Project Service 的 Project Finder Mobile 应用程序功能
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132952"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="d2b53-103">启用 Project Finder Mobile 应用程序功能 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d2b53-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d2b53-104">您的资源可在其具有 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的手机上使用 Project Finder Mobile 应用程序来查找要处理的新项目和更新技能集。</span><span class="sxs-lookup"><span data-stu-id="d2b53-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="d2b53-105">此应用程序可用于 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] 手机和 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]。</span><span class="sxs-lookup"><span data-stu-id="d2b53-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="d2b53-106">您需要在部门的参数设置中设置以下几个选项以允许用户查看项目资源要求和更新其技能。</span><span class="sxs-lookup"><span data-stu-id="d2b53-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d2b53-107">Project Finder Mobile 应用程序仅使用 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]（无内部部署安装）。</span><span class="sxs-lookup"><span data-stu-id="d2b53-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="d2b53-108">转到 **Project Service > 参数**。</span><span class="sxs-lookup"><span data-stu-id="d2b53-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d2b53-109">单击您要用于允许 Project Finder Mobile 应用程序功能的参数设置。</span><span class="sxs-lookup"><span data-stu-id="d2b53-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="d2b53-110">在 **常规** 区域中，设置 **资源要求对资源可见** 为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d2b53-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="d2b53-111">将 **允许由资源进行技能更新** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d2b53-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="d2b53-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="d2b53-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="d2b53-113">这是一个全局设置。</span><span class="sxs-lookup"><span data-stu-id="d2b53-113">This is a global setting.</span></span> <span data-ttu-id="d2b53-114">项目经理可以设置单个项目是否在该项目的 **项目团队** 页面上可见。</span><span class="sxs-lookup"><span data-stu-id="d2b53-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="d2b53-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="d2b53-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="d2b53-116">电子邮件通知</span><span class="sxs-lookup"><span data-stu-id="d2b53-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="d2b53-117">将有关资源请求的电子邮件在以下时间发送给以下收件人：</span><span class="sxs-lookup"><span data-stu-id="d2b53-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="d2b53-118">收件人</span><span class="sxs-lookup"><span data-stu-id="d2b53-118">Recipient</span></span>|<span data-ttu-id="d2b53-119">重要活动</span><span class="sxs-lookup"><span data-stu-id="d2b53-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="d2b53-120">项目经理</span><span class="sxs-lookup"><span data-stu-id="d2b53-120">Project manager</span></span>|<span data-ttu-id="d2b53-121">-   当资源使用 Project Finder Mobile 应用程序注册项目时。</span><span class="sxs-lookup"><span data-stu-id="d2b53-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="d2b53-122">资源</span><span class="sxs-lookup"><span data-stu-id="d2b53-122">Resource</span></span>|<span data-ttu-id="d2b53-123">-   当资源注册的项目工作已由其他资源执行时。</span><span class="sxs-lookup"><span data-stu-id="d2b53-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="d2b53-124">-   当技能审批请求被批准或拒绝时。</span><span class="sxs-lookup"><span data-stu-id="d2b53-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="d2b53-125">-   当项目注册请求被批准或拒绝时。</span><span class="sxs-lookup"><span data-stu-id="d2b53-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="d2b53-126">隐私声明</span><span class="sxs-lookup"><span data-stu-id="d2b53-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="d2b53-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2b53-127">See Also</span></span>  
 [<span data-ttu-id="d2b53-128">设置资源</span><span class="sxs-lookup"><span data-stu-id="d2b53-128">Set up resources</span></span>](../psa/set-up-resources.md)
