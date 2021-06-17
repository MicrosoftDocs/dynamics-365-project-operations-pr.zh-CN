---
title: 实际值
description: 本主题提供有关如何在 Microsoft Dynamics 365 Project Operations 中使用实际值的信息。
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996600"
---
# <a name="actuals"></a>实际值 

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

实际值表示项目中已审阅和批准的财务和计划进度。 之所以创建它们，是因为审批了时间、支出、材料使用条目以及日记帐条目和发票。

## <a name="journal-lines-and-time-submission"></a>日记帐行和时间提交

有关时间条目的详细信息，请参阅[时间条目概述](../time/time-entry-overview.md)。

### <a name="time-and-materials"></a>时间和材料

当提交的时间条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。

### <a name="fixed-price"></a>固定价格

当提交的时间条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。

### <a name="default-pricing"></a>默认定价

有关创建默认价格的逻辑在日记帐行中。 时间条目中的字段值将复制到该日记帐行中。 这些值包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。

对默认定价有影响的字段（如 **角色** 和 **资源单位**）用于在日记帐行上确定相应的价格。 您可以在时间条目中添加自定义字段。 如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。 使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。 有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="journal-lines-and-basic-expense-submission"></a>日记帐行和基本支出提交

有关支出条目的详细信息，请参阅[支出概述](../expense/expense-overview.md)。

### <a name="time-and-materials"></a>时间和材料

当提交的基本支出条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。

### <a name="fixed-price"></a>固定价格

将提交的基本支出条目链接到映射至固定价格合同子项的项目时，系统会为成本创建一个日记帐行。

### <a name="default-pricing"></a>默认定价

为支出输入默认价格的逻辑基于支出类别。 交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。 对默认定价有影响的字段（如 **交易类别** 和 **单位**）用于在日记帐行上确定相应的价格。 不过，只有当价目表中的定价方法是 **单价** 时，这才起作用。 如果定价方式为 **按成本** 或 **成本加价**，则创建支出条目时输入的价格用于成本，并且会根据定价方式计算销售日记帐行上的价格。 

您可以对支出条目添加自定义字段。 如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。 使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。 有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="journal-lines-and-material-usage-log-submission"></a>日记帐行和材料使用日志提交

有关支出条目的详细信息，请参阅[材料使用日志](../material/material-usage-log.md)。

### <a name="time-and-materials"></a>时间和材料

当已提交的材料使用日志条目链接到映射至时间和材料合同子项的项目时，系统将创建两个日记帐行，一个是成本日记帐行，一个是未记帐销售的日记帐行。

### <a name="fixed-price"></a>固定价格

将提交的材料使用日志条目链接到映射至固定价格合同子项的项目时，系统会为成本创建一个日记帐行。

### <a name="default-pricing"></a>默认定价

用于输入材料默认价格的逻辑基于产品和单位组合。 交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。 对默认定价有影响的字段（如 **产品 ID** 和 **单位**）用于在日记帐行上确定相应的价格。 不过，这仅对目录产品有效。 对于目录外产品，创建材料使用日志条目时输入的价格用于日记帐行上的成本和销售价格。 

您可以对 **材料使用日志** 条目添加自定义字段。 如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。 使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。 有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="use-entry-journals-to-record-costs"></a>使用条目日记帐记录成本

您可以使用条目日记帐记录材料、费用、时间、支出或税务交易类的成本或收入。 日记帐可以用于以下目的：

- 将交易实际值从另一个系统移到 Microsoft Dynamics 365 Project Operations。
- 记录另一个系统中发生的成本。 这些成本可能包括采购成本或分包成本。

> [!IMPORTANT]
> 应用程序不验证日记帐行类型或在日记帐行中输入的相关定价。 因此，只有完全了解实际值对项目产生的会计影响的用户才应使用条目日记帐创建实际值。 由于此日记帐类型的影响，您应该仔细选择有权创建条目日记帐的人。

## <a name="record-actuals-based-on-project-events"></a>基于项目事件记录实际值

Project Operations 记录项目期间发生的财务交易。 这些交易记录为实际值。 下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>资源与项目的合同签订部门属于同一个部门

