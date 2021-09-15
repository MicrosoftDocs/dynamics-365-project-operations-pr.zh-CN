---
title: 产品的分包合同子项
description: 本主题介绍如何记录c产品的分包合同子项，以及如何使用各字段记录向供应商购买产品。
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323675"
---
# <a name="subcontract-lines-for-products"></a>产品的分包合同子项

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Dynamics 365 Project Operations 中的分包合同中可以包含产品的分包合同子项。 这些子项允许项目经理向供应商购买可购买的产品，然后将其用于项目任务。

若要在 Project Operations 中为产品创建分包合同子项，请完成以下步骤。

1. 在导航页中，选择 **分包合同**，然后打开要处理的分包合同。 
2. 在 **分包合同子项** 选项卡中，选择 **+ 新建** 创建一个新的分包合同子项。
3. 在 **快速创建** 页的 **交易分类** 字段中，选择 **材料**，然后输入或选择必填字段信息。 
4. 选择 **保存**。

下表提供有关 **分包合同子项详细信息** 页和 **快速创建** 页中的字段的信息，因为其与购买产品有关。

| 字段 | 描述 |
| ----- | ----------- |
| 客户 | 分包合同子项的名称。 |
| 描述 | 分包合同子项中正在订购的产品的简短说明。 |
| 线路类型 | 此字段值默认为 **基于数量**。 |
| 记帐方法 |  分包合同子项的记帐方法。 固定价格记帐方法可使用基于里程碑的发票计划。 |
| 交易分类 | 此字段值默认为 **时间**。 若要为购买产品创建分包合同子项，请在 **交易分类** 字段中选择 **材料**。 此选择指示分包合同子项用于记录要在项目中使用的产品的购买。 |
| 选择产品 | 选择正在购买的产品在产品目录中有，还是是目录外产品。 |
| 产品 | 从目录中选择有效产品。 仅当 **选择产品** 设置为 **现有** 时，此字段才可用。 |
| 目录外产品 | 输入目录外产品的名称。 仅当 **选择产品** 设置为 **目录外** 时，此字段才可用。  |
| 请求的交付日期 | 选择产品所需的交付日期。 此日期也用于从分包合同的附加项目价目表提取项目价目表。 然后，分包合同子项中的产品成本默认取自该价目表。 |
| 合同交付日期 | 选择合同中同意的产品交付日期。  |
| 已订购数量 | 输入正在向供应商购买的产品的数量。 如果项目经理透支了此数量，将出现警报。 |
| 单位组 | 该值默认仅针对目录产品。 如果同时选择了 **产品** 和 **请求的交付日期**，系统将根据交付日期选择适合的价目表。 将查询相关价目表项以查找匹配的产品。 计价单位和计价单位组默认取自价目表项记录。 |
| 计价单位 | 此值默认为价目表项记录中设置的计价单位。 可以根据需要将此值更改为其他计价单位。 产品和计价单位的组合用于设置现有目录产品的分包合同子项中的默认单价。 |
| 单价 | 单价默认值的确定方法是，使用与适用于分包合同子项请求的交付日期的项目价目表有关的价目表项中的产品和计价单位的组合。  |
| 小计 | 如果同时在两个字段中均输入了值，则此只读字段值的计算方法为“数量 x 单价”。 如果 **数量** 字段和/或 **单价** 字段为空，可以手动输入值。  |
| 销售税 | 输入销售税值。 |
| 总额 | 此计算字段显示分包合同的含税总金额。 此字段中的值的计算方法是小计 + 税。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]