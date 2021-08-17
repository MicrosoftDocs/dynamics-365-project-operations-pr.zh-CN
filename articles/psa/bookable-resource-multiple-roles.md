---
title: 当可预订资源为项目担任多个角色时，估计项目销售和成本
description: 本主题提供有关定价维度如何用来支持为项目中担任多个角色的资源进行定价和成本核算的信息。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987470"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>当可预订资源为项目担任多个角色时，估计项目销售和成本 

[!include [banner](../includes/psa-now-project-operations.md)]

基于项目的公司通常需要一个资源来执行项目的多个角色。 每个角色的定价和成本可能不同，这意味着项目中的同一个资源的时间可能会根据每个角色的记帐费率和成本费率而得到不同的财务估算值。 使用 Project Service Automation，可设置指定资源的团队成员记录中的值，并可以对分配给团队成员的每个任务执行不同的替代。

下面的示例说明了此值的简单替代如何让资源可以在具有不同成本费率和记帐费率的项目中有多个角色。

## <a name="create-tasks"></a>创建任务
为任务 A 和任务 B 分别创建一个 40 小时的项目任务。选择任务 A 作为任务 B 的前导任务。

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>为通用项目团队成员设置角色和部门

1. 在 **计划** 页上，选择任务 A 的 **任务** 行。 
2. 在 **资源** 字段中，从下拉列表中选择 **创建**。
3. 在 **团队成员快速创建** 页上，指定可执行此任务的通用团队成员的属性。
4. 选择相应的角色和部门，然后选择 **保存并关闭**。 将创建一个通用团队成员，并将其分配给此任务。 

对任务 B 重复这些步骤，并确保为任务 B 创建的通用团队成员中的角色和部门与任务 A 不同。 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>为项目任务设置角色和部门

1. 创建任务后，选择该任务，然后选择 **编辑任务**。
2. 在 **任务详细信息** 页上，找到 **角色** 和 **部门** 字段，添加要执行此任务的资源所需的值。 

  > [!NOTE]
  > 如果您使用 Project Service Automation 演示数据完成此场景，角色选择 **咨询负责人**，部门选择 **Fabrikam US**。

3. 选择任务 B，然后选择 **编辑任务**。
4. 在 **任务详细信息** 页上，找到 **角色** 和 **部门** 字段，添加要执行此任务的资源所需的值。 确保任务 B 的 **角色** 和 **组织单位** 字段中的值与任务 A 的值不同。 

  > [!NOTE]
  > 如果您使用 Project Service Automation 演示数据完成此场景，角色选择 **网络技术人员**，部门选择 **Fabrikam US**。

5. 保存并关闭 **任务详细信息** 页。 

## <a name="team-member-and-estimates-behavior"></a>团队成员和估计行为 

1. 在 **任务详细信息** 页上的 **团队成员** 中，选择两个通用团队成员，然后选择 **生成要求**。 
2. 选择 **咨询负责人** 的团队成员行，然后选择 **预订**。 日程安排板将打开并为该要求预订资源。
3. 选择 **网络技术人员** 的团队成员行，然后选择 **预订**。 日程安排板将打开并在该要求中预订同一个资源。

### <a name="team-member-grid"></a>团队成员网格 
在 **团队成员** 网格上，注意两个通用团队成员记录已删除，并替换为一个资源。 该资源有一组值，显示 **角色** 和 **部门** 的一组默认值。
当您展开该团队成员记录的行时，您可以看到这两个任务的团队成员记录中显示不同的工作。 每个工作行都具有任务特定的 **角色** 和 **部门** 值。 

### <a name="estimates-grid"></a>估算网格 
当您导航到 **估算** 网格时，您会注意到同一资源的两项工作的定价不同。
任务 A 中的资源的工作使用 **咨询负责人** 的 **角色** 属性值定价。 任务 B 中的同一个资源的工作使用 **网络技术人员** 的 **角色** 属性值定价。



[!INCLUDE[footer-include](../includes/footer-banner.md)]