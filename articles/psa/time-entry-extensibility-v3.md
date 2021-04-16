---
title: 自定义周时间条目
description: 此主题介绍如何实施为组织的业务提供支持的自定义业务规则。
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f1c8e150500334e87b25a1c8d04cf28c7b7beaeb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282052"
---
# <a name="customize-weekly-time-entry"></a>自定义每周时间条目 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Microsoft Dynamics 365 Project Service Automation 版本 3.3 中，Microsoft 引入了一个新型网格，供项目资源一次性快速输入最多一周的时间。 这个新的周时间条目网格可以按日期、行或周显示条目的总计。 资源可以创建周内时间条目的副本，还可以从之前周批量复制。 系统定制员可以自定义视图，方法是添加字段，添加对其他实体的查找，以及实施自定义业务规则以支持其组织的业务。

时间条目和新的周时间网格通过站点地图访问。 早期 PSA 版本的不可扩展自定义时间条目体验已被可扩展周时间条目网格取代和只读网格和日历中的替代体验取代。 由于此项更改，用户可以以周为量输入时间。

## <a name="page-layout"></a>页面布局
新的周时间条目网格是一个自定义控件，其拥有一个工具栏和两个主部分，即 **维度** 和 **持续时间**。 工具栏中有一个仅适用于时间条目网格的此自定义控件的按钮。 相对而言，页面顶部操作窗格中的按钮适用于三种支持时间条目的控件：周时间条目控件、只读控件和日历控件。

### <a name="dimensions"></a>维度
**维度** 显示为列标题，其中显示可再次输入的所有时间维度。 下图为支持的自带维度：

- 项目
- 项目任务
- 角色
- 类型 
- 条目状态

**维度** 部分不允许内联编辑。 此部分受一个视图支持，该视图支持向周时间条目网格添加自定义字段。 有关如何添加自定义字段的信息，请参阅此主题后文的“扩展性”部分。

### <a name="duration"></a>持续时间
“持续时间”部分将星期几显示为列标题。 此部分允许内联编辑。 创建了具有相应维度的时间条目行之后，用户可快速内联输入用在这些维度上的时间量。

## <a name="create-a-new-time-entry"></a>创建新时间条目
若要在时间条目网格中输入新时间条目，请选择 **新建**。 将显示 **时间条目快速创建** 对话框。 在此对话框中，用户可选择时间条目日期，然后输入 **项目**、**项目任务**、**角色** 和 **持续时间** 维度的数据，以分钟、小时或天为单位，方法是键入 **h**、**m** 或 **d** 和数字。 用户也可以为时间条目输入可在外部共享的描述和注释。 用户保存自己的更改时，将在 **维度** 部分中显示为维度输入的值。 其在 **持续时间** 字段中输入的持续时间信息在为其创建时间条目的日期上显示。

查找字段受系统视图支持。 例如，用户进入项目后，**项目任务** 字段默认设置为 **复制** 视图。 若要为尚未分派给用户的任务创建时间条目，请在查找对话框中选择 **更改视图**，然后选择 **所有可用的项目任务** 视图。

## <a name="edit-a-time-entry"></a>编辑时间条目
周时间条目网格中不显示时间条目页中某些字段（如 **描述** 和 **外部注释**）内的详细信息。 而是在具有这些额外详细信息的持续时间单元格中显示一个小三角指示器。 选择此类单元格，然后选择 **编辑详细信息** 可在 **快速编辑** 窗格中查看这些数据。 若要编辑不属于周时间条目网格的某个特定时间条目的详细信息，用户必须打开 **快速编辑** 窗格。

## <a name="copy-a-time-entry-row"></a>复制时间条目行
创建第一个时间条目行之后，用户可选择 **复制行** 将整行复制到新行。 如果按照这种方法复制行，也将复制维度和持续时间。 用户还可以选择 **编辑行** 以在 **持续时间** 部分中内联更新维度值和持续时间。

## <a name="open-a-time-entry"></a>打开时间条目
为了支持最醒目字段中的最佳快速条目，周时间条目网格显示一小组选定维度和持续时间。 若要查看一个时间条目的所有详细信息，请在 **编辑条目** 下选择 **打开**。

