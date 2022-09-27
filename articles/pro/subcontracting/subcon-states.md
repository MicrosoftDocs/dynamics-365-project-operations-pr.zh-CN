---
title: 分包合同的状态转换
description: 本文介绍创建、执行和关闭分包合同时 Microsoft Dynamics 365 Project Operations 中分包合同的状态转换。
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522875"
---
# <a name="state-transitions-on-a-subcontract"></a>分包合同的状态转换 

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

本文介绍 Microsoft Dynamics 365 Project Operations 中分包合同的状态转换。 每个状态都表示为草稿、已确认、已结束或已取消。 下图表示状态转换。

![分包合同状态模型](../media/SubconStates.png)  

下表描述了每种状态在 Project Operations 内分包合同生命周期中所表示的含意。

| 州 | 步骤 | 允许的转换 |
| --- | --- | --- |
| 草稿 | 这表示分包合同的初始状态。 正在与供应商进行谈判。 可能会修改这些行和定价。 这种状态下的分包合同可用于估算项目的资源和材料要求并按要求配备人员。 还可以在项目的时间、费用和材料使用情况中引用该状态。 可以编辑和删除处于此状态的分包合同。 | 已确认 |
| 已确认 | 这表示与供应商就定价和购买的行项目进行谈判后分包合同所处的阶段。 然而，分包资源实际上仍在交付材料和/或工作。 这种状态下的分包合同可用于估算项目的资源和材料要求并按要求配备人员。 还可以在项目的时间、费用和材料使用情况中引用该状态。 无法编辑或删除处于此状态的分包合同。 **取消** 按钮允许您取消确认的分包合同。 **重新打开** 按钮允许您重新打开分包合同，以将其重新恢复为 **草稿** 状态。 使用 **关闭** 按钮关闭确认的分包合同。 | 关闭 <br> 已取消 <br> 草稿 |
| 关闭 | 这表示分包资源实际交付材料和/或工作完成时的分包合同阶段。 这种状态下的分包合同无法再用于估算项目的资源和材料要求并按要求配备人员。 此外，也无法再在项目的时间、费用和材料使用情况中引用该状态。 无法编辑或删除处于此状态的分包合同。 | None |
| 已取消 | 这表示分包资源不再需要实际交付材料和/或工作时的分包合同阶段。 此状态下的分包合同不能用于估算项目的资源和材料要求并按要求配备人员，也不能在项目的时间、费用和材料使用情况中被引用。 无法编辑或删除处于此状态的分包合同。 | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
