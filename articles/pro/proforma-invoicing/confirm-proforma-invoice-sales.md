---
title: 确认估价项目账单
description: 本文提供有关在 Project Operations 中确认估价项目发票的信息。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922211"
---
# <a name="confirm-a-proforma-project-invoice"></a>确认估价项目账单 

_**适用于：** 精简部署 - 估价交易开票_


估价发票确认后，项目发票的状态将更新为 **已确认**。 发票确认后，将变为只读。 今后，仅当有客户发起的更正或信用额度时，才可以更正发票。

下表列出了系统创建的实际值。 在确认草稿项目发票之前对草稿项目发票执行某些操作时会创建这些实际值。

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
为预付款或保留款开票 </p>
            </td>
            <td width="408" valign="top">
                <p>
对于预付款或保留款中的金额，将创建类型为<strong>保留款</strong>的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
要用于对帐的负保留款或预付款金额的未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
对发票上的保留款或预付款完全对帐之后。
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
此发票上金额的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
对发票上的保留款或预付款部分对帐之后。
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
此发票上金额的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
要用于对未来发票进行对帐的剩余保留款或预付款金额的负未记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为草稿发票未进行任何编辑的时间交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间审批中时数和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始时间审批中时数和金额的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
为进行了编辑以减少数量的时间交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间审批中时数和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中扣除更正的数字后剩余时数不应计费的新未记帐实际销售额，实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为进行了编辑以增加数量的时间交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间审批中时数和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为草稿发票未进行任何编辑的支出交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始支出审批中数量和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始支出审批中数量和金额的已记帐实际销售额 </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
为进行了编辑以减少数量的支出交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始支出审批中数量和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为进行了编辑以增加数量的支出交易开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始支出审批中数量和金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
在未对草稿发票进行任何编辑的情况下对材料交易开具发票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始材料使用审批中数量和金额的未记帐销售冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始材料使用审批中数量和金额的记帐销售实际值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
对为减少数量而编辑的材料交易开具发票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始时间使用审批中数量和金额的未记帐销售冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
对为增加数量而编辑的材料交易开具发票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始材料使用审批中数量和金额的未记帐销售冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
为费用开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始日记帐行中费用金额的未记帐销售额冲销。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始费用日记帐行中数量和金额的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
为里程碑开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
项目合同子项上原始里程碑上的里程碑金额的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
为基于产品的合同子项开票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
数量和金额来自基于产品的合同子项的产品明细的已记帐实际销售额。
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
