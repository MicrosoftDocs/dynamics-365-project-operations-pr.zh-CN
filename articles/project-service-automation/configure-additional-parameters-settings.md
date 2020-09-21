---
title: 配置其他参数设置
description: 如何在 Project Service 中配置其他参数设置
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749798"
---
# <a name="configure-additional-parameter-settings-project-service"></a>配置其他参数设置 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

一旦您在之前主题中配置了项目，您需要设置其他项目参数以使用项目。 首次安装 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时，您创建了参数设置以首先创建运行 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 所需的所有记录。 现在是时间返回并为这些设置配置其他字段。  
  
 您需要已经配置了以下设置：  
  
-   部门  
  
-   发票频率  
  
-   工作时间模板  
  
-   价目表  
 
在此步骤中，您还可以指出所需的资源分配类型：  
  
- **中心**。 只有资源经理可以将资源分配到项目中。  
  
- **混合**。 资源经理、项目经理和客户经理可以将资源分配到项目中。  
  
 
设置项目参数：  
  
1. 转到 **Project Service > 参数**。  
  
2. 单击要配置的参数设置（首次安装 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时创建的参数设置），或单击**新建**新建一个。  
  
3. 在**常规**区域，为您的项目参数设置所有选项。  
  
4. 在**价目表**区域中，单击 **+** 添加价目表，在**项目参数价目表**下拉列表中选择价目表，然后单击**保存**。  
  
5. 在屏幕右下角，单击**保存**按钮。  

> [!NOTE]
> 若要使 Project Service 能够正常运行，必须维护项目参数记录。 不应删除该记录。

### <a name="see-also"></a>另请参阅  
 [设置资源](../project-service/set-up-resources.md)