## <a name="submit-a-time-entry"></a>提交时间条目
用户可提交一个或一组时间条目，方法是选择单元格区域或整个时间条目行，然后选择 **提交**。 提交的时间条目在审批者的 **审批** 页中显示为待审批条目。 时间条目在成功提交后不可编辑。

## <a name="recall-a-time-entry"></a>撤消时间条目
可撤销已提交的时间条目。 可撤销一个、一部分或整行时间条目。 资源可编辑已撤销的时间条目。

## <a name="time-entry-status"></a>时间条目状态
将为新时间条目自动分派 **草稿** 状态。 提交时间条目时，其状态更新为 **已提交**。 批准已提交的时间条目时，其状态更新为 **已批准**。 如果拒绝了时间条目，其状态将更新为 **已返回**，并且可更正和重新提交该条目。 只能删除状态为 **草稿** 的时间条目。

## <a name="view-rejection-comments"></a>查看拒绝注释
审批者在拒绝时间条目时，可能会添加拒绝注释来帮助资源了解拒绝原因。 若要查看时间条目的拒绝注释，请选择 **打开条目**。 将在时间线中显示拒绝注释。 用户在重新提交条目之前，可在时间线中响应拒绝注释。

## <a name="copy-week"></a>复制周
创建一些时间条目之后，用户可以选择 **复制周** 批量创建更多时间条目。 将显示 **复制** 对话框。 在 **开始期间** 部分中，使用 **开始日期** 和 **结束日期** 字段定义要复制的时间条目所属日期范围。 在 **目标期间** 部分中 **开始日期** 字段内，指定要为其创建时间条目的日期。 然后选择 **复制**。 对于“目标”期间内的指定日期，将为“开始”期间中相应星期几的时间条目创建一个副本。 例如，将把上周星期一的时间条目复制到指定为“目标”期间的周的星期一。

## <a name="import"></a>导入
同样的基本流程用于从预订、分派和交换导入。 用户可指定导入的预订所属日期范围。 然后必须明确选择应该复制到草稿时间条目中的预订。 在上一个版本中，建议的时间条目在网格和日历中显示，刷新会话后会消失。

## <a name="extensibility"></a>扩展性
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>向其他实体添加具有查找的自定义字段
向周时间条目网格添加自定义字段主要分三步。

1.  将自定义字段添加到快速创建对话框。
2.  配置网格以显示该自定义字段。
3.  根据需要将该自定义字段添加到行编辑任务流或单元格编辑任务流。

还必须确保新字段在行或单元格编辑任务流中进行必需的验证。 此步骤中，必须基于时间条目状态锁定字段。

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>将自定义字段添加到快速创建对话框
必须将自定义字段添加到“创建时间条目快速创建”对话框。 这样，用户就可以在使用 **新建** 按钮添加时间条目时为其输入值。

#### <a name="configure-the-grid-to-show-the-custom-field"></a>配置网格以显示该自定义字段
可通过两种方法向周时间条目网格添加自定义字段。 第一种方法是自定义 **我的周时间条目** 视图并向其添加自定义字段。 可选择自定义字段在网格中的位置和大小，方法是在视图中编辑这些属性。

第二个选项是创建新的自定义时间条目视图，然后将其设置为默认视图。 除了网格中需要的列，此视图中还应包含 **描述** 和 **外部注释** 字段。 可选择网格的位置、大小和默认排序顺序，方法是在视图中编辑这些属性。 接下来，配置此视图的自定义控件，使其成为 **时间条目网格** 控件。 将此控件添加到视图，然后选择将其用于 Web、手机和平板电脑。 接下来，配置周时间条目网格的参数。 将 **开始日期** 字段设置为 **msdyn_date**，将 **持续时间** 字段设置为 **msdyn_duration**，将 **状态** 字段设置为 **msdyn_entrystatus**。 对于默认视图，**只读状态列表** 字段设置为 **192350002,192350003,192350004**，**行编辑任务流** 字段设置为 **msdyn_timeentryrowedit**，**单元格编辑任务流** 字段设置为 **msdyn_timeentryedit**。 可自定义这些字段以添加或删除只读状态，或使用其他基于任务的体验 (TBX) 编辑行或单元格。 应将这些字段绑定到静态值。

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>将自定义字段添加到相应编辑任务流
用于编辑的 TBX 页位于 **流程** 下。 默认页为 **Project Service - 时间条目行编辑** 和 **Project Service - 时间条目编辑**。 然后可编辑这些默认页或创建新的自定义 TBX 页。

