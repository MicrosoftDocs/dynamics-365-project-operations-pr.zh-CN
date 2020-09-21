---
title: Project Service Automation V3 更新版本 12 中的新增功能
description: 本主题介绍 Project Service Automation V3 更新版本 12 中的新增功能。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749705"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3，更新版本 12
我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 12 中新增或更改的功能和修复。 该版本的内部版本号为 V3.10.2.34，并且在 2019 年 10 月通过自行更新公开发布。

## <a name="update-release-12"></a>更新发布 12

### <a name="bug-fixes"></a>提供错误修补程序

- 时间和支出

    - 已修复：已使用更相关的上下文更新了时间条目错误消息。
    - 已修复：时间条目网格和计划在必要时会正确显示垂直滚动条。
    - 已修复：可以批准提交的支出和时间条目。
    - 已修复：“取消审批确认”对话框消息已更正，以在将**已批准**更改为**已提交**后反映审批状态。
    - 已修复：在批准支出记录后，**价格**、**单位**和**数量**字段现在在支出记录上已被锁定。

- 项目管理

    - 已修复：已删除针对**团队成员**主窗体的**新**操作。
    - 已修复：已更新资源分派以解决导致任务结束日期发生变化的不准确舍入错误。
    - 已修复：在任务网格中，将向用户呈现相关的服务器端错误。
    - 已修复：团队成员的名称现在呈现在任务人员选取器中，而不是呈现在职位名称中。

- 资源管理

    - 已修复：根据模板创建的项目的资源要求详细信息现在使用项目日历。
    - 已修复：技能和资格现在从角色主数据默认为针对该角色创建的资源要求。

- Sales

    - 已修复：在**合同主**窗体中发现重复的对象 ID。
    - 已修复：已更新逻辑以使**报价单分析**选项卡可见，以便显示该选项卡的元数据设置。
    - 已修复：实际记录上的会计日期现在来自时间/支出条目日期，而不是审批日期。
