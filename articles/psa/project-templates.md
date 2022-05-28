---
title: 项目模板
description: 此主题介绍如何使用项目模板快速设置项目。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: aff6fc5bb855fe1e9007933fdc1a88eb020da0ad
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586011"
---
# <a name="project-templates"></a>项目模板 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

项目模板是一种预定义的框架，可帮助您快速、轻松地启动项目。 单击一次，即可使用预定义的模板创建新项目。 至于项目，必须为项目模板定义先决条件。 必须为每个项目模板定义项目日历，并且必须在组织中预定义角色和价目表，因此模板的组件中包含有用的数据。

项目模板有三个组件组成：计划、项目估算和项目团队成员。

## <a name="schedule"></a>Schedule

项目模板中的计划与项目中的计划拥有同一组元素。 您可以创建任务层次结构，将角色与任务关联，定义计划属性，以及设置依赖项。 项目模板中的计划也支持每个任务拥有任务模式。 因此，支持计划引擎。 必须将项目日历与项目关联。 创建工作计划时，项目模板和项目之间没有差异。

## <a name="project-estimates"></a>项目估算

项目模板中的项目估算与项目中的项目估算的工作方式相同。 但是，将从参数中定义的默认成本和销售价目表提取成本和销售价。

## <a name="creating-a-project-from-a-template"></a>从模板创建项目
 
可通过多种方法从项目模板创建项目：

- 在根据报价单创建项目时，您可以在 **快速创建: 项目** 窗体中选择项目模板。

> ![“快速创建: 项目”对话框。](media/project-11.png)

- 通过选择 **新建项目** 创建项目时，保存记录之前将显示 **项目** 页。 在 **选取模板** 字段中，选择组织中的一个预定义项目模板。
- 使用 **模板实体** 页上的 **从模板创建项目**。

## <a name="copying-components-of-template-to-project"></a>将模板组件复制到项目

将项目模板的组件复制到项目时，可能进行一些替代，具体取决于项目中的设置。

### <a name="copying-the-schedule"></a>复制计划

在从项目模板复制计划时，如果项目的项目日历与模板不同，项目日历的工作时间将应用于任务计划。 这样，将调整计划以匹配基础项目日历。 同样，计划的第一项任务获取项目的开始日期，并基于在模板中指定的持续时间和依赖项更新层次结构其余部分的计划。 

### <a name="copying-project-estimates"></a>复制项目估算 

在项目估算明细之间进行复制时，将更新价目表。 对于成本价目表，这些更新基于项目的负责单位。 对于销售价目表，则基于客户。 对于与销售实体关联的项目，单位成本和销售价根据这些价目表确定。

### <a name="copying-a-project-team"></a>复制项目团队

在将项目团队从项目模板复制到项目时，通用资源与模板中定义的技能和专长一起复制。 通用资源分派也与项目模板中一样进行维护。 项目模板中不支持指定资源。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
