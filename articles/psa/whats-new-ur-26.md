---
title: Project Service Automation V3 更新版本 26 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 26 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: fa526e97a366c01dae2547d79d0eda2fb204e07d0f6383b991165b9eecd836e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004255"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation V3 更新版本 26

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation 更新版本 26 V3 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.44.59，通过 2020 年 12 月的自动更新公开发布。

## <a name="update-release-26"></a>更新发布 26

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 用户可以对已批准/已提交的时间条目更改任务。
- 保存时间条目时发生“未设置对象引用”错误。
- 从资源分配中导入时间条目会创建日期/时间值不正确的时间条目。
- 在安装了 Project Service Automation 和 Field Service 应用后，会针对 Field Service 应用中的时间条目在命令栏上显示两次 **新建** 按钮。
- **允许使用计价单位** 和 **计价单位组** 单元格更新现在对 **支出估算** 网格起作用。
- **更新时间条目编辑** 窗体包含 **时间线**。
- 在搜索项目审批者角色时，非项目时间条目的时间审批会阻止系统。

**资源管理**

已修复以下问题：

- 在 **PostProjectCreate** 插件中添加了验证，以在创建之前检查主要要求。
- 如果从窗体中删除字段，则 **项目团队成员** 快速创建窗体会引发 null 引用异常。
- 针对一年生成 12 小时的要求将失败。
- 改进了创建资源要求期间出现的错误消息 null 引用异常。

**项目管理**

已修复以下问题：

- 改进了验证以解决 **PreProjectUpdate** 插件中出现的 null 引用异常。
- Microsoft Project 桌面加载项发布的项目将删除未分配的工作。
- 由于 **PreValidateProjectTaskUpdate** 插件中出现 null 引用异常而在任务项目引用无效时添加了新验证。
- 团队成员网格不显示团队成员记录中的不同工作。
- 由于 **PreProjectTaskDelete** 插件中出现 null 引用异常而添加了新的验证和错误消息。

**Sales**

已修复以下问题：

- 在报价单或合同中选择基于项目的行时，**建议** 按钮应仅在选择与现有产品关联的基于产品的行时才可见。
- 从 **Create_ProjectContract** 特权中分开了 **Create_Product** 特权。
- 删除账单明细将导致 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 上出现 null 引用错误。


[!INCLUDE[footer-include](../includes/footer-banner.md)]