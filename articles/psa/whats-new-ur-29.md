---
title: Project Service Automation V3 更新版本 29 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 29 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010460"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Project Service Automation V3 更新版本 29 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 29 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.47.7，通过 2021 年 2 月的自动更新公开发布。

## <a name="update-release-29"></a>更新发布 29

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 用户无法在时间条目网格中看到记录在非工作日上的工作时间。
- 可以在此网格上编辑已批准的支出条目。

**项目管理**

已修复以下问题：

- 缺少验证逻辑，因此无法确保资源分派工作小时数不能为负数。
- 自定义操作 **AssignResourcesForTask** 会更新所有字段，而不是只更新已更改的字段。
- 在具有在 **CreateProject** 事件中注册的插件或工作流的环境中复制项目时，如果 **CopyWBSToProject** 失败，则不会更新 **msdyn_bulkgenerationstatus** 属性。
- 展开项目日历时，工作日未按升序排序，从而导致某些项目任务更新失败。
- 对现有项目更改项目经理会触发组织单位默认逻辑。

**销售**

已修复以下问题：

- 如果没有合同子项，则初始化过程中，**合同** 页面上的 **合同绩效** 选项卡会失败而不给出提示。