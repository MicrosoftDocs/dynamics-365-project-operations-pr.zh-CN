---
title: 管理项目发票方案
description: 本主题提供有关使用面向资源/非库存场景的 Project Operations 处理面向客户的发票的详细信息。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089212"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="19b26-103">管理项目发票方案</span><span class="sxs-lookup"><span data-stu-id="19b26-103">Manage project invoice proposals</span></span>

<span data-ttu-id="19b26-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="19b26-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="19b26-105">满足以下两个条件时，您的账单部门可以处理项目发票方案：</span><span class="sxs-lookup"><span data-stu-id="19b26-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="19b26-106">项目经理在 Microsoft Dataverse 中确认估价发票。</span><span class="sxs-lookup"><span data-stu-id="19b26-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="19b26-107">估价发票中包含的所有时间和材料未记帐的销售交易都使用 Dynamics 365 **Project Operations 集成** 日记帐过帐。</span><span class="sxs-lookup"><span data-stu-id="19b26-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="19b26-108">使用以下步骤在 Dynamics 365 Finance 中完成项目发票方案。</span><span class="sxs-lookup"><span data-stu-id="19b26-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="19b26-109">查看时间和材料交易的账单信息，并发布 **Project Operations 集成** 日记帐。</span><span class="sxs-lookup"><span data-stu-id="19b26-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="19b26-110">查看固定价格记帐里程碑的记帐信息。</span><span class="sxs-lookup"><span data-stu-id="19b26-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="19b26-111">查看并设置项目发票方案的格式。</span><span class="sxs-lookup"><span data-stu-id="19b26-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="19b26-112">发布和打印项目发票。</span><span class="sxs-lookup"><span data-stu-id="19b26-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="19b26-113">在 Project Operations 集成日记帐中管理记帐信息</span><span class="sxs-lookup"><span data-stu-id="19b26-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="19b26-114">在 Dataverse 中创建的项目实际值将由项目会计在 Finance 中审核和过帐。</span><span class="sxs-lookup"><span data-stu-id="19b26-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="19b26-115">有关使用集成日记帐的详细信息，请参阅 [Project Operations 中的集成日记帐](../project-accounting/project-operations-integration-journal.md)。</span><span class="sxs-lookup"><span data-stu-id="19b26-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="19b26-116">成本实际值和未记帐实际销售额作为单独的行添加到集成日记帐中：</span><span class="sxs-lookup"><span data-stu-id="19b26-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="19b26-117">成本实际值中的单位成本费和成本金额默认来自 Dataverse 中的项目实际成本交易。</span><span class="sxs-lookup"><span data-stu-id="19b26-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="19b26-118">未记帐销售交易中的销售单价和销售金额默认来自 Dataverse 中项目的实际未记帐销售交易。</span><span class="sxs-lookup"><span data-stu-id="19b26-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="19b26-119">记帐销售税</span><span class="sxs-lookup"><span data-stu-id="19b26-119">Billing sales tax</span></span>

<span data-ttu-id="19b26-120">账单的销售税计算由 **Project Operations 集成** 日记帐行上未记帐销售记录中的 **记帐销售税组** 和 **记帐物料销售税组** 字段组合确定。</span><span class="sxs-lookup"><span data-stu-id="19b26-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="19b26-121">系统根据 **项目管理和会计参数** 页上 **财务** 选项卡上的设置来设置这些字段值的默认值。</span><span class="sxs-lookup"><span data-stu-id="19b26-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="19b26-122">**销售税组方法** 确定记帐销售税组的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="19b26-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="19b26-123">**项目**：将始终根据项目设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="19b26-124">您可以在 **所有项目** 页上选择 **显示默认会计** 来查看或更改项目中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="19b26-125">**项目合同**：将始终根据项目合同设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="19b26-126">您可以在 **项目合同** 页上选择 **显示默认会计** 来查看或更改项目合同中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="19b26-127">**客户**：将始终根据客户设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="19b26-128">**搜索**：将搜索上述所有实体，然后选择第一个可用值。</span><span class="sxs-lookup"><span data-stu-id="19b26-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="19b26-129">搜索从 **项目** 实体开始，然后是 **项目合同** 实体，最后是 **客户** 实体。</span><span class="sxs-lookup"><span data-stu-id="19b26-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="19b26-130">**物料销售税组方法** 确定记帐物料销售税组的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="19b26-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="19b26-131">对于时间、支出和费用交易类型，记帐物料销售税组将始终默认来自 **项目类别** 实体。</span><span class="sxs-lookup"><span data-stu-id="19b26-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="19b26-132">对于材料交易类型，记帐物料销售税组根据 **项目管理和会计参数** 中的 **物料销售税组方法** 设置设置默认值。</span><span class="sxs-lookup"><span data-stu-id="19b26-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="19b26-133">物料编号默认来自 **已发布产品** 实体的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="19b26-134">类别默认来自 **项目类别** 实体的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="19b26-135">财务维度</span><span class="sxs-lookup"><span data-stu-id="19b26-135">Financial dimensions</span></span>

