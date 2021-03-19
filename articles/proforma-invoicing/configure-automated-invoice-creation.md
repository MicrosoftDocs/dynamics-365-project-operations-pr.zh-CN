---
title: 配置发票自动创建
description: 此主题提供有关如何将系统配置为自动生成发票的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287902"
---
# <a name="configure-automatic-invoice-creation"></a>配置发票自动创建

_**适用于：** 面向资源/非库存场景的 Project Operations_


完成以下步骤以在 Dynamics 365 Project operations 中配置发票自动运行。

1. 转到 **设置** > **批处理作业**。
2. 创建一个批处理作业，将其命名为 **Project operations 创建发票**。 此批处理作业的名称中必须包含词语“创建发票”。
3. 在 **作业类型** 字段中，选择 **无**。 默认情况下，**每天频率** 和 **可用** 选项设置为 **是**。
4. 选择 **运行工作流**。 在 **查找记录** 对话框中，您将看到三个工作流：

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. 选择 **ProcessRunCaller**，然后选择 **添加**。
6. 在下一个对话框中，选择 **确定**。 **Sleep** 工作流后是 **Process** 工作流。

  > [!NOTE]
  > 可以选择步骤 5 中的 **ProcessRunner**。 然后，当您选择 **确定** 时，**Process** 工作流后是 **Sleep** 工作流。

**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。 **ProcessRunCaller** 调用 **ProcessRunner**。 **ProcessRunner** 是真正创建发票的工作流。 它浏览必须为其创建发票的所有合同子项，然后为这些子项创建发票。 为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。 如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。 如果没有需要为其创建发票的交易，作业将跳过发票创建。

**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。 然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。 此计时器结束时，将关闭 **ProcessRunCaller**。

用于创建发票的批处理作业是周期性作业。 如果多次运行此批处理流程，将创建多个作业实例，并导致出错。 因此，仅应启动此批处理流程一次，并且仅当其停止运行时才应重新启动它。

> [!NOTE]
> 仅为按发票计划配置的项目合同子项运行批处理开票。 必须为采用固定价格记帐方法的合同子项配置里程碑。 将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。 这同样适用于基于项目的合同子项。     


[!INCLUDE[footer-include](../includes/footer-banner.md)]