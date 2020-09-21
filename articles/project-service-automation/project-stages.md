---
title: 项目阶段
description: 本主题提供有关项目阶段的信息。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749679"
---
# <a name="project-stages"></a>项目阶段 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

项目进行中，将更新项目阶段以体现项目的状态。 默认业务流程将自动更新项目的某些阶段，而其他阶段则由项目经理手动更新。 

默认 BPF 中定义了以下阶段：

- 新建
- 报价单
- 规划
- 交付
- 完成
- 结束 

## <a name="new"></a>新建

创建项目时，项目阶段设置为**新建**。 如果项目是从模板创建的，则项目中可能包含计划、估算和团队数据。 否则，只是项目的轮廓，并且必须输入其余组成部分。

## <a name="quote"></a>报价单

当您将项目与报价单关联或从报价单创建项目时，项目阶段设置为**报价单**，并且估算的开始和结束日期也会更新。 当项目处于**报价单**阶段时，**项目实体**页的**销售**选项卡显示报价单的详细信息。

## <a name="plan"></a>规划

当您获得与项目相关的报价单时，并且当项目转到**合同**阶段时，项目阶段将更新为**规划**。 当项目处于**规划**阶段时，**项目实体**页显示合同的详细信息。

## <a name="deliver"></a>交付

昂项目规划完成，并且您已准备好启动项目时，项目经理应该将项目阶段更新为**交付**以表示项目已启动。

## <a name="complete"></a>完成 

当项目的工作已完成时，项目经理可以将阶段更新为**完成**。 项目经理可以通过将项目阶段更新为**完成**来指示项目已 100% 完成，但是项目仍然保持打开，以便记录任何待定时间或支出条目。

## <a name="close"></a>结束

当记录了项目的所有交易时，项目经理可以将阶段更新为**结束**。 此时不能记录任何交易，并且项目设置为只读。
