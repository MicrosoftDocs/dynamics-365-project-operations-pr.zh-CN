---
title: 确认项目供应商发票
description: 本文说明如何在 Microsoft Dynamics 365 Project Operations 中确认项目供应商发票以及确认项目供应商发票的财务影响。
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475406"
---
# <a name="confirm-project-vendor-invoices"></a>确认项目供应商发票

_ **适用于：** 面向资源/非库存场景的 Project Operations

当 **Manual confirmation by PM is required** 参数启用时，在 Microsoft Dataverse 中创建的供应商发票具有 **草稿** 状态。 以这种方式创建的供应商发票必须经过审核和手动确认。 当 **Manual confirmation by PM is required** 参数被禁用时，在 Dataverse 中创建的供应商发票将被自动确认。 无需进一步操作。 

在 Dynamics 365 Project Operations 中验证供应商发票上的所有行后，选择 **确认** 确认供应商发票。

当您在供应商发票上选择 **确认** 时，会发生以下行为：

1. 供应商发票的状态将更新为 **已确认**。
1. 确认的供应商发票及其相关记录将变为只读状态，无法编辑或删除。
1. 如果任何实际成本在匹配过程中引用供应商发票明细，与引用的供应商发票明细关联的所有实际成本都将被冲销。
1. 将使用供应商发票明细上的信息创建新实际成本。
1. 您无法再创建更正日记帐、处理时间条目撤消或取消对已冲销的原始时间、支出或材料实际值的审批。
1. 在 Dynamics 365 Finance 中，**项目成本** 值通过使用项目集成日记帐进行更新，采购集成科目在项目集成日记帐过帐后 *冲销*。

> [!NOTE]
> 如果供应商发票上有任何行的验证状态不是 **完成**，供应商发票将无法确认。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
