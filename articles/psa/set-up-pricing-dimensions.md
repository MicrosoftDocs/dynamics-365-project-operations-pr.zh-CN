---
title: 将自定义字段设置为定价维度
description: 此主题介绍如何设置自定义定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150342"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>将自定义字段设置为定价维度 

[!include [banner](../includes/psa-now-project-operations.md)]

首先，此主题假设您已完成了主题[创建自定义字段和实体](create-custom-fields-entities.md)和[向价格设置和交易实体添加自定义字段](field-references.md)中的过程。 如果尚未完成这些过程，请回去完成，然后回到此主题。 

此主题介绍如何设置自定义定价维度。 Project Service Web 界面中 **参数** 页 **基于金额的定价维度** 选项卡显示定价维度实体中的记录。 默认情况下，安装 Project Service 将在此选项卡上的网格中创建2 行：

- **msdyn_resourcecategory**（角色）
- **msdyn_OrganizationalUnit**（部门）

> [!IMPORTANT]
> 请勿删除这些行。 但是如果不需要，可以通过将 **适用于成本**、**适用于销售** 和 **适用于购买** 全部设置为 **否**，使其在特定上下文中不可用。 将这些属性值设置为 **否** 与将该字段设置为定价维度的效果相同。

要使字段成为定价维度，该字段必须：

- 创建为 **角色价格** 和 **角色价格加价** 实体中的字段。 有关如何执行此操作的详细信息，请参阅[向价格设置和交易实体添加自定义字段](field-references.md)。
- 创建为 **定价维度** 表中的行。 例如，添加定价维度行，如下图中所示。 

![基于金额的定价维度行](media/Amt-based-PD.png)

请注意，资源工作时间 (**msdyn_resourceworkhours**) 已作为基于加价的维度添加，并已添加到 **基于加价的定价维度** 选项卡上的网格中。

![基于加价的定价维度行](media/Markup-based-PD.png)

> [!IMPORTANT]
> 仅当刷新了缓存，才会把对此表中定价维度数据进行的任何更改传播到 Project Service 定价逻辑。 缓存刷新时间最多可能需要 10 分钟。 留出这样长的时间，以便查看一定会导致定价维度数据更改的价格默认设置逻辑更改。


## <a name="attributes-of-the-pricing-dimensions-table"></a>“定价维度”表的属性
以下部分介绍 **定价维度** 表中的不同属性。

### <a name="pricing-dimension-name"></a>定价维度名称
此值应该与添加到自定义定价维度的 **角色价格** 表中的字段的架构名称完全相同。 有关将字段添加到 **角色价格** 表的详细信息，请参阅[向价格设置和交易实体添加自定义字段](field-references.md)。

### <a name="type-of-dimension"></a>维度类型
有两种类型的定价维度：
  
  - **基于金额的维度**：将把来自输入上下文的维度值与 **角色价格** 明细中的维度值进行匹配，而默认价格/成本则直接从 **角色价格** 表中提取。
  - **基于加价的维度**：在这些维度中，Project Service 采用下面的三步式流程获取价格/成本。
 
    1. Project Service 将来自输入上下文的，基于非加价的维度值与角色价格明细进行匹配以获取基础费率。
    2. Project Service 将来自输入上下文的所有的维度值与 **角色价格加价** 明细进行匹配以获取加价百分比。
    3. Project Service 将第二步的加价百分比应用于第一步中从 **角色价格** 表获取的基础费率以获取最终价格/成本。
   
   下表介绍价格加价的计算。
  
| 角色        | 部门    |工作位置      |标准标题      |资源工作时间      |  加价|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso 印度|现场            |                    |加班                 |15     |
|             | Contoso 印度|本地             |                    |加班                 |10     |
|             | Contoso US   |本地             |                    |加班                 |20     |


如果 Contoso 印度中一位基础费率为 100 美元的资源在现场工作，并且在时间条目中记录了 8 小时的正常工时和 2 小时的加班，Project Service 定价引擎将对 8 小时使用基础费率 100，从而记录 800 美元。 至于 2 小时的加班，则为基础费率 100 应用 15% 的加价，因此单价为 115 美元，记录的总成本为 230 美元。

### <a name="applicable-to-cost"></a>适用于成本 
如果此项设置为 **是**，则指示在检索成本和加价费率时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。

### <a name="applicable-to-sales"></a>适用于销售
如果此项设置为 **是**，则指示在检索记帐和加价费率时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。

### <a name="applicable-to-purchase"></a>适用于购买
如果此项设置为 **是**，则指示在检索购买价格时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。 Project Service 目前不支持分包方案，因此不使用此字段。 

### <a name="priority"></a>优先级
设置维度优先级有助于 Project Service 定价生成价格，即使无法找到输入维度值与 **角色价格** 或 **角色价格加价** 表中的值之间的精确匹配项也不例外。 在此方案中，Project Service 通过按照维度的优先级为维度加权，对不匹配维度值使用空值。

- **成本优先级**：维度的成本优先级值指示与成本价格设置进行匹配时，该维度的权重。 **成本优先级** 的值在 **适用于成本** 的维度之间必须唯一。
- **销售优先级**：维度的销售优先级值指示与销售价格设置进行匹配时，该维度的权重。 **销售优先级** 的值在 **适用于销售** 的维度之间必须唯一。


[!INCLUDE[footer-include](../includes/footer-banner.md)]