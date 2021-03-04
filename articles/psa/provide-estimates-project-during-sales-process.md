---
title: 在销售流程中提供项目的工作估计
description: 如何在 Project Service 中的销售流程中提供项目的工作估计
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147957"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>在销售流程中提供项目的工作估计 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

在销售流程期间，您可以使用报价单明细从新执行销售估计。 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能提供更科学、更确定性的进行销售估计的方法，此方法是通过划分工作项，并关联参与工作分解结构中项目的估计的相关属性来执行。  
  
 一旦您赢得销售，您可以在项目计划中使用关联的工作分解结构，并根据项目成功完成的需要进行调整。  
  
## <a name="link-a-project-to-a-quote-line"></a>链接项目到报价单明细  
 如果创建基于项目的报价单明细，您可以从报价单明细创建一个新项目。 然后可以使用项目模板，其可以是您的组织常用的预配置的标准项目计划和财务估计，也可以是过去项目的项目计划副本和估计。 在创建项目时，选择项目模板将提供调整项目计划、估计和角色要求的基础。 通过从报价单创建项目，项目将自动与报价单明细关联。  
  
## <a name="project-estimate-components"></a>项目估计组件  
 项目的工作分解结构提供将工作分解到任务，维护任务层次结构，以及分派完成每项任务所需的工作估计的方法。 您还可以将角色分派到任务以指示完成任务和计划所需的资源类型的估计。  
  
 工作分解结构帮助您确定工作任务和计划估计。 默认情况下，项目使用您之前定义的默认价目表。 在价目表中定义的成本和销售价格帮助确定项目的工作分解的财务估计。  
  
 如果项目与报价单关联，报价单将具有不同的默认价目表，报价单的价目表将用于财务估计。  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>将估计从项目导入到报价单  
 当您的项目中有项目估计后，您可以将这些估计导入到报价单明细：  
  
-   在 **报价单明细详细信息** 中，单击 **从估计导入**。 

-   选择是否导入按交易类型、角色或工作分解结构节点级别汇总的项目估计。  
  
### <a name="see-also"></a>另请参阅  
 [项目经理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]