<span data-ttu-id="19b26-136">**Project Operations 集成** 日记帐中的未记帐销售记录的财务维度默认来自 **项目** 实体。</span><span class="sxs-lookup"><span data-stu-id="19b26-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="19b26-137">可以通过选择 **分配金额** 来查看和调整财务维度。</span><span class="sxs-lookup"><span data-stu-id="19b26-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="19b26-138">如果您需要在过帐集成日记帐之后但在确认估价发票之前更改未记帐销售记录的财务维度，请转到 **所有项目** > **管理** > **已过帐交易**，选择交易，然后选择 **处理** > **调整会计**。</span><span class="sxs-lookup"><span data-stu-id="19b26-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="19b26-139">汇率</span><span class="sxs-lookup"><span data-stu-id="19b26-139">Exchange rates</span></span>

<span data-ttu-id="19b26-140">Dataverse 中的未记帐交易货币在 Finance 中用作交易货币，将使用 Finance 中定义的汇率转换为公司的会计币种。</span><span class="sxs-lookup"><span data-stu-id="19b26-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="19b26-141">管理记帐里程碑的财务属性</span><span class="sxs-lookup"><span data-stu-id="19b26-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="19b26-142">使用固定价格记帐方法的项目合同子项通过[固定价格里程碑](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line)开票。</span><span class="sxs-lookup"><span data-stu-id="19b26-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="19b26-143">项目会计可以转到 **项目管理和会计** > **所有项目** > **管理** > **记帐交易** 来查看 Finance 中的记帐里程碑。</span><span class="sxs-lookup"><span data-stu-id="19b26-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="19b26-144">记帐销售税</span><span class="sxs-lookup"><span data-stu-id="19b26-144">Billing sales tax</span></span>

<span data-ttu-id="19b26-145">当在 Dataverse 中创建新的记帐里程碑时，**销售税组** 和 **物料销售税组** 值默认来自设置。</span><span class="sxs-lookup"><span data-stu-id="19b26-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="19b26-146">系统根据 **项目管理和会计参数** 页上 **财务** 选项卡上的设置来将这些字段设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="19b26-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="19b26-147">**销售税组方法** 确定 **记帐销售税组** 的设置默认值逻辑：</span><span class="sxs-lookup"><span data-stu-id="19b26-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="19b26-148">**项目** 将始终根据项目设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="19b26-149">您可以在 **所有项目** 页上选择 **显示默认会计** 来查看或更改项目中的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="19b26-150">**项目合同** 将始终根据项目合同设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="19b26-151">您可以在 **项目合同** 页上选择 **显示默认会计** 来查看或更改项目合同中的默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="19b26-152">**客户** 将始终根据客户设置默认记帐销售税组。</span><span class="sxs-lookup"><span data-stu-id="19b26-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="19b26-153">**搜索** 将搜索此列表中的所有实体，然后选择第一个可用值。</span><span class="sxs-lookup"><span data-stu-id="19b26-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="19b26-154">搜索从 **项目** 实体开始，然后是 **项目合同** 实体，再然后是 **客户** 实体。</span><span class="sxs-lookup"><span data-stu-id="19b26-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="19b26-155">**固定价格里程碑物料销售税组** 用于将默认值设置为 **物料销售税组** 字段。</span><span class="sxs-lookup"><span data-stu-id="19b26-155">**Fixed price milestone item sales tax group** is used to default the value to the **Item sales tax group** field.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="19b26-156">财务维度</span><span class="sxs-lookup"><span data-stu-id="19b26-156">Financial dimensions</span></span>

<span data-ttu-id="19b26-157">固定价格记帐里程碑的默认财务维度在项目合同子项上设置。</span><span class="sxs-lookup"><span data-stu-id="19b26-157">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="19b26-158">转到 **项目合同** > **显示默认会计**，在 **合同子项** 选项卡上，选择 **价格合同子项**，然后设置您要用作默认值的财务维度值 。</span><span class="sxs-lookup"><span data-stu-id="19b26-158">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="19b26-159">项目会计可以编辑发票里程碑上的销售税和财务维度信息，直到项目发票方案创建。</span><span class="sxs-lookup"><span data-stu-id="19b26-159">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="19b26-160">创建项目发票方案</span><span class="sxs-lookup"><span data-stu-id="19b26-160">Create project invoice proposals</span></span>

