---
title: 确定项目成本和收入预计
description: 如何在 Project Service 中确定项目成本和收入估算
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749670"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>确定项目成本和收入预计 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

项目估算提供项目工作分解结构中预计和计划工作的财务视图。 估算视图通知您计划工作的成本和收入影响。 估算视图提供查看有关大量预定义维度的信息的一种工具，以让您最佳了解项目的财务影响。  
  
## <a name="cost-and-sales-value-of-the-project"></a>项目的成本和销售值  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]价目表定义项目所使用角色的成本和记帐费率。 根据与项目工作分解结构中任务相关的角色，您可以确定所涉及工作的成本和收入影响。  
  
## <a name="cost-price-defaulting"></a>默认成本费  
每个项目属于一个组织（在项目的**负责部门**中指示）。 与负责部门相关的价目表确定单位成本费。 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]通过在成本价目表中搜索角色、单位和部门的组合来确定角色的成本费，以获得估算明细生效日期的正确成本费。  
  
如果角色、单位和 部门的组合不导致来自负责部门价目表的成本费，则为了支持角色和部门的组合，该单位将被忽略。 如果存在成本费，此价格将转换为您在估算明细上选择的单位。  
  
如果角色和部门的组合不导致成本费，则为了支持角色和部门组合，部门将被忽略，并且如果需要，在应用任何转换后，价格为默认价格。  
  
 如果该角色没有价格，则成本费在估算明细上默认为 0.00。  
  
 项目成本估算明细上的所有成本额以负责部门的货币记帐。  
  
## <a name="sales-price-defaulting"></a>默认售价  
销售价目表基于项目被附加的销售实体。 与报价单或合同相关的销售价目表确定销售单价。 如果报价单或合同具有自定义价目表，此价目表将为项目估算的默认销售价目表。 如果与销售实体没有关联，则在参数设置中配置的默认销售价目表将为项目的默认销售价目表。 每个估算明细都具有关联的资源部门，以指示为完成任务将预订其资源的部门。 关联角色的售价通过在销售价目表中搜索角色、单位和资源部门的组合来确定，以获得估算明细生效日期的正确售价。  
  
如果角色、单位和资源部门的组合不导致销售价目表中的售价，则系统将忽略单位，并将搜索角色和资源部门的组合。 如果发现有售价，此售价将转换为您在销售估算明细上选择的单位。  
  
如果系统未发现该角色的价格，则售价在估算明细上必须默认为 0.00。  
  
估算视图具有一个网格视图，该视图显示了具有单位、总成本和售价的估算明细的平面网格。  
  
## <a name="time-phased-view-of-project-estimates"></a>项目估算的分时段视图  
在项目估算的分时段视图中，网格视图中的估算数据默认按角色透视，并显示所选时间刻度的某个时间表的一系列估算数据。  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>基于任务模式的工作量估算分配  
在分时段视图中，通过分配所选时间刻度的每单位时间的特定工作量小时数来发布任务的总估算工作量。 在 Project Service 中，任务模式确定如何在任务的持续时间内分配工作量。 这两种分配分别为均匀分配和基于工作时间的分配  
  
## <a name="work-hours-based-allocation"></a>基于工作时间的分配  
任务的自动计划任务模式管理对于任务估算的资源数，估算为每天完整工作时间要使用的资源数。 当通过在分时段视图中在任务的持续时间内进行分割来分配工作量时，上述也适用。 例如，在“天”时间刻度，对于估算通过一个资源完工的任务，每天分配的工作量将不会超过项目日历中定义的每天工作时间。 因此，工作量分配总是确保资源估计可使用一整天。  
  
## <a name="even-distribution"></a>均匀分配  
手动计划任务模式不接受任务上定义的工作时间、项目日历或资源数。 任务计划基于用户输入。 对于此类任务，所选时间刻度的每单位时间工作量分配没有任何限制因素。 任务的总工作量均匀分割并对所选时间刻度上的每单位时间进行分配。  
  
这样，在任务上定义的任务模式确定工作量分配或分时段估算中每单位时间的工作量分配。  
  
## <a name="grouping-and-time-phasing-options"></a>分组和分时段选项  
该视图可帮助您了解每天、每周、每月或每年的工作量、成本和销售估算的分配。 按选项分组允许在两个其他维度透视估算数据：类别和资源。 在网格视图和分时段视图上，您可以选择要显示的字段。 每个时间块的总值显示在底部，指示该日、周、月或年的总估算工作量、成本 和销售。  
  
成本和售价默认为生效日期—当角色的费率发生变化时，若按周查看“资源”和分时段视图中透视的估算数据时，则在分时段视图中更为明显。  
  
## <a name="expense-estimates"></a>费用估算  
项目中招致且与人力花费不直接相关的任何费用可记录在项目估算的网格视图中。 使用网格视图中的**添加费用估算**选项，可完成此操作。 可对特定的任务或整个项目记录费用估算；您可在这些行上选择费用类别，并选择费用预期发生的一个暂定日期。 如果相关成本和销售价目表具有默认价格，或为费用类别定义了加价百分比，则在关联时将为估算明细上的默认值。  
  
### <a name="see-also"></a>另请参阅  
 [项目经理指南](../project-service/project-manager-guide.md)
