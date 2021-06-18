---
title: 定价和定成本维度主页
description: 此主题概述定价维度。
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
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009245"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>定价和定成本维度主页

[!include [banner](../includes/psa-now-project-operations.md)]

在基于项目的组织中，用于设置人工定价和成本核算的维度受以下属性影响：

- 从事与自己的经验、角色或地理位置相似的工作的人员
- 所执行的与其复杂性或一天中的时间相似的工作

鉴于工作的这些属性和执行工作所需的人员的典型性质，Project Service Automation 中提供了两种类型的定价维度值： 

- **选项集** - 这种属性是一组值的固定枚举。
- **基于实体的值** - 这种属性可以具有一组有限的可变值，但可以随时间变化。

## <a name="pricing-dimensions"></a>定价维度

PSA 随附了一组默认定价维度。 可通过转到 **Project Service** > **参数** 查看。 在参数记录中 **基于金额的定价维度** 选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段 **适用于销售** 和 **适用于成本** 是否设置为 **是**。 这样就可以为每个角色与部门的组合设置价格和成本。

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

有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。 **交易类别** (**msdyn_transactioncategory**) 和 **可预订资源** (**bookableresource**) 之类字段就是候选维度。 

应注意定价维度应该是表还是选项集。 如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，则创建非选项集实体。 若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数业务用户可以向表添加新行。

以下示例显示基于资源所属角色和资源部门设置的记帐费率。 成本费率通常基于员工的工资级别和员工所属部门。 在此示例中，记帐费率和成本费率表如下所示。

**示例记帐费率**

| 角色        | 部门    |计价单位      |单价      |货币  |
| ------------|-------------|----------|----------:|----------|
| 开发人员   | Contoso US  |小时 | 200|USD     |
| 开发人员   | Contoso 印度 |小时|   112|USD     |


**示例成本费率**

| 工资级别     | 部门    |计价单位      |单价      |货币  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |小时 | 145|USD     |
| My company_Band2 | Contoso 印度 |小时|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]