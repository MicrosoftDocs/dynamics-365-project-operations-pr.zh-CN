---
title: Project Service Automation V3 更新版本 40 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 40 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912781"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Project Service Automation V3 更新版本 40 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 40 V3 的新增和更改的功能和修补程序。 此版本的内部版本号为 V3.10.61.61，通过 2022 年 2 月的自动更新公开发布。

## <a name="update-release-40"></a>更新发布 40

### <a name="features"></a>功能
从 Project Service Automation 升级到 Project Operations - Lite 的第 1 阶段将于 2022 年 2 月向所有客户发布。 要确认是否有资格，请参阅[从 Project Service Automation 升级到 Project Operations](upgrade-project-operations-non-stocked.md)。 如果应用程序未出现您在 Power Platform 管理中心的实例中，请联系支持部门，请求为您的环境启用外部测试版。 您的请求必须包含需要启用外部测试版的环境 ID 列表。

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**时间和支出**
- 当时间条目被拒绝或取消时，缺少注释条目。 

**销售**

- 当您使用现成可用的插件更新成本或销售估算时，您被错误地允许发送在用户界面之外无效的 JSON 有效负载。
- 当您使用快速视图更新报价单明细时，您可以激活报价单。