<span data-ttu-id="19b26-161">可以在 **项目管理和会计** 模块中转到 **项目发票** > **项目发票方案** 来查看项目发票方案。</span><span class="sxs-lookup"><span data-stu-id="19b26-161">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="19b26-162">项目发票方案标头将在 Dataverse 中确认估价发票后在 Finance 中创建。</span><span class="sxs-lookup"><span data-stu-id="19b26-162">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="19b26-163">为便于对帐，系统将 Finance 中的项目发票方案编号设置为与 Dataverse 中的估价发票 ID 相同的编号。</span><span class="sxs-lookup"><span data-stu-id="19b26-163">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="19b26-164">由于估价发票不一定按创建顺序确认，因此 Finance 中的项目发票方案编号规则必须允许更改为更小和高大数字。</span><span class="sxs-lookup"><span data-stu-id="19b26-164">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="19b26-165">按照以下步骤配置编号规则：</span><span class="sxs-lookup"><span data-stu-id="19b26-165">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="19b26-166">在Finance 中，转到 **组织管理** > **编号规则** > **编号规则**。</span><span class="sxs-lookup"><span data-stu-id="19b26-166">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="19b26-167">在 **区域** 筛选器中，选择 **项目**。</span><span class="sxs-lookup"><span data-stu-id="19b26-167">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="19b26-168">在 **引用** 筛选器中，选择 **发票方案**。</span><span class="sxs-lookup"><span data-stu-id="19b26-168">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="19b26-169">使用 **公司** 字段筛选启用了 Project Operations Dataverse 集成的每个法人。</span><span class="sxs-lookup"><span data-stu-id="19b26-169">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="19b26-170">打开 **编号规则详细信息**，在 **常规** 选项卡上：</span><span class="sxs-lookup"><span data-stu-id="19b26-170">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="19b26-171">**允许用户更改为: 更小数字** = **是**</span><span class="sxs-lookup"><span data-stu-id="19b26-171">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="19b26-172">**允许用户更改为: 更大数字** = **是**</span><span class="sxs-lookup"><span data-stu-id="19b26-172">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="19b26-173">项目发票方案行将由系统使用定期流程 **从暂存表导入**（**项目管理和会计** > **定期** > **Project Operations 集成** > **从暂存表导入**）添加。</span><span class="sxs-lookup"><span data-stu-id="19b26-173">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="19b26-174">此流程可以手动运行，也可以使用定期计划运行。</span><span class="sxs-lookup"><span data-stu-id="19b26-174">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="19b26-175">在所有行都准备好开票之前，系统不会在发票方案文档中添加行。</span><span class="sxs-lookup"><span data-stu-id="19b26-175">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="19b26-176">时间和材料交易仅在使用 **Project Operations 集成** 日记帐过帐后才可以开票。</span><span class="sxs-lookup"><span data-stu-id="19b26-176">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="19b26-177">设置发票方案的格式和打印</span><span class="sxs-lookup"><span data-stu-id="19b26-177">Format and print invoice proposals</span></span>

<span data-ttu-id="19b26-178">项目会计可以使用 **设置发票方案的格式** 页和打印管理功能自定义项目发票的打印输出。</span><span class="sxs-lookup"><span data-stu-id="19b26-178">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="19b26-179">设置发票方案的格式</span><span class="sxs-lookup"><span data-stu-id="19b26-179">Format invoice proposals</span></span>

