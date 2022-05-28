---
title: 处理支出报表上的个人支出
description: 本主题提供有关如何处理因公出差所产生的员工个人支出的信息。
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586517"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>处理支出报表上的个人支出

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

在出差期间，员工可能会使用公司信用卡支付个人支出。 如果未定义处理个人支出的流程，当员工提交分项的支出报表时，支出报表审批流程可能会中断。

您可以使用两种方法来处理员工的个人支出：

  - **员工支付**：组织不支付公司信用卡帐单上出现的个人支出。 而是由员工直接向信用卡供应商付款。 
  - **由公司支付**：您的组织将全额支付公司信用卡的账单，然后从工作人员的账户中扣除个人支出。

您可以在 **支出管理参数** 页面中选择组织使用的方法。


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>为个人金额字段定义值后启用拆分支出功能

功能 **为个人金额字段定义值后启用拆分支出功能** 仅适用于使用行级工作流审批的费用报表 通过转到 **处理支出报表** > **分配给我的支出报表** > **打开支出报表** 来批准报表。 

若要启用此功能，请转到 **工作区** > **功能管理**，选择 **为个人金额字段定义值后启用拆分支出功能**，然后选择 **立即启用**。 

启用该功能后，在提交报表时，使用此功能的支出行会生成两行。 将生成两行，以便审批者可以分别审批每一行。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
