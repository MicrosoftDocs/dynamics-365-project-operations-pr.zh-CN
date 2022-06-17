---
title: 2022 年 2 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2022 年 2 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922809"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>2022 年 2 月新增功能 - Project Operations 精简部署

_适用范围：精简部署 - 估价交易开票_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.28.0.120

## <a name="features-included-in-this-release"></a>此版本中包括的功能

在此版本开始，您最多可以将 300 个团队成员添加到单个项目中。 之前，对团队成员数量的限制是 150。 有关详细信息，请参阅[项目限制](../../project-management/create-wbs.md#project-limitations)。

## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2497369 | 材料更正必须遵从 **更正** 参数中的日期值。 |
| 计费和定价 | 2498697 | 改进了 **时间条目撤消** 的安全配置。 |
| 计费和定价 | 2517455 | 不允许 **刷新发票明细交易** 操作针对同一个发票同时触发多次。 |
| 计费和定价 | 2517465 | **停用发票明细详细信息** 操作由于不受支持被阻止。 |
| 计费和定价 | 2556660 | 修复了对附加到项目参数记录的价目表进行的时效检查。 |
|   商机管理 | 2369202 | 更正了验证具有重叠生效日期的价目表能否附加到同一项目合同的业务逻辑。 |
|   商机管理 | 2385965 | 更正了选择 **保存并关闭** 时 **项目合同** 页面的 **客户** 选项卡上的行为。 |
