---
title: Project Service Automation V3 更新版本 35 中的新增功能或更改
description: 本主题列出了 Microsoft Dynamics 365 Project Service Automation 更新发行版 35, V3 中的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473254"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Project Service Automation V3 更新版本 35 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation 更新版本 35 V3 中新增或更改的功能和修复。 此版本具有内部版本号 V3.10.56.110，并且于 2021 年 9 月通过自助更新公开发布。

## <a name="update-release-35"></a>更新发布 35

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**时间和支出**

- 项目审批者在使用 **项目审批者** 角色审批支出条目时，遇到读取权限错误。
- 项目审批者使用 **项目审批者** 角色取消已审批的时间条目时，遇到了 **msdyn_projectapproval** 发生写入权限错误。
- 在适用于手机的 Dynamics 365 - 项目资源中心应用模块中的时间条目内选择 **复制周** 时，发生了以下错误：“...\OfficeProductivity_RibbonRules.js.map: HTTP 错误：状态代码 404，net::ERR_HTTP_RESPONSE_CODE_FAILURE。”
- **重试** 策略自动审批以前拒绝的条目。
- **审批集** 子网格显示不适用的功能区操作。
- **时间条目** 实体中的 **项目任务** 和 **资源角色** 缺少图标。
- 导入资源分配时，导入的时间条目中通过手动模式任务创建的分配的持续时间不正确。
- **时间条目高级查找记录** 页面中缺少 **删除**。
- **时间条目信息** 页面中缺少 **保存**。 此问题在关闭页面时阻止保存更改。

**项目规划**

- **资源分配** 和 **资源协调** 网格不按字母顺序为分组的属性排序。
- 如果日期行为自定义为 **仅限日期**，则不能创建任务。

**资源管理**

- 如果同时安装了 Dynamics 365 Field Service 和 Project Service Automation，则将 **资源要求关联视图** 与主页面关联时，将发生重叠问题。
- 双击 **团队成员快速创建** 对话框中的 **保存** 可以阻止创建资源要求。

**销售**

- 如果删除与状态为 **赢单** 的报价单关联的任务，将引发异常。
