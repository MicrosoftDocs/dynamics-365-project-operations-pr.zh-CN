---
title: 取消项目供应商发票
description: 本主题说明如何在 Microsoft Dynamics 365 Project Operations 中取消项目供应商发票以及取消项目供应商发票的财务影响。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580629"
---
# <a name="cancel-a-project-vendor-invoice"></a>取消项目供应商发票

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

供应商发票确认后，无法编辑或删除。 如果已确认的供应商发票有错误，您可以使用取消操作冲销供应商发票的影响并创建新的供应商发票。

当您在供应商发票上选择 **取消** 时，会发生以下行为：

1. 供应商发票的状态将更新为 **已取消**。
2. 取消的供应商发票及其相关记录将变为只读状态，无法编辑或删除。
3. 作为供应商发票确认的一部分，基于供应商发票明细创建的任何实际成本都将被冲销。
4. 如果作为匹配流程的一部分将任何实际成本链接到供应商发票明细，原始供应商发票确认会冲销成本。 在取消供应商发票期间，这些实际成本将重新创建。 来源指向时间、支出或材料使用条目。
5. 取消供应商发票后，您可以再次创建更正日记帐、处理时间条目撤消以及取消对原始时间、支出或材料实际值的审批。

> [!NOTE]
> 只有已确认的项目供应商发票可以取消。 其他状态的供应商发票不能取消。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
