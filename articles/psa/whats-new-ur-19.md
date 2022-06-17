---
title: Project Service Automation V3 更新版本 19 中的新增功能或更改
description: 本文列出了 Project Service Automation 更新版 19 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915495"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation V3 更新版本 19

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 PSA V3 更新版 19 的新增和更改的功能和修补程序。 该版本的内部版本号为 V3.10.30.41，并且在 2020 年 5 月通过自行更新公开发布。

## <a name="update-release-19"></a>更新发布 19

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题： 

- 不能正确显示导入时间条目产生的错误。
- “时间条目”网格不支持 **仅限日期** 字段行为。
- 项目资源无法为项目创建支出。

**项目管理**

已修复以下问题： 

-  在完成 (EAC) 计算期间孙任务导致工作量估算不正确。

**Sales**

已修复以下问题： 

- **重新计算** 操作不支持支出合同子项详细信息或报价单明细详细信息。
- 费用估算缺少 **更新价格**。
-  客户无法从 **项目合同** 页面选择自定义合同状态描述。
- 客户在通过报价单创建自定义价目表时遇到了性能下降。
- 客户遇到了 **报价单明细详细信息** 与 **合同子项详细信息** 页中 **计价单位** 默认值不一致。
- 向应计费合同子项添加非应计费交易类别项不采用交易类别的 **非应计费** 记帐类型。
- 客户在以前创建的合同中不能使用新添加的角色和类别。
- 客户在 PreValidateProjectTeamMemberUpdate.cs 中进行不必要的检索时遇到性能下降
- 不应将 **资源类别** 列表中设置为不应计费的角色作为项目合同子项中的 **不应计费** 添加到 **应计费角色** 选项卡。
- 客户在创建项目时可能遇到性能下降，因为 **GetBookableResourceIdFromUser** 检索所有可预订资源列，而不是仅检索主 ID。
- **TransactionType** 实体缺少用于防止输入对交易类型无效的 **计价单位** 和 **计价单位组** 的前期验证更新插件。
- **删除** 步骤在导入时间条目时无效。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
