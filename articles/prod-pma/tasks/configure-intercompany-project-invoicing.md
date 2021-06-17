---
title: 配置内部公司项目开票
description: 此主题显示如何设置贵组织内部两个公司之间的项目开票。
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001190"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="88d16-103">配置内部公司项目开票</span><span class="sxs-lookup"><span data-stu-id="88d16-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88d16-104">此主题显示如何设置贵组织内部两个公司之间的项目开票。</span><span class="sxs-lookup"><span data-stu-id="88d16-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="88d16-105">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="88d16-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="88d16-106">在导航窗格中，转到 **模块 > 应付帐款 > 供应商 > 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="88d16-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="88d16-107">在 **所有供应商** 列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="88d16-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="88d16-108">在操作窗格上，选择 **常规**。</span><span class="sxs-lookup"><span data-stu-id="88d16-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="88d16-109">选择 **内部公司**。</span><span class="sxs-lookup"><span data-stu-id="88d16-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="88d16-110">将 **有效** 设置为 **是** 以启用内部公司贸易。</span><span class="sxs-lookup"><span data-stu-id="88d16-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="88d16-111">在 **客户公司** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="88d16-112">在 **我的帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="88d16-113">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="88d16-113">Select **Save**.</span></span>
9. <span data-ttu-id="88d16-114">关闭页面将返回到主页。</span><span class="sxs-lookup"><span data-stu-id="88d16-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="88d16-115">在导航窗格中，转到 **模块 > 项目管理和核算 > 设置 > 项目管理与核算参数**。</span><span class="sxs-lookup"><span data-stu-id="88d16-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="88d16-116">选择 **内部公司** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="88d16-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="88d16-117">将滑块移到 **是** 以启用公司间资源计划编制和工时单。</span><span class="sxs-lookup"><span data-stu-id="88d16-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="88d16-118">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="88d16-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="88d16-119">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="88d16-119">Select **New**.</span></span>
15. <span data-ttu-id="88d16-120">在 **借人方法人** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="88d16-121">选中 **应计收入** 复选框。</span><span class="sxs-lookup"><span data-stu-id="88d16-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="88d16-122">在 **默认工时单类别** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="88d16-123">在 **默认费用类别** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="88d16-124">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="88d16-124">Select **Save**.</span></span>
20. <span data-ttu-id="88d16-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="88d16-125">Close the page.</span></span>
21. <span data-ttu-id="88d16-126">在导航窗格中，转到 **模块 > 项目管理与核算 > 设置 > 过帐 > 分类帐过帐设置**。</span><span class="sxs-lookup"><span data-stu-id="88d16-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="88d16-127">在 **会计科目类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="88d16-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="88d16-128">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="88d16-128">Select **New**.</span></span>
24. <span data-ttu-id="88d16-129">在新行的 **主科目** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="88d16-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="88d16-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="88d16-130">Select **Save**.</span></span>
26. <span data-ttu-id="88d16-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="88d16-131">Close the page.</span></span>
27. <span data-ttu-id="88d16-132">在导航窗格中，转到 **模块 > 项目管理与核算 > 设置 > 价格 > 转让价格**。</span><span class="sxs-lookup"><span data-stu-id="88d16-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="88d16-133">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="88d16-133">Select **New**.</span></span>
29. <span data-ttu-id="88d16-134">在 **生效日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="88d16-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="88d16-135">在 **借人方法人** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="88d16-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="88d16-136">在 **转让价格模型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="88d16-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="88d16-137">在 **定价** 字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="88d16-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="88d16-138">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="88d16-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]