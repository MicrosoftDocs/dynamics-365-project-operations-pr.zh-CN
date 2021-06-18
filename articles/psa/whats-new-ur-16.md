---
title: Project Service Automation V3 更新版本 16 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 16 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006770"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation V3 更新版本 16

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。  此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新首选解决方案](/dynamics365/project-service/upgrade-psa-home-page)。
本主题列出了 PSA V3 更新版本 16 中新增或更改的功能和修复。 该版本的内部版本号为 V3.10.6.34，并且在 2020 年 1 月通过自行更新公开发布。


## <a name="update-release-16"></a>更新发布 16

### <a name="bug-fixes"></a>提供错误修补程序

-   时间和支出

    -   已修复：尝试提交已删除时间和支出条目以供审批的用户现在将收到相关错误消息。

-   项目管理

    -   已修复：采用了在模板中为团队成员定义的资源单位，并且对新项目应用了模板。

    -   已修复：改进了记录所有权重新分派的处理。

    -   已修复：将不允许复制正在进行复制的项目，直到完成所有复制操作为止。

-   资源管理

    -   已修复：扩展预订现在可正确处理较短持续时间，不会再为扩展预订创建零小时的持续时间。

    -   已修复：现在，当项目时区为 +5:30 GMT 且用户的时区不同时，会呈现协调视图。

-   Sales

    -   已修复：在删除映射到合同子项的项目并映射新项目时，不会根据合同子项中定义的记帐和定价规则重新评估该新项目中的实际记录。 此版本中已修复该问题。 根据合同子项的定价和记帐规则，新映射项目中的定价和实际记录将被正确冲销并重新创建。 未映射项目的实际记录也将被重新评估并重新创建为一项结果。

    -   已修复：已将其他验证添加到评估行的 **金额** 字段中，以确保不会保留 null 值。

    -   已修复：对项目更新了实际值后，向项目主表单中添加了刷新按钮，以允许用户重新同步实际值。

    -   已修复：当用户从 2.X 升级到 3.X 时，将允许项目名称为 NULL 值的项目。



[!INCLUDE[footer-include](../includes/footer-banner.md)]