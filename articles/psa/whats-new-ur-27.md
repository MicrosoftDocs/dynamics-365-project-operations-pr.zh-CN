---
title: Project Service Automation V3 更新版本 27 中的新增功能或更改
description: 本文列出了 Project Service Automation 更新版 27 V3 中提供的功能和修补程序。
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912919"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Project Service Automation V3 更新版本 27 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation V3 更新版 27 的新增和更改的功能和修补程序。 该版本的内部版本号为 V3.10.45.98，并且在 2021 年 1 月通过自行更新公开发布。

## <a name="update-release-27"></a>更新发布 27

### <a name="bug-fixes"></a>Bug 修复

**常规**

已修复以下问题：

- 由 Project Service Automation 中的插件生成的日志尚未设置为自动删除。
- 自动升级将因为 Project Service Automation 解决方案包含旧的 null NavBarArea 和 title 元素而失败。

**时间和支出**

已修复以下问题：

- **时间条目** 网格为 **时区无关** 日期行为显示了不正确数据。
- **时间条目** 网格为 **时区无关** 日期行为创建了不正确的时间。
- 任务查找不限于 **编辑时间条目** 页上的选定项目。
- 非项目时间条目的时间审批因为系统在查找项目审批者而被阻止。
- “实际值”上的正确条目显示不正确的错误消息。
- 当任务包含实际成本的 null 值，在刷新项目总计时，出现以下错误：“字典中不存在给定键”。
- 在特定情况下，**项目估算** 选项卡上的 **分组依据** 筛选器不显示支出估算。
- **夏令时** 间隔对于时间条目不正确。

**项目管理**

已修复以下问题：

- 改进了缓存，增强了与加载 **项目** 页相关的性能。
- 过时的业务规则阻止项目任务完成。
- Microsoft Project 加载项信息未遵循加载项的日历，导致资源要求不正确。
- 从模板创建项目错误地设置了分配日期，并阻止生成资源要求。
- 用户无法使用键盘访问 **类别**、**说明**、**状态** 选项。
- 项目的实际销售值不包括费用和材料销售值。
- 实际销售额和实际成本的聚合在不同汇率下会不正确。
- **默认工作时间模板** 中的说明具有误导性。
- 如果不刷新，缩进任务不删除用户界面中的 **类别**。
- 不允许忽略验证以确保将项目移到结束日期之后。

**Sales**

已修复以下问题：

- 项目报价单行上生成 null 引用异常，因为在未选择项目时，**从项目估算导入** 可见。
- 当作为 **赢单** 结束报价单时，发生以下错误：“对象引用未设置为对象的实例”。
- 从合同子项中取消链接项目过程中，未在实际冲销期间设置调整状态。
- 当同时安装了 Dynamics 365 Field Service 和 Project Service Automation 时，**发票** 页上未同时显示 **锁定定价** 和 **使用当前定价** 选项。
- 对于日语，存在与其他基于日历的页面不一致的翻译。
- **激活** 和 **停用** 已从 Project Service Automation 中的 **价目表关联** 实体中删除。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
