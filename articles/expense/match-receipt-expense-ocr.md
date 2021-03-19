---
title: 使用 OCR 捕获收据
description: 此主题提供有关收据的光学字符识别 (OCR) 处理的信息。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499840"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="873a0-103">使用 OCR 捕获收据</span><span class="sxs-lookup"><span data-stu-id="873a0-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="873a0-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="873a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="873a0-105">通过引入对收据的光学字符识别 (OCR) 处理，支出输入得到了增强。</span><span class="sxs-lookup"><span data-stu-id="873a0-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="873a0-106">此功能的目的是改进用户创建支出报表的体验。</span><span class="sxs-lookup"><span data-stu-id="873a0-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="873a0-107">主要功能</span><span class="sxs-lookup"><span data-stu-id="873a0-107">Key features</span></span>

- <span data-ttu-id="873a0-108">系统从收据中提取商家名称、日期和总金额。</span><span class="sxs-lookup"><span data-stu-id="873a0-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="873a0-109">系统会尝试将未附加的收据与未附加的支出交易记录匹配。</span><span class="sxs-lookup"><span data-stu-id="873a0-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="873a0-110">您可以创建从收据手动输入的支出交易记录。</span><span class="sxs-lookup"><span data-stu-id="873a0-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="873a0-111">将收据附加到支出报表</span><span class="sxs-lookup"><span data-stu-id="873a0-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="873a0-112">若要在创建支出报表时自动附加包含信用卡交易记录的收据，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="873a0-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="873a0-113">打开 **支出管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="873a0-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="873a0-114">在 **收据** 选项卡上，验证是否存在未附加的收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="873a0-115">您还可以在 **收据** 选项卡上上载收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="873a0-116">在 **支出** 选项卡上，验证是否存在未附加的支出。</span><span class="sxs-lookup"><span data-stu-id="873a0-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="873a0-117">通常情况下，支出管理员从信用卡提供商处导入这些支出。</span><span class="sxs-lookup"><span data-stu-id="873a0-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="873a0-118">选择 **新建支出报表**。</span><span class="sxs-lookup"><span data-stu-id="873a0-118">Select **New expense report**.</span></span> <span data-ttu-id="873a0-119">请注意，在您创建支出报表时，现在还可以包括支出和收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="873a0-120">如果同时添加支出和收据，则会触发根据支出自动匹配收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="873a0-121">创建收据或将其与支出报表匹配</span><span class="sxs-lookup"><span data-stu-id="873a0-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="873a0-122">若要创建支出，或从收据匹配支出，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="873a0-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="873a0-123">在支出报表的 **收据** 选项卡上，选择 **添加收据** 来附加收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="873a0-124">在上载的收据图像下，注意 **创建** 和 **匹配** 选项。</span><span class="sxs-lookup"><span data-stu-id="873a0-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="873a0-125">选择 **创建** 来创建手动输入的支出交易记录，并填写从收据中提取的值。</span><span class="sxs-lookup"><span data-stu-id="873a0-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="873a0-126">如果选择 **匹配**，系统将尝试匹配现有支出与收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="873a0-127">安装</span><span class="sxs-lookup"><span data-stu-id="873a0-127">Installation</span></span>

<span data-ttu-id="873a0-128">若要使用这些高级支出功能，请安装适用于 Microsoft Dynamics 365 Finance 的支出管理服务加载项，并启用您的实例中的功能。</span><span class="sxs-lookup"><span data-stu-id="873a0-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="873a0-129">您可以从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目访问该加载项。</span><span class="sxs-lookup"><span data-stu-id="873a0-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="873a0-130">登录到 LCS，打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="873a0-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="873a0-131">转到 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="873a0-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="873a0-132">选择 **维护**，或向下滚动到 **环境加载项** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="873a0-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="873a0-133">选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="873a0-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="873a0-134">选择 **支出管理服务**。</span><span class="sxs-lookup"><span data-stu-id="873a0-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="873a0-135">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="873a0-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="873a0-136">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="873a0-136">Select **Install**.</span></span>

<span data-ttu-id="873a0-137">在 **功能管理** 工作区中，打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="873a0-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="873a0-138">重新打造支出报表</span><span class="sxs-lookup"><span data-stu-id="873a0-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="873a0-139">自动匹配并从收据创建支出</span><span class="sxs-lookup"><span data-stu-id="873a0-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="873a0-140">当您启用这些功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="873a0-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="873a0-141">现有的 **支出管理** 工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="873a0-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="873a0-142">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="873a0-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="873a0-143">您仍然可以转到 **支出管理 > 我的支出 > 支出报表** 来打开以前的 **支出报表** 页面。</span><span class="sxs-lookup"><span data-stu-id="873a0-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="873a0-144">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="873a0-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="873a0-145">收据将通过 Microsoft Azure Cognitive Services 处理，并将提取和添加元数据。</span><span class="sxs-lookup"><span data-stu-id="873a0-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="873a0-146">添加了一个选项，使您可以创建包含匹配的未附加收据的支出报表。</span><span class="sxs-lookup"><span data-stu-id="873a0-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="873a0-147">添加到支出报表的一个选项，使您可以从收据创建支出行，或尝试将现有收据与现有支出行匹配。</span><span class="sxs-lookup"><span data-stu-id="873a0-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="873a0-148">常见问题</span><span class="sxs-lookup"><span data-stu-id="873a0-148">Frequently asked questions</span></span>

<span data-ttu-id="873a0-149">**Microsoft 是否在其模型中使用我的数据？**</span><span class="sxs-lookup"><span data-stu-id="873a0-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="873a0-150">否，Microsoft 已经为其收据处理服务构建了常规的机器学习模型。</span><span class="sxs-lookup"><span data-stu-id="873a0-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="873a0-151">此模型不基于您上载的收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="873a0-152">**哪里提供和处理此功能？**</span><span class="sxs-lookup"><span data-stu-id="873a0-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="873a0-153">目前，支持在美国使用。</span><span class="sxs-lookup"><span data-stu-id="873a0-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="873a0-154">**我的收据会去向哪里？**</span><span class="sxs-lookup"><span data-stu-id="873a0-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="873a0-155">Finance 将与 Cognitive Services 连接来提取字段数据。</span><span class="sxs-lookup"><span data-stu-id="873a0-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="873a0-156">在进行处理时，Cognitive Services 最长会将您的收据副本保留 24 小时。</span><span class="sxs-lookup"><span data-stu-id="873a0-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="873a0-157">处理完成后，Cognitive Services 将删除收据。</span><span class="sxs-lookup"><span data-stu-id="873a0-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="873a0-158">收据仍存储在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="873a0-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="873a0-159">有关详细信息，请参阅[使用表单识别器的新功能支持收据了解功能](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。</span><span class="sxs-lookup"><span data-stu-id="873a0-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
