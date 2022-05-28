---
title: 确认项目供应商发票
description: 本主题说明如何在 Microsoft Dynamics 365 Project Operations 中确认项目供应商发票以及确认项目供应商发票的财务影响。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595717"
---
# <a name="confirm-a-project-vendor-invoice"></a>确认项目供应商发票

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

在 Microsoft Dynamics 365 Project Operations 中验证供应商发票上的所有行后，您可以使用确认操作来确认供应商发票。

当您在供应商发票上选择 **确认** 时，会发生以下行为：

1. 供应商发票的状态将更新为 **已确认**。
2. 确认的供应商发票及其相关记录将变为只读状态，无法编辑或删除。
3. 如果任何实际成本在匹配过程中引用供应商发票明细，与引用的供应商发票明细关联的所有实际成本都将被冲销。
4. 将使用供应商发票明细上的信息创建新实际成本。
5. 确认供应商发票后，您无法再创建更正日记帐、处理时间条目撤消或取消对已冲销的原始时间、支出或材料实际值的审批。

> [!NOTE]
> 如果供应商发票上有任何行的验证状态不是 **完成**，供应商发票将无法确认。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
