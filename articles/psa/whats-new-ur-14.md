---
title: Project Service Automation V3 更新版本 14 中的新增功能或更改
description: 本主题介绍 Project Service Automation V3 更新版本 14 中的新增功能。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147147"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation V3 更新版本 14

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 PSA V3 更新版本 14 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.4.21，并且按以下计划提供：

- **公开发布（自行更新）：** 2020 年 1 月
- **自动更新：** 2020 年 2 月

## <a name="update-release-14"></a>更新发布 14

### <a name="enhancements"></a>增强功能

- Sales

     - 当报价单更新为 **作为赢单结束** 时，**报价单明细详细信息** 中的自定义字段值会复制到 **项目合同子项详细信息** 中。
     - 已确认的项目可以 **作为赢单结束**。

- 资源管理

     - 在扩展预订时，系统将用确认对话框提示用户汇总预订结果并提供指向“维护预订”的链接。


### <a name="bug-fixes"></a>提供错误修补程序

- 时间和支出

     - 已修复：在用户尚未选择任何要更正的条目的情况下改善了用户体验。

- 资源管理

     - 已修复：多次预订资源会使可预订资源的名称溢出。

- Sales

     - 已修复：在用户还输入项目的支出估计成本价之前，不会计算总销售价。
     - 已修复：如果关联的项目合同未处于 **草稿** 状态，则以 **赢得** 形式结束报价单将会失败。



[!INCLUDE[footer-include](../includes/footer-banner.md)]