---
title: Project Service Automation V3 更新版本 28 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 28 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150612"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Project Service Automation V3 更新版本 28 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

此主题列出了作为 Project Service Automation V3 更新版 28 的新增或更改功能的功能或修补程序。此版本的版本号为 V3.10.46.32，通过 2021 年 1 月的自动更新公开发布。

## <a name="update-release-28"></a>更新发布 28

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 用户可以使用 **批量编辑** 来更新已批准和提交的时间条目。

**项目管理**

已修复以下问题：

- 在将任务 GUID 解释为数字的情况下，无法使用 **工作分解结构** 页上功能区中的 **编辑任务** 打开任务进行编辑。

**Sales**

已修复以下问题：

- 调用 **GetEstimatesForProject** 插件时，生成 null 引用异常。
- 除了已更新的 **InvoiceStatus** 属性外，里程碑网格上的 **标记为已准备好开票** 仅部分更新了属性。

