---
title: 定价和定成本维度主页
description: 此主题概述定价维度。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749686"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>定价和定成本维度主页

人力资源中用于设置定价和成本的维度分为两种类别：

- 人员
- 计划的工作

因此， Project Service Automation (PSA) 中的定价维度值有两种： 

- **选项集** - 这种维度是一组值的固定枚举。
- **基于实体的值** - 这种维度可以是一组可变值。

## <a name="pricing-dimensions"></a>定价维度

PSA 随附了一组默认定价维度。 可通过转到 **Project Service** > **参数**查看。 在参数记录中**基于金额的定价维度**选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段**适用于销售**和**适用于成本**是否设置为**是**。 这样就可以为每个角色与部门的组合设置价格和成本。

![“适用于销售”已突出显示的 Project Service 参数的屏幕截图](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> 如果在 PSA 版本 3 之前已将角色和部门的自带字段用作定价维度，则不存在任何显而易见的更改。 可以继续正常使用 Project Service。 

如果需要使用更多属性制订资源的价格或成本，可以创建自定义的字段、实体和维度。 有关详细信息，请参阅以下主题，但是请注意，必须按照下列顺序完成过程：

- [创建自定义字段和实体](create-custom-fields-entities.md)
- [向价格设置和交易实体添加自定义字段](field-references.md)
- [将自定义字段设置为定价维度](set-up-pricing-dimensions.md)
- [更新插件属性以包括新定价维度](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>为人力资源时间定价
组织如何为人力资源时间定价通常是直接影响组织利润率的重要战略注意事项。 当组织准备好确定希望如何设置人力资源时间的记帐费率和成本费率时，请与财务团队和业务主管合作。

有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。 **交易类别** (**msdyn_transactioncategory**) 和**可预订资源** (**bookableresource**) 之类字段就是候选维度。 

还应注意定价维度应该是表还是选项集。 如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，可以创建非选项集实体。 若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数用户可以向表添加新行。

以下示例显示基于资源所属角色和资源部门设置的记帐费率。 成本费率通常基于员工的工资级别和员工所属部门。 在此示例中，记帐费率和成本费率表如下所示。

**示例记帐费率**

| 角色        | 部门    |单位      |价格      |货币  |
| ------------|-------------|----------|----------:|----------|
| 开发人员   | Contoso US  |Hour | 200|USD     |
| 开发人员   | Contoso 印度 |Hour|   112|USD     |


**示例成本费率**

| 工资级别     | 部门    |单位      |价格      |货币  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hour | 145|USD     |
| My company_Band2 | Contoso 印度 |Hour|   67|USD     |
