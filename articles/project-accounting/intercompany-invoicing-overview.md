---
title: 内部公司开票概述
description: 本主题提供了有关内部公司项目开票的信息和示例。
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002630"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="6df38-103">内部公司开票概述</span><span class="sxs-lookup"><span data-stu-id="6df38-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="6df38-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6df38-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6df38-105">您的组织可能具有多个为项目彼此转移产品和服务的分公司、附属机构和其他法人。</span><span class="sxs-lookup"><span data-stu-id="6df38-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="6df38-106">提供服务或产品的法律实体称为 *贷款法律实体*。</span><span class="sxs-lookup"><span data-stu-id="6df38-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="6df38-107">接收服务或产品的法律实体称为 *借款法律实体*。</span><span class="sxs-lookup"><span data-stu-id="6df38-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="6df38-108">下图显示了一个典型方案，其中，两个法人实体 Contoso Robotics USA（借款法人实体）和 Contoso  Robotics UK（贷款法人实体）共享资源以为客户 Adventure works 交付项目。</span><span class="sxs-lookup"><span data-stu-id="6df38-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="6df38-109">对于此情形，Contoso Robotics USA 签订合同以向 Adventure Works 交付工作。</span><span class="sxs-lookup"><span data-stu-id="6df38-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![内部公司开票](./media/IntercompanyScenario.png) 

<span data-ttu-id="6df38-111">Dynamics 365 Project Operations 使用以下流来处理内部公司交易：</span><span class="sxs-lookup"><span data-stu-id="6df38-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="6df38-112">贷款法律实体中的资源按贷款法律实体中项目的预定时间和支出来记录内部公司的时间或支出交易。</span><span class="sxs-lookup"><span data-stu-id="6df38-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="6df38-113">使用借款公司的单位成本价目表将时间和支出成本记录在贷款公司中。</span><span class="sxs-lookup"><span data-stu-id="6df38-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="6df38-114">使用借款公司的单位成本价目表将内部公司未记帐销售交易记录在贷款公司中。</span><span class="sxs-lookup"><span data-stu-id="6df38-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="6df38-115">使用项目合同销售价目表将未记帐收入记录在借款公司中。</span><span class="sxs-lookup"><span data-stu-id="6df38-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="6df38-116">记录未记帐收入后，可以对客户进行计费。</span><span class="sxs-lookup"><span data-stu-id="6df38-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="6df38-117">客户不必等到内部公司账单处理完成。</span><span class="sxs-lookup"><span data-stu-id="6df38-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="6df38-118">在贷款公司中定期创建内部公司客户账单。</span><span class="sxs-lookup"><span data-stu-id="6df38-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="6df38-119">账单是手动创建或使用定期自动流程创建的。</span><span class="sxs-lookup"><span data-stu-id="6df38-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="6df38-120">可以为每个借款法律实体创建单个账单，也可以按项目创建单独的账单。</span><span class="sxs-lookup"><span data-stu-id="6df38-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="6df38-121">在贷款法律实体中过帐内部公司客户账单后，会在借款法律实体中创建相应的待定供应商账单。</span><span class="sxs-lookup"><span data-stu-id="6df38-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="6df38-122">过帐账单后，待定供应商账单中的成本将记录到项目子分类帐中。</span><span class="sxs-lookup"><span data-stu-id="6df38-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="6df38-123">下图说明了内部公司开票，因为它与会计事件和预期过帐到总帐有关。</span><span class="sxs-lookup"><span data-stu-id="6df38-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![内部公司流](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="6df38-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="6df38-125">Additional resources</span></span>

- [<span data-ttu-id="6df38-126">配置内部公司开票</span><span class="sxs-lookup"><span data-stu-id="6df38-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="6df38-127">记录内部公司交易</span><span class="sxs-lookup"><span data-stu-id="6df38-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="6df38-128">创建内部公司客户和供应商账单</span><span class="sxs-lookup"><span data-stu-id="6df38-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]