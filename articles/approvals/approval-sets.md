---
title: 审批集
description: 本文介绍如何使用审批集、请求以及这些操作的子集。
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918071"
---
# <a name="approval-sets"></a>审批集

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

审批集将审批请求一起组成一个较小的操作子集。 此分组允许项目按特定顺序处理审批，并允许重试和排序。 对于大量审批来说，将审批请求组合到一起可以提升审批处理的可靠性和可跟踪性。

审批集指示其相关记录的整体处理状态。 使用审批集处理审批记录时，记录将从 **已提交** 转移到 **已审批**，并且不再链接到审批集。 如果记录在提交审批后失败，则记录会保持 **已提交** 状态，并且审批集会标记为失败。 审批集会记录失败的错误消息。

## <a name="processing-approvals-and-approval-sets"></a>处理审批和审批集
排队等待处理的审批在 **处理审批** 视图中可见。 系统以异步方式多次处理所有条目，包括之前尝试失败后重试审批。

**审批集生存期** 字段记录了在将集标记为失败之前剩余的集处理尝试次数。

审批集通过基于名为 **Project Service - 定期安排项目审批集** 的 **云端流** 的定期激活进行处理。 它可以在名为 **Project Operations** 的 **解决方案** 中找到。 

确保通过完成以下步骤激活流。

1. 作为管理员，登录到 [flow.microsoft.com](https://powerautomate.microsoft.com)。
2. 在右上角，切换到您用于 Dynamics 365 Project Operations 的环境。
3. 选择 **解决方案** 列出安装在环境中的解决方案。
4. 在解决方案列表中，选择 **Project Operations**。
5. 将筛选器从 **所有** 更改为 **云端流**。
6. 验证 **Project Service – 定期安排项目审批集** 流是否设置为 **开**。 如果没有，选择流，然后选择 **打开**。
7. 查看 Project Operations Dataverse 环境中 **设置** 区域中的 **系统作业** 列表，验证处理是否每五分钟进行一次。

## <a name="failed-approvals-and-approval-sets"></a>失败的审批和审批集
**未通过的审批** 视图列出了需要用户干预的所有审批。 打开关联的审批集日志以确定失败的原因。
选择 **重试** 可添加到审批集生存期计数中，将审批集重新设置为 **正在处理** 状态，并尝试处理其余记录。

## <a name="configure-approval-sets"></a>配置审批集

### <a name="enable-the-approval-sets-feature"></a>启用“审批集”功能
在启用“审批集”功能之前，确认当前没有正在处理审批。

- 转到 **项目参数** 页并选择 **功能控制** > **启用现代审批**。

### <a name="turn-off-the-approval-sets-feature"></a>关闭“审批集”功能
在关闭“审批集”功能之前，确认当前没有正在处理审批。

- 转到 **项目参数** 页并选择 **功能控制** > **禁用现代审批**。

### <a name="configuring-the-asynchronous-threshold"></a>配置异步阈值 
创建审批集后，当选定的审批记录数超过指示的阈值时，处理会移到后台。 使用 **异步阈值** 字段配置应该同步或异步运行审批处理的时间。 请选择以下值之一：

  - 零：应异步处理所有请求。 
  - 大于零的数字：仅在提交审批数超过此值时异步处理审批。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
