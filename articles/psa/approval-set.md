---
title: Project Service Automation 中的审批集
description: 本主题提供有关审批集、请求和这些操作的子集的信息。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323540"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation 中的审批集

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

审批集将审批请求一起组成一个较小的操作子集。 此分组允许按项目顺序处理审批，并允许重试和排序。 对于大量审批，分组提高了审批处理的可靠性和可追溯性。

审批集指示其相关记录的整体处理状态。 在使用审批集处理审批记录时，记录会从 **已提交** 转变为 **已审批**，并且与审批集不关联。 如果记录在提交审批后失败，则记录会保持 **已提交** 状态，并且审批集会标记为失败。 审批集会记录失败的错误消息。

## <a name="processing-approvals-and-approval-sets"></a>处理审批和审批集
排队等待处理的审批在 **处理审批** 视图中可见。 系统尝试多次异步处理所有条目，包括在先前尝试失败时重试审批。

**审批集生存期** 字段记录了在将集标记为失败之前剩余的集处理尝试次数。

## <a name="failed-approvals-and-approval-sets"></a>失败的审批和审批集
**失败的审批** 视图会列出需要用户干预的所有审批。 打开关联的审批集日志以确定失败的原因。
选择 **重试** 可添加到审批集生存期计数中，将审批集重新设置为 **正在处理** 状态，并尝试处理其余记录。

## <a name="configure-approval-sets"></a>配置审批集

###  <a name="enable-the-approval-sets-feature"></a>启用“审批集”功能
在启用“审批集”功能之前，确认当前没有正在处理审批。

- 转到 **项目参数** 页并选择 **功能控制** > **启用现代审批**。

### <a name="turn-off-the-approval-sets-feature"></a>关闭“审批集”功能
在关闭“审批集”功能之前，确认当前没有正在处理审批。

- 转到 **项目参数** 页并选择 **功能控制** > **禁用现代审批**。

### <a name="configuring-the-asynchronous-threshold"></a>配置异步阈值 
创建审批集后，当选定的审批记录数超过指示的阈值时，处理会移到后台。 使用 **异步阈值** 字段配置应该同步或异步运行审批处理的时间。
有效值为：

  - 零：应异步处理所有请求。 
  - 大于零的数字：仅在提交审批数超过此值时异步处理审批。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
