---
title: Project Service Automation V3 更新版本 15 中的新增功能
description: 本主题介绍 Project Service Automation V3 更新版本 15 中的新增功能。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749702"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3，更新版本 15

我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 PSA V3 更新版本 15 中新增或更改的功能和修复。 该版本的内部版本号为 V3.10.5.28，并且在 2020 年 1 月通过自行更新公开发布。

## <a name="update-release-15"></a>更新发布 15 

### <a name="enhancements"></a>增强功能

- 项目管理

### <a name="bug-fixes"></a>提供错误修补程序

- 时间和支出

  - 已修复：在协调视图中添加加载时错误处理。
  - 已修复：项目资源中心：重命名**金额**以减少多义性。
  - 已修复：调整**复制时间条目列**视图以包括类型。
  - 已修复：在网格视图中使用小数编辑时间条目持续时间导致某些数字出现未知错误。

- 项目管理

  - 已修复：**用于跟踪视图**的下拉菜单现在将根据选项宽度进行扩展。
  - 已修复：在 +13 时区中管理项目时，任务计算显示的结果不准确。
  - 已修复：使用 24 小时制日历时，已更正**团队成员结束时间**。
  - 已修复：重新激活了 **msdyn_project**主窗体中的 **BPF**。
  - 已修复：工作计算不再忽略一天。
  - 已修复：当用户和项目的时区不同时，向项目窗体中添加了新通知横幅。

- Sales

  - 已修复：支出估计类别查找可用于筛选重复项。
  - 已修复：**PluginDomain.ExecuteInTryCatchBlock(..)** 中的代码不再隐藏异常的来源。
  - 已修复：当有 1000 个以上的项目时，不再在**报价单明细**窗体内的**项目查找**中获取错误消息。
  - 已修复：人工估算和支出估算的**估计**网格现在显示正确的货币符号。
  - 已修复：组织将 PSA 从更新版本 14 更新为更新版本 15 之后，**计划**选项卡在**项目**窗体上不再显示为空白。
