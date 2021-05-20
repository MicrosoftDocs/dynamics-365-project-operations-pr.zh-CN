---
title: 创建内部公司客户和供应商账单
description: 本主题提供了有关如何创建内部公司客户和供应商账单的信息。
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 92d08537fe0c2a1deba486974db53e7ebe1ff2d8
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948378"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="819dc-103">创建内部公司客户和供应商账单</span><span class="sxs-lookup"><span data-stu-id="819dc-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="819dc-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="819dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="819dc-105">贷款法律实体中的项目会计会为要转移到借款实体的项目成本创建内部公司客户账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="819dc-106">在批准和过帐内部公司客户账单后，贷款法律实体会将内部公司账单发送给借款法律实体。</span><span class="sxs-lookup"><span data-stu-id="819dc-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="819dc-107">贷款法律实体的项目会计可以设置一个批处理流程，以定期生成内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="819dc-108">项目会计会指定批量创建内部公司账单的条件（如特定项目）。</span><span class="sxs-lookup"><span data-stu-id="819dc-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="819dc-109">为项目交易手动创建内部公司客户账单</span><span class="sxs-lookup"><span data-stu-id="819dc-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="819dc-110">使用此过程为项目交易手动创建内部公司客户账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="819dc-111">搜索员工在借款法律实体的项目上过帐的小时数，以及您的法律实体代表借款法律实体产生的费用。</span><span class="sxs-lookup"><span data-stu-id="819dc-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="819dc-112">您可以按法律实体名称、项目合同编号、项目编号、日期范围或这些选项的任意组合进行搜索。</span><span class="sxs-lookup"><span data-stu-id="819dc-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="819dc-113">在搜索结果中，选择要添加到内部公司账单中的交易。</span><span class="sxs-lookup"><span data-stu-id="819dc-113">In the search results, select the transactions to add to an intercompany invoice.</span></span> 

<span data-ttu-id="819dc-114">必须在贷款法人中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="819dc-114">The following steps must be performed in the lending legal entity.</span></span> 

1. <span data-ttu-id="819dc-115">在 Dynamics 365 Finance 中，转到 **项目管理和会计** > **项目账单** > **内部公司客户账单**。</span><span class="sxs-lookup"><span data-stu-id="819dc-115">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="819dc-116">在 **内部公司客户账单** 列表页中的操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="819dc-116">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="819dc-117">在 **创建内部公司账单** 页上的 **法律实体** 字段中，选择一个借款法律实体。</span><span class="sxs-lookup"><span data-stu-id="819dc-117">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="819dc-118">可选：输入特定的项目合同和项目编号。</span><span class="sxs-lookup"><span data-stu-id="819dc-118">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="819dc-119">通过选择日期范围来缩小搜索范围。</span><span class="sxs-lookup"><span data-stu-id="819dc-119">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="819dc-120">在 **开始日期** 和 **结束日期** 字段中输入特定日期。</span><span class="sxs-lookup"><span data-stu-id="819dc-120">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="819dc-121">只有在此日期范围内过帐的内部公司交易才会显示在搜索结果中。</span><span class="sxs-lookup"><span data-stu-id="819dc-121">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="819dc-122">将 **项目高级日记帐行参数** 设置为 **是** 并选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="819dc-122">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="819dc-123">在搜索结果中，选择要包含在内部公司账单方案中的交易，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="819dc-123">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="819dc-124">在 **内部公司客户账单** 页上，将显示您从搜索结果中选择的内部公司项目交易。</span><span class="sxs-lookup"><span data-stu-id="819dc-124">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="819dc-125">若要在将账单发送到借款法律实体之前修改交易，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="819dc-125">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="819dc-126">在 **内部公司客户发票** 页上，打开发票详细信息，然后选择 **添加明细**。</span><span class="sxs-lookup"><span data-stu-id="819dc-126">On the **Intercompany customer invoice** page, open the invoice details, and then select **Add line**.</span></span>
    2. <span data-ttu-id="819dc-127">若要删除行，请选择该行，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="819dc-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="819dc-128">在发票明细详细信息上查看有关所选明细的注释、原因、财务维度及其他信息。</span><span class="sxs-lookup"><span data-stu-id="819dc-128">View comments, reasons, financial dimensions, and other information about a selected line on the invoice line details.</span></span>
    
