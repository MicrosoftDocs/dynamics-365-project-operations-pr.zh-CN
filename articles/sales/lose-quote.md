---
title: 复制基于项目的报价单
description: 此主题提供有关如何在 Project Operations 中复制基于项目的报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278137"
---
# <a name="copy-project-based-quotes"></a><span data-ttu-id="be89f-103">复制基于项目的报价单</span><span class="sxs-lookup"><span data-stu-id="be89f-103">Copy project-based quotes</span></span>

<span data-ttu-id="be89f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="be89f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be89f-105">您可以通过复制现有项目报价单轻松地创建新的项目报价单。</span><span class="sxs-lookup"><span data-stu-id="be89f-105">You can easily create a new Project quote by copying an existing one.</span></span> 

- <span data-ttu-id="be89f-106">要复制项目报价单，在 **项目报价单** 列表页或 **项目报价单** 详细信息页上，选择要复制的项目报价单，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="be89f-106">To copy a Project quote, on the **Project Quotes** list page or the **Project Quote** details page, select the Project quote you want to copy, and then select **Copy**.</span></span>

<span data-ttu-id="be89f-107">这将打开一个对话页面，您可以在其中输入副本的参数。</span><span class="sxs-lookup"><span data-stu-id="be89f-107">This will open a dialog page where you can enter the parameters of the copy.</span></span> <span data-ttu-id="be89f-108">下表列出了对话页面中包含的字段。</span><span class="sxs-lookup"><span data-stu-id="be89f-108">The following table lists the fields that are included in the dialog page.</span></span> <span data-ttu-id="be89f-109">根据您选择的值，复制过程可能会有变化。</span><span class="sxs-lookup"><span data-stu-id="be89f-109">Depending on the values you select, the copy process may change.</span></span>

| <span data-ttu-id="be89f-110">**字段**</span><span class="sxs-lookup"><span data-stu-id="be89f-110">**Field**</span></span> | <span data-ttu-id="be89f-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="be89f-111">**Description**</span></span> | <span data-ttu-id="be89f-112">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="be89f-112">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="be89f-113">主题</span><span class="sxs-lookup"><span data-stu-id="be89f-113">Topic</span></span> | <span data-ttu-id="be89f-114">输入目标报价单的相关主题或名称。</span><span class="sxs-lookup"><span data-stu-id="be89f-114">Enter the relevant topic, or name, of the target quote.</span></span> <span data-ttu-id="be89f-115">当对话打开时，系统会将其设置为源报价单的主题，并附加 **-copy**。</span><span class="sxs-lookup"><span data-stu-id="be89f-115">When the dialog opens, the system will set it to the topic of the source quote with **-copy** appended to it.</span></span> | |
| <span data-ttu-id="be89f-116">潜在客户</span><span class="sxs-lookup"><span data-stu-id="be89f-116">Potential Customer</span></span> | <span data-ttu-id="be89f-117">对客户的公司或客户记录的引用。</span><span class="sxs-lookup"><span data-stu-id="be89f-117">Reference to the customer's company or account record.</span></span> <span data-ttu-id="be89f-118">当对话打开时，系统会将其设置为源报价单上的客户。</span><span class="sxs-lookup"><span data-stu-id="be89f-118">When the dialog opens, the system will set it to the account on the source quote.</span></span> | <span data-ttu-id="be89f-119">此字段是报价单上的主要客户。</span><span class="sxs-lookup"><span data-stu-id="be89f-119">This field is the primary customer on the quote.</span></span> |
| <span data-ttu-id="be89f-120">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="be89f-120">Contracting Unit</span></span> | <span data-ttu-id="be89f-121">负责交付与此交易关联的项目的部门。</span><span class="sxs-lookup"><span data-stu-id="be89f-121">The organization unit that is responsible for the delivery of the project(s) associated with this deal.</span></span>
<span data-ttu-id="be89f-122">当对话打开时，系统会将其设置为源报价单的合同签订部门。</span><span class="sxs-lookup"><span data-stu-id="be89f-122">When the dialog opens, the system will set it to the contracting unit of the source quote.</span></span> | <span data-ttu-id="be89f-123">合同签订部门是在交易完成后将执行项目的公司的部门。</span><span class="sxs-lookup"><span data-stu-id="be89f-123">Contracting unit is the division of the company that will execute the projects after the deal is closed.</span></span> <span data-ttu-id="be89f-124">每个合同签订部门有一种货币。</span><span class="sxs-lookup"><span data-stu-id="be89f-124">Every contracting unit has a currency.</span></span> <span data-ttu-id="be89f-125">此货币用于报告项目执行过程中产生的预估成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="be89f-125">The currency is used to report estimated and actual costs incurred during the execution of the project.</span></span> |
| <span data-ttu-id="be89f-126">货币</span><span class="sxs-lookup"><span data-stu-id="be89f-126">Currency</span></span> | <span data-ttu-id="be89f-127">这是进行交易所使用的货币。</span><span class="sxs-lookup"><span data-stu-id="be89f-127">This is the currency that the deal is transacted in.</span></span> <span data-ttu-id="be89f-128">当对话打开时，系统会将其设置为源报价单的货币。</span><span class="sxs-lookup"><span data-stu-id="be89f-128">When the dialog opens, the system will set it to the currency of the source quote.</span></span> <span data-ttu-id="be89f-129">此字段可以修改，如果更改，**复制定价** 字段始终设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="be89f-129">This can be modified and if it is change, the **Copy Pricing** field is always set to **No**.</span></span> <span data-ttu-id="be89f-130">这是因为与源报价单上的价目表不再相关。</span><span class="sxs-lookup"><span data-stu-id="be89f-130">This is because the price lists on source quote are no longer relevant.</span></span> | <span data-ttu-id="be89f-131">货币用于为价目表确定默认值、在报价单上生成财务估算值，最终用于在交易赢单时为客户开票。</span><span class="sxs-lookup"><span data-stu-id="be89f-131">Currency is used to default a price list, to build a financial estimate on the quote,  and eventually to invoice the customer when the deal is won.</span></span> |
| <span data-ttu-id="be89f-132">要求交货日期</span><span class="sxs-lookup"><span data-stu-id="be89f-132">Requested Delivery Date</span></span> | <span data-ttu-id="be89f-133">这是客户要求的交货日期。</span><span class="sxs-lookup"><span data-stu-id="be89f-133">This is the date of delivery requested by the customer.</span></span> | <span data-ttu-id="be89f-134">在按照特定频率创建开票日期时，此字段用作结束日期。</span><span class="sxs-lookup"><span data-stu-id="be89f-134">This is used as the end date when creating invoicing dates along a specific frequency.</span></span> |
| <span data-ttu-id="be89f-135">复制定价</span><span class="sxs-lookup"><span data-stu-id="be89f-135">Copy pricing</span></span> | <span data-ttu-id="be89f-136">“是/否”值指示是否应从源报价单复制报价单上的定价。</span><span class="sxs-lookup"><span data-stu-id="be89f-136">A Yes/No value indicates whether the pricing on the quote should be copied from the source quote.</span></span> | <span data-ttu-id="be89f-137">如果选择 **是**，会将项目价目表和产品价目表引用从源报价单复制到目标报价单。</span><span class="sxs-lookup"><span data-stu-id="be89f-137">If **Yes** is selected, the project price list and product price list references are copied from the source quote to the target quote.</span></span> <span data-ttu-id="be89f-138">如果选择 **否**，会根据客户或项目参数上设置的最新价目表重新设置价目表的默认值。</span><span class="sxs-lookup"><span data-stu-id="be89f-138">If **No** is selected, price lists are re-defaulted based on the latest price lists that were set up on the account or project parameters.</span></span> |

