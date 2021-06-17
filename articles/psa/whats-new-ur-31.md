---
title: Project Service Automation V3 更新版本 31 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 31 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999120"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Project Service Automation V3 更新版本 31 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 31 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.52.77，通过 2021 年 5 月的自我更新正式发布。

## <a name="update-release-31"></a>更新发布 31

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- **可预订资源** 页上的时间条目控件命令按钮令人迷惑。
- 审批时间条目时，**Project.SetTrackingFields** 中生成了 null 引用异常。

**资源管理**

已修复以下问题：

- **创建团队成员** 未正确显示 **默认预订已提交状态** 的预订设置元数据设置。
- 从 PSA 1.X 升级到 3.X 时，升级流程在 **UpgradeResourceRequirements** 处失败。


**销售**

已修复以下问题：

- 实际收入将金额转换为跟踪网格中的项目货币。
- 在组织的基础货币与项目货币不同的情况下创建日记帐行、报价单明细和合同子项时，货币默认值不清楚。
- **挂起的更正日记帐验证** 查询未按项目筛选。
- 剩余销售额在项目上的计算不正确。
- 基于联系人的报价单在创建时如果没有价目表将失败。
- 处理微调框在您选择 **确认发票** 时未显示。
- 处理微调框在您选择 **创建发票** 时未显示。
- 作为丢单结束报价单时未取消预订。







