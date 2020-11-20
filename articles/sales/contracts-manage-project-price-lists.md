---
title: 管理项目合同上的项目价目表
description: 此主题提供有关管理项目合同中的项目价格表的信息。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133290"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="be23b-103">管理项目合同上的项目价目表</span><span class="sxs-lookup"><span data-stu-id="be23b-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="be23b-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="be23b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be23b-105">Dynamics 365 Project Operations 中的项目合同设计为支持合同上的多个有时效的销售价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="be23b-106">在 Project Operations 中，有一个名为 **项目价目表** 的新的关联实体。</span><span class="sxs-lookup"><span data-stu-id="be23b-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="be23b-107">此实体与项目合同之间具有一对多关系。</span><span class="sxs-lookup"><span data-stu-id="be23b-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="be23b-108">项目价目表用于对项目的时间和支出交易进行定价。</span><span class="sxs-lookup"><span data-stu-id="be23b-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="be23b-109">当合同有一个或多个项目价目表时，这些价目表用于为通过合同子项与合同关联的项目中的时间和支出估计值和实际值定价。</span><span class="sxs-lookup"><span data-stu-id="be23b-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="be23b-110">如果项目合同中没有项目价目表，您将看到一条警告消息，指示没有项目价目表，您的估计值、实际项目工作和支出不会定价。</span><span class="sxs-lookup"><span data-stu-id="be23b-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="be23b-111">销售值不会有价格。</span><span class="sxs-lookup"><span data-stu-id="be23b-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="be23b-112">关联或取消关联项目合同中的项目价目表</span><span class="sxs-lookup"><span data-stu-id="be23b-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="be23b-113">创建或关联特定价目表以估算基于项目的工作和支出</span><span class="sxs-lookup"><span data-stu-id="be23b-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="be23b-114">在项目合同上，选择 **项目价目表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="be23b-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="be23b-115">在子网格中，选择 **+ 添加新项目价目表**。</span><span class="sxs-lookup"><span data-stu-id="be23b-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="be23b-116">在 **快速创建** 滑块上，选择一个价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="be23b-117">下拉列表显示将上下文设置为 **销售** 的所有价目表，价目表中的货币与合同中的货币匹配。</span><span class="sxs-lookup"><span data-stu-id="be23b-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="be23b-118">为项目价目表关联输入说明，请选择 **保存**，然后关闭 **快速创建** 滑块。</span><span class="sxs-lookup"><span data-stu-id="be23b-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="be23b-119">将创建项目价目表关联。</span><span class="sxs-lookup"><span data-stu-id="be23b-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="be23b-120">重复步骤 1-4，将多个项目价目表与项目合同关联。</span><span class="sxs-lookup"><span data-stu-id="be23b-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="be23b-121">如果您在每个关联项目价目表上有不同时效，这种情况下才会创建多个项目价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="be23b-122">Project Operations 不支持重叠项目价目表的时效。</span><span class="sxs-lookup"><span data-stu-id="be23b-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="be23b-123">如果交易有给定日期的多个项目价目表，该交易中的价格将默认为零。</span><span class="sxs-lookup"><span data-stu-id="be23b-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="be23b-124">删除项目价目表关联</span><span class="sxs-lookup"><span data-stu-id="be23b-124">Remove a project price list association</span></span>

- <span data-ttu-id="be23b-125">选择项目价目表，然后在子网格中选择 **删除合同项目价目表**。</span><span class="sxs-lookup"><span data-stu-id="be23b-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="be23b-126">价目表将被从合同上的项目价目表中删除。</span><span class="sxs-lookup"><span data-stu-id="be23b-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="be23b-127">价目表本身不会被删除。</span><span class="sxs-lookup"><span data-stu-id="be23b-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="be23b-128">只会删除与合同的关联。</span><span class="sxs-lookup"><span data-stu-id="be23b-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="be23b-129">设置合同上的项目价格表的自动默认设置</span><span class="sxs-lookup"><span data-stu-id="be23b-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="be23b-130">项目价目表可以设置为项目合同上的默认列表。</span><span class="sxs-lookup"><span data-stu-id="be23b-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="be23b-131">此设置可以帮助确保您的组织中的所有合同始终以该价格期间的标准价目表开始。</span><span class="sxs-lookup"><span data-stu-id="be23b-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="be23b-132">设置项目价目表的组织默认值</span><span class="sxs-lookup"><span data-stu-id="be23b-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="be23b-133">转到 **设置** > **常规**，然后选择 **参数**。</span><span class="sxs-lookup"><span data-stu-id="be23b-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="be23b-134">在 **可用参数** 列表页上，选择并双击记录将其打开。</span><span class="sxs-lookup"><span data-stu-id="be23b-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="be23b-135">双击时，请确保没有单击超链接字段值。</span><span class="sxs-lookup"><span data-stu-id="be23b-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="be23b-136">在 **可用参数** 页上，选择 **价目表** 选项卡。一个子网格将显示默认价目表的列表。</span><span class="sxs-lookup"><span data-stu-id="be23b-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="be23b-137">这是包含标准成本和销售价目表的列表。</span><span class="sxs-lookup"><span data-stu-id="be23b-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="be23b-138">在此处为您销售所使用的每种货币关联一个 **销售** 价目表，确保此销售价目表是您为以此货币进行交易的客户创建的任何合同上的默认价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="be23b-139">设置特定于客户的项目价目表</span><span class="sxs-lookup"><span data-stu-id="be23b-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="be23b-140">在与客户商定了主定价协议后，您还可以设置特定于客户的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="be23b-141">转到 **销售** > **客户**。</span><span class="sxs-lookup"><span data-stu-id="be23b-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="be23b-142">从可用客户列表中，选择有特殊价目表的客户。</span><span class="sxs-lookup"><span data-stu-id="be23b-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="be23b-143">选择客户记录将其打开，然后选择 **项目价目表** 选项卡。一个子网格将显示特定于此客户的项目价目表的列表。</span><span class="sxs-lookup"><span data-stu-id="be23b-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="be23b-144">在此处创建新的价目表关联，以获得特定于此客户的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="be23b-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="be23b-145">项目合同上的自定义定价</span><span class="sxs-lookup"><span data-stu-id="be23b-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="be23b-146">在您有了组织的特定于客户的默认项目价目表之后，您的项目合同将自动创建，并具有这些项目价目表关联。</span><span class="sxs-lookup"><span data-stu-id="be23b-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="be23b-147">但是，项目合同上的项目价目表复制时始终带有向其追加的日期和合同名称。</span><span class="sxs-lookup"><span data-stu-id="be23b-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="be23b-148">客户和项目经理随后可以开始对这些副本上的价格进行编辑。</span><span class="sxs-lookup"><span data-stu-id="be23b-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="be23b-149">这些更改的价格仅适用于此项目合同。</span><span class="sxs-lookup"><span data-stu-id="be23b-149">These changed prices will be applicable to this project contract only.</span></span>
