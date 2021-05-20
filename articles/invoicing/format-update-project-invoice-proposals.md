---
title: 管理项目发票方案
description: 本主题提供有关使用面向资源/非库存场景的 Project Operations 处理面向客户的发票的详细信息。
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6b8eacf2b43219a9adad897637b78a9c94351554
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950703"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="d0333-103">管理项目发票方案</span><span class="sxs-lookup"><span data-stu-id="d0333-103">Manage project invoice proposals</span></span>

<span data-ttu-id="d0333-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d0333-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d0333-105">满足以下两个条件时，您的账单部门可以处理项目发票方案：</span><span class="sxs-lookup"><span data-stu-id="d0333-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="d0333-106">项目经理在 Microsoft Dataverse 中确认估价发票。</span><span class="sxs-lookup"><span data-stu-id="d0333-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="d0333-107">估价发票中包含的所有时间和材料未记帐的销售交易都使用 Dynamics 365 **Project Operations 集成** 日记帐过帐。</span><span class="sxs-lookup"><span data-stu-id="d0333-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="d0333-108">使用以下步骤在 Dynamics 365 Finance 中完成项目发票方案。</span><span class="sxs-lookup"><span data-stu-id="d0333-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="d0333-109">查看时间和材料交易的账单信息，并发布 **Project Operations 集成** 日记帐。</span><span class="sxs-lookup"><span data-stu-id="d0333-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="d0333-110">查看固定价格记帐里程碑的记帐信息。</span><span class="sxs-lookup"><span data-stu-id="d0333-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="d0333-111">查看并设置项目发票方案的格式。</span><span class="sxs-lookup"><span data-stu-id="d0333-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="d0333-112">发布和打印项目发票。</span><span class="sxs-lookup"><span data-stu-id="d0333-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="d0333-113">在 Project Operations 集成日记帐中管理记帐信息</span><span class="sxs-lookup"><span data-stu-id="d0333-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="d0333-114">在 Dataverse 中创建的项目实际值将由项目会计在 Finance 中审核和过帐。</span><span class="sxs-lookup"><span data-stu-id="d0333-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="d0333-115">有关使用集成日记帐的详细信息，请参阅 [Project Operations 中的集成日记帐](../project-accounting/project-operations-integration-journal.md)。</span><span class="sxs-lookup"><span data-stu-id="d0333-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="d0333-116">成本实际值和未记帐实际销售额作为单独的行添加到集成日记帐中：</span><span class="sxs-lookup"><span data-stu-id="d0333-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="d0333-117">成本实际值中的单位成本费和成本金额默认来自 Dataverse 中的项目实际成本交易。</span><span class="sxs-lookup"><span data-stu-id="d0333-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="d0333-118">未记帐销售交易中的销售单价和销售金额默认来自 Dataverse 中项目的实际未记帐销售交易。</span><span class="sxs-lookup"><span data-stu-id="d0333-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="d0333-119">记帐销售税</span><span class="sxs-lookup"><span data-stu-id="d0333-119">Billing sales tax</span></span>

<span data-ttu-id="d0333-120">账单的销售税计算由 **Project Operations 集成** 日记帐行上未记帐销售记录中的 **记帐销售税组** 和 **记帐物料销售税组** 字段组合确定。</span><span class="sxs-lookup"><span data-stu-id="d0333-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="d0333-121">系统根据 **项目管理和会计参数** 页上 **财务** 选项卡上的设置来设置这些字段值的默认值。</span><span class="sxs-lookup"><span data-stu-id="d0333-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="d0333-122">**销售税组方法** 确定记帐销售税组的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="d0333-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="d0333-123">**项目**：将始终根据项目设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="d0333-124">您可以在 **所有项目** 页上选择 **显示默认会计** 来查看或更改项目中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="d0333-125">**项目合同**：将始终根据项目合同设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="d0333-126">您可以在 **项目合同** 页上选择 **显示默认会计** 来查看或更改项目合同中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="d0333-127">**客户**：将始终根据客户设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="d0333-128">**搜索**：将搜索上述所有实体，然后选择第一个可用值。</span><span class="sxs-lookup"><span data-stu-id="d0333-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="d0333-129">搜索从 **项目** 实体开始，然后是 **项目合同** 实体，最后是 **客户** 实体。</span><span class="sxs-lookup"><span data-stu-id="d0333-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="d0333-130">**物料销售税组方法** 确定记帐物料销售税组的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="d0333-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="d0333-131">对于时间、支出和费用交易类型，记帐物料销售税组将始终默认来自 **项目类别** 实体。</span><span class="sxs-lookup"><span data-stu-id="d0333-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="d0333-132">对于材料交易类型，记帐物料销售税组根据 **项目管理和会计参数** 中的 **物料销售税组方法** 设置设置默认值。</span><span class="sxs-lookup"><span data-stu-id="d0333-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="d0333-133">物料编号默认来自 **已发布产品** 实体的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="d0333-134">类别默认来自 **项目类别** 实体的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="d0333-135">财务维度</span><span class="sxs-lookup"><span data-stu-id="d0333-135">Financial dimensions</span></span>

