---
title: Project Operations 中的集成日记帐
description: 此主题提供有关在 Project Operations 中使用集成日记帐的信息。
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0021147530d1aa9f82cc54ca8c92b9977c1eea2c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287227"
---
# <a name="integration-journal-in-project-operations"></a>Project Operations 中的集成日记帐

_**适用于：** 面向资源/非库存场景的 Project Operations_

时间和支出条目创建表示按照项目完成的工作的运作视图的 **实际** 交易。 Dynamics 365 Project Operations 为会计人员提供了一个审查交易并根据需要调整会计属性的工具。 审查和调整完成后，交易将过帐到项目子分类帐和总帐。 会计人员可以使用 **Project Operations 集成** 日记帐（**Dynamics 365 Finance** > **项目管理和会计** > **日记帐** > **Project Operations 集成** 日记帐）执行这些活动。

![集成日记帐流](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>在 Project Operations 集成日记帐中创建记录

Project Operations 集成日志中的记录使用定期流程 **从暂存表导入** 创建。 您可以转到 **Dynamics 365 Finance** > **项目管理和会计** > **定期** > **Project Operations 集成** > **从暂存表导入** 来运行此流程。 您可以根据需要以交互方式运行此流程，或将其配置为在后台运行。

当定期流程运行时，将找到尚未添加到 Project Operations 集成日记帐中的所有实际值。 将为每个实际交易创建一个日记帐行。
系统会根据在 **Project Operations 集成日记帐中的期间单位** 字段（**Finance** > **项目管理和会计** > **设置** > **项目管理和会计参数**，**Dynamics 365 Customer Engagement 上的 Project Operations** 选项卡）中选择的值将日记帐行分组为单独的日记帐。 此字段的可能值包括：

  - **天**：实际值按交易日期分组。 为每一天创建单独日记帐。
  - **月**：实际值按日历月分组。 为每个月创建单独日记帐。
  - **年**：实际值按日历年分组。 为每一年创建单独日记帐。
  - **所有**：所有实际交易都包含在同一集成日记帐中。 如果日记帐在定期流程运行时不可用（例如，日记帐正处于过帐交易过程中），将创建新日记帐。

日记帐行基于项目实际值创建。 以下列表包含一些更值得注意的默认规则和转换规则：

  - 每个项目实际交易在 Project Operations 集成日记帐中都有一行。 时间和材料计费类型的成本和未记帐销售交易显示在单独的行上。
  - **日期** 字段表示交易的日期。 **会计日期** 字段表示交易记录到分类帐的日期。 如果会计日期在 [已结束的财务期间](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end)内，并且在 **项目管理和会选参数** 页的 **财务** 选项卡上设置了参数 **将会计日期自动设置到未结分类帐期间**，系统会将交易的会计日期调整为下一个未结分类帐期间的第一个日期。
  - **凭证** 字段显示每个实际交易的凭证号。 凭证编号规则在 **项目管理和会计参数** 页的 **编号规则** 选项卡上定义。 每一行分配一个新编号。 在过帐凭证后，您可以选择 **凭证交易** 页上的 **相关凭证** 来查看成本和未记帐销售交易的关系。
  - **类别** 字段表示项目交易，基于相关项目实际值的交易类别设定默认值。
    - 如果在项目实际值中设置了 **交易类别**，并且给定法人中存在相关 **项目类别**，类别将默认为此项目类别。
    - 如果项目实际值中未设置 **交易类别**，系统将使用 **项目管理和会计参数** 页 **Dynamics 365 Customer Engagement 上的 Project Operations** 选项卡上的 **项目类别默认值** 字段中的值。
  - **资源** 字段表示与此交易相关的项目资源。 资源在项目发票方案中用作对客户的引用。
  - **汇率** 字段默认来自 Dynamics 365 Finance 中设置的 **货币汇率**。 如果缺少汇率设置，**从暂存导入** 定期流程不会将记录添加到日记帐中，一条错误消息将添加到作业执行日志中。
  - **行属性** 字段表示项目实际值中的计费类型。 行属性和计费类型映射在 **项目管理和会计参数** 页上的 **Dynamics 365 Customer Engagement 上的 Project Operations** 选项卡上定义。

只有以下会计属性可以在 Project Operations 集成日记帐行中更新：

- **计费销售税组** 和 **计费物料销售税组**
- **财务维度**（使用 **分配金额** 操作）

集成日记帐行可以删除，但是在您重新运行 **从暂存导入** 定期流程后，任何未过帐的行将再次插入到日记帐中。

过帐集成日记帐时，将创建项目子分类帐和总帐交易。 这些将在下游的客户开票、收入确认和财务报告中使用。


[!INCLUDE[footer-include](../includes/footer-banner.md)]