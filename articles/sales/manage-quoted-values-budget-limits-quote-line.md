---
title: 项目报价单明细概述
description: 本主题提供有关使用项目报价单明细进行项目工作的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858012"
---
# <a name="project-quote-lines-overview"></a>项目报价单明细概述

_**适用于：** 面向资源/非库存场景的 Project Operations_

基于项目的报价单明细用于帮助预估协定中的项目工作。 基于项目的报价单明细的结构可以通过以下概念为项目预估进行扩展：

- 记帐方法
- 项目映射
- 包括的交易类
- 上限
- 应计费设置
- 使用报价单明细详细信息的预估
- 报价单明细客户

下表提供了有关基于项目的报价单明细的 **常规** 选项卡上字段的信息。 这些字段帮助为项目工作的详细、全面的预估建立基础。

| **字段** | **说明** | **下游影响** |
| --- | --- | --- |
| 客户 | 应会帮助您识别正在预估的报价单的分散部分的报价单明细的名称。 | 将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 记帐方法 | 在从商机创建的报价单中，此值从商机明细中的相应字段复制。 此字段包括 Dynamics 365 Project Operations 支持的两个主要合同模型：</br>- 固定价格</br>- 时间和材料。| 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| Project | 使用此可选字段可以识别将用于交付此协定中的工作的项目。 将项目映射到报价单明细时，它将帮助设置应计费任务，还可以帮助将基于项目的预估作为报价单明细详细信息引入报价单明细。 当项目未映射到基于项目的报价单明细时，应通过创建每个报价单明细详细信息来手动创建预估。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 包括时间 | **是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的时间交易或人工成本。 **否** 值指示此报价单明细的预估中将不包括时间交易或人工成本。 **是** 值指示此报价单明细的预估中将包括时间交易或人工成本。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 包括支出 | **是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的支出成本。 **否** 值指示此报价单明细的预估中将不包括支出成本。 **是** 值指示此报价单明细的预估中将包括支出成本。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 包括费用 | **是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的费用。 **否** 值指示此报价单明细的预估中将不包括费用。 **是** 值指示此报价单明细的预估中将包括费用。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 配额数量 | 这是将针对此基于项目的报价单明细上预测的所有工作向客户报价的金额。 在从商机创建的报价单中，此值从商机明细中的 **客户预算** 字段复制。 当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的金额汇总。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 预计税款 | 这是一个可编辑字段，供用户在报价单明细中添加预估税款金额。 当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的税款金额汇总。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 税后报价金额 | 此字段是税后的报价单明细金额，是只读的。 此字段中的金额计算为 *报价金额 + 税款*。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 上限 | 此字段可编辑，仅在具有 **时间和材料** 计费方法的基于项目的报价单明细中可用。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |
| 客户预算 | 此字段可编辑，如果报价单是从商机创建的，此字段将从商机明细中的相应字段复制。 | 此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。 |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>基于项目的报价单明细的“常规”选项卡上字段的验证规则

**规则 1**：所选项目上的某个交易类只能包含在报价单的一个基于项目的报价单明细中。

**规则 2**：如果商机有多个报价单，可能存在来自不同报价单的报价单明细，它们均引用同一个项目并包含相同的交易类。

**规则 3**：如果报价单不属于同一商机，则不能包括同一个项目和交易类。

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>商机</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>报价单</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>报价单明细</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包括时间</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包括支出</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>添加</strong>
                </p>
                <p>
                    <strong>费用</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>有效/无效</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>原因</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
违反规则 #1。 P1 项目的时间、支出和费用包含在两个报价单明细 QL1 和 QL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
违反规则 #1。 P1 项目的时间和费用包含在两个报价单明细 QL1 和 QL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
P1 项目的时间和费用包含在 QL1 上。
P1 项目的支出包含在 QL2 中。
每个报价单明细中包含的内容没有重叠，因此是有效的。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
违反上方的规则 #1 </p>
                <p>
Q1 包含整个项目 P1 的时间、支出和费用。
                </p>
                <p>
QL2 包括整个项目 P1 的时间、支出和费用，与 Q1 中所包含的内容重叠。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
根据规则 #2，Q1 和 Q2 是同一个商机中的两个报价单，因此它们都可以针对项目的相同组件进行预估。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Q2 上的 QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
根据规则 #3，Q1 和 Q2 是不同商机中的两个报价单，因此它们不能针对项目的相同组件进行预估。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="48" valign="top">
                <p>
是 </p>
            </td>
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="54" valign="top">
                <p>
无效 </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
