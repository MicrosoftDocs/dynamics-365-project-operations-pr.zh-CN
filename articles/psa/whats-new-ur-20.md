---
title: Project Service Automation V3 更新版本 20 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 20 中可用的功能和修复
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147102"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation V3 更新版本 20

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 20 中新增或更改的功能和修复。 该版本的内部版本号为 V 3.10.31.37，并且在 2020 年 6 月通过自行更新公开发布。

## <a name="update-release-20"></a>更新发布 20

### <a name="bug-fixes"></a>Bug 修复

**项目管理**

已修复以下问题：

- 如果使用需要数小时的分配方法导入项目团队成员，而指定的小时数为零，则会产生不明错误消息。
- 如果在项目任务的 **说明** 字段中输入的字符达到了最大数量，用户将收到“不正确”错误。
- 如果用户的语言设置设置为日语，**Microsoft Dynamics 365 Project Service Automation 加载项下载** 页面将重定向到英文下载页面。
- 发生服务器错误时，**项目** 窗体 **日程安排** 选项卡上的同步标签有时不会消失。
- 修改任务，正在向服务器发送冗余任务更新。

**Sales**

已修复以下问题：

- 在 **合同** 窗体中，双击 **创建发票** 会为一条实际值记录创建两张发票。
- 在 Internet Explorer 11 中，用户不能创建支出条目。
- 成本冲销和未记帐实际销售值冲销不链接。
- **项目** 窗体上的 **刷新实际值** 按钮不刷新 **任务实际工时**。
- 当 **msdyn_isgenericresourceprojectscoped** 设置为 **False** 时，**PreValidateProjectTeamMemberCreate** 创建可以创建重复的通用可预订资源。
- **重新计算** 将清除基于产品的报价单明细详细信息和合同子项详细信息的应计成本。
- 在特定情况下，**PostEstimateLineUpdate** 插件显示空引用异常错误。
- **利润率分析图表** 中的时间分段持续时间与报价单中固定价格报价单明细详细信息中的成本持续时间不匹配。
- 为 **合同子项详细信息** 和 **报价单明细详细信息** 窗体中的费用类别设置的计价单位和计价单位组的值不正确。
- **部门成本费** 列表允许时效重叠。
- 当订单类型不基于工作时，不允许用户更改 **部门**，因为这将导致空引用异常错误。
- 尝试离开 **报价单明细详细信息** 窗体回到 **报价单** 选项卡时，窗体将刷新并显示 **摘要** 选项卡。


[!INCLUDE[footer-include](../includes/footer-banner.md)]