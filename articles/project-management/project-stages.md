---
title: 项目阶段
description: 此主题提供 Microsoft Dynamics Project Operations 中提供的项目阶段的相关信息。
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea8b74813e8a51930a03571eab0d962e14f66a8fd6cb978d3435570a01ce5c5d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003040"
---
# <a name="project-stages"></a>项目阶段

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

项目阶段旨在反映项目在进行中的状态。 自定义项可用于通过业务流程、Power Automate 或插件扩展自动更新阶段。

默认业务流程流中定义了以下阶段：

- 新建​​
- 报价单
- 计划
- 交付
- 完成
- 结束 

## <a name="new"></a>新建​​

创建项目时，项目阶段设置为 **新建**。 如果项目是从模板创建的，则项目中可能包含计划、估算和团队数据。 否则，是项目的轮廓，并且必须输入其余组成部分。

## <a name="quote"></a>报价单

当您将项目与报价单关联或从报价单创建项目时，项目阶段设置为 **报价单**，并且估算的开始和结束日期也会更新。 当项目处于 **报价单** 阶段时，**项目实体** 页的 **销售** 选项卡显示报价单的详细信息。

## <a name="plan"></a>规划

当您获得与项目相关的报价单时，并且当项目转到 **合同** 阶段时，项目阶段将更新为 **规划**。 当项目处于 **规划** 阶段时，**项目实体** 页显示合同的详细信息。

## <a name="deliver"></a>交付

昂项目规划完成，并且您已准备好启动项目时，项目经理应该将项目阶段更新为 **交付** 以表示项目已启动。

## <a name="complete"></a>完成 

当项目的工作已完成时，项目经理可以将阶段更新为 **完成**。 项目经理可以通过将项目阶段更新为 **完成** 来指示项目已 100% 完成，但是项目仍然保持打开，以便记录任何待定时间或支出条目。

## <a name="close"></a>结束

当记录了项目的所有交易时，项目经理可以将阶段更新为 **结束**。 此时不能记录任何交易，并且项目设置为只读。



[!INCLUDE[footer-include](../includes/footer-banner.md)]