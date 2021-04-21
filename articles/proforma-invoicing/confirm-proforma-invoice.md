---
title: 确认估价基于项目的发票
description: 此主题提供有关确认估价基于项目的发票的信息。
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867119"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>确认估价基于项目的发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

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
用于对帐的保留款或预付款为负金额的未记帐销售实际值。
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
一个新的未记帐销售实际值，在减去编辑的发票明行明细上的更正数字、销售实际值冲销和等值的已记帐销售实际值后，该未记帐销售实际值为非应计费。
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
原始支出审批中数量和金额的已记帐实际销售额。
                </p>
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
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
