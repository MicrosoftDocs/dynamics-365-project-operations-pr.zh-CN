---
title: 已更正发票 - 精简
description: 此主题提供有关 Project Operations 中的更正发票的信息
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274222"
---
# <a name="corrected-invoices---lite"></a>已更正发票 - 精简

_**适用于：** 精简部署 - 估价交易开票_

确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。

若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。 

> [!NOTE]
> 除非项目发票已确认，否则此选择不可用。

将从已确认的发票创建新的草稿发票。 之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。 以下是用于了解新的更正发票上的明细详细信息的一些要点：

- 所有数量都更新为零。 应用程序假定所有已开票的项均已完全贷记。 如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。 根据您输入的数量，应用程序将计算贷记的数量。 在确认更正发票时，此金额会反映在创建的实际值中。 如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。
- 之前已确认的基于产品的合同子项不会复制。 不支持在基于产品的项目发票上处理更正。
- 里程碑更正始终处理为完全贷记。
- 如果客户开票的金额不正确，可以更正保留款或预付款金额。
- 如果使用了不正确的金额与之前确认的发票上的费用对帐，可以更正保留款或预付款的对帐。

> [!IMPORTANT]
> 作为其他已开票费用的更正内容的发票明细详细信息，会将字段 **更正** 设置为 **是**。 包含更正发票明细详细信息的发票具有名为 **具有更正** 的字段，此字段也会设置为 **是**。

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>确认纠正发票时创建的实际值：

以下是应用程序在确认之前，基于对草稿纠正发票执行的操作确认纠正时创建的实际值。

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
项目合同子项上的里程碑发票或记帐状态将更新为 **可开票**。
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
        <tr>
            <td width="216" valign="top">
                <p>
之前已开票的基于产品的合同子项的贷记和更正。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
不支持 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]