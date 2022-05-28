---
title: 配置报价单明细的应计费组件
description: 此主题提供有关在基于项目的报价单明细上设置应计费和非应计费组件的信息。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598385"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>配置报价单明细的应计费组件 

_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_

基于项目的报价单明细具有 *包含* 组件和 *应计费* 组件概念。

包含组件受以下各项约束：

  - 计费方法和客户拆分
  - 上限 
  - 基于项目的报价单明细中定义的发票频率设置

包含组件的子集可以使用 **记帐类型** 字段标记为应计费。 **记帐类型** 字段是一个选项集，允许在报价单明细的上下文中使用以下值：

  - 应计费
  - 非应计费

应计费组件可以在任务、角色和交易类别中定义。

应计费在报价单明细的任务中定义，应用于该报价单明细中包括的所有交易类。 如果 **包含任务** 字段设置为 **整个项目** 或留空，**应计费任务** 选项卡将不可用。

应计费在报价单明细的角色中定义，仅应用于 **时间** 交易类。 如果 **包含时间** 字段在项目报价单明细中设置为 **否**，**应计费角色** 选项卡将不可用。

应计费在报价单明细的交易类别中定义，仅应用于 **支出** 交易类。 如果 **包含支出** 字段在项目报价单明细中设置为 **否**，**应计费类别** 选项卡将不可用。

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>将项目任务更新为应计费或非应计费

项目任务在特定的基于项目的报价单明细的上下文中可以是应计费或非应计费，这样可以进行以下设置。

如果基于项目的报价单明细包含 **时间** 和任务 **T1**，该任务将作为应计费与报价单明细关联。 如果有另一个包含 **支出** 的报价单明细，您可以将该报价单明细上的 **T1** 任务作为非应计费关联。 结果是，任务中记录的所有时间都为应计费，任务中记录的所有支出都为非应计费。

任务的计费类型可以通过更新 **报价单明细任务** 子网格上的 **计费类型** 字段在基于项目的报价单明细的 **应计费任务** 选项卡上配置。 或者，您可以更新显示与任务关联的报价单明细的项目任务计费设置中，子网格上 **计费类型** 字段中项目任务的计费类型。

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>将角色更新为应计费或非应计费

角色在特定的基于项目的报价单明细的上下文中可以为应计费或非应计费。

角色的计费类型可以通过更新 **应计费角色** 子网格上的 **计费类型** 字段在报价单明细的 **应计费角色** 选项卡上配置。

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>将交易类别更新为应计费或非应计费

交易类别在特定报价单明细中可以为应计费或非应计费。

交易的计费类型可以通过更新 **应计费类别** 子网格上的 **计费类型** 字段在报价单明细的 **应计费类别** 选项卡上配置。

### <a name="resolve-chargeability"></a>解析应计费
仅在以下情况下才会将为时间创建的估算或实际值视为应计费：

   - 报价单明细中包含 **时间**。
   - 在报价单明细上将 **角色** 配置为应计费。
   - 在报价单明细上将 **包括的任务** 设置为 **选定任务**。 

如果这三种情况属实，则还会将 **任务** 配置为应计费。 

仅在以下情况下才会将为支出创建的估算或实际值视为应计费： 

   - 报价单明细中包含 **支出**。
   - 在报价单明细上将 **交易类别** 配置为应计费。
   - 在报价单明细上将 **包括的任务** 设置为 **选定任务**。

如果这三种情况属实，则还会将 **任务** 配置为应计费。 

仅在以下情况下才会将为材料创建的估算或实际值视为应计费：

   - 报价单明细中包含 **材料**。
   - 在报价单明细上将 **包括的任务** 设置为 **选定任务**。

如果这两种情况属实，则还应将 **任务** 配置为应计费。 


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
时间实际值的计费：应计费 </p>
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
应计费 </p>
            </td>
            <td width="350" valign="top">
                <p>
时间实际值的计费：应计费 </p>
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
