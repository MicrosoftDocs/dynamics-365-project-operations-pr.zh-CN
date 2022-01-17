---
title: 分包合同的状态转换
description: 本主题介绍创建、执行和关闭分包合同时 Microsoft Dynamics 365 Project Operations 中分包合同的状态转换。
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903343"
---
# <a name="state-transitions-on-a-subcontract"></a>分包合同的状态转换 

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

本主题介绍 Microsoft Dynamics 365 Project Operations 中分包合同的状态转换。 每个状态都表示为草稿、已确认、已结束或已取消。 下图表示状态转换。

![分包合同状态模型](../media/SubconStates.png)  

下表描述了每种状态在 Project Operations 内分包合同生命周期中所表示的含意。

| 州 | 步骤 | 允许的转换 |
| --- | --- | --- |
| 草稿 | 这表示分包合同的初始状态。 正在与供应商进行谈判。 可能会修改这些行和定价。 这种状态下的分包合同可用于估算项目的资源和材料要求并按要求配备人员。 还可以在项目的时间、费用和材料使用情况中引用该状态。 可以编辑和删除处于此状态的分包合同。 | 已确认 |
| 已确认 | 这表示与供应商就定价和购买的行项目进行谈判后分包合同所处的阶段。 然而，分包资源实际上仍在交付材料和/或工作。 这种状态下的分包合同可用于估算项目的资源和材料要求并按要求配备人员。 还可以在项目的时间、费用和材料使用情况中引用该状态。 无法编辑或删除处于此状态的分包合同。 **取消** 按钮允许您取消确认的分包合同。 **重新打开** 按钮允许您重新打开分包合同，以将其重新恢复为 **草稿** 状态。 使用 **关闭** 按钮关闭确认的分包合同。 | 关闭 <br> 已取消 <br> 草稿 |
| 关闭 | 这表示分包资源实际交付材料和/或工作完成时的分包合同阶段。 这种状态下的分包合同无法再用于估算项目的资源和材料要求并按要求配备人员。 此外，也无法再在项目的时间、费用和材料使用情况中引用该状态。 无法编辑或删除处于此状态的分包合同。 | None |
| 已取消 | 这表示分包资源不再需要实际交付材料和/或工作时的分包合同阶段。 此状态下的分包合同不能用于估算项目的资源和材料要求并按要求配备人员，也不能在项目的时间、费用和材料使用情况中被引用。 无法编辑或删除处于此状态的分包合同。 | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
