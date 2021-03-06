---
title: 配置发票自动创建
description: 此主题提供有关如何将系统配置为自动生成发票的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898115"
---
# <a name="configure-automated-invoice-creation"></a>配置发票自动创建

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

完成以下步骤以在 Project operations 中配置发票自动运行。

1. 转至**设置** \> **批处理作业**。
2. 创建一个批处理作业，将其命名为 **Project operations 创建发票**。 此批处理作业的名称中必须包含术语“创建发票”。
3. 在**作业类型**字段中，选择**无**。 默认情况下，**每天频率**和 **可用**选项设置为**是**。
4. 选择**运行工作流**。 在**查找记录**对话框中，您将看到三个工作流：

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. 选择 **ProcessRunCaller**，然后选择**添加**。
6. 在下一个对话框中，选择**确定**。 **Sleep** 工作流后是 **Process** 工作流。

    可以选择步骤 5 中的 **ProcessRunner**。 然后，当您选择**确定**时，**Process** 工作流后是 **Sleep** 工作流。

**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。 **ProcessRunCaller** 调用 **ProcessRunner**。 **ProcessRunner** 是真正创建发票的工作流。 它浏览必须为其创建发票的所有合同子项，然后为这些子项创建发票。 为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。 如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。 如果没有需要为其创建发票的交易，作业将跳过发票创建。

**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。 然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。 此计时器结束时，将关闭 **ProcessRunCaller**。

用于创建发票的批处理作业是周期性作业。 如果多次运行此批处理流程，将创建多个作业实例，并导致出错。 因此，仅应启动此批处理流程一次，并且仅当其停止运行时才应重新启动它。

> [!NOTE]
> 仅为按发票计划配置的项目合同子项运行批处理开票。 必须为采用固定价格记帐方法的合同子项配置里程碑。 将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。 这同样适用于基于项目的合同子项。     
