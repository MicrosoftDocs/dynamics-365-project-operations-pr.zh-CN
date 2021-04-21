---
title: 基于项目的合同子项概述
description: 此主题提供有关处理基于项目的合同子项的信息。
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858147"
---
# <a name="project-based-contract-lines-overview"></a>基于项目的合同子项概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 中的基于项目的合同子项用于保留参与项目中项目工作特定组成部分的估算和计费协议。 基于项目的合同子项的结构已针对存在以下概念的项目估算和计费方案扩展：

- 计费方法
- 项目和任务映射
- 包括的交易类
- 上限
- 应计费设置
- 使用合同子项详细信息估算
- 合同子项客户

下表包括基于项目的合同子项的 **常规** 选项卡上的字段，这些字段帮助为基于项目的工作设定详细的基础估算和计费安排的基础。

| 字段 | 描述 | 下游影响 |
| --- | --- | --- |
| **客户** | 合同子项的名称。 标识正在估算的合同的独立部分。 对于从报价单创建的项目合同，从基于项目的报价单明细的相应值复制此值。 | 创建发票时复制到从此合同子项创建的项目发票明细的名称。 |
| **记帐方法** | 在从报价单创建的项目合同上，从报价单明细上的相应字段复制此值。 这是一个选项集，代表 Project Operations 支持的两个主要合同签订模型：</br>- **固定价格**</br>- **时间和材料** | 根据引用的合同子项的计费方法，将处理实际交易。 如果实际值引用的合同子项具有时间和材料计费方法，将创建成本和未记帐实际销售额记录。 如果实际值引用的合同子项具有固定价格计费方法，将仅创建成本实际值。 |
| **Project** | 使用此字段来标识将用于交付此参与项目中的工作的项目。 | 该值将与 **包含的任务** 和 **包含的交易分类** 结合使用，以解析实际或估计行记录中的合同子项参考。 |
| **包含的任务** | 指示此合同子项是包含所选项目的所有项目任务，还是只包含部分任务。 这是具有以下可能值的选项集：</br>- **所有项目任务**</br>- **仅所选项目任务**。 此字段中的空值等同于选择 **所有项目任务**。 | 如果选择 **仅所选任务**，则可以在 **项目** 页面上的 **任务计费设置** 选项卡上选择特定任务并将其与此合同子项关联。 此值将与 **项目** 和 **包含的交易** 类结合使用，来解析实际或估算明细记录中的合同子项引用。 |
| **包括时间** | **是**/**否** 值指明所选项目的时间交易或人工成本是否将包含在此合同子项中。 **否** 值指示时间交易或人工成本将不包括在此合同子项中。 **是** 值指示包括。 | 该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。 |
| **包括支出** | **是**/**否** 值指明所选项目的支出成本是否将包含在此合同子项中。 **否** 值指示支出成本将不包括在此合同子项中。 **是** 值指示包括。 | 该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。 |
| **包括材料** | **是**/**否** 值指明所选项目的材料成本是否将包含在此合同子项中。 **否** 值指明材料成本将不包含在此合同子项中。 **是** 值指示包括。 | 该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。 |
| **包括费用** | **是**/**否** 值指明所选项目的费用是否将包含在此合同子项中。 **否** 值指示费用将不包括在此合同子项中。 **是** 值指示包括。 | 该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。 |
| **合同金额** | 在固定价格合同子项上，此金额是将为与此合同子项关联的所有工作组成部分向客户开票的商定值。 在时间和材料合同子项上，此金额是将为与此合同子项关联的所有工作组成部分向客户开票的估计值。 在从报价单创建的项目合同上，从报价单明细上的相应字段复制此值。 当基于项目的合同子项具有明细详细信息时，此字段将被锁定以进行编辑，值从合同子项详细信息中的金额汇总得出。 | 当合同子项具有明细详细信息时，可以通过更改明细详细信息中的金额来修改此值。 在固定价格合同子项中，此值用于生成定期计费里程碑上的税前金额。 |
| **预计税款** | 用户可以编辑此字段来在合同子项上输入估算税额。 当基于项目的合同子项具有明细详细信息时，此字段将被锁定以进行编辑，值从合同子项详细信息中的税额汇总得出。 | 当合同子项具有明细详细信息时，可以通过更改明细详细信息中的税额来修改此值。 在固定价格合同子项中，此值用于生成定期计费里程碑上的税款。 |
| **税后合同金额** | 税后合同子项金额。 此字段为只读字段，计算公式为 **合同金额 + 税款**。 | 在固定价格合同子项中，此值用于生成定期计费里程碑。 |
| **上限** | 用户可以编辑此字段，它仅在将计费方法设置为时间和材料的基于项目的合同子项上可用。 | 用户可以编辑此字段。 当时间和材料的实际值引用此合同子项以获取时间和材料值时，实际值中的金额将根据合同子项中的上限计算。 此计算在计入已花费和提交的金额后完成。 |
| **客户预算** | 如果合同是从报价单创建的，此字段可以编辑，值从报价单明细上的相应字段复制。 | 此字段仅用于提供信息，对下游没有任何意义。 |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>基于项目的合同子项的“常规”选项卡上选项的验证规则

规则 1：如果 **包含的任务** 字段为空或设置为 **所有项目任务**，项目的所有任务都将包含在合同子项中。

规则 2：当 **包含的任务** 字段为空或明确设置为 **所有项目任务** 时，项目和特定交易类只能包含在合同的一个基于项目的合同子项中。

规则 3：当 **包含的任务** 字段设置为 **仅所选项目任务** 时，项目和特定交易类可以包含在合同的多个基于项目的合同子项中。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>合同</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>合同子项</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>包含的任务</strong>
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
                    <strong>包括材料</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>有效/无效</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>原因</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
违反规则 #2。 P1 项目的时间、支出、材料和费用均包含在合同子项 CL1 和 CL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
违反规则 #2。 P1 项目的时间、材料和费用均包含在合同子项 CL1 和 CL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 项目的时间、材料和费用包含在 CL1 中。
                </p>
                <ul>
                    <li>
P1 项目的支出包含在 CL2 中。
                    </li>
                </ul>
                <p>
每个合同子项中包含的内容均无重叠，因此有效。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
仅所选任务 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
无效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
违反规则 #2 </p>
                <p>
C1 包括项目 P1 中任务子集的时间、材料、支出和费用。
                </p>
                <p>
CL2 包括整个项目 P1 的时间、材料、支出和费用，因此与 C1 中包含的内容重叠。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
仅所选任务 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
根据规则 #3 </p>
                <p>
C1 包括项目 P1 中任务子集的时间、支出、材料和费用。
                </p>
                <p>
CL2 包括项目 P1 中任务子集的时间、支出、材料和费用。
                </p>
                <p>
唯一的额外验证是验证 CL1 上的任务子集是否与 CL2 上的任务子集不同，以确保没有重叠。 当任务关联时，这由系统完成。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
仅所选任务 </p>
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
            <td width="42" valign="top">
                <p>
是 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
