---
title: 固定价格参与中的实际值影响
description: 本主题提供有关 Microsoft Dynamics 365 Project Operations 中固定价格参与生命周期中各事件的实际值表的影响的信息。
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579217"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>固定价格参与中的实际值影响

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

下表列出了在固定价格参与的各个事件中创建的不同交易类型的实际值。

| 活动 | 实际成本 | 未记帐实际销售额 | 已记帐实际销售额 | 示例 |
|---|---|---|---|---|
| 创建时间。 | 不适用 | 不适用 | 不适用 | <p>来自 Fabrikam US 部门的 Bob Kozack 的成本费率为每小时 100 美元 (USD 100)，他正在参与一个名为 "Arm Installation at Adatum" 的项目。 此项目映射到合同子项上的固定价格记帐方法。 以下是 Bob Kozak 的示例时间条目：</p><p>Bob Kozack - 8 小时</p> |
| 提交时间。 | 不适用 | 不适用 | 不适用 | 为时间条目创建成本日记帐行。 在日记帐条目中输入默认成本费率。 |
| 时间条目在批准前被撤消。 | 不适用 | 不适用 | 不适用 | |
| 时间已得到批准。 | 创建实际成本。 | 不适用 | 不适用 | <p>创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元</li></ul> |
| 取消时间审批。 | <p>原始实际成本的调整状态更新为 **已调整**。</p><p>创建调整状态为 **不可调整** 的冲销实际成本。</p> | 不适用 | 不适用 | <p>更新的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元，*已调整*</li></ul><p>为冲销先前的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，（8 小时），（800 美元），*不可调整*</li></ul> |
| 时间条目在批准后被撤消。 | <p>原始实际成本的调整状态更新为 **已调整**。</p><p>创建调整状态为 **不可调整** 的冲销实际成本。</p> | 不适用 | 不适用 | <p>更新的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元，*已调整*</li></ul><p>为冲销先前的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，（8 小时），（800 美元），*不可调整*</li></ul> |
| 确认合同。 | <p>旧实际成本的调整状态更新为 **已调整**。</p><p>创建调整状态为 **不可调整** 的冲销实际成本。</p><p>重新评估合同规则后会创建新的实际成本。</p> | 不适用 | 不适用 | <p>更新的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元，*已调整*</li></ul><p>为冲销先前的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，（8 小时），（800 美元），*不可调整*</li></ul><p>为重新评估的财务影响创建的新实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元</li></ul> |
| 创建发票。 | 不适用 | 不适用 | 不适用 | |
| 发票通过里程碑确认。 | 不适用 | 不适用 | 将创建新的基于里程碑的已记帐实际销售额。 | <p>保持不变的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元</li></ul><p>为记录已记帐销售值创建的新实际值：</p><ul><li>**已记帐实际销售额：** 里程碑 5,000 美元</li></ul> |
| 对发票进行更正以记入里程碑。 | 不适用 | 不适用 | 创建冲销已记帐实际销售额。 | <p>保持不变的现有实际值：</p><ul><li>**实际成本：** Bob Kozack，8 小时，800 美元</li></ul><p>更新的现有实际值：</p><ul><li>**已记帐实际销售额：** 里程碑 5,000 美元，*已调整*</li></ul><p>为冲销先前的已记帐销售值创建的新实际值：</p><ul><li>**已记帐实际销售额：** 里程碑（5,000 美元），*已调整*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