<table>
<thead>
<tr>
<th rowspan="3">事件</th>
<th colspan="4">可记帐项目或已售项目</th>
<th rowspan="3">售前阶段的项目</th>
<th rowspan="3">内部项目</th>
</tr>
<tr>
<th colspan="2">时间和材料</th>
<th colspan="2">固定价格</th>
</tr>
<tr>
<th>实际</th>
<th>交易货币</th>
<th>固定价格</th>
<th>交易货币</th>
</tr>
</thead>
<tbody>
<tr>
<td>创建时间条目。</td>
<td colspan="6">实际值条目中无活动</td>
</tr>
<tr>
<td>提交时间条目。</td>
<td colspan="6">实际值条目中无活动</td>
</tr>
<tr>
<td rowspan="2">批准时间，并且审批期间可记帐工时不变或不增加。</td>
<td>成本实际值</td>
<td>合同签订部门货币</td>
<td rowspan="2">实际成本</td>
<td rowspan="2">合同签订部门货币
<td rowspan="2">成本实际值</td>
<td rowspan="2">成本实际值</td>
</tr>
<tr>
<td>未记帐实际销售额 – 应计费</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="3">批准时间，并且审批期间可记帐工时不变或不减少。</td>
<td>实际成本</td>
<td>合同签订部门货币</td>
<td rowspan="3">实际成本</td>
<td rowspan="3">合同签订部门货币</td>
<td rowspan="3">实际成本</td>
<td rowspan="3">实际成本</td>
</tr>
<tr>
<td>未记帐实际销售额 – 新数量的应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>未记帐实际销售额 – 差额的非应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="2">确认发票，并且审批期间可记帐工时不变或不增加。</td>
<td>未记帐销售额冲销</td>
<td>项目合同货币</td>
<td rowspan="2">里程碑的已记帐销售额</td>
<td rowspan="2">项目合同货币</td>
<td rowspan="2">不适用</td>
<td rowspan="2">不适用</td>
</tr>
<tr>
<td>已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="3">确认发票，并且可记帐工时减少。</td>
<td>未记帐销售额冲销</td>
<td>项目合同货币</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
</tr>
<tr>
<td>已记帐销售额 – 新数量的应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>已记帐实际销售额 – 差额的非应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="2">更正发票以增加应计费数量。</td>
<td>已记帐销售额 - 冲销</td>
<td>项目合同货币</td>
<td rowspan="5">
<ul>
<li>里程碑的已记帐销售额冲销</li>
<li>里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></li>
</ul>
</td>
<td rowspan="5">项目合同货币</td>
<td rowspan="5">不适用</td>
<td rowspan="5">不适用</td>
</tr>
<tr>
<td>已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="3">更正发票以减少应计费数量。</td>
<td>已记帐销售额 - 冲销</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>新数量的已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>未记帐销售额 – 差额的应计值</td>
<td>项目合同货币</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>资源与项目的合同签订部门不属于同一个部门

<table>
<thead>
<tr>
<th rowspan="3">事件</th>
<th colspan="4">可记帐项目或已售项目</th>
<th rowspan="3">售前阶段的项目</th>
<th rowspan="3">内部项目</th>
</tr>
<tr>
<th colspan="2">时间和材料</th>
<th colspan="2">固定价格</th>
</tr>
<tr>
<th>实际</th>
<th>交易货币</th>
<th>固定价格</th>
<th>交易货币</th>
</tr>
</thead>
<tbody>
<tr>
<td>创建时间条目。</td>
<td colspan="6">实际值条目中无活动</td>
</tr>
<tr>
<td>提交时间条目。</td>
<td colspan="6">实际值条目中无活动</td>
</tr>
<tr>
<td rowspan="4">批准时间，并且审批期间可记帐工时不变或不增加。</td>
<td>成本实际值</td>
<td>合同签订部门货币</td>
<td rowspan="4">实际成本</td>
<td rowspan="4">合同签订部门货币</td>
<td rowspan="4">成本实际值</td>
<td rowspan="4">成本实际值</td>
</tr>
<tr>
<td>未记帐实际销售额 – 应计费</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>资源单位成本</td>
<td>资源单位货币</td>
</tr>
<tr>
<td>组织间销售</td>
<td>合同签订部门货币</td>
</tr>
<tr>
<td rowspan="5">批准时间，并且审批期间可记帐工时不变或不减少。</td>
<td>实际成本</td>
<td>合同签订部门货币</td>
<td rowspan="5">实际成本</td>
<td rowspan="5">合同签订部门货币</td>
<td rowspan="5">实际成本</td>
<td rowspan="5">实际成本</td>
</tr>
<tr>
<td>资源单位成本</td>
<td>资源单位货币</td>
</tr>
<tr>
<td>组织间销售</td>
<td>合同签订部门货币</td>
</tr>
<tr>
<td>未记帐实际销售额 – 新数量的应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>未记帐实际销售额 – 差额的非应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="2">确认发票，并且审批期间可记帐工时不变或不增加。</td>
<td>未记帐销售额冲销</td>
<td>项目合同货币</td>
<td rowspan="2">里程碑的已记帐销售额</td>
<td rowspan="2">项目合同货币</td>
<td rowspan="2">不适用</td>
<td rowspan="2">不适用</td>
</tr>
<tr>
<td>已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="3">确认发票，并且可记帐工时减少。</td>
<td>未记帐销售额冲销</td>
<td>项目合同货币</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
<td rowspan="3">不适用</td>
</tr>
<tr>
<td>已记帐销售额 – 新数量的应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>已记帐实际销售额 – 差额的非应计值</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="2">更正发票以增加应计费数量。</td>
<td>已记帐销售额 - 冲销</td>
<td>项目合同货币</td>
<td rowspan="5">
<ul>
<li>里程碑的已记帐销售额冲销</li>
<li>里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></li>
</ul>
</td>
<td rowspan="5">项目合同货币</td>
<td rowspan="5">不适用</td>
<td rowspan="5">不适用</td>
</tr>
<tr>
<td>已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td rowspan="3">更正发票以减少应计费数量。</td>
<td>已记帐销售额 - 冲销</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>新数量的已记帐销售额</td>
<td>项目合同货币</td>
</tr>
<tr>
<td>未记帐销售额 – 差额的应计值</td>
<td>项目合同货币</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
