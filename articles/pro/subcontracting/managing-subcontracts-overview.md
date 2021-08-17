---
title: Project Operations 中的分包合同管理
description: 本主题概述了 Microsoft Dynamics 365 Project Operations 中的端到端分包合同管理流程。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994220"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations 中的分包合同管理

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Microsoft Dynamics 365 Project Operations 中的分包功能支持以下业务流程。

![分包流程](../media/SubcontractingProcessFlow.png)

以下是分包流程的分步说明。

1. 项目经理与供应商创建分包合同。 默认情况下，附加到供应商记录的价目表用于分包合同。 供应商客户具有 **供应商** 或 **提供商** 关系类型。
2. 项目经理可以将所有采购作为分包合同的行项逐项列出。 分包合同子项可以用于时间、支出或产品。 在每个分包合同子项中选择的交易分类决定了该行所用于的内容。
3. 供应商客户经理和项目经理可以迭代分包合同。 可以在附加到分包合同的采购价目表中调整定价。
4. 在流程中的此位置或稍后位置，如果分包合同子项用于时间，则供应商客户经理会将联系人与每个分包合同子项相关联。 该关联向处理分包合同的项目经理提供信息。 当联系人与分包合同子项关联时，如果可预订的资源尚不存在，系统会自动根据联系人创建可预订的资源。
5. 每个分包合同子项中的记帐方法可以是 **固定价格** 或 **时间和材料**。 对于固定价格分包合同子项，您可以设置基于里程碑的发票计划。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
