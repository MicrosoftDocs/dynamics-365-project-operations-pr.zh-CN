---
title: Project Service Automation V3 更新版本 45 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 45 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169148"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Project Service Automation V3 更新版本 45 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 45 V3 的新增和更改的功能和修补程序。 此版本具有内部版本号 V3.10.76.168，并且于 2022 年 7 月通过自助更新公开发布。

## <a name="update-release-45"></a>更新发布 45

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**销售**

- 用户在尝试创建没有任何未计费销售的发票后，如果他们也在查看页面的同一实例并且不刷新它，则他们无法成功创建发票。

**时间和支出**

- 启用“现代审批”并批准撤销的项目审批后，记录阶段会错误地更新为 **撤消已批准的请求**。
- 启用“现代审批”且云端流处于非活动状态时，审批流程不会成功，并且不会通知提交或审批用户。
