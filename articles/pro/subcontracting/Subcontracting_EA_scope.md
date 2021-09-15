---
title: 2021 年 10 月的分包抢先体验发行版
description: 本主题概述 Project Operations 中的分包功能，这些功能属于 2021 年 10 月抢先体验发行版。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383684"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>2021 年 10 月的分包抢先体验发行版

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

本主题概述 Dynamics 365 Project Operations 中的分包功能，这些功能属于 2021 年 10 月抢先体验发行版。 此功能集尚未为生产环境或实际环境做好准备，所以这些功能将一直保留在抢先体验发行版中，直到发布整个功能集。 强烈建议您在预览横幅消失前，不要对实际生产方案使用分包功能集。 

以下列表概述了 2021 年 10 月抢先体验发行版中目前提供的功能。

1. 项目经理与供应商创建分包合同。 默认情况下，附加到供应商记录的价目表用于分包合同。 供应商客户具有 **供应商** 或 **提供商** 关系类型。

2. 项目经理可以将所有采购作为分包合同的行项逐项列出。 分包合同子项可以用于时间、支出或产品。 分包合同子项的交易分类决定了子项所用于的内容。

3. 供应商客户经理和项目经理可以迭代分包合同。 可以在附加到分包合同的采购价目表中调整定价。

4. 在流程中的此位置或稍后位置，如果分包合同子项用于时间，则供应商客户经理会将供应商联系人与每个分包合同子项相关联。 该关联向处理分包合同的项目经理提供信息。 当供应商联系人与分包合同子项关联时，如果可预订的资源尚不存在，系统会自动根据联系人创建可预订的资源。

5. 每个分包合同子项中的记帐方法可以是 **固定价格** 或 **时间和材料**。 对于固定价格分包合同子项，将设置基于里程碑的发票计划。

目前不提供“概述”中概述的分包功能业务流程内的其余步骤。 随着新功能的加入，也会更新本主题。 

下图对比分包抢先体验发行版与端到端业务流程。

![分包流程](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>基于数量和基于工作的分包合同子项抢先体验发行版
在 2021 年 10 月抢先体验发行版中，仅支持基于数量的分包合同子项。 这意味着，分包合同子项可用于向供应商购买时间、支出或材料，但是不能购买所有工作。 这意味着可以在系统中的任何项目内使用分包合同子项中正在购买的数量（时间单位、支出或材料的数量）。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
