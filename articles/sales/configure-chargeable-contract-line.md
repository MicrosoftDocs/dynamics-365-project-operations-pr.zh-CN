---
title: 配置基于项目的合同子项的应计费组件
description: 此主题提供有关在合同子项上的包含、应计费和非应计费组件的信息。
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278677"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>配置基于项目的合同子项的应计费组件

_**适用于：** 面向资源/非库存场景的 Project Operations_

基于项目的合同子项具有包含组件、应计费组件和非应计费组件概念。

包含组件受基于项目的合同子项上定义的计费方法、客户拆分、上限以及发票频率设置的限制。

包含组件的子集可以通过更新 **记帐类型** 字段标记为应计费。

应计费组件可以在角色和交易类别中定义。

对于项目合同子项，角色中定义的应计费仅应用于 **时间** 交易类。 如果 **包含时间** 在项目合同子项上设置为 **否**，**应计费角色** 选项卡将不可用。

在项目合同子项的交易类别中定义的应计费仅应用于 **支出** 交易类。 如果 **包含支出** 在项目合同子项上设置为 **否**，**应计费类别** 选项卡将不可用。

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>将角色更新为应计费或非应计费

角色在特定的基于项目的合同子项上可以为应计费或非应计费。

在基于项目合同子项的 **应计费角色** 选项卡上，在 **应计费类别** 子网格中的 **计费类型** 字段中，更新角色的计费类型。

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>将交易类别更新为应计费或非应计费

交易类别在特定的基于项目的合同子项上可以为应计费或非应计费。

在基于项目合同子项的 **应计费类别** 选项卡上，在 **应计费类别** 子网格中的 **计费类型** 字段中，更新交易的计费类型。

### <a name="resolve-chargeability"></a>解析应计费

仅在合同子项上包含时间且角色在合同子项上配置为应计费时，为时间创建的估计值或实际值才会被视为应计费。

仅在合同子项上包含支出且交易类别在合同子项上配置为应计费时，为支出创建的估计值或实际值才会被视为应计费。

| 包括时间 | 包括支出 | 角色 | 类别 | 任务 |
| --- | --- | --- | --- | --- |
| 是 | 是 | 应计费 | 应计费 | 时间实际值的计费：应计费 </br>支出实际值的计费：应计费 |
| 是 | 是 | 非应计费 | 应计费 | 时间实际值的计费：非应计费 </br>支出实际值的计费：应计费 |
| 是 | 是 | 非应计费 | 非应计费 | 时间实际值的计费：非应计费 </br>支出实际值的计费：非应计费 |
| No | 是 | 无法设置 | 应计费 | 时间实际值的计费：不可用 </br>支出实际值的计费：应计费 |
| No | 是 | 无法设置 | 非应计费 | 时间实际值的计费：不可用 </br>支出实际值的计费：非应计费 |
| 是 | No | 应计费 | 无法设置 | 时间实际值的计费：应计费 </br>支出实际值的计费：不可用 |
| 是 | No | 非应计费 | 无法设置 | 时间实际值的计费：非应计费 </br> 支出实际值的计费：不可用 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]