<span data-ttu-id="19b26-180">**设置发票方案的格式** 页允许自定义分组交易显示在客户项目发票中。</span><span class="sxs-lookup"><span data-stu-id="19b26-180">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="19b26-181">在 **项目发票方案** 页上，选择 **打印** > **设置发票方案的格式**。</span><span class="sxs-lookup"><span data-stu-id="19b26-181">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="19b26-182">选择 **新建** 为项目发票打印输出创建新的分组。</span><span class="sxs-lookup"><span data-stu-id="19b26-182">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="19b26-183">在 **详细信息/摘要** 字段中，选择用于此分组的选项：</span><span class="sxs-lookup"><span data-stu-id="19b26-183">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="19b26-184">选择 **详细信息** 可以打印客户发票的交易详细信息。</span><span class="sxs-lookup"><span data-stu-id="19b26-184">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="19b26-185">选择 **摘要** 可以打印客户发票的交易摘要。</span><span class="sxs-lookup"><span data-stu-id="19b26-185">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="19b26-186">在 **设置发票方案的格式** 页的 **详细信息/摘要** 字段中的选择，将覆盖在 **发票方案** 页的 **发票格式** 字段中选择的打印详细发票或摘要发票的选项。</span><span class="sxs-lookup"><span data-stu-id="19b26-186">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="19b26-187">在 **可用交易** 选项卡上选择要包括在此部分的交易明细，然后选择 **包括交易** 将其移到 **选定交易** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="19b26-187">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="19b26-188">选择 **上移** 和 **下移** 更改各个部分的顺序。</span><span class="sxs-lookup"><span data-stu-id="19b26-188">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="19b26-189">选择 **打印预览** 预览设置了格式的发票。</span><span class="sxs-lookup"><span data-stu-id="19b26-189">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="19b26-190">打印管理</span><span class="sxs-lookup"><span data-stu-id="19b26-190">Print management</span></span>

<span data-ttu-id="19b26-191">打印管理使用不同的报表文件来打印、指定目标和自定义发票的页脚文本。</span><span class="sxs-lookup"><span data-stu-id="19b26-191">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="19b26-192">打印管理可以在模块级别设置，但是对于特定客户、合同或发票方案，可以替代这些设置。</span><span class="sxs-lookup"><span data-stu-id="19b26-192">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="19b26-193">要在 **项目发票方案** 页上访问此功能，请选择 **打印** > **打印管理**。</span><span class="sxs-lookup"><span data-stu-id="19b26-193">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="19b26-194">打印管理设置显示为树视图，其中的每个节点级别显示要调整的可用文档。</span><span class="sxs-lookup"><span data-stu-id="19b26-194">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="19b26-195">您可以在模块、客户、合同或发票方案文档级别分配自定义打印输出。</span><span class="sxs-lookup"><span data-stu-id="19b26-195">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="19b26-196">要修改原始文档的打印输出，请展开所需节点，然后选择 **原始项**。</span><span class="sxs-lookup"><span data-stu-id="19b26-196">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="19b26-197">在 **报表格式** 字段中，选择要用于打印的报表格式。</span><span class="sxs-lookup"><span data-stu-id="19b26-197">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="19b26-198">您可以通过使用[业务文档管理框架](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management)来使用自定义报表格式。</span><span class="sxs-lookup"><span data-stu-id="19b26-198">You can use custom report formats by using [Business Document Management framework](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="19b26-199">发布发票方案</span><span class="sxs-lookup"><span data-stu-id="19b26-199">Post invoice proposals</span></span>

<span data-ttu-id="19b26-200">在查看和编辑发票并且发票方案行令人满意后，请检查发票总额和销售税。</span><span class="sxs-lookup"><span data-stu-id="19b26-200">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="19b26-201">在 **详细信息** 组中，选择 **总额**，然后选择 **发布** 发布发票。</span><span class="sxs-lookup"><span data-stu-id="19b26-201">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="19b26-202">要在发布前查看发票，请清除 **发布** 复选框。</span><span class="sxs-lookup"><span data-stu-id="19b26-202">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="19b26-203">**估价** 将被打印在发票上，以表示它是示例发票。</span><span class="sxs-lookup"><span data-stu-id="19b26-203">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="19b26-204">要打印发票，请选中 **打印发票** 复选框。</span><span class="sxs-lookup"><span data-stu-id="19b26-204">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="19b26-205">除了 **发票方案** 页之外，还可以通过运行定期作业 **发布发票方案** 来发布发票方案。</span><span class="sxs-lookup"><span data-stu-id="19b26-205">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="19b26-206">要查找此作业，请转到 **项目管理和会计** > **定期** > **项目发票** > **发布发票方案**。</span><span class="sxs-lookup"><span data-stu-id="19b26-206">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="19b26-207">此页面显示所有准备好发布的发票方案。</span><span class="sxs-lookup"><span data-stu-id="19b26-207">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="19b26-208">您可以通过选择 **批处理** 来计划发票方案的发布。</span><span class="sxs-lookup"><span data-stu-id="19b26-208">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="19b26-209">将 **批处理参数** 设置为 **是**，然后通过选择 **定期** 设置批处理的定期模式。</span><span class="sxs-lookup"><span data-stu-id="19b26-209">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>
