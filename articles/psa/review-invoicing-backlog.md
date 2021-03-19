---
title: 审阅项目和项目合同的开票积压
description: 此主题介绍如何审阅时间、支出和产品积压，以及如何将其标记为可开票。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282772"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="e1bd8-103">审阅项目和项目合同的开票积压</span><span class="sxs-lookup"><span data-stu-id="e1bd8-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e1bd8-104">当交易准备就绪，可以创建和处理发票时，应该将该交易标记为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="e1bd8-105">此主题介绍可创建的交易类型。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="e1bd8-106">审阅时间和材料记帐积压</span><span class="sxs-lookup"><span data-stu-id="e1bd8-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="e1bd8-107">为项目提交和审批时间或支出条目时，PSA 将创建项目实际值。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="e1bd8-108">如果将项目与交易分类的组合映射到时间和材料项目的合同子项，则批准了该条目时将创建两项实际值：</span><span class="sxs-lookup"><span data-stu-id="e1bd8-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="e1bd8-109">成本实际值</span><span class="sxs-lookup"><span data-stu-id="e1bd8-109">Cost actual</span></span> 
- <span data-ttu-id="e1bd8-110">未记帐实际销售额</span><span class="sxs-lookup"><span data-stu-id="e1bd8-110">Unbilled sales actual</span></span>

<span data-ttu-id="e1bd8-111">未记帐实际销售额表示记帐积压，其记帐状态必须设置为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="e1bd8-112">创建项目发票时，将复制标记为 **可开票** 的未记帐实际销售额并替换发票明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="e1bd8-113">若要审阅时间和材料的记帐积压，请转到 **Sales** \> **记帐** \> **时间和材料记帐积压**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="e1bd8-114">选择可开票的所有未记帐实际销售额，然后选择 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e1bd8-115">这些实际值的记帐状态将更改为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![时间和材料记帐积压](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="e1bd8-117">审阅产品记帐积压</span><span class="sxs-lookup"><span data-stu-id="e1bd8-117">Review the product billing backlog</span></span>

<span data-ttu-id="e1bd8-118">在 PSA 中，当项目合同中包含基于产品的合同子项时，只要为项目合同创建发票，都将考虑为这些明细开票。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="e1bd8-119">将把具有标记为 **可开票** 的合同子项的所有产品作为项目发票明细复制到项目发票。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="e1bd8-120">若要审阅产品的记帐积压，请转到 **Sales** \> **记帐** \> **产品记帐积压**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="e1bd8-121">选择可开票的所有基于产品的合同子项，然后选择 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e1bd8-122">这些明细的记帐状态将更改为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![产品记帐积压](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="e1bd8-124">审阅固定价格合同的记帐里程碑</span><span class="sxs-lookup"><span data-stu-id="e1bd8-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="e1bd8-125">每项采用固定价格记帐方法的项目合同子项都必须定义合同里程碑。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="e1bd8-126">这些合同里程碑只有在带有 **可开票** 标记时，才可以开票。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="e1bd8-127">若要审阅记帐里程碑，请转到 **Sales** \> **记帐** \> **固定价格里程碑**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="e1bd8-128">选择可开票的里程碑，然后选择 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="e1bd8-129">这些里程碑的记帐状态将更改为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="e1bd8-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![固定价格里程碑](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]