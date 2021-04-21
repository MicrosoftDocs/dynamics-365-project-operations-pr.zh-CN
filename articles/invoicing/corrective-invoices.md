---
title: 创建更正基于项目的发票
description: 此主题提供有关 Project Operations 的更正发票的信息。
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788836"
---
# <a name="create-corrective-project-based-invoices"></a>创建更正基于项目的发票 

_**适用于：** 面向资源/非库存场景的 Project Operations_

确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。

若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。 

> [!NOTE]
> 除非项目发票已确认，否则此选择不可用。

将从已确认的发票创建新的草稿发票。 之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。 以下是一些要点，可帮助您详细了解有关新更正发票的行详细信息：

- 所有数量都更新为零。 这假定已开发票的所有项目已全部贷记。 如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。 根据您输入的数量，应用程序将计算贷记的数量。 在确认更正发票时，此金额会反映在创建的实际值中。 如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。
- 里程碑更正始终处理为完全贷记。
- 如果客户开票的金额不正确，可以更正保留款或预付款金额。
- 如果使用了不正确的金额与之前确认的发票上的费用对帐，可以更正保留款或预付款的对帐。

> [!IMPORTANT]
> 用于更正其他已开票费用的发票明细详细信息的 **更正** 字段设置为 **是**。 包含更正发票明细详细信息的发票具有名为 **具有更正** 的字段，此字段也会设置为 **是**。

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>确认纠正发票时创建的实际值

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
            <td width="216" rowspan="4" valign="top">
                <p>
确认已开票预付款或保留款的更正。<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
为对帐创建的保留款或预付款的未记帐销售额冲销。 此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
将为保留款或预付款中的金额创建已记帐销售额冲销实际值，以冲销原始已记帐销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
将为基于保留款或预付款的更正发票明细上的更正金额创建新的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
基于保留款或预付款的更正发票明细的负金额的未记帐实际销售额，将用于对帐。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
确认之前对帐的保留款或预付款的更正。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
为对帐创建的保留款或预付款的未记帐销售额冲销。 此金额为正值，用于取消之前对帐发生时创建的负值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
之前发票上金额的已记帐销售额冲销实际值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
更正发票上应用的更正保留款金额的新的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
具有更正的剩余保留款或预付款的负金额的未记帐实际销售额，将用于以后发票的对帐。
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
里程碑上的发票状态从<b>客户发票已过帐</b>更新为<b>已准备好开单</b>。
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
不支持 </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
