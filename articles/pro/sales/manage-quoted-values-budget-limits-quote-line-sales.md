---
title: 基于项目的报价单明细概述
description: 此主题提供为项目工作使用基于项目的报价单明细的信息。
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a9661d9b91ffeece4c66b129846632b30ebebc8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591071"
---
# <a name="project-based-quote-lines-overview"></a>基于项目的报价单明细概述 

_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_

基于项目的报价单明细用于帮助预估协定中的项目工作。 基于项目的报价单明细的结构可以通过以下概念为项目预估进行扩展：

- 记帐方法
- 项目和任务映射
- 包括的交易类
- 上限
- 应计费设置
- 使用报价单明细详细信息的预估
- 报价单明细客户

下表提供了有关基于项目的报价单明细的 **常规** 选项卡上字段的信息。 这些字段帮助为项目工作的详细、全面的预估建立基础。

| **字段** | **说明** | **下游影响** |
| --- | --- | --- |
| 客户 | 报价单明细的名称，可帮助您确定估计的报价单的离散组件。 | 将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 记帐方法 | 在从商机创建的报价单中，此值从商机明细中的相应字段复制。 此字段包括 Dynamics 365 Project Operations 支持的两个主要合同模型：</br>- 固定价格</br>- 时间和材料。| 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| Project | 使用此可选字段可以识别将用于交付此协定中的工作的项目。 将项目映射到报价单明细时，它将帮助设置应计费任务，还可以帮助将基于项目的预估作为报价单明细详细信息引入报价单明细。 当项目未映射到基于项目的报价单明细时，应通过创建每个报价单明细详细信息来手动创建预估。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。|
| 包含的任务 | 指示此报价单明细是否用于所选项目的全部或部分项目任务。 此字段具有以下可能的值：</br>- 所有项目任务</br>- 仅所选项目任务</br>此字段中的空白值等效于 **所有项目任务** 选项。 | 如果在项目页上选择了 **仅限选定的项目任务**，则 **任务记帐设置** 选项卡允许您选择特定任务，以将这些任务与此报价单明细关联。 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 包括时间 | **是**/**否** 值指明所选项目的时间交易或人工成本是否将包含在此报价单明细估算中。 **否** 值指示此报价单明细的预估中将不包括时间交易或人工成本。 **是** 值指示此报价单明细的预估中将包括时间交易或人工成本。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 包括支出 | **是**/**否** 值指明所选项目的支出成本是否将包含在此报价单明细估算中。 **否** 值指示此报价单明细的预估中将不包括支出成本。 **是** 值指示此报价单明细的预估中将包括支出成本。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 包括材料 | **是**/**否** 值指明所选项目的材料成本是否将包含在此报价单明细估算中。 **否** 值指明材料成本将不包含在此报价单明细估算中。 **是** 值指明材料成本将包含在此报价单明细估算中。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 包括费用 | **是**/**否** 值指明所选项目的费用是否将包含在此报价单明细估算中。 **否** 值指示此报价单明细的预估中将不包括费用。 **是** 值指示此报价单明细的预估中将包括费用。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 配额数量 | 这是针对基于项目的报价单明细中预测的所有工作将向客户报价的金额。 在从商机创建的报价单中，此值从商机明细中的 **客户预算** 字段复制。 当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的金额汇总。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 预计税款 | 这是一个可编辑字段，供用户在报价单明细中添加预估税款金额。 当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的税款金额汇总。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 税后报价金额 | 此字段是税后的报价单明细金额，是只读的。 此字段中的金额计算为 *报价金额 + 税款*。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 上限 | 此字段可编辑，仅在具有 **时间和材料** 计费方法的基于项目的报价单明细中可用。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |
| 客户预算 | 此字段可编辑，如果报价单是从商机创建的，此字段将从商机明细中的相应字段复制。 | 该值复制到赢得报价单时从此报价单明细创建的项目合同子项。 |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>基于项目的报价单明细的“常规”选项卡上字段的验证规则

**规则 1**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目将包含在报价单明细中。

**规则 2**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目和特定交易类只能包含在报价单的一个基于项目的报价单明细中。

**规则 3**：如果 **包含的任务** 字段设置为 **仅所选项目任务**，项目和特定交易类可以包含在报价单的多个基于项目的报价单明细中。

**规则 4**：如果商机有多个报价单，可能存在来自不同报价单的报价单明细，它们均引用同一个项目并包含相同的交易类。

**规则 5**：如果报价单不属于同一商机，则不能包括同一个项目和交易类。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>商机</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>报价单</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>报价单明细</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>包含的任务</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>包括时间</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>包括支出</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>包括材料</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>添加</strong>
                </p>
                <p>
                    <strong>费用</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>有效/无效</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>原因</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
违反规则 #2。 P1 项目的时间、支出和费用包含在报价单明细 QL1 和 QL2 中 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
违反规则 #2。 P1 项目的时间、材料和费用包含在报价单明细 QL1 和 QL2 中 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1 项目的时间、材料和费用包含在 QL1 中 <br>
P1 项目的支出包含在 QL2 中 <br>
每个报价单明细中包含的内容均无重叠，因此有效。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
违反规则 #2 </p>
                <p>
Q1 包括项目 P1 中任务子集的时间、材料、支出和费用 </p>
                <p>
QL2 包含整个项目 P1 的时间、支出和费用，因此与 Q1 中包含的内容重叠。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
根据规则 #3， </p>
                <p>
Q1 包括项目 P1 中任务子集的时间、材料、支出和费用。
                </p>
                <p>
QL2 包括项目 P1 中任务子集的时间、材料、支出和费用。
                </p>
                <p>
唯一的额外验证是验证 QL1 上的任务子集是否与 QL2 上的任务子集不同，以确保没有重叠。 当任务关联时，这由系统完成。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
仅所选任务 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
所有项目任务或空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
按照规则 #5，Q1 和 Q2 是相同商机的两个报价单，因此可以对项目的相同组件对其进行估算。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
所有项目任务或空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
所有项目任务或空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
按照规则 #4，Q1 和 Q2 是不同商机的两个报价单，因此不能对相同项目的相同组件对其进行估算。
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
所有项目任务或空白 </p>
            </td>
            <td width="45" valign="top">
                <p>
是 </p>
            </td>
            <td width="46" valign="top">
                <p>
是 </p>
            </td>
            <td width="43" valign="top">
                <p>
是 </p>
            </td>
            <td width="41" valign="top">
                <p>
是 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
