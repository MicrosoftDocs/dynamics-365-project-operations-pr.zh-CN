---
title: 过帐支出报表
description: 本文介绍如何过帐支出报表。
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524858"
---
# <a name="post-expense-reports"></a>过帐支出报表

在支出报表被批准并转移到常规日记帐后，可以将其过帐。 在您过帐支出报表时，将标识符合增值税 (VAT) 退税条件的支出。 验证和退回增值税付款的任务将分配给负责验证支出报表的员工。

如果支出报表上的支出是由雇用该员工的公司以外的其他公司收取的，您必须同时验证这些支出所属于的公司和欠款公司。 例如，提交支出报表的员工为 DAT 公司工作，但向 DIR 公司收取费用。 在这种情况下，DAT 是支出被欠公司，DIR 是欠款公司。 验证这些日记帐行后，您可以将支出明细过帐到总帐。

若要过帐支出报表，在 **批准的支出报表** 页上，选择支出报表，然后在操作窗格上选择 **过帐**。

您也可以同时在列表中过帐所有支出报表。 选择所有支出报表，然后选择 **过帐**。

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>启用“能够以现金付款方式的供应商货币过帐支出负债”功能

**能够以现金付款方式的供应商货币过帐支出负债** 功能让支出报表能够以现金付款方式的供应商货币过帐。

目前，当您提交现金支出时，支出报表以会计币种过帐。 由于交易币种、会计币种和供应商货币之间的金额转换，如果支出的交易日期与实际付款日期的汇率不同，将向供应商支付错误的金额。

此功能将确保在过帐支出报表时以供应商货币记录供应商余额。

1. 转到 **工作区** \> **功能管理**。
2. 在列表中，找到并选择 **能够以现金付款方式的供应商货币过帐支出负债**，然后选择 **立即启用**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
