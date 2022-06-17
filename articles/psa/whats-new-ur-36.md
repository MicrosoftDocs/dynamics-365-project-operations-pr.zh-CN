---
title: Project Service Automation V3 更新版本 36 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 36 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924971"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Project Service Automation V3 更新版本 36 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 36 V3 的新增和更改的功能和修补程序。 该版本的内部版本号为 V3.10.57.152，并且在 2021 年 10 月通过自行更新公开发布。

## <a name="update-release-36"></a>更新发布 36

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**常规**
- **项目参数** 页上未正确翻译 **默认工作小时模板** 字段名称。
- 异步插件不能正确处理与 **SharedVariableService** 相关的异常。

**时间和支出**
- 如果缺少日记帐行或用户没有正确的特权来读取日记帐行，则取消项目审批时会出现错误。
- 当支出或时间条目具有多个相关项目审批时，用户无法取消审批。
- 在 **时间条目** 快速创建页面上查找时，**缺勤** 和 **休假** 被错误地翻译成中文。

**资源管理**
- 当视图模式设置为 **日**、**周** 或 **月** 时，用户无法在 **日程安排助理** 中搜索资源。
- 错误地允许普通资源具有空职位名称。 
- 作为丢单结束合同不会取消未来的预订。

**销售**
- 当环境具有大量产品时，**材料评估** 网格中的性能会降低。
- 利用模板创建项目时，项目货币不会默认为相应的项目经理合同单位。
- 实际金额并不总是与到期项目上反映的金额相匹配，或者在特定取消情况下金额变为负数。
- 将根据项目模板创建的项目关联到合同子项时会发生错误。
- 用户可以删除里程碑为 **已准备好开单** 和 **已创建发票** 的合同子项。 这应该是不允许的。
- 从项目导入估算值时，如果为报价行启用了基于任务的记帐，则报价行明细可计费性设置不正确。
- 添加固定价格记帐里程碑时，在刷新页面之前，里程碑不会反映到里程碑子网格中。
- 创建报价单名称为 Null 的项目合同时，会生成 Null 引用异常。
- 项目货币与资源货币不同的手动模式任务会导致价格估计值不正确。
- 用户无法取消已通过正确发票成功更正的交易。
- 停用的交易类别会出现在 **支出估计值** 网格中。



