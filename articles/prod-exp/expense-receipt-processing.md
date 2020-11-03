---
title: 支出收据处理
description: 此主题提供有关收据的光学字符识别 (OCR) 处理的信息。 此功能适合在 Microsoft Dynamics 365 Finance 中创建支出报表时改善用户体验。
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072762"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="a88fc-104">支出收据处理</span><span class="sxs-lookup"><span data-stu-id="a88fc-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a88fc-105">通过引入对收据的光学字符识别 (OCR) 处理，支出输入得到了增强。</span><span class="sxs-lookup"><span data-stu-id="a88fc-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="a88fc-106">此功能适合在创建支出报表时改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="a88fc-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="a88fc-107">主要功能</span><span class="sxs-lookup"><span data-stu-id="a88fc-107">Key features</span></span>

- <span data-ttu-id="a88fc-108">从收据中提取商户名称、日期和总金额。</span><span class="sxs-lookup"><span data-stu-id="a88fc-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="a88fc-109">该功能尝试将未附加的收据与未附加的支出交易记录匹配。</span><span class="sxs-lookup"><span data-stu-id="a88fc-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="a88fc-110">用户可以根据收据创建手动输入的支出交易记录。</span><span class="sxs-lookup"><span data-stu-id="a88fc-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="a88fc-111">用法示例</span><span class="sxs-lookup"><span data-stu-id="a88fc-111">Usage examples</span></span>

<span data-ttu-id="a88fc-112">若要自动附加创建支出报表时包括信用卡交易记录的收据，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="a88fc-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="a88fc-113">打开 **支出管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="a88fc-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="a88fc-114">在 **收据** 选项卡上，验证是否存在未附加的收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="a88fc-115">您还可以在 **收据** 选项卡上上载收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="a88fc-116">在 **支出** 选项卡上，验证是否存在未附加的支出。</span><span class="sxs-lookup"><span data-stu-id="a88fc-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="a88fc-117">通常情况下，支出管理员从信用卡提供商处导入这些支出。</span><span class="sxs-lookup"><span data-stu-id="a88fc-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="a88fc-118">选择 **新建支出报表** 。</span><span class="sxs-lookup"><span data-stu-id="a88fc-118">Select **New expense report**.</span></span> <span data-ttu-id="a88fc-119">请注意，在您创建支出报表时，现在还可以包括支出和收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="a88fc-120">如果同时添加支出和收据，则会触发根据支出自动匹配收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="a88fc-121">若要创建支出，或匹配收据中的支出，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="a88fc-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="a88fc-122">在支出报表的 **收据** 选项卡上，选择 **添加收据** 来附加收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="a88fc-123">在上载的收据图像下，注意 **创建** 和 **匹配** 选项。</span><span class="sxs-lookup"><span data-stu-id="a88fc-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="a88fc-124">选择 **创建** 来创建手动输入的支出交易记录，并填写从收据中提取的值。</span><span class="sxs-lookup"><span data-stu-id="a88fc-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="a88fc-125">如果选择 **匹配** ，系统将尝试匹配现有支出与收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="a88fc-126">安装</span><span class="sxs-lookup"><span data-stu-id="a88fc-126">Installation</span></span>

