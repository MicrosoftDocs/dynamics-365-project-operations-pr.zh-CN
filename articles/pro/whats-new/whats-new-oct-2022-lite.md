---
title: 2022 年 10 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2022 年 10 月版 Microsoft Dynamics 365 Project Operations 精简部署中可用的质量更新的信息。
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806597"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>2022 年 10 月新增功能 - Project Operations 精简部署

_**适用于：** 精简部署 - 估价交易开票_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.57.0.176

## <a name="features-included-in-this-release"></a>此版本中包括的功能

| 功能区域 | 功能名称 | 详细信息 |
| --- | --- | --- |
| 项目规划和跟踪 | **Project Operations 外部计划**<br>外部计划模式允许客户使用本地 Dataverse API 在本地创建、更新和删除与工作分解结构 (WBS) 相关的实体，但不受 Project for the Web 执行的当前限制的约束。 | [外部计划](/dynamics365/project-operations/project-management/external-scheduling) |
| 部署和配置 | <p>**允许客户选择部署类型**<br>当环境中安装了双重写入核心和业务流程解决方案时，Project Operations 的产品驱动更新 (PDU) 用于自动安装 Project Operations 双重写入解决方案。</p><p>此功能在项目参数中引入了一个新的 **解决方案升级行为** 参数。 当此参数设置为 **仅 Lite** 时，即使环境中安装了双重写入核心和业务流程解决方案，PDU 也不再自动安装 Project Operations 双重写入解决方案。 如果客户计划使用双重写入解决方案将销售订单集成到财务和运营应用中，但希望在 Lite 模式下使用 Project Operations（即不集成到财务和运营应用中），则此行为将使他们受益。</p> | |

## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2316317 | 系统允许创建没有应计费交易的发票。 |
| 计费和定价 | 2737300 | 访问窗体之前验证“客户”字段的可用性。 |
| 计费和定价 | 2744948 | 为计费方法添加 Null 检查。 |
| 计费和定价 | 2763515 | 缺少发票销售合同时的 Null 引用错误处理。 |
| 计费和定价 | 2844301 | 由于出现错误，批量发票创建失败。 |
| 计费和定价 | 2845869 | 组织服务存储不正确。 |
| 计费和定价 | 2853729 | 修改计费类型后，角色和价格详细信息将更新。 |
| 计费和定价 | 2940350 | 对实际项进行定价后，只应自动输入活动价目表。 |
| 部署和配置 | 3001206 | msdyn\_replaylogheader 实体阻止升级客户组织。 |
| 商机管理 | 2755582 | 拆分计费规则帮助程序中和 Null 引用异常处理。 |
| 商机管理 | 2761477 | 使用拆分计费时，删除里程碑（标题）会保留孤立的里程碑。 |
| 商机管理 | 2767595 | 在主窗体中打开资料使用情况记录时，该记录的可预订资源会更改为当前登录用户。 |
| 项目规划和跟踪 | 2790384 | 待定 OperationSet 超时过短。 |
| 资源管理 | 2751560 | 资源要求中的首选组织单位不一致。 |
| 转包 | 2907231 | 供应商发票的流程阶段无法推进。 |
| 时间和支出 | 2867363 | 当记录排队等待批准时，它们不会从“待审批的缺勤/休假”视图中消失。 |
| 时间和支出 | 2894405 | TESA：未使用的 POC 目录将导致合规性问题。 |