<span data-ttu-id="d0333-136">**Project Operations 集成** 日记帐中的未记帐销售记录的财务维度默认来自 **项目** 实体。</span><span class="sxs-lookup"><span data-stu-id="d0333-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="d0333-137">可以通过选择 **分配金额** 来查看和调整财务维度。</span><span class="sxs-lookup"><span data-stu-id="d0333-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="d0333-138">如果您需要在过帐集成日记帐之后但在确认估价发票之前更改未记帐销售记录的财务维度，请转到 **所有项目** > **管理** > **已过帐交易**，选择交易，然后选择 **处理** > **调整会计**。</span><span class="sxs-lookup"><span data-stu-id="d0333-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="d0333-139">汇率</span><span class="sxs-lookup"><span data-stu-id="d0333-139">Exchange rates</span></span>

<span data-ttu-id="d0333-140">Dataverse 中的未记帐交易货币在 Finance 中用作交易货币，将使用 Finance 中定义的汇率转换为公司的会计币种。</span><span class="sxs-lookup"><span data-stu-id="d0333-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="d0333-141">管理记帐里程碑的财务属性</span><span class="sxs-lookup"><span data-stu-id="d0333-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="d0333-142">使用固定价格记帐方法的项目合同子项通过[固定价格里程碑](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line)开票。</span><span class="sxs-lookup"><span data-stu-id="d0333-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="d0333-143">项目会计可以转到 **项目管理和会计** > **所有项目** > **管理** > **记帐交易** 来查看 Finance 中的记帐里程碑。</span><span class="sxs-lookup"><span data-stu-id="d0333-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="d0333-144">记帐销售税</span><span class="sxs-lookup"><span data-stu-id="d0333-144">Billing sales tax</span></span>

<span data-ttu-id="d0333-145">当在 Dataverse 中创建新的记帐里程碑时，**销售税组** 和 **物料销售税组** 值默认来自设置。</span><span class="sxs-lookup"><span data-stu-id="d0333-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="d0333-146">系统根据 **项目管理和会计参数** 页上 **财务** 选项卡上的设置来将这些字段设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="d0333-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="d0333-147">**销售税组方法** 确定 **记帐销售税组** 的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="d0333-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="d0333-148">**项目** 将始终根据项目设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="d0333-149">您可以在 **所有项目** 页上选择 **显示默认会计** 来查看或更改项目中的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="d0333-150">**项目合同** 将始终根据项目合同设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="d0333-151">您可以在 **项目合同** 页上选择 **显示默认会计** 来查看或更改项目合同中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="d0333-152">**客户** 将始终根据客户设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="d0333-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="d0333-153">**搜索** 将搜索此列表中的所有实体，然后选择第一个可用值。</span><span class="sxs-lookup"><span data-stu-id="d0333-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="d0333-154">搜索从 **项目** 实体开始，然后是 **项目合同** 实体，再然后是 **客户** 实体。</span><span class="sxs-lookup"><span data-stu-id="d0333-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="d0333-155">**固定价格里程碑物料销售税组** 用作记帐里程碑的 **物料销售税组** 字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="d0333-155">**Fixed price milestone item sales tax group** is used as the default value in the **Item sales tax group** field for the billing milestone.</span></span> <span data-ttu-id="d0333-156">会计可以在 **帐户内交易** 页查看和修改此值。</span><span class="sxs-lookup"><span data-stu-id="d0333-156">The accountant can review and modify this value on the **On-account transactions** page.</span></span> <span data-ttu-id="d0333-157">创建项目发票方案明细时，系统将使用帐户内交易中的值。</span><span class="sxs-lookup"><span data-stu-id="d0333-157">The system uses the value from the on-account transaction when creating a project invoice proposal line.</span></span>
 

### <a name="financial-dimensions"></a><span data-ttu-id="d0333-158">财务维度</span><span class="sxs-lookup"><span data-stu-id="d0333-158">Financial dimensions</span></span>