<span data-ttu-id="a88fc-127">此功能与 **已重构的支出报表** 功能联合使用，有助于简化支出体验。</span><span class="sxs-lookup"><span data-stu-id="a88fc-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="a88fc-128">此功能仅可用于二级以上环境，即沙盒和生产。</span><span class="sxs-lookup"><span data-stu-id="a88fc-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="a88fc-129">若要使用这些高级支出功能，请安装适用于 Microsoft Dynamics 365 Finance 的支出管理服务加载项，并启用您的实例中的功能。</span><span class="sxs-lookup"><span data-stu-id="a88fc-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="a88fc-130">您可以从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目访问该加载项。</span><span class="sxs-lookup"><span data-stu-id="a88fc-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="a88fc-131">登录到 LCS，打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="a88fc-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="a88fc-132">转到 **完整详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="a88fc-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="a88fc-133">选择 **维护** ，或向下滚动到 **环境加载项** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a88fc-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="a88fc-134">选择 **安装新加载项** 。</span><span class="sxs-lookup"><span data-stu-id="a88fc-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="a88fc-135">选择 **支出管理服务** 。</span><span class="sxs-lookup"><span data-stu-id="a88fc-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="a88fc-136">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="a88fc-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="a88fc-137">选择 **安装** 。</span><span class="sxs-lookup"><span data-stu-id="a88fc-137">Select **Install**.</span></span>

<span data-ttu-id="a88fc-138">在 **功能管理** 工作区中，打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="a88fc-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="a88fc-139">重新打造支出报表</span><span class="sxs-lookup"><span data-stu-id="a88fc-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="a88fc-140">自动匹配并从收据创建支出</span><span class="sxs-lookup"><span data-stu-id="a88fc-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="a88fc-141">当您启用这些功能时，会发生以下操作：</span><span class="sxs-lookup"><span data-stu-id="a88fc-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="a88fc-142">现有的 **支出管理** 工作区将替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="a88fc-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a88fc-143">将添加用于显示支出字段的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="a88fc-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a88fc-144">您仍然可以转到 **支出管理 > 我的支出 > 支出报表** 来打开以前的 **支出报表** 页面。</span><span class="sxs-lookup"><span data-stu-id="a88fc-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="a88fc-145">工作流和所有审批仍会将您带到现有的支出报表页。</span><span class="sxs-lookup"><span data-stu-id="a88fc-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="a88fc-146">收据将通过 Microsoft Azure Cognitive Services 处理，并将提取和添加元数据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="a88fc-147">添加了一个选项，使您可以创建包含匹配的未附加收据的支出报表。</span><span class="sxs-lookup"><span data-stu-id="a88fc-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="a88fc-148">添加到支出报表的一个选项，使您可以从收据创建支出行，或尝试将现有收据与现有支出行匹配。</span><span class="sxs-lookup"><span data-stu-id="a88fc-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="a88fc-149">有关已重构的支出报表功能的更多信息，请参见[已重构的支出报表](ExpenseWorkspaceNew.md)。</span><span class="sxs-lookup"><span data-stu-id="a88fc-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a88fc-150">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="a88fc-150">Frequently asked questions</span></span>

<span data-ttu-id="a88fc-151">**Microsoft 是否在其模型中使用我的数据？**</span><span class="sxs-lookup"><span data-stu-id="a88fc-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="a88fc-152">否，Microsoft 已经为其收据处理服务构建了常规的机器学习模型。</span><span class="sxs-lookup"><span data-stu-id="a88fc-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="a88fc-153">此模型不基于您上载的收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="a88fc-154">**哪里提供和处理此功能？**</span><span class="sxs-lookup"><span data-stu-id="a88fc-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="a88fc-155">目前，支持在美国使用。</span><span class="sxs-lookup"><span data-stu-id="a88fc-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="a88fc-156">**我的收据会去向哪里？**</span><span class="sxs-lookup"><span data-stu-id="a88fc-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="a88fc-157">Finance 将与 Cognitive Services 连接来提取字段数据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="a88fc-158">在进行处理时，Cognitive Services 最长会将您的收据副本保留 24 小时。</span><span class="sxs-lookup"><span data-stu-id="a88fc-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="a88fc-159">处理完成后，Cognitive Services 将删除收据。</span><span class="sxs-lookup"><span data-stu-id="a88fc-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="a88fc-160">收据仍存储在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="a88fc-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="a88fc-161">有关详细信息，请参阅[使用表单识别器的新功能支持收据了解功能](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。</span><span class="sxs-lookup"><span data-stu-id="a88fc-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
