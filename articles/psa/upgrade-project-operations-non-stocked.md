---
title: 从 Project Service Automation 升级到 Project Operations
description: 本文概括介绍从 Microsoft Dynamics 365 Project Service Automation 升级到 Dynamics 365 Project Operations 的过程。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686964"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>从 Project Service Automation 升级到 Project Operations

我们很高兴宣布从 Microsoft Dynamics 365 Project Service Automation 升级到 Microsoft Dynamics 365 Project Operations 进入到三个阶段的第二阶段。 本文为即将踏上这一激动人心的旅程的客户提供概述。 

升级交付计划将分为三个阶段。

| 升级交付 | 第 1 阶段（2022 年 1 月） | 第 2 阶段（2022 年 11 月） | 第 3 阶段（2023 年 4 月波次）  |
|------------------|------------------------|---------------------------|---------------------------|
| 项目不依赖工作分解结构 (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations 的当前受支持限制内的 WBS | | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations 的当前受支持限制外的 WBS，包括对 Project Desktop Client 的支持 | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>升级流程功能 

在升级过程中，我们已将升级日志添加到站点地图，让管理员能够更轻松地诊断故障。 除了新接口，还将添加新验证规则以确保升级后的数据完整性。 以下验证将添加到升级流程中。

| 验证 | 第 1 阶段（2022 年 1 月） | 第 2 阶段（2022 年 11 月） | 第 3 阶段  |
|-------------|------------------------|---------------------------|---------------------------|
| 系统将根据常见的数据完整性违规情况（例如，资源分配与同一父任务关联但具有不同父项目）验证 WBS。 | | :heavy_check_mark: | :heavy_check_mark: |
| 系统将根据 [Project for the Web 的已知限制](/project-for-the-web/project-for-the-web-limits-and-boundaries)验证 WBS。 | | :heavy_check_mark: | :heavy_check_mark: |
| 系统将根据 Project Desktop Client 的已知限制验证 WBS。 | |  | :heavy_check_mark: |
| 系统将根据常见的不兼容日历规则例外来评估可预订资源和项目日历。 | | :heavy_check_mark: | :heavy_check_mark: |

在第 2 阶段，升级到 Project Operations 的客户的现有项目将升级到项目规划只读体验。 在此只读体验中，完整的 WBS 将会显示在跟踪网格中。 要编辑 WBS，项目经理可以在项目的主页上选择 [**转换**](/PSA-Upgrade-Project-Conversion.md)。 然后，后台进程将更新项目，以便支持 Project for the Web 中的新项目计划体验。 此阶段适用于项目符合 [Project for the Web 已知限制](/project-for-the-web/project-for-the-web-limits-and-boundaries)的客户。

在第 3 阶段，将添加对 Project Desktop Client 的支持，以使希望继续从该应用程序编辑其项目的客户受益。 但是，如果将现有项目转换为新的 Project for the Web 体验，则会对每个转换后的项目都禁用加载项访问。

## <a name="prerequisites"></a>先决条件

要获得第 1 阶段升级的资格，您必须满足以下条件：

- 目标环境不得包含 **msdyn_projecttask** 实体中的任何记录。
- 必须将有效的 Project Operations 许可证分配给所有活动用户。 
- 您必须在至少一个包含与生产数据一致的代表性数据集的非生产环境中验证升级过程。
- 目标环境必须更新为 Project Service Automation 更新版 37 (V3.10.58.120) 或更高版本。

要获得第 2 阶段升级的资格，您必须满足以下条件：

- 必须将有效的 Project Operations 许可证分配给所有活动用户。 
- 您必须在至少一个包含与生产数据一致的代表性数据集的非生产环境中验证升级过程。
- 目标环境必须更新为 Project Service Automation 更新版 37 (V3.10.58.120) 或更高版本。
- 仅当每个项目的任务总数为 500 或以下时，才支持包含任务 (msdyn_projecttask) 的环境。

第 3 阶段的先决条件将随着正式发布日期的临近更新。

## <a name="licensing"></a>许可

如果您拥有可用的 Project Service Automation 许可证，则您可以安装和使用 Project Operations，其中包括 Project Service Automation 的所有功能及更多功能。 之后，继续在生产中使用 Project Service Automation 时，您可以在单独的环境中测试 Project Operations 的功能。 在您的 Project Service Automation 许可证到期后，您必须转换到 Project Operations。 在计划此转换时，您必须考虑到 Project Operations 许可证不包括 Project Service Automation 许可证这一事实。

## <a name="testing-and-refactoring-customizations"></a>测试并重构自定义项

首先，将所有自定义项导入干净的 Project Operations（精简）环境，以确认导入成功，并且业务运营表现正常。

以下是一些需要关注的事项：

- 导入可能会因缺少依赖项而失败。 换句话说，自定义项引用字段或 Project Operations 中已删除的其他组件。 在这种情况下，从开发环境中移除这些依赖项。
- 如果您的非托管和托管解决方案包含未自定义的组件，请从解决方案中删除这些组件。 例如，在自定义 **项目** 实体时，请仅将实体标题添加到解决方案中。 不要添加所有字段。 如果您以前添加了所有子组件，则您可能必须手动创建新解决方案，并向其添加相关组件。
- 窗体和视图可能不会按预期显示。 在某些情况下，如果您自定义了任何现成的窗体或视图，则自定义项可能会阻止 Project Operations 中的新更新生效。 为了识别这些问题，我们建议您并排查看 Project Operations 的全新安装和包含您的自定义项的 Project Operations 安装。 比较您的业务中最常用的窗体，以确认窗体版本仍然有意义，并且未缺少干净窗体版本中的内容。 对已自定义的任何视图执行相同类型的并排查看。
- 业务逻辑在运行时可能会失败。 由于在导入时未验证对插件中字段的引用，因此，业务逻辑可能会因引入了不再存在的字段而失败，并且您可能会收到类似于以下示例的错误消息：“‘项目’实体不包含 Name = "msdyn_plannedhours" 且 NameMapping = "Logical" 的属性”。在这种情况下，请修改您的自定义项，以便它们使用新字段。 如果在插件逻辑中使用自动生成的代理类和强类型引用，请考虑从干净安装中重新生成这些代理。 这样，您可以轻松确定插件依赖于弃用的字段的所有位置。

在您更新您的自定义以干净地导入 Project Operations 后，请继续执行后续步骤。

## <a name="end-to-end-testing-in-development-environments"></a>在开发环境中进行端到端测试

### <a name="initiate-upgrade"></a>启动升级 

1. 在 Power Platform 管理中心，查找并选择您的环境。 然后在应用程序中，查找并选择 **Dynamics 365 Project Operations**。
2. 选择 **安装** 以开始升级。 Power Platform 管理中心将此安装显示为新安装。 但是，将检测到是否存在早期版本的 Project Service Automation，并且将升级现有安装。

    升级完成后，环境应显示已安装 Project Operations，但未安装 Project Service Automation。

    根据环境中的数据量，升级可能需要几个小时的时间。 管理升级的核心团队应该相应地进行计划并在非工作时间运行升级。 在某些情况下，如果数据量很大，应该在周末进行升级。 关于日程安排的决定应该基于较低等环境中的测试结果。

3. 可在适当时升级自定义解决方案。 此时，请部署您在本文的[测试并重构自定义项](#testing-and-refactoring-customizations)一节中对自定义项所做的任何更改。
4. 转到 **设置** \> **解决方案**，然后选择卸载 **Project Operations 已弃用的组件** 解决方案。

    此解决方案是一个临时解决方案，用于保存升级过程中提供的现有数据模型和组件。 通过移除此解决方案，可以删除所有不再使用的字段和组件。 这样，您可以帮助简化界面并使集成和扩展更容易。
    
### <a name="upgrade-to-project-operations-lite"></a>升级到 Project Operations Lite

以下步骤描述了升级过程和相关的错误记录：

1. **PSA 版本检查：** 要安装 Project Operations，必须安装 V3.10.58.120 或更高版本。
1. **预验证**：当管理员启动升级时，系统会对作为 Project Operations 解决方案核心的每个实体运行预验证操作。 此步骤会验证所有实体引用是否有效，并确保与 WBS 相关的数据在 Project for the Web 的发布限制范围内。
1. **元数据升级**：预验证成功后，系统将启动对架构的更改并创建弃用的组件解决方案。 在完成所有必需的自定义重构后，您可以删除此弃用的解决方案。 此步骤是升级过程中最长的一部分，最长可能需要四个小时完成。
1. **数据升级**：在元数据升级步骤中完成所有需要的架构更改后，您的数据将被迁移到新架构，任何所需的默认设置和重新计算都会完成。
1. **项目计划引擎更新：** 成功升级数据后，主页上的 **计划** 选项卡将重新标记为 **任务**。 当用户在升级后选择此选项卡时，系统会指示他们导航到跟踪网格查看 WBS 的只读版本。 要编辑 WBS，他们必须启动计划[转换过程](/PSA-Upgrade-Project-Conversion.md)。 所有没有预先存在的 WBS 的项目都可以直接使用新的计划体验，不需要转换。
 
### <a name="validate-common-scenarios"></a>验证常见场景

当您验证您的特定自定义时，我们建议您同时查看跨应用程序支持的业务流程。 这些业务流程包括但不限于创建销售实体（如报价单和合同），以及创建包含 WBS 和实际值审批的项目。

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation 和 Project Operations 之间的主要变化

本节概述了可以期待的 Project Service Automation 和 Project Operations 之间的主要变化。

### <a name="project-planning"></a>项目规划

Project Operations 中的项目计划功能不再依赖于客户端逻辑和服务器端逻辑的组合。 相反，Project Operations 将 Project for the Web 用作其计划引擎。 此日程安排功能更改可实现多项新功能，例如板块和甘特图视图、资源驱动的规划、[任务清单项](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)和项目日程安排模式。 一组丰富的新[应用编程接口 (API)](../project-management/schedule-api-preview.md) 也支持新日程安排功能。 这些 API 旨在帮助确保在 WBS 中创建、更新或删除实体的编程操作不会破坏计划中的计算字段。

### <a name="billing-and-pricing"></a>计费和定价

在持续投资于 Project Operations 的过程中，帐单和定价中可使用多项新功能。 以下是一些示例：

- [记录项目和项目任务的材料使用情况](../material/material-usage-log.md)
- [分包合同管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [预付款和保留款合同](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [合同上限状态和验证](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- 基于任务的记帐

### <a name="resource-management"></a>资源管理

Project Operations 为 Universal Resource Scheduling (URS) 板和日程安排助理提供可选支持。 此新体验将在 2023 年 4 月波次中成为强制功能。

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>升级当前支持哪些部署类型？

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite 部署                        | 受支持               |
| Dynamics 365 Finance 项目管理和会计 | Project Operations Lite 部署                        | 当前不支持 |
| Finance 项目管理和会计              | 面向资源/非库存场景的 Project Operations     | 当前不支持 |
| Project Service Automation 3.x                         | 面向资源/非库存场景的 Project Operations     | 当前不支持 |
| Project for the Web（专用环境）            | Project Operations Lite 部署                        | 当前不支持 |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>如何在升级工具可用之前安装 Project Operations？

在升级工具可用之前安装 Project Operations 有两个选项：

- 设置新环境。
- 在没有 Project Service Automation 的任何销售组织上单独部署 Project Operations。

如果在组织上安装了 Project Service Automation，但未使用它，则可以将其卸载。 完全删除 Project Service Automation 后，可以在同一组织中安装 Project Operations。
