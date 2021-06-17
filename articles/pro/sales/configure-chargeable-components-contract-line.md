---
title: 配置基于项目的合同子项的应计费组件
description: 此主题提供有关如何在 Project Operations 中向合同子项添加应计费组件的信息。
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003710"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>配置基于项目的合同子项的应计费组件

_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_

基于项目的合同子项具有 *包含* 组件和 *应计费* 组件。

包含组件是受以下各项约束的组件：

  - 计费方法和客户拆分
  - 上限 
  - 基于项目的合同子项上定义的发票频率设置

包含组件的子集可以使用 **记帐类型** 字段标记为应计费。 **记帐类型** 字段是一个选项集，允许在合同子项的上下文中使用以下值：

  - 应计费
  - 非应计费

应计费组件可以在任务、角色和交易类别中定义。

应计费在项目合同子项的任务中定义，应用于合同子项中包括的所有交易类。 如果合同子项上的 **包含任务** 字段为空或设置为 **整个项目**，**应计费任务** 选项卡将不可用。

在项目合同子项的角色中定义的应计费仅应用于 **时间** 交易类。 如果合同子项上的 **包含时间** 字段设置为 **否**，**应计费角色** 选项卡将不可用。

在项目合同子项的交易类别中定义的应计费仅应用于 **支出** 交易类。 如果 **包含支出** 字段设置为 **否**，**应计费类别** 选项卡将不可用。

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>将项目任务更新为应计费或非应计费

项目任务在特定合同子项上可以是应计费或非应计费，这样可以进行以下设置：

如果基于项目的合同子项包含 **时间** 和某个任务，**T1** 将作为应计费与其关联。 如果有另一个包含 **支出** 的合同子项，您可以将该合同子项上的 T1 任务作为非应计费关联。 结果是，任务中记录的所有时间都为应计费，所有支出都为非应计费。

任务的计费类型可以通过更新合同子项任务子网格上的 **计费类型** 字段在合同子项的 **应计费任务** 选项卡上配置。 或者，您可以更新显示与任务关联的合同子项的项目任务计费设置子网格上的 **计费类型** 字段。

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>将角色更新为应计费或非应计费

角色在特定合同子项上可以为应计费或非应计费。

角色的计费类型可以在合同子项的 **应计费角色** 选项卡上配置。 要执行此操作，请更新 **应计费角色** 子网格中的 **计费类型** 字段 。

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>将交易类别更新为应计费或非应计费

交易类别在特定合同子项上可以为应计费或非应计费。

交易的计费类型可以在基于项目的合同子项的 **应计费类别** 选项卡上配置。 要执行此操作，请更新 **应计费类别** 子网格中的 **计费类型** 字段 。

### <a name="resolve-chargeability"></a>解析应计费

仅在以下情况下才会将为时间创建的估算或实际值视为应计费：

   - 合同子项中包含 **时间**。
   - 在合同子项上将 **角色** 配置为应计费。
   - 在合同子项上将 **包括的任务** 设置为 **选定任务**。
 
 如果这三种情况属实，则还会将任务配置为应计费。 

仅在以下情况下才会将为支出创建的估算或实际值视为应计费：

   - 合同子项中包含 **支出**
   - 在合同子项上将 **交易类别** 配置为应计费
   - 在合同子项上将 **包括的任务** 设置为 **选定任务**
  
 如果这三种情况属实，则还会将 **任务** 配置为应计费。 

仅在以下情况下才会将为材料创建的估算或实际值视为应计费：

   - 合同子项中包含 **材料**
   - 在合同子项上将 **包括的任务** 设置为 **选定任务**

如果这两种情况属实，则还会将 **任务** 配置为应计费。 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>包括时间</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>包括支出</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>包括材料</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>包含的任务</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>角色</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>类别</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>任务</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>应计费影响</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>应计费</strong>
                </p>
                <p>
支出实际值的计费：<strong>应计费</strong>
                </p>
                <p>
材料实际值的计费类型：<strong>应计费</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>应计费</strong>
                </p>
                <p>
支出实际值的计费：<strong>应计费</strong>
                </p>
                <p>
材料实际值的计费类型：<strong>应计费</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费：应计费 </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>非应计费</strong>
                </p>
                <p>
材料实际值的计费类型：<strong>非应计费</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>非应计费</strong>
                </p>
                <p>
材料实际值的计费类型：<strong>非应计费</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>非应计费</strong>
                </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>应计费</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>不可用</strong>
                </p>
                <p>
支出实际值的计费：应计费 </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>不可用</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>非应计费</strong>
                </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="70" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：应计费 </p>
                <p>
支出实际值的计费类型：<strong>不可用</strong>
                </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>不可用</strong>
                </p>
                <p>
材料实际值的计费类型：应计费 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="70" valign="top">
                <p>
应计费 </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：应计费 </p>
                <p>
支出实际值的计费：应计费 </p>
                <p>
材料实际值的计费类型：<strong>不可用</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
是 </p>
            </td>
            <td width="78" valign="top">
                <p>
是 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
整个项目 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>非应计费</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
无法设置 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：<strong>非应计费</strong>
                </p>
                <p>
支出实际值的计费类型：<strong>非应计费</strong>
                </p>
                <p>
材料实际值的计费类型：<strong>不可用</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