<span data-ttu-id="d0333-159">固定价格记帐里程碑的默认财务维度在项目合同子项上设置。</span><span class="sxs-lookup"><span data-stu-id="d0333-159">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="d0333-160">转到 **项目合同** > **显示默认会计**，在 **合同子项** 选项卡上，选择 **价格合同子项**，然后设置您要用作默认值的财务维度值 。</span><span class="sxs-lookup"><span data-stu-id="d0333-160">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="d0333-161">项目会计可以编辑发票里程碑上的销售税和财务维度信息，直到项目发票方案创建。</span><span class="sxs-lookup"><span data-stu-id="d0333-161">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="d0333-162">创建项目发票方案</span><span class="sxs-lookup"><span data-stu-id="d0333-162">Create project invoice proposals</span></span>

<span data-ttu-id="d0333-163">可以在 **项目管理和会计** 模块中转到 **项目发票** > **项目发票方案** 来查看项目发票方案。</span><span class="sxs-lookup"><span data-stu-id="d0333-163">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="d0333-164">项目发票方案标头将在 Dataverse 中确认估价发票后在 Finance 中创建。</span><span class="sxs-lookup"><span data-stu-id="d0333-164">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="d0333-165">为便于对帐，系统将 Finance 中的项目发票方案编号设置为与 Dataverse 中的估价发票 ID 相同的编号。</span><span class="sxs-lookup"><span data-stu-id="d0333-165">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="d0333-166">由于估价发票不一定按创建顺序确认，因此 Finance 中的项目发票方案编号规则必须允许更改为更小和高大数字。</span><span class="sxs-lookup"><span data-stu-id="d0333-166">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="d0333-167">按照以下步骤配置编号规则：</span><span class="sxs-lookup"><span data-stu-id="d0333-167">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="d0333-168">在Finance 中，转到 **组织管理** > **编号规则** > **编号规则**。</span><span class="sxs-lookup"><span data-stu-id="d0333-168">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="d0333-169">在 **区域** 筛选器中，选择 **项目**。</span><span class="sxs-lookup"><span data-stu-id="d0333-169">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="d0333-170">在 **引用** 筛选器中，选择 **发票方案**。</span><span class="sxs-lookup"><span data-stu-id="d0333-170">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="d0333-171">使用 **公司** 字段筛选启用了 Project Operations Dataverse 集成的每个法人。</span><span class="sxs-lookup"><span data-stu-id="d0333-171">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="d0333-172">打开 **编号规则详细信息**，在 **常规** 选项卡上：</span><span class="sxs-lookup"><span data-stu-id="d0333-172">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="d0333-173">**允许用户更改为: 更小数字** = **是**</span><span class="sxs-lookup"><span data-stu-id="d0333-173">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="d0333-174">**允许用户更改为: 更大数字** = **是**</span><span class="sxs-lookup"><span data-stu-id="d0333-174">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="d0333-175">项目发票方案行将由系统使用定期流程 **从暂存表导入**（**项目管理和会计** > **定期** > **Project Operations 集成** > **从暂存表导入**）添加。</span><span class="sxs-lookup"><span data-stu-id="d0333-175">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="d0333-176">此流程可以手动运行，也可以使用定期计划运行。</span><span class="sxs-lookup"><span data-stu-id="d0333-176">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="d0333-177">在所有行都准备好开票之前，系统不会在发票方案文档中添加行。</span><span class="sxs-lookup"><span data-stu-id="d0333-177">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="d0333-178">时间和材料交易仅在使用 **Project Operations 集成** 日记帐过帐后才可以开票。</span><span class="sxs-lookup"><span data-stu-id="d0333-178">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="d0333-179">设置发票方案的格式和打印</span><span class="sxs-lookup"><span data-stu-id="d0333-179">Format and print invoice proposals</span></span>

<span data-ttu-id="d0333-180">项目会计可以使用 **设置发票方案的格式** 页和打印管理功能自定义项目发票的打印输出。</span><span class="sxs-lookup"><span data-stu-id="d0333-180">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="d0333-181">设置发票方案的格式</span><span class="sxs-lookup"><span data-stu-id="d0333-181">Format invoice proposals</span></span>

