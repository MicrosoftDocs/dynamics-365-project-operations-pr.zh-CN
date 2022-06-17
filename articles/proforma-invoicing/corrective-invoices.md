---
title: 更正基于项目的发票
description: 本文提供有关如何在 Project Operations 中创建和确认基于项目的更正发票的信息。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931089"
---
# <a name="corrective-project-based-invoices"></a>更正基于项目的发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。

若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。 

> [!NOTE]
> 除非已确认项目发票，或者基于项目的发票具有预付款或保留款，或具有预付款或保留款的对帐信息，否则将无法进行此选择。

将从已确认的发票创建新的草稿发票。 之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。 以下是用于了解新的更正发票上的明细详细信息的一些要点：

- 所有数量都更新为零。 Dynamics 365 Project Operations 假定已开发票的所有项目已全部贷记。 如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。 根据您输入的数量，应用程序将计算贷记的数量。 在确认更正发票时，此金额会反映在创建的实际值中。 如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。
- 里程碑更正始终处理为完全贷记。


> [!IMPORTANT]
> 对于用于更正其他已开票费用的发票明细详细信息，**更正** 字段设置为 **是**。 对于具有更正的发票明细详细信息的发票，**具有更正** 字段设置为 **是**。

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>确认更正发票后创建的实际值

下表列出了确认纠正发票后创建的实际值。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>方案</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>确认时创建的实际值</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为之前开票的时间交易的完全贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间发票明细详细信息中时数和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始时间发票明细详细信息中时数和金额的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
为时间交易中的部分贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间发票明细详细信息中已开票时数和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
扣除发票明细详细信息中的更正数字后，剩余时数和金额应计费的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为之前开票的支出交易的完全贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始支出发票明细详细信息中数量和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始支出发票明细详细信息中数量和金额的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
为之前开票的支出交易的部分贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始支出发票明细详细信息中已开票数量和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
更正后的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
对先前已开票材料交易的全部贷记开具发票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始材料发票明细详细信息中数量和金额的记帐销售冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始材料发票明细详细信息中数量和金额的新未记帐销售实际值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
对材料交易上的部分贷记开具发票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始材料发票明细详细信息中开票的数量和金额的记帐销售冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
一个新的未记帐销售实际值，对于编辑的发票明行明细上的数量和金额、其冲销和等值的已记帐销售实际值，该未记帐销售实际值为非应计费。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为之前开票的费用交易的完全贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始费用发票明细详细信息中数量和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始费用发票明细详细信息中数量和金额的新的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为之前开票的费用交易的部分贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始费用发票明细详细信息中已开票数量和金额的已记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑后的纠正发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
为之前开票的里程碑的完全贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始里程碑发票明细详细信息中金额的已记帐销售额冲销。
                </p>
                <p>
里程碑的发票状态从<b>客户发票已过帐</b>更新为<b>已准备好开单</b>。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
为之前开票的里程碑的部分贷记开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
不支持这种情况。
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
