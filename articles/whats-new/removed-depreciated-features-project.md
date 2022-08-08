---
title: Dynamics 365 Project Operations 中已删除或弃用的功能
description: 本文介绍 Dynamics 365 Project Operations 中已经删除或计划删除的功能。
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028318"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Dynamics 365 Project Operations 中已删除或弃用的功能

_**适用范围：** 面向资源/非库存场景的 Project Operations，精简部署 - 估价交易开票，以及面向库存/生产订单场景的 Project Operations_

本文介绍 Dynamics 365 Project Operations 中已经删除或计划删除的功能。

- *已删除* 的功能在产品中已不再可用。
- *已弃用* 的功能不在活动开发中，可能会在以后的更新中删除。

该列表旨在帮助您为自己的计划考虑这些删除和弃用。

> [!NOTE]
> [**技术参考报告**](/dynamics/s-e/global/axtechrefrep_61)中提供了有关财务和运营应用中的对象的详细信息。 可比较这些报告的不同版本，以了解财务和运营应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operations 2022 年 3 月版中删除或弃用的功能

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>项目管理和会计 "Always create adjustment transaction" 参数

| &nbsp; | &nbsp; |
|--------|--------|
| **弃用/移除的原因** | 进行审核时需要调整交易。 弃用后，此参数将处于隐藏状态。 系统将始终创建调整交易，就像当前将参数设置为 **是** 时所做的一样。 |
| **已由其他功能取代？** | No |
| **受影响的产品区域** | 应用程序 |
| **部署选项** | 面向生产/库存场景的 Project Operations |
| **状态** | 已弃用：到 2023 年 3 月 1 日，我们将隐藏此参数并更改系统行为，以始终创建调整交易。 |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>项目管理和会计 "Use adjustment date as new project date" 参数

| &nbsp; | &nbsp; |
|--------|--------|
| **弃用/移除的原因** | 此参数最初用于允许在会计期间关闭时进行调整。 但是，不再需要此参数，因为可以将交易的会计日期更改为未结期间的第一个日期（如果已配置）。 项目日期不能更改，因为它表示交易发生的日期。 |
| **已由其他功能取代？** | No |
| **受影响的产品区域** | 应用程序 |
| **部署选项** | 面向生产/库存场景的 Project Operations |
| **状态** | 已弃用：到 2023 年 3 月 1 日，我们将隐藏参数并更改系统行为，以使项目日期在调整时永远不会被更改。 |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>基于库存/生产场景的 Project Operations 的资源请求工作流

| &nbsp; | &nbsp; |
|--------|--------|
| **弃用/移除的原因** | 由于低使用率和交易量限制，已弃用。 |
| **已由其他功能取代？** | No |
| **受影响的产品区域** | 应用程序 |
| **部署选项** | 面向生产/库存场景的 Project Operations |
| **状态** | 已弃用：到 2023 年 3 月 1 日，我们将禁用使用工作流为项目请求资源的选项。 |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>没有标题和行视图的项目发票方案页面

| &nbsp; | &nbsp; |
|--------|--------|
| **弃用/移除的原因** | 已弃用，对与 **使用带有标题和行视图的项目发票方案和发票日记帐窗体** 功能键一起引入的页面进行了改进。 |
| **已由其他功能取代？** | 是 |
| **受影响的产品区域** | 应用程序 |
| **部署选项** | 生产/库存场景的 Project Operations；资源/非库存场景的 Project Operations |
| **状态** | 已弃用：到 2023 年 3 月 1 日，我们将关闭早期的（旧版）页面并默认启用 **使用带有标题和行视图的项目发票方案和发票日记帐窗体** 功能键。 |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Project Operations 2021 年 12 月版中删除或弃用的功能

### <a name="collaboration-workspaces"></a>协作工作区

[创建或链接到协作工作区（项目）](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **弃用/移除的原因** | 由于使用率较低，因此已弃用。 使用面向资源/非库存场景的 Project Operations 的客户可以利用[与 Office 组协作](../project-management/collaboration-groups.md)功能。 |
| **已由其他功能取代？** | No |
| **受影响的产品区域** | 应用程序  |
| **部署选项** | 面向生产/库存场景的 Project Operations |
| **状态** | 已弃用：2022 年 12 月 1 日，我们计划不再支持协作工作区。 |
