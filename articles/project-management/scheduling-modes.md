---
title: 计划模式
description: 本主题介绍计划模式。
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 41e56d01c3cfa62558b10e178085a4408a0aadb023f3f7347a61d121f542bb08
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987740"
---
# <a name="scheduling-modes"></a>计划模式

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


Dynamics 365 Project Operations 让组织能够定义他们如何管理工作分解结构内任务中关键变量的更改。 根据组织的特定需求，项目经理可以在创建项目时更改计划模式。

Project Operations 中有三个计划模式：

  - 固定持续时间（这是默认模式）
  - 固定工作量（*工作*）
  - 固定的单位

受特定计划模式的定义影响的值由以下公式确定：

  工作量 = 持续时间 x 单位

定义项目的计划模式时，您将设置以下值之一，之后此值将无法更改。 将此值保持为常数会对其赋予优先级，这会通知系统在其他两个值更改时不要更改它。 下表提供了有关选择特定模式的影响的信息。

| **在此任务中**             | **如果您修订单位**   | **如果您修订持续时间** | **如果您修订工作量**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| 固定单位任务     | 将重新计算持续时间。 | 将重新计算工作量。    | 将重新计算持续时间。 |
| 固定工作量任务    | 将重新计算持续时间。 | 将重新计算单位。    | 将重新计算持续时间。 |
| 固定持续时间任务  | 将重新计算工作量。   | 将重新计算工作量。    | 将重新计算单位。   |

有关给定模式的影响的详细信息，请参阅[更改任务类型以进行更准确地计划](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)。 在该主题中，使用的是 **工作** 一词，而不是 **工作量**。

## <a name="change-the-organizations-scheduling-mode"></a>更改组织的计划模式

完成以下步骤来定义组织的计划模式。

1. 转到 **设置**\>**常规**\>**参数**，然后选择项目参数。 
2. 在 **项目参数** 页上，为组织选择默认的计划模式，然后为项目经理定义在创建新项目时替代设置的能力。

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>更改项目上的计划模式设置

如果组织允许项目经理替代默认计划模式，项目经理可以在创建新项目时进行更改。 但是，保存项目后，将无法更改计划模式。

## <a name="copied-projects"></a>复制的项目

由于在执行复制项目操作时创建了项目，因此项目经理无法设置计划模式。 目标项目将始终默认为在组织级别定义的模式。

## <a name="copied-tasks"></a>复制的任务

将任务从一个项目复制到另一个项目时，该任务将继承目标项目的计划模式。
