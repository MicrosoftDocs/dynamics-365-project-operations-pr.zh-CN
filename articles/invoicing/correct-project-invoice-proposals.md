---
title: 在草稿项目发票方案上更正会计
description: 本主题说明了如何在草稿发票方案上调整与会计相关的信息。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251183"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="30293-103">在草稿项目发票方案上更正会计</span><span class="sxs-lookup"><span data-stu-id="30293-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="30293-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="30293-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="30293-105">项目发票的 *操作详细信息* 由项目经理针对估价发票进行维护。</span><span class="sxs-lookup"><span data-stu-id="30293-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="30293-106">这些详细信息包括有关必须开具发票的小时数、支出、材料或里程碑、汇率以及预付款和保留款应用的决策。</span><span class="sxs-lookup"><span data-stu-id="30293-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="30293-107">在确认原始估价发票后，您可以通过创建并确认[更正估价发票](../proforma-invoicing/corrective-invoices.md)调整操作详细信息。</span><span class="sxs-lookup"><span data-stu-id="30293-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="30293-108">项目发票的 *会计详细信息* 在面向客户的发票文档中进行维护。</span><span class="sxs-lookup"><span data-stu-id="30293-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="30293-109">这些详细信息包括应用于发票的销售税款计算和财务维度。</span><span class="sxs-lookup"><span data-stu-id="30293-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="30293-110">本主题提供有关如何在草稿项目发票方案上调整这些会计详细信息的详细信息。</span><span class="sxs-lookup"><span data-stu-id="30293-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="30293-111">调整销售税</span><span class="sxs-lookup"><span data-stu-id="30293-111">Adjust sales tax</span></span>

<span data-ttu-id="30293-112">可以直接在发票方案文档上调整默认的记帐销售税组和物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="30293-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="30293-113">若要调整这些组，请选择 **编辑**，然后在每个项目发票方案行上，在 **销售税组** 或 **物料销售税组** 字段中输入新值。</span><span class="sxs-lookup"><span data-stu-id="30293-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="30293-114">调整财务维度</span><span class="sxs-lookup"><span data-stu-id="30293-114">Adjust financial dimensions</span></span>

<span data-ttu-id="30293-115">不能直接在项目发票方案行上编辑财务维度。</span><span class="sxs-lookup"><span data-stu-id="30293-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="30293-116">而是按照以下步骤在项目发票方案上调整财务维度。</span><span class="sxs-lookup"><span data-stu-id="30293-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="30293-117">在项目发票方案上，选择 **全部删除** 以删除项目发票方案行。</span><span class="sxs-lookup"><span data-stu-id="30293-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30293-118">**全部删除** 按钮仅在系统管理员在 **功能管理** 工作区中启用 **在针对基于资源/非库存的方案使用 Project Operations 时删除发票方案行** 功能后才可用。</span><span class="sxs-lookup"><span data-stu-id="30293-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="30293-119">调整财务维度：</span><span class="sxs-lookup"><span data-stu-id="30293-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="30293-120">**记帐交易（记帐里程碑）：** 转到 **所有项目** \> **管理** \> **记帐交易**，并选择需要调整的里程碑。</span><span class="sxs-lookup"><span data-stu-id="30293-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="30293-121">然后，在 **财务维度** 选项卡上，根据需要更新值。</span><span class="sxs-lookup"><span data-stu-id="30293-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="30293-122">**时间、支出和材料交易：** 在 **过帐的项目交易** 页面上，选择 **调整会计** 以更新财务维度。</span><span class="sxs-lookup"><span data-stu-id="30293-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="30293-123">调整完财务维度值后，转到 **项目管理和会计** \> **定期** \> **Project Operations 集成**，然后选择 **从暂存表中导入** 以运行定期流程。</span><span class="sxs-lookup"><span data-stu-id="30293-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="30293-124">该流程使用更新的财务维度值来重新创建项目发票方案行。</span><span class="sxs-lookup"><span data-stu-id="30293-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="30293-125">然后，在过帐项目发票时，将更新的值用于项目分类帐和总帐。</span><span class="sxs-lookup"><span data-stu-id="30293-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
