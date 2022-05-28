---
title: Project Service Automation V3 更新版本 34 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 34 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588679"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Project Service Automation V3 更新版本 34 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 34 中新增或更改的功能和修复。 此版本具有内部版本号 V3.10.55.38，并且于 2021 年 7 月通过自助更新公开发布。

## <a name="update-release-34"></a>更新发布 34

### <a name="bug-fixes"></a>Bug 修复
已修复以下问题。

**常规**

- 发布者驱动的更新不会激活新的现代审批工作流。
- **审批集** 主页上缺少 **目标状态** 和 **操作类型** 属性。

**时间和支出**

- 无法使用现代审批流审批撤消请求。
- 复制与登录用户无关的条目时，复制一周的时间条目不起作用。

**项目规划**

- 从 Microsoft Project 桌面加载项导入时，资源分配概况已损坏。

**资源管理**

- 当您从 Microsoft Project 桌面客户端加载项发布项目时，现有要求的结束日期会更改。
- 扩展预订确认对话框中的小数精度超过两位小数。

**销售**

- 当您在项目合同中添加带有现有产品的基于产品的行时，会显示 **在字典中找不到密钥** 异常。
- 当订单类型从潜在顾客映射到商机时，不能对潜在顾客授予资格。
