---
title: 管理项目报价单上的项目价目表
description: 此主题提供有关使用报价单上的项目价目表的信息。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 926581f877f91e3a351d51cac9c2b1daba035126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994890"
---
# <a name="manage-project-price-lists-on-project-quotes"></a><span data-ttu-id="bb79b-103">管理项目报价单上的项目价目表</span><span class="sxs-lookup"><span data-stu-id="bb79b-103">Manage project price lists on project quotes</span></span> 

<span data-ttu-id="bb79b-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="bb79b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb79b-105">项目报价单设计为支持多个有时效的销售价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-105">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="bb79b-106">通过 Dynamics 365 Project Operations，添加了名为 **项目价目表** 的新关联实体。</span><span class="sxs-lookup"><span data-stu-id="bb79b-106">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="bb79b-107">此实体与项目报价单之间具有一对多关系。</span><span class="sxs-lookup"><span data-stu-id="bb79b-107">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="bb79b-108">项目价目表用于为项目的时间、材料和支出交易定价。</span><span class="sxs-lookup"><span data-stu-id="bb79b-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="bb79b-109">当报价单具有一个或多个项目价目表时，这些价目表用于通过报价单明细对与该报价单关联的项目的时间、材料、支出估计和实际值进行定价。</span><span class="sxs-lookup"><span data-stu-id="bb79b-109">When a quote has one or more project price lists, these price lists are used to price time, material, expense estimates, and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="bb79b-110">当项目报价单上没有项目价目表时，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="bb79b-110">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="bb79b-111">此消息指出，由于没有项目价目表，不会对您的预估和实际项目工作和支出进行定价。</span><span class="sxs-lookup"><span data-stu-id="bb79b-111">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="bb79b-112">它们的销售值将为零 (0) 价格。</span><span class="sxs-lookup"><span data-stu-id="bb79b-112">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="bb79b-113">关联或取消关联项目报价单上的项目价目表</span><span class="sxs-lookup"><span data-stu-id="bb79b-113">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="bb79b-114">若要创建或选择特定价目表以预估基于项目的工作和支出，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bb79b-114">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="bb79b-115">在报价单上，选择 **项目价格** 选项卡，在子网格中，选择 **+ 添加新项目价目表**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-115">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="bb79b-116">在“快速创建”页上，选择一个价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-116">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="bb79b-117">下拉列表显示将上下文设置为 **Sales** 且货币与报价单上的货币匹配的所有价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-117">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="bb79b-118">为项目价目表关联输入说明，然后选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-118">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="bb79b-119">将创建项目价目表关联。</span><span class="sxs-lookup"><span data-stu-id="bb79b-119">A project price list association is created.</span></span>

<span data-ttu-id="bb79b-120">如果需要将多个项目价目表与项目报价单关联，可以重复此过程。</span><span class="sxs-lookup"><span data-stu-id="bb79b-120">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="bb79b-121">如果您在每个关联的项目价目表中有不同的生效日期，则仅创建多个项目价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-121">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="bb79b-122">Project Operations 不支持项目价目表有重叠的有效期。</span><span class="sxs-lookup"><span data-stu-id="bb79b-122">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="bb79b-123">如果给定日期的交易有多个项目价目表，该交易的价格将默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="bb79b-123">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="bb79b-124">若要删除项目价目表关联，请选择该项目价目表，然后选择 **删除报价单项目价目表**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-124">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="bb79b-125">价目表将被从报价单的项目价目表中删除，但价目表本身不会被删除。</span><span class="sxs-lookup"><span data-stu-id="bb79b-125">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="bb79b-126">只会删除与报价单的关联。</span><span class="sxs-lookup"><span data-stu-id="bb79b-126">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="bb79b-127">在报价单上设置默认项目价目表</span><span class="sxs-lookup"><span data-stu-id="bb79b-127">Set up default project price lists on a quote</span></span>

<span data-ttu-id="bb79b-128">可以在项目报价单上将项目价目表设置为默认填充值。</span><span class="sxs-lookup"><span data-stu-id="bb79b-128">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="bb79b-129">此设置可确保组织中的所有报价单始终从该价格期间的标准价目表开始。</span><span class="sxs-lookup"><span data-stu-id="bb79b-129">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="bb79b-130">为项目价目表设置组织默认值</span><span class="sxs-lookup"><span data-stu-id="bb79b-130">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="bb79b-131">转到 **设置** > **常规** > **参数**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-131">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="bb79b-132">在 **可用参数** 列表页上，找到记录并双击将其打开。</span><span class="sxs-lookup"><span data-stu-id="bb79b-132">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="bb79b-133">在 **参数** 页上，选择 **价目表** 选项卡。您可以看到默认价目表的列表已显示。</span><span class="sxs-lookup"><span data-stu-id="bb79b-133">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="bb79b-134">这是标准成本和销售价目表列表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-134">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="bb79b-135">在此处为您销售所使用的每种货币关联一个销售价目表，将确保您为使用此货币进行交易的客户创建的任何报价单均默认选择此销售价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-135">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="bb79b-136">设置特定于客户的项目价目表</span><span class="sxs-lookup"><span data-stu-id="bb79b-136">Set up customer-specific project price lists</span></span>

<span data-ttu-id="bb79b-137">特定于客户的项目价目表也可以在与客户商定主定价协议后设置。</span><span class="sxs-lookup"><span data-stu-id="bb79b-137">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="bb79b-138">若要设置特定于客户的项目价目表，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bb79b-138">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="bb79b-139">在 **销售** 区域中，选择 **客户**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-139">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="bb79b-140">在活动客户列表中，选择并打开您有特殊价目表的客户记录。</span><span class="sxs-lookup"><span data-stu-id="bb79b-140">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="bb79b-141">在 **项目价目表** 选项卡上，可以创建一个新的价目表关联，以获得特定于此客户的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="bb79b-141">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="bb79b-142">在项目报价单上创建自定义定价</span><span class="sxs-lookup"><span data-stu-id="bb79b-142">Create custom pricing on a project quote</span></span>

<span data-ttu-id="bb79b-143">有了组织和客户特定的默认项目价目表后，您的项目报价单将使用这些项目价目表关联自动创建。</span><span class="sxs-lookup"><span data-stu-id="bb79b-143">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="bb79b-144">不过，在某些情况下，您可能需要为特定的项目报价单创建自定义定价。</span><span class="sxs-lookup"><span data-stu-id="bb79b-144">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="bb79b-145">在 **项目报价单上** 的 **项目价目表** 选项卡上，在子网格中确认未选择特定价目表记录。</span><span class="sxs-lookup"><span data-stu-id="bb79b-145">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="bb79b-146">选择 **创建自定义定价**。</span><span class="sxs-lookup"><span data-stu-id="bb79b-146">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="bb79b-147">这将复制当前与报价单关联的所有标准价目表，并将这些副本与报价单关联。</span><span class="sxs-lookup"><span data-stu-id="bb79b-147">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="bb79b-148">与标准价目表的现有关联将被删除。</span><span class="sxs-lookup"><span data-stu-id="bb79b-148">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="bb79b-149">销售员随后可以开始对这些副本中的价格进行编辑。</span><span class="sxs-lookup"><span data-stu-id="bb79b-149">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="bb79b-150">这些更改后的价格仅适用于此项目报价单。</span><span class="sxs-lookup"><span data-stu-id="bb79b-150">These changed prices will be applicable to this project quote only.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
