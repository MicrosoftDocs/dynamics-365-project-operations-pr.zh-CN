---
title: 启用 Project Finder Mobile 应用程序功能
description: 如何启用 Project Service 的 Project Finder Mobile 应用程序功能
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144537"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>启用 Project Finder Mobile 应用程序功能 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

您的资源可在其具有 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的手机上使用 Project Finder Mobile 应用程序来查找要处理的新项目和更新技能集。  
  
 此应用程序可用于 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] 手机和 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]。  
    
 要允许用户查看项目资源要求和更新技能，必须在部门的参数设置中选择选项。
  
> [!NOTE]
>  Project Finder Mobile 应用程序仅使用 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]（无内部部署安装）。  
  
1. 转到 **Project Service > 参数**。  
  
2. 单击您要用于允许 Project Finder Mobile 应用程序功能的参数设置。  
  
3. 在 **常规** 区域中，设置 **资源要求对资源可见** 为 **是**。  
  
4. 将 **允许由资源进行技能更新** 设置为 **是**。  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   这是一个全局设置。 项目经理可以设置单个项目是否在该项目的 **项目团队** 页面上可见。  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>电子邮件通知  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 将有关资源请求的电子邮件在以下时间发送给以下收件人：  
  
|收件人|重要活动|  
|---------------|-----------|  
|项目经理|- 资源使用 Project Finder Mobile 应用注册项目。|  
|资源|- 资源注册的项目工作已由其他资源执行。<br />- 技能审批请求被批准或拒绝。<br />- 项目注册请求被批准或拒绝。|  
  
## <a name="privacy-notice"></a>隐私声明  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>另请参阅  
 [设置资源](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]