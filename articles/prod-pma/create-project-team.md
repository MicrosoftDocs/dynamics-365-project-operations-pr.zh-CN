---
title: 创建项目团队
description: 本主题提供有关如何创建和管理项目团队的信息。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270847"
---
# <a name="create-a-project-team"></a>创建项目团队

[!include [banner](../includes/banner.md)]

若要使用之前在项目中设置的角色，项目经理必须将角色与项目关联。 可以为一个项目分配多个角色。 为了避免混淆，在预留期间将自动标记这些角色。 例如，如果项目经理需要三位软件工程师，将自动生成具有 **软件工程师 1**、**软件工程师 2** 和 **软件工程师 3** 作为其标签的软件工程师角色。 如果之前为角色设置了角色特性，则在搜索资源期间，它们将应用为筛选器。 其他特性可以根据需要添加以进一步调整搜索。

查看设置还可以自定义以提供资源可用性的更好的视图。 具有显示每小时、每日、每周、每月、每季度和每年可用性的选项。 还有可以显示可用资源和剩余资源产能的选项。 在您评估活动或资源可用性的可用时间时，此选项对时间管理很有用。

项目经理可在页面上选择角色，然后，如果存在满足该需求的一个可用资源，选择预留符合角色的资源。 请注意，资源不必在计划阶段的此时间点预留。 在您创建 WBS 时，可以使用项目的雇用资源替换角色。 如果角色替换为 WBS 中的雇用资源，资源设置将自动更新项目团队列表和计划。

[![包括角色和实际资源的项目团队列表](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

项目经理具有预订项目资源的不同选项，例如 **剩余产能**、**全部产能**、**产能百分比** 和 **指定工时**。 如果资源分配更改，这些预订选项可以在任何时间取消。 支持以下两种预订类型：

- **硬性预订** – 针对指定的持续时间审核并确认处理约定的资源预留。
- **软性预订** – 针对指定的持续时间暂时设置处理约定的资源预留。

以下过程说明如何创建项目团队。

## <a name="create-a-project-team"></a>创建项目团队

1. 在 **所有项目** 列表页上，选择一个项目，然后选择 **编辑**。
2. 在 **项目团队和计划编制** 选项卡上，在 **计划结束日期** 字段中，输入计划开始日期再加上一个月。 例如，如果计划开始日期为 2017 年 6 月 24 日 (24/06/2017)，输入 **24/07/2017**。
3. 选择 **添加**。
4. 在 **将角色添加到项目** 窗格中，在 **角色** 字段中，选择 **高级项目经理**。
5. 选择 **所需能力**。
6. 默认情况下，在 **选择特性** 页上，选择您之前为高级项目经理角色设置的特性。 选择 **确定**。
7. 在 **将角色添加到项目** 页上，在 **资源数** 字段中，输入 **1**。
8. 在 **资源** 字段中，查找显示具有所需能力的所有资源。 选择 **Daniel Goldschmidt**，然后选择 **创建**。
9. 在 **项目** 页上，选择 **添加**。
10. 在 **将角色添加到项目** 窗格中，在 **角色** 字段中，选择 **团队成员**。 在 **资源数** 字段中输入 **5**。
11. 选择 **创建**。
12. 在 **项目** 页上，选择 **完成资源**。

## <a name="monitor-project-teams"></a>监控项目团队
1. 在 **所有项目** 页上，选择 **XYZ 升级第 2 阶段** 项目的 **项目 ID** 链接。
2. 在 **项目团队和计划编制** 快速选项卡上，确认列出的项目资源是正确的。


[!INCLUDE[footer-include](../includes/footer-banner.md)]