---
title: 创建项目模板
description: 如何在 Project Service 中创建项目模板
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149352"
---
# <a name="create-a-project-template-project-service"></a>创建项目模板 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

如果您的公司是对类似的项目类型定期投标，项目模板将节约您的时间。 它们提供项目类型的一组标准角色和估计时间。 客户经理和项目经理可以基于项目模板创建项目，也可以复制模板和制作一个他们自己的模板。  
  
## <a name="components-of-project-template"></a>项目模板组件
 项目模板具有三个组件：  
  
- **工作分解结构**：项目模板中的工作分解结构具有与项目相同的一组元素。 您可以创建任务层次结构，将角色关联到任务，定义计划属性，设置依赖项并在甘特图中查看所有数据。 项目模板中的工作分解结构还支持各项任务的任务模式。 在创建工作计划时，项目模板和项目之间没有差异。  
  
- **项目估算**：除默认的价目表外，模板中的项目估算方式与项目中的方式相同，成本价和销售价始终是在[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]参数中定义的默认成本和销售价目表。 此功能的其他部分与项目中的功能相同。  
  
- **项目团队建立**：在为项目模板建立项目团队时，您不能在模板中预订指定的资源。 您在工作分解结构中可以使用 **生成项目团队** 来生成一套通用资源。 您还可以为通用资源指定所需的技能和专长。 您不能在项目模板中使用可预订资源替代通用资源。  
  
## <a name="create-a-project-from-a-template"></a>从模板创建项目  
 您可以按照以下方法从模板创建项目：  
  
-   在根据报价单创建一个项目时，您可以在项目快速创建窗体中选择项目模板。  
  
-   在通过单击 **新建项目** 创建项目时，项目窗体将在您保存记录前显示。 在此，您可以单击 **选取模板** 字段从您组织的预定义项目模板列表中选择模板。  
  
-   单击 **项目模板** 页上的 **从模板创建项目** 来从模板创建项目。  
  
## <a name="copying-components-of-a-template-to-a-project"></a>将模板组件复制到项目  
 在将模板组件复制到项目时，您应当了解一些事项。  
  
 **复制工作分解结构**：在从项目模板复制工作分解结构时，如果项目的项目日历与模板不同，项目日历的上班时间将应用于任务计划。 这会将计划调整为支持项目日历。 同样，工作分解结构的第一项任务获取项目的开始日期，这样任务层次结构计划的其余部分基于在模板的工作分解结构中指定的持续时间和依赖项更新。  
  
 **复制项目估算**：当您跨项目估算复制时，价目表基于成本价目表的项目和销售价目表的客户的负责部门更新。 单位成本和销售价格从与销售实体关联的项目中的这些价目表确定。  
  
 **复制项目团队**：在将项目团队从模板复制到项目时，通用资源跨在模板中定义的技能和专长并与其一起复制。 通用资源分派也与项目模板中一样进行维护。  
  
### <a name="see-also"></a>另请参阅  
 [项目经理指南](../psa/project-manager-guide.md)