> [!NOTE] 
> 两种选项都会移除对 **项目** 和 **项目任务** 实体的一些自带筛选，因此将显示这些实体的所有查找视图。 只有相关查找视图才会默认显示。

必须确定自定义字段的相应任务流。 最可能的是，如果将字段添加到了网格，则应进入对适用于整行时间条目的字段使用的行编辑任务流。 如果自定义字段每天有唯一值（如 **结束时间** 的自定义字段），则应进入单元格编辑任务流。

若要将自定义字段添加到任务流，请将一个 **字段** 元素拖到页中的相应位置，然后设置其属性。 将 **来源** 属性设置为 **时间条目**，将 **数据字段** 属性设置为自定义字段。 **字段** 属性指定在 TBX 页上的显示名称。 选择 **应用** 保存对字段进行的更改。 选择 **更新** 保存对页进行的更改。

若要改用新的自定义 TBX 页，请创建一个新流程。 将类别设置为 **业务流程**，将实体设置为 **时间条目**，将业务流程类型设置为 **将流程作为任务流运行**。 应将 **属性** 下的 **页面名称** 属性设置为页面的显示名称。 将所有相关字段添加到 TBX 页。 保存并激活流程，然后将相关任务流的自定义控件属性更新为流程中的 **名称** 的值。

### <a name="add-new-option-set-values"></a>添加新选项集值
若要向自带字段添加选项集值，请打开该字段的编辑页，然后在 **类型** 下选择该选项集旁边的 **编辑**。 接下来，添加一个采用自定义标签和颜色的选项。 如果要添加新的时间条目状态，则自带字段将命名为 **条目状态**，而不是 **状态**。

### <a name="designate-a-new-time-entry-status-as-read-only"></a>将新时间条目状态指定为只读
若要将新时间条目状态指定为只读，请将新时间条目值（编号，而不是标签）添加到 **只读状态列表** 属性中。 将对具有新状态的行锁定时间条目的可编辑部分。
接下来，添加业务规则以锁定 **时间条目行编辑** 和 **时间条目编辑** TBX 页中的所有字段。 可以访问这些页的业务规则，方法是打开页的业务流程编辑器，然后选择 **业务规则**。 可向现有规则中的条件添加新状态，也可以为新状态添加新业务规则。

### <a name="add-custom-validation-rules"></a>添加自定义验证规则
可以为周时间条目网格体验添加两种类型的验证规则：•   快速创建对话框和 TBX 页中支持的客户端业务规则 •   适用于所有时间条目更新的服务器端插件验证

#### <a name="business-rules"></a>业务规则
可使用业务规则锁定和解锁字段，在字段中输入默认值，以及定义仅需要来自当前时间条目记录的信息的验证。 可以访问 TBX 页的业务规则，方法是打开页的业务流程编辑器，然后选择 **业务规则**。 然后可以编辑现有业务规则或添加新的业务规则。 对于自定义程度甚至更高的验证，可以使用业务规则运行 JavaScript。

#### <a name="plug-in-validations"></a>插件验证
应该将插件验证用于需要的上下文比单个时间条目记录中的可用上下文多的任何验证，或用于要对网格中的内联更新运行的任何验证。 若要完成验证，请在 **时间条目** 实体中创建一个自定义插件。

> [!IMPORTANT] 
> 现在，当更新未通过插件验证时，TBX 页中的一项已知问题阻止用户更正信息和重新选择“完成”。 解决方法是，设置业务规则验证以尽量避免这种情况发生。


[!INCLUDE[footer-include](../includes/footer-banner.md)]