<span data-ttu-id="be89f-139">当您在对话页面上选择 **确定** 时，系统将根据在对话中选择的参数创建项目报价单的副本。</span><span class="sxs-lookup"><span data-stu-id="be89f-139">When you select **OK** on the dialog page, the system creates a copy of the project quote based on the parameters selected in the dialog.</span></span> <span data-ttu-id="be89f-140">新项目报价单此时将打开。</span><span class="sxs-lookup"><span data-stu-id="be89f-140">The new project quote opens.</span></span> 

> [!NOTE]
> <span data-ttu-id="be89f-141">以下信息不会从源报价单复制到目标报价单：</span><span class="sxs-lookup"><span data-stu-id="be89f-141">The following information is not copied from the Source to the Target quote:</span></span>
>
> - <span data-ttu-id="be89f-142">发票计划</span><span class="sxs-lookup"><span data-stu-id="be89f-142">Invoice schedules</span></span>
> - <span data-ttu-id="be89f-143">报价单和报价单明细客户</span><span class="sxs-lookup"><span data-stu-id="be89f-143">Quote and quote line customers</span></span>
> - <span data-ttu-id="be89f-144">基于项目的报价单明细上的项目引用 – 客户预算信息</span><span class="sxs-lookup"><span data-stu-id="be89f-144">Project reference on the project – based quote lines -Customer budget information</span></span>
>
><span data-ttu-id="be89f-145">由于此信息对于每个报价单都非常特定，因此不会复制这些字段和记录。</span><span class="sxs-lookup"><span data-stu-id="be89f-145">Because this information is very specific to each quote, these fields and records are not copied.</span></span> <span data-ttu-id="be89f-146">项目和产品的报价单明细、报价单明细详细信息中的估算值以及报价单级别的上限值将被复制。</span><span class="sxs-lookup"><span data-stu-id="be89f-146">Quote lines for projects and products, estimates on quote line details, and not-to-exceed values at the quote level are copied.</span></span> <span data-ttu-id="be89f-147">价格和成本率默认值取决于在 **复制参数** 对话页面上选择的 **复制定价** 选项。</span><span class="sxs-lookup"><span data-stu-id="be89f-147">Price and cost rate defaults depend on the **Copy pricing** option selected on the **Copy parameters** dialog page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]