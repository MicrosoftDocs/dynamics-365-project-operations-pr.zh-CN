---
title: 创建项目
description: 如何在 Project Service 中创建项目
author: ruhercul
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
ms.openlocfilehash: 0ef83873dd902a5ace6400e373a06091280e4df5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995026"
---
# <a name="create-a-project-project-service"></a>创建项目 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

如果要为基于项目的服务创建商机、报价单或合同，请使用 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能创建项目。 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能可帮助您管理从商机到完成的一应项目事务。 创建项目时，还将创建工作分解结构，该结构可影响报价单、成本预计和资源管理。  
  
1.  转到 **Project Service > 项目**。  
  
2.  单击 **新建项目**。  
  
3.  在 **摘要** 区域中，输入项目的名称，然后尽量填写详细信息。 标有红色星号 (*) 的项为必填项。  
  
4.  单击 **保存** 创建项目，以便继续编辑。  
  
接下来将为项目创建工作分解结构，以便定义项目所需的任务、时间安排和资源角色。  

> [!NOTE]
> 在进行计划时，Project Service Automation 将采用所应用的 **工作时间** 模板的时区。 但是，在查看计划任务时，任务的开始和结束日期将以用户的时区显示。 这适用于 **项目** 窗体中的其他分时段视图。 如果用户的时区与应用于项目的工作时间模板的时区不匹配，将出现警告，说明存在差异。 
  
### <a name="see-also"></a>另请参阅  
 [项目经理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]