8. <span data-ttu-id="819dc-129">若要过帐内部公司客户账单，请在操作窗格上选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="819dc-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="819dc-130">如果您的组织要求在过帐内部公司账单之前对其进行审核，则系统管理员可能会为内部公司账单设置工作流。</span><span class="sxs-lookup"><span data-stu-id="819dc-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="819dc-131">如果没有为内部公司账单设置工作流，则可以过帐内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="819dc-132">为内部公司账单创建批处理作业</span><span class="sxs-lookup"><span data-stu-id="819dc-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="819dc-133">您可以同时为所有借款法律实体创建多个内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="819dc-134">例如，您可以使用搜索功能搜索由借款员工过帐并且与其他法律实体管理的项目相关的所有交易。</span><span class="sxs-lookup"><span data-stu-id="819dc-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="819dc-135">然后，对于每个借款法律实体，您可以为搜索结果中提供的交易创建内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="819dc-136">转到 **项目管理和会计** > **定期** > **项目账单** > **创建内部公司客户账单**。</span><span class="sxs-lookup"><span data-stu-id="819dc-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="819dc-137">在 **创建内部公司客户账单** 页上的 **公司** 字段中，选择一个法律实体以开票。</span><span class="sxs-lookup"><span data-stu-id="819dc-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="819dc-138">如果您没有选择公司，则会为所有借款法律实体显示满足搜索条件的所有交易。</span><span class="sxs-lookup"><span data-stu-id="819dc-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="819dc-139">在 **创建一张发票的依据** 中，选择是基于项目还是基于借款法律实体创建内部公司交易的账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="819dc-140">可选：若要选择要为其创建内部公司账单的特定项目和项目合同，请单击 **选择**。</span><span class="sxs-lookup"><span data-stu-id="819dc-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="819dc-141">在 **查询** 页上的 **条件** 字段中，选择项目合同和/或项目编号，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="819dc-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="819dc-142">在 **批处理** 选项卡上，设置批量处理以定期创建内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="819dc-143">有关详细信息，请参阅[从窗体提交批量处理作业](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form)。</span><span class="sxs-lookup"><span data-stu-id="819dc-143">For more information, see [Submit a batch processing job from a form](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="819dc-144">若要过帐内部公司账单，请在操作窗格上选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="819dc-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="819dc-145">如果您的组织要求在过帐内部公司账单之前对其进行审核，则系统管理员可能会为内部公司账单设置工作流。</span><span class="sxs-lookup"><span data-stu-id="819dc-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="819dc-146">如果没有为内部公司账单设置工作流，则可以过帐内部公司账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="819dc-147">过帐内部公司供应商账单</span><span class="sxs-lookup"><span data-stu-id="819dc-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="819dc-148">在过帐相应的内部公司客户账单时，借款法律实体中的项目会计可以查看内部公司待定供应商账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="819dc-149">在 Finance 内的借款法律实体中，转到 **应付帐款** > **账单** > **待定供应商账单**。</span><span class="sxs-lookup"><span data-stu-id="819dc-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="819dc-150">待定账单编号将与内部公司客户账单编号匹配。</span><span class="sxs-lookup"><span data-stu-id="819dc-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="819dc-151">验证账单是否正确，然后过帐账单。</span><span class="sxs-lookup"><span data-stu-id="819dc-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="819dc-152">过帐内部公司供应商账单可创建项目子分类帐和总帐交易，以反映借款法律实体中的交易成本。</span><span class="sxs-lookup"><span data-stu-id="819dc-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
