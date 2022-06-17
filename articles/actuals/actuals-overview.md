---
title: 实际值
description: 本文提供有关如何在 Microsoft Dynamics 365 Project Operations 中使用实际值的信息。
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924787"
---
# <a name="actuals"></a>实际值

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

实际值表示项目中已审阅和批准的财务和计划进度。 这些值在时间、支出以及材料使用条目、日记帐条目和发票获得批准时创建。

> [!IMPORTANT]
> 不应从系统中编辑或删除实际值。 否则，财务完整性以及与其他财务和会计系统的任何集成都可能受到不利影响。 Microsoft Dynamics 365 Project Operations 允许您使用冲销和替换实际值来编辑项目业务流程生命周期中各个点的实际值。

## <a name="recording-actuals-based-on-project-events"></a>基于项目事件记录实际值

Project Operations 会将在项目参与生命周期中发生的财务交易记录为实际值。 生命周期中不同事件的实际值创建情况各不相同，具体取决于项目参与是使用时间和材料记帐模型还是固定价格记帐模型，以及是处于售前阶段还是内部项目。

以下文章解释了不同变体的各个事件的实际值表的影响：

- [时间和材料参与中的实际值影响](ActualsonTM.md)
- [固定价格参与中的实际值影响](ActualonFP.md)
- [参与的售前阶段的实际值影响](ActualonPreSales.md)
- [内部项目的实际值影响](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
