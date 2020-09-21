---
title: 实际
description: 本主题提供有关项目实际值的信息。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749767"
---
# <a name="actuals"></a>实际

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

实际值是已完成的项目工作量。 可将项目实际值回溯到其源文档。 这些源文档包括时间、支出和日记帐条目，以及发票。

![如何将项目实际值跟踪到源文档](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>提交时间条目

在 PSA 中，为映射到时间和材料合同子项的项目提交时间条目时，将创建两个日记帐行。 一行针对成本，另一行针对未记帐销售。 为映射到固定价格合同子项的项目提交时间条目时，仅为成本创建一个日记帐行。 

有关输入默认价格的逻辑在日记帐行中。 时间条目中的所有字段值将复制到该日记帐行中。 这些字段中包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。 

会影响默认价格的字段（如**角色**和**部门**）会导致默认在日记帐行中输入相应价格。 如果在时间条目中添加自定义字段，并且希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。

## <a name="submitting-an-expense-entry"></a>提交支出条目

在 PSA 中，为映射到时间和材料合同子项的项目提交支出条目时，将创建两个日记帐行。 一行针对成本，另一行针对未记帐销售。 为映射到固定价格合同子项的项目提交支出条目时，仅为成本创建一个日记帐行。

用于输入支出的默认价格的逻辑基于在**支出条目**页中选择的支出类别。 交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。 但是，对于价格本身，默认情况下将直接在成本和销售额的相关支出日记帐行中设置用户输入的金额。

在当前 PSA 版本中，不能在支出条目中基于类别录入默认单价。

## <a name="using-journals-to-record-costs"></a>使用日记帐记录成本

在 PSA 中，日记帐用于记录材料、费用、时间、支出或税务交易分类的成本或收入。 日记帐有标题、行和**确认**操作。 下面是一些可能需要使用日记帐的场景：

- 必须记录项目的材料实际成本和销售额。
- 必须将交易实际值从另一个系统移到 PSA。
- 必须记录另一个系统中出现的成本，如采购成本或分包成本。

## <a name="recording-actuals-based-on-project-events"></a>基于项目事件记录实际值

PSA 记录项目期间发生的财务交易。 这些交易记录为**实际值**。 下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。

**资源与项目的合同签订部门属于同一个部门**

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

**资源与项目的合同签订部门不属于同一个部门**

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
