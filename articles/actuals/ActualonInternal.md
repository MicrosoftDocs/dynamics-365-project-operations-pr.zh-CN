---
title: 内部项目的实际值影响
description: 本主题提供有关 Microsoft Dynamics 365 Project Operations 中内部项目各个事件的实际值表的影响的信息。
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579755"
---
# <a name="actuals-impact-for-an-internal-project"></a>内部项目的实际值影响

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

下表列出了在内部项目参与的各个事件中创建的不同交易类型的实际值。

| 活动 | 实际成本 | 示例 |
|---|---|---|
| 创建时间。 | 不适用 | <p>来自 Fabrikam US 部门的 Bob Kozack 的成本费率为每小时 100 美元 (USD 100)，他正在参与一个名为 "Arm Installation at Adatum" 的项目。 此项目映射到合同子项上的固定价格记帐方法。 以下是 Bob Kozak 的示例时间条目：</p><p>Bob Kozack - 8 小时</p> |
| 提交时间。 | 不适用 | 为时间条目创建成本日记帐行。 在日记帐条目中输入默认成本费率。 |
| 时间条目在批准前被撤消。 | 不适用 | |
| 时间已得到批准。 | 创建实际成本。 | <p>创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元</li></ul> |
| 取消时间审批。 | <p>原始实际成本的调整状态更新为 **已调整**。</p><p>创建调整状态为 **不可调整** 的冲销实际成本。</p> | <p>更新的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元，*已调整*</li></ul><p>为冲销先前的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，（8 小时），（800 美元），*不可调整*</li></ul> |
| 时间条目在批准后被撤消。 | <p>原始实际成本的调整状态更新为 **已调整**。</p><p>创建调整状态为 **不可调整** 的冲销实际成本。</p> | <p>更新的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元，*已调整*</li></ul><p>为冲销先前的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，（8 小时），（800 美元），*不可调整*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]