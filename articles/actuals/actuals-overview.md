---
title: 实际值
description: 此主题提供有关如何在 Microsoft Dynamics 365 Project Operations 中使用实际值的信息。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126292"
---
# <a name="actuals"></a>实际值 

_**适用于：** 面向资源/非库存场景的 Project Operations_

实际值是已完成的项目工作量。 它们是根据时间和支出条目以及日记帐条目和发票创建的。

## <a name="journal-lines-and-time-submission"></a>日记帐行和时间提交

有关时间条目的详细信息，请参阅[时间条目概述](../time/time-entry-overview.md)。

### <a name="time-and-materials"></a>时间和材料

当提交的时间条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。

### <a name="fixed-price"></a>固定价格

当提交的时间条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。

### <a name="default-pricing"></a>默认定价

有关创建默认价格的逻辑在日记帐行中。 时间条目中的字段值将复制到该日记帐行中。 这些值包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。

会影响默认定价的字段（如 **角色** 和 **部门**）用于确定日记帐行中的适当价格。 您可以在时间条目中添加自定义字段。 如果您希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。

## <a name="journal-lines-and-basic-expense-submission"></a>日记帐行和基本支出提交

有关支出条目的详细信息，请参阅[支出概述](../expense/expense-overview.md)。

### <a name="time-and-materials"></a>时间和材料

当提交的基本支出条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。

### <a name="fixed-price"></a>固定价格

当提交的基本支出条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。

### <a name="default-pricing"></a>默认定价

为支出输入默认价格的逻辑基于支出类别。 交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。 但是，默认情况下，将直接在成本和销售额的相关支出日记帐行中设置为价格本身输入的金额。

不能在支出条目中基于类别输入默认单价。

## <a name="use-entry-journals-to-record-costs"></a>使用条目日记帐记录成本

您可以使用条目日记帐记录材料、费用、时间、支出或税务交易类的成本或收入。 日记帐可以用于以下目的：

- 记录项目的材料实际成本和销售额。
- 将交易实际值从另一个系统移至 Microsoft Dynamics 365 Project Operations。
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
