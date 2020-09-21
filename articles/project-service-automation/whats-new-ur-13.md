---
title: Project Service Automation V3 更新版本 13 中的新增功能
description: 本主题介绍 Project Service Automation V3 更新版本 13 中的新增功能。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749704"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3，更新版本 13
我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 13 中新增或更改的功能和修补。 此版本的内部版本号为 V3.10.3.18，并且按以下计划提供：

- **公开发布（自行更新）：** 2019 年 11 月
- **自动更新：** 2019 年 12 月


## <a name="update-release-13"></a>更新发布 13 

### <a name="bug-fixes"></a>提供错误修补程序

- 时间和支出

     - 已修复：按支出用途搜索时，**支出审批**页面上的搜索功能不起作用。

- 资源管理

     - 已修复：已将协调中的数字更新为右对齐。
     - 已修复：无法通过**计划**选项卡将指定的资源分派给任务。

- 项目管理

     - 已修复：当 **TransactionType** 缺少 **Unit** 和 **DefaultGroup** 的设置信息时，分配团队成员期间会出现空引用异常。

- Sales

     - 已修复：创建角色价格记录时，重复的交易类型记录会返回错误。
     - 已修复：在“商机”、“报价单”、“订单产品”和基于项目的行子网格的命令中，**商机**、**报价单**、**订单明细**和**添加产品**的额外按钮可见。


