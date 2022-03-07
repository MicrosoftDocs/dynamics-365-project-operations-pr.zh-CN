---
title: 将交易类别用作定价维度
description: 本主题提供有关如何使用“交易类别”字段作为定价维度的信息。
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8093aca9a33bbbaef41c6fc7d33cad930bfadd13b0f7587c3de9032ac0d630
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996110"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>将交易类别用作定价维度


_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


本主题说明了如何将 **交易类别** 字段用作定价维度。 

## <a name="prerequisites"></a>先决条件
在完成本主题中的步骤之前，您必须为组织提供一个新的定价维度解决方案。 如果尚未创建，请参阅[创建自定义字段和实体作为定价维度](create-custom-fields-entities-pricing-dimensions.md)。

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>向窗体和视图添加“交易类别”字段
若要使 **交易类别** 字段显示在定价维度解决方案中，您需要将此字段作为实体添加到所有窗体和视图中。

下表按实体列出了所有现成的窗体和视图。 您还需要将新字段添加到自定义实体中的任何其他窗体或视图。

|  Entity        | 表单     |视图        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色价格| 信息 |- 可用的资源类别价格<br> - 关联的资源类别价格 |
|  角色价格加价| 信息|- 可用角色价格加价<br>- 关联的角色价格加价 |
|  报价单明细详细信息|- 项目信息<br>- 项目快速创建| - 可用的报价单明细详细信息<br>- 合并的报价单明细详细信息<br>- 关联的报价单明细详细信息 |
|  项目合同子项详细信息|- 项目信息<br>- 项目快速创建|- 合并的合同子项详细信息<br>- 可用的合同子项详细信息<br>- 关联的合同子项详细信息 |
|  项目任务|- 信息<br>- 新窗体| &nbsp; |
|  项目团队成员|- 信息<br>- 新窗体|- 可用的项目团队成员<br>- 项目团队成员<br>- 关联的项目团队成员 |
|  时间条目|- 信息<br>- 创建时间条目|- 我的按日期列出的时间条目<br>- 我本周的时间条目<br>- 供审批的时间条目|
|  日记帐行|- 信息<br>- 快速创建|- 可用的日记帐行<br>- 关联的日记帐行|
|  发票明细详细信息|- 信息<br>- 快速创建|- 可用的发票明细详细信息<br>- 应计费发票交易记录<br>- 免费发票交易<br>- 关联的发票明细详细信息 <br>- 非应计费发票交易|
|  实际|- 信息<br>- 可用的实际值| 关联的实际项 |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>将“交易类别”字段设置为定价维度

1. 转到 **设置** > **参数**。 
2. 在 **参数** 页上的 **基于金额的定价维度** 选项卡上，验证网格是否显示 **定价维度** 实体中的记录。
3. 向此列表添加 **交易类别**，然后将 **适用于成本** 和 **适用于销售** 字段设置为 **是**。
4. 在 **维度类型** 字段中，选择 **基于金额**，然后选择与成本和销售有关的 **交易类别** 的优先级。


[!INCLUDE[footer-include](../includes/footer-banner.md)]