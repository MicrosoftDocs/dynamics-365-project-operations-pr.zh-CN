---
title: 供应商发票的状态转换
description: 本主题介绍 Microsoft Dynamics 365 Project Operations 中供应商发票的状态转换。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584677"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>供应商发票的状态转换

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

本主题介绍 Microsoft Dynamics 365 Project Operations 中供应商发票的状态转换。 使用以下状态：**草稿**、**审阅中**、**已确认**、**暂停** 和 **已取消**。

下图显示了状态转换。

![分包合同状态转换模型。](../media/VI_State_Model.jpg)

下表说明了每种状态在 Project Operations 内供应商发票生命周期中所表示的含意。

| 州 | 说明  | 允许的转换 |
| --- | --- | --- |
| 草稿 | 此状态是供应商发票的初始状态。 可能会修改这些行和定价。 此状态的供应商发票无法编辑和删除。 | 正在进行 |
| 审阅中 | 此状态表示供应商发票的处理状态。 至少有一个供应商发票明细的验证状态为 **正在进行**。 | 已确认、暂停 |
| 已确认 | 此状态表示应用程序已为每个供应商发票明细创建实际成本的供应商发票的阶段。 与供应商发票明细匹配的任何链接实际成本已被冲销并替换为来自这些供应商发票明细的实际成本。 此状态的供应商发票无法编辑或删除。 您可以使用 **取消** 按钮取消已确认的供应商发票。 “取消”操作将冲销“确认”操作的影响。 | 已取消 |
| 暂停 | <p>此状态表示供应商发票的一个阶段：由于发票或供应商状态存在问题，供应商发票无法移动。 此状态的供应商发票无法确认、取消、编辑或删除。</p><p>您可以使用重新打开操作将供应商发票移到 **草稿** 或 **审阅中** 状态。 如果供应商发票上至少有一行的验证状态为 **正在进行** 或 **完成**，供应商发票将以 **审阅中** 状态重新打开。 如果供应商发票上的所有行的验证状态均为 **未开始**，供应商发票将以 **草稿** 状态重新打开。</p> | 草稿、审阅中 |
| 已取消 | 此状态表示分包资源不再需要实际交付材料和/或工作的分包合同阶段。 此状态下的分包合同不能用于估算项目的资源和材料要求并按要求配备人员，也不能在项目的时间、支出和材料使用中被引用。 无法编辑或删除处于此状态的分包合同。 | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]