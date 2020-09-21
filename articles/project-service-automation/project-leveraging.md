---
title: 销售额估算和项目
description: 此主题介绍如何在销售流程中利用计划和估算。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749683"
---
# <a name="sales-estimates-and-projects"></a>销售额估算和项目

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

销售流程中，可通过将项目链接到销售报价单来创建销售额估算。 这样，就可以在销售流程中进行临时估算，以利用项目计划和估算产能。 如果销售通过，可将用于销售估算目的的计划用作进一步优化项目计划的基础。

## <a name="linking-a-project-to-a-quote-line"></a>将项目链接到报价单明细

创建基于项目的报价单明细时，可在**报价单明细**页中创建新项目或关联现有项目。 

> ![“报价单明细”窗体](media/project-8.png)
 
基于报价单明细详细信息创建新项目时，可利用项目模板。 项目模板是用于表示组织中的典型标准项目计划和财务估算的模型项目。 也可以表示来自过去项目的项目计划和估算的副本。

> ![报价单明细详细信息](media/project-9.png)
  
基于报价单创建项目时，项目将自动与报价单明细关联。

## <a name="components-of-estimates-in-a-project"></a>项目中的估算的组件

可通过计划将工作拆分为任务，维护任务层次结构，确定需要哪些资源才能完成任务，以及分派完成任务所需工作量的估算。

可通过使用**项目**页的**计划**选项卡上的字段定义工作量和计划估算。 因为价目表与项目关联，所以使用在价目表中定义的成本和销售价计算财务估算。

## <a name="importing-estimates-from-a-project-into-a-quote"></a>将估计从项目导入到报价单

定义项目估算之后，可将其导入报价单明细中。 在**报价单明细详细信息**页中，选择功能区中的**从估算导入**以按交易类型、角色或任务级别汇总项目估算。
