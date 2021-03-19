---
title: 确认估价账单
description: 本主题提供有关确认估价账单的信息。
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287857"
---
# <a name="confirm-a-proforma-invoice"></a>确认估价账单

_**适用于：** 面向资源/非库存场景的 Project Operations_

估价发票确认后，项目发票的状态将更新为 **已确认**。 发票确认后，将变为只读。 之后，只有在发票标记为已支付的情况下，在有任何客户发起更正或贷记时才可以更正发票。

下表列出了系统创建的实际值。 在确认草稿项目发票之前对草稿项目发票执行某些操作时会创建这些实际值。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>方案</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>确认时创建的实际值</strong>
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
编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
编辑的发票明细详细信息中扣除更正的数字后剩余时数不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。
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
编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和已记帐实际销售额的对等值。
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