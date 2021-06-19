---
title: 处理支出报表上的个人支出
description: 本主题提供有关如何处理因公出差所产生的员工个人支出的信息。
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025673"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="ba10a-103">处理支出报表上的个人支出</span><span class="sxs-lookup"><span data-stu-id="ba10a-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="ba10a-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="ba10a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba10a-105">在出差期间，员工可能会使用公司信用卡支付个人支出。</span><span class="sxs-lookup"><span data-stu-id="ba10a-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="ba10a-106">如果未定义处理个人支出的流程，当员工提交分项的支出报表时，支出报表审批流程可能会中断。</span><span class="sxs-lookup"><span data-stu-id="ba10a-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="ba10a-107">您可以使用两种方法来处理员工的个人支出：</span><span class="sxs-lookup"><span data-stu-id="ba10a-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="ba10a-108">**员工支付**：组织不支付公司信用卡帐单上出现的个人支出。</span><span class="sxs-lookup"><span data-stu-id="ba10a-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ba10a-109">而是由员工直接向信用卡供应商付款。</span><span class="sxs-lookup"><span data-stu-id="ba10a-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="ba10a-110">**由公司支付**：您的组织将全额支付公司信用卡的账单，然后从工作人员的账户中扣除个人支出。</span><span class="sxs-lookup"><span data-stu-id="ba10a-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ba10a-111">您可以在 **支出管理参数** 页面中选择组织使用的方法。</span><span class="sxs-lookup"><span data-stu-id="ba10a-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="ba10a-112">为个人金额字段定义值后启用拆分支出功能</span><span class="sxs-lookup"><span data-stu-id="ba10a-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="ba10a-113">功能 **为个人金额字段定义值后启用拆分支出功能** 仅适用于使用行级工作流审批的费用报表</span><span class="sxs-lookup"><span data-stu-id="ba10a-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="ba10a-114">通过转到 **处理支出报表** > **分配给我的支出报表** > **打开支出报表** 来批准报表。</span><span class="sxs-lookup"><span data-stu-id="ba10a-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="ba10a-115">若要启用此功能，请转到 **工作区** > **功能管理**，选择 **为个人金额字段定义值后启用拆分支出功能**，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="ba10a-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="ba10a-116">启用该功能后，在提交报表时，使用此功能的支出行会生成两行。</span><span class="sxs-lookup"><span data-stu-id="ba10a-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="ba10a-117">将生成两行，以便审批者可以分别审批每一行。</span><span class="sxs-lookup"><span data-stu-id="ba10a-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
