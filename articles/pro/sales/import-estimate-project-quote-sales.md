---
title: 将项目估算导入到基于项目的报价单明细 - 精简
description: 此主题提供有关如何将估算从项目导入报价单明细的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f3f18644a51d87cf3bb5b4effba2236eaf3d81a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273412"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line---lite"></a>将项目估算导入到基于项目的报价单明细 - 精简

_**适用于：** 精简部署 - 估价交易开票_

如果在预售阶段创建了项目，您可以选择将财务预估从项目导入到基于项目的报价单明细。

1. 确保基于项目的报价单明细在 **项目** 字段中有项目信息。
2. 在 **报价单明细详细信息** 选项卡上，选择 **从项目预估导入**。
3. 在打开的对话页面上，选择以下摘要选项之一。

  - **交易分类**
  - **类别**
  - **角色** 
  - **项目任务**

根据您的选择，将复制此报价单明细中包括的所有交易类的项目预估。 要检查包括哪些交易类，选择基于项目的报价单明细上的 **常规** 选项卡，并检查 **包括时间**、**包括支出** 和 **包括费用**。  若要检查所包括的任务，选择报价单明细上的 **应计费任务** 选项卡。

根据关联的任务和包括交易类，这些任务和交易类组合的所有估算将被全部导入到报价单明细。

导入预估时，系统将基于报价单所附的项目价目表和在基于项目的报价单明细上设置的计费类型默认选择定价。 如果在基于项目的报价单明细上将任务、角色或类别设置为非应计费，导入的预估明细将设置为非应计费，不会加总报价单明细的报价值。

当报价单明细包含明细详细信息时，报价单明细上的 **报价单值** 和 **预计税款** 字段将汇总，无法进行编辑。

选择多个汇总选项时，系统会尝试按所有选择的选项汇总。 结果是如果与仅选择一个汇总选项相比，导入的报价单明细的输出会更多。

例如，如果项目具有以下支出估算明细。

| 任务 | 类别 | 日期 | 数量 | 单价 | 应收总额 |
| --- | --- | --- | --- | --- | --- |
| 任务 A | 机票 | 10/1/2020 | 4 | 400 | 1600 |
| 任务 B | 酒店 | 10/1/2020 | 4 | 200 | 800 |
| 任务 C | 酒店 | 11/1/2020 | 2 | 200 | 400 |

当用户选择按交易类进行汇总时，将导入以下信息。

| 任务 | 类别 | 日期 | 数量 | 单价 | 应收总额 |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

当用户选择按交易类和类别进行汇总时，将导入以下信息。

| 任务 | 类别 | 日期 | 数量 | 单价 | 应收总额 |
| --- | --- | --- | --- | --- | --- |
| 任务 A | 机票 | 10/1/2020 | 4 | 400 | 1600 |
| | 酒店 | 10/1/2020 | 6 | 200 | 1200 |

当用户选择按交易类、类别和叶节点任务进行汇总时，将导入以下信息。 请注意，此结果与项目上的结果相同。

| 任务 | 类别 | 日期 | 数量 | 单价 | 应收总额 |
| --- | --- | --- | --- | --- | --- |
| 任务 A | 机票 | 10/1/2020 | 4 | 400 | 1600 |
| 任务 B | 酒店 | 10/1/2020 | 4 | 200 | 800 |
| 任务 C | 酒店 | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]