<span data-ttu-id="d0333-182">**设置发票方案的格式** 页允许自定义分组交易显示在客户项目发票中。</span><span class="sxs-lookup"><span data-stu-id="d0333-182">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="d0333-183">在 **项目发票方案** 页上，选择 **打印** > **设置发票方案的格式**。</span><span class="sxs-lookup"><span data-stu-id="d0333-183">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="d0333-184">选择 **新建** 为项目发票打印输出创建新的分组。</span><span class="sxs-lookup"><span data-stu-id="d0333-184">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="d0333-185">在 **详细信息/摘要** 字段中，选择用于此分组的选项：</span><span class="sxs-lookup"><span data-stu-id="d0333-185">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="d0333-186">选择 **详细信息** 可以打印客户发票的交易详细信息。</span><span class="sxs-lookup"><span data-stu-id="d0333-186">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="d0333-187">选择 **摘要** 可以打印客户发票的交易摘要。</span><span class="sxs-lookup"><span data-stu-id="d0333-187">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="d0333-188">在 **设置发票方案的格式** 页的 **详细信息/摘要** 字段中的选择，将覆盖在 **发票方案** 页的 **发票格式** 字段中选择的打印详细发票或摘要发票的选项。</span><span class="sxs-lookup"><span data-stu-id="d0333-188">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="d0333-189">在 **可用交易** 选项卡上选择要包括在此部分的交易明细，然后选择 **包括交易** 将其移到 **选定交易** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="d0333-189">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="d0333-190">选择 **上移** 和 **下移** 更改各个部分的顺序。</span><span class="sxs-lookup"><span data-stu-id="d0333-190">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="d0333-191">选择 **打印预览** 预览设置了格式的发票。</span><span class="sxs-lookup"><span data-stu-id="d0333-191">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="d0333-192">打印管理</span><span class="sxs-lookup"><span data-stu-id="d0333-192">Print management</span></span>

<span data-ttu-id="d0333-193">打印管理使用不同的报表文件来打印、指定目标和自定义发票的页脚文本。</span><span class="sxs-lookup"><span data-stu-id="d0333-193">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="d0333-194">打印管理可以在模块级别设置，但是对于特定客户、合同或发票方案，可以替代这些设置。</span><span class="sxs-lookup"><span data-stu-id="d0333-194">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="d0333-195">要在 **项目发票方案** 页上访问此功能，请选择 **打印** > **打印管理**。</span><span class="sxs-lookup"><span data-stu-id="d0333-195">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="d0333-196">打印管理设置显示为树视图，其中的每个节点级别显示要调整的可用文档。</span><span class="sxs-lookup"><span data-stu-id="d0333-196">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="d0333-197">您可以在模块、客户、合同或发票方案文档级别分配自定义打印输出。</span><span class="sxs-lookup"><span data-stu-id="d0333-197">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="d0333-198">要修改原始文档的打印输出，请展开所需节点，然后选择 **原始项**。</span><span class="sxs-lookup"><span data-stu-id="d0333-198">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="d0333-199">在 **报表格式** 字段中，选择要用于打印的报表格式。</span><span class="sxs-lookup"><span data-stu-id="d0333-199">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="d0333-200">您可以通过使用[业务文档管理框架](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management)来使用自定义报表格式。</span><span class="sxs-lookup"><span data-stu-id="d0333-200">You can use custom report formats by using [Business Document Management framework](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="d0333-201">发布发票方案</span><span class="sxs-lookup"><span data-stu-id="d0333-201">Post invoice proposals</span></span>

<span data-ttu-id="d0333-202">在查看和编辑发票并且发票方案行令人满意后，请检查发票总额和销售税。</span><span class="sxs-lookup"><span data-stu-id="d0333-202">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="d0333-203">在 **详细信息** 组中，选择 **总额**，然后选择 **发布** 发布发票。</span><span class="sxs-lookup"><span data-stu-id="d0333-203">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="d0333-204">要在发布前查看发票，请清除 **发布** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d0333-204">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="d0333-205">**估价** 将被打印在发票上，以表示它是示例发票。</span><span class="sxs-lookup"><span data-stu-id="d0333-205">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="d0333-206">要打印发票，请选中 **打印发票** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d0333-206">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="d0333-207">除了 **发票方案** 页之外，还可以通过运行定期作业 **发布发票方案** 来发布发票方案。</span><span class="sxs-lookup"><span data-stu-id="d0333-207">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="d0333-208">要查找此作业，请转到 **项目管理和会计** > **定期** > **项目发票** > **发布发票方案**。</span><span class="sxs-lookup"><span data-stu-id="d0333-208">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="d0333-209">此页面显示所有准备好发布的发票方案。</span><span class="sxs-lookup"><span data-stu-id="d0333-209">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="d0333-210">您可以通过选择 **批处理** 来计划发票方案的发布。</span><span class="sxs-lookup"><span data-stu-id="d0333-210">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="d0333-211">将 **批处理参数** 设置为 **是**，然后通过选择 **定期** 设置批处理的定期模式。</span><span class="sxs-lookup"><span data-stu-id="d0333-211">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
