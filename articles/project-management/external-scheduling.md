---
title: 外部计划
description: 本文介绍外部计划。
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736955"
---
# <a name="external-scheduling"></a>外部计划

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

外部计划模式允许您本地创建、更新和删除与工作分解结构 (WBS) 相关的实体，但不受 Microsoft Project for the Web 执行的当前限制的约束。 它还提供有限的验证。 此模式只能由以下客户使用：

- 具有在 Project Operations 提供的计划逻辑之外定义 WBS 所需工具的客户
- 必须管理计划层次结构、依赖关系或任务持续时间的客户

> [!IMPORTANT]
> 未在 WBS 相关实体中正确输入的数据可能无法在资源协调网格、估算网格、跟踪网格或资源分配网格中呈现。

## <a name="configuration"></a>Configuration

本功能默认启用。 但是，在项目现成可用的主页上，相关字段默认不可见。 要启用此字段，在 Maker portal 中，打开项目实体的主页，选择 **计划引擎** 字段，然后将此字段更改为 **默认情况下可见**。 如果您不使用现成可用的项目主页，编辑现有页面，在其中添加 **计划引擎** 字段。

## <a name="settings"></a>设置

要使用外部计划模式，您必须首先创建一个新项目，并在项目主页的下拉列表中选择 **外部计划** 计划引擎。 为项目设置此模式后，将无法更改。

## <a name="viewing-the-wbs"></a>查看 WBS

如果项目是外部计划的，该项目对 Project for the Web 的访问将受到限制。 要查看 WBS，您必须转到跟踪网格，其中会显示完整的 WBS。

## <a name="creating-and-editing-the-wbs"></a>创建和编辑 WBS

如果为项目启用了外部计划，您必须为所有与 WBS 相关的实体定义数据，包括任务、团队成员、资源分配和依赖项。

下图显示了项目计划的数据模型。

![项目计划数据模型。](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>功能限制

不允许在外部计划的项目上执行以下操作。

### <a name="project-planning"></a>项目规划

- **复制项目** – 外部计划项目不支持此操作。
- **移动项目** – 对项目开始日期的更改不会移动 WBS 中任务或资源分配的开始。
- **更新项目经理** – 在项目转换之前，对项目主页上的项目经理所做的更改不会自动创建新的项目团队成员。
- **更新项目的工作时间模板** – 对项目的工作时间模板的更改不会重新计算项目的计划。
- **资源分配信息** – 创建资源分配不会自动更新 **mdyn\_PlannedWork** 字段。 此字段用于存储资源分配工作的信息。 如果在资源分配网格或资源协调网格中显示分时段的工作，您必须定义有效的资源分配信息。 这些信息必须正确设置格式，以触发成本信息和销售价格信息的计算。 我们建议您创建 Project for the Web 计划的测试项目，然后查看相关数据，确认要求和格式。

### <a name="resource-management"></a>资源管理

- **常规资源履行** – 外部计划项目不支持常规资源履行。 尝试履行活动的未满足要求将创建新的项目团队成员，但不会删除通用团队成员或替换任何现有资源分配中的通用团队成员。
- **删除团队成员** – 删除团队成员不会自动删除资源分配。

### <a name="quoting-and-contracting"></a>报价与合同签订

- **导入报价单明细和合同子项详细信息** – 从项目导入报价单明细和合同子项详细信息时，应用程序已经过测试，在 WBA 中最多只能支持 500 个任务，每个任务最多只能支持 20 个分配。

### <a name="actuals-and-invoicing"></a>实际值和开票

- 虽然 WBS 和财务交易之间的现有验证没有变化，但您必须遵从现成的数据模型，以确保所有下游交易按预期运行。
