---
title: 定价维度概述
description: 本主题提供有关 Dynamics 365 Project Operations 中定价维度的信息。
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004970"
---
# <a name="pricing-dimensions-overview"></a>定价维度概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

人力资源中用于设置定价和成本的维度分为两种类别：

- 人员
- 计划的工作

因此，定价维度值有两种：

- **选项集**：这种维度是一组值的固定枚举。
- **基于实体的值**：这种维度可以是一组可变值。

## <a name="pricing-dimensions"></a>定价维度

Dynamics 365 Project Operations 随附了一组默认定价维度。 可通过转到 **Project Operations** > **参数** 查看这些定价维度。 在参数记录中 **基于金额的定价维度** 选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段 **适用于销售** 和 **适用于成本** 是否设置为 **是**。 启用这些字段后，您可以为每个角色与部门的组合设置价格和成本。

![“适用于销售”已突出显示的 Project Service 参数的屏幕截图](media/PS-OOB-parameters.png)

如果需要使用更多属性制订资源的价格或成本，可以创建自定义的字段、实体和维度。 有关详细信息，请参阅以下文主题。 
  
  > [!NOTE]
  > 必须按列出的顺序完成这些步骤。

1. [为自定义定价维度创建解决方案](../sales/create-solution-custompd.md)
2. [创建自定义字段和实体](create-custom-fields-entities-pricing-dimensions.md)
3. [为价格设置和交易实体添加自定义字段](add-custom-fields-price-setup-transactional-entities.md)
4. [将自定义字段设置为定价维度](set-up-custom-fields-pricing-dimensions.md)
5. [更新插件属性以包括新定价维度](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>为人力资源时间定价
组织如何为人力资源时间定价通常是直接影响组织利润率的重要战略注意事项。 当组织准备好确定希望如何设置人力资源时间的记帐费率和成本费率时，请与财务团队和业务主管合作。

有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。 **交易类别** (**msdyn_transactioncategory**) 和 **可预订资源** (**bookableresource**) 之类字段就是候选维度。 

应注意定价维度应该是表还是选项集。 如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，可以创建非选项集实体。 若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数用户可以向表添加新行。

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