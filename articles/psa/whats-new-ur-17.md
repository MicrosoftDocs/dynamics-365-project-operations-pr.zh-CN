---
title: Project Service Automation V3 更新版本 17 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 17 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 70749646f5b67db3cf868a6d9a83c14dc490793a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585080"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation V3 更新版本 17

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。  此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 PSA V3 更新版本 17 中新增或更改的功能和修复。 该版本的内部版本号为 V3.10.6.34，并且在 2020 年 3 月通过自行更新公开发布。


## <a name="update-release-17"></a>更新发布 17

### <a name="bug-fixes"></a>提供错误修补程序

**常规**

- 已修复：更新 Project Service Automation 以强制使用 Team Member 许可证（项目资源中心将包括 Team Member Service 计划元数据 3.x）
 
**时间和支出**

- 已修复：不能将支出估计值从非零价格更改为零 (0)。 该更改被忽略。

**项目管理**

- 已修复：已为团队成员的职位名称添加了 null 值检查功能。
- 已修复：**msdyn_resourceassignment** 实体的 **msdyn_userresourceid** 字段已被弃用。
- 已修复：从 2.x 升级到 3.x，现在可针对任务分配处理空工作量等值线。

**Sales**

- 已修复：**Invoice.PreValidateInvoiceUpdate** 现在可以正确处理重新分派记录负责人的方案。
- 已修复：当交易分类是 **时间** 时，对于所有实体（包括 **QuoteLineDetails**、**JournalLine**、**InvoiceLineDetail** 和 **ContractLineDetails**），**UnitGroup** 均不可编辑。 但是，**单位** 仅对 **JournalLine** 和 **InvoiceLineDetails** 不可编辑。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
