---
title: 在 Office 365 日历中管理项目和预订
description: 如何在 Office 365 日历中管理项目和预订
author: ruhercul
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
ms.openlocfilehash: 575f3c94f886d12717496445d0e6357fdc01246b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000380"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>在日历中管理项目和预订 (Project Service)

> [!Note]
> 已弃用：此功能已被弃用，无法再使用。

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

可使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历查看个人约会、项目工作预订以及现场服务工作订单分派情况。  
  
 由于所有内容汇集在一处，所以非常容易管理日常工作。 会议、约会、预订和任务全都在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历中。  
  
 如果在使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，还可以在 Project Service 时间条目视图中输入个人约会。 这样项目和资源经理就可以了解您对项目的可用性。 还可以解决时间，因为您不必输入有关个人约会的信息两次。 只需将个人约会从日历导入 Project Service 时间条目视图。  
  
 日历将同步当天到接下来四周的项目和工作订单预订情况。 不能更改此设置。  
  
 仅支持从 PSA 到 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历的单向同步。 您可以按相反的顺序进行同步。 
  
 若要了解如何使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历，请参阅 [Outlook 中的日历在网上的商用](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)。  
  
## <a name="setup"></a>设置  
 需要先进行一些设置，才能在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历中查看和管理预订。  
  
- 需要 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 全局管理员或系统管理员凭据。  
  
- 您的管理员需要配置电子邮件服务器配置文件，而每位用户则需要配置自己的邮箱。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [通过服务器端同步设置电子邮件处理](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>为组织开启同步（管理员任务）  
  
1.  在主菜单中单击 **设置** > **管理**。  
  
2.  单击 **系统设置**。  
  
3.  单击 **同步** 选项卡。  
  
4.  在 **选择是否为资源预订启用同步** 下，选中 **与 Outlook 同步资源预订**。  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>为用户配置文件开启同步（用户任务）  
  
1.  单击屏幕右上角的 **设置** 按钮。  
  
2.  单击 **选项**。  
  
3.  单击 **同步** 选项卡。  
  
4.  在 **与 Outlook 同步资源预订** 下，选中 **与 Outlook 同步资源预订**。  
  
## <a name="import-your-personal-appointments-user-task"></a>导入个人约会（用户任务）  
 可以将个人约会从日历导入 Project Service Automation 时间条目视图。  
  
1. 打开 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 日历并单击 **导入数据**。  
  
2. 在“筛选器”屏幕中，选择 **来自 Exchange 的约会**，然后单击 **应用**。  
  
3. 系统将把约会提取到时间条目视图，充当本周的建议条目。 若要添加另一周的条目，请单击 **上一周** 或 **下一周**。  
  
4. 选择要添加到 Project Service Automation 时间条目视图的约会。  
  
5. 在 **时间条目** 弹出框中，选择相应选项，以便将约会转换为 Project Service Automation 时间条目视图。  
  
6. 单击 **保存**。  
  
### <a name="see-also"></a>另请参阅  
 [时间、费用和协作指南](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]