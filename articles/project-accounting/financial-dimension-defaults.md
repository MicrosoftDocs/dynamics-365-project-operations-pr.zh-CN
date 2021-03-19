---
title: 财务维度默认值
description: 此主题提供有关如何设置财务维度默认值的信息。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287362"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="2beba-103">财务维度默认值</span><span class="sxs-lookup"><span data-stu-id="2beba-103">Financial dimension defaults</span></span>

<span data-ttu-id="2beba-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2beba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2beba-105">Dynamics 365 Project Operations 使用 Dynamics 365 Finance 中的[财务维度](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions)框架提供有关项目子分类帐和总帐交易的其他见解。</span><span class="sxs-lookup"><span data-stu-id="2beba-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="2beba-106">默认财务维度可以在客户、项目资金来源、里程碑、项目合同子项或项目上设置。</span><span class="sxs-lookup"><span data-stu-id="2beba-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="2beba-107">定义客户的默认财务维度</span><span class="sxs-lookup"><span data-stu-id="2beba-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="2beba-108">客户维度默认值在 Finance 中指定。</span><span class="sxs-lookup"><span data-stu-id="2beba-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="2beba-109">完成以下步骤设置维度默认值。</span><span class="sxs-lookup"><span data-stu-id="2beba-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="2beba-110">转到 **应收帐款** > **客户** > **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="2beba-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="2beba-111">在 **客户** 页上的 **财务维度** 选项卡上，为特定客户设置财务维度值。</span><span class="sxs-lookup"><span data-stu-id="2beba-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="2beba-112">定义项目合同的默认财务维度</span><span class="sxs-lookup"><span data-stu-id="2beba-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="2beba-113">项目合同在 Common Data Service (CDS) 中创建和维护。</span><span class="sxs-lookup"><span data-stu-id="2beba-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="2beba-114">项目合同的会计属性在 Finance 中的 **项目管理和会计** 模块中设置。</span><span class="sxs-lookup"><span data-stu-id="2beba-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="2beba-115">为项目资金来源设置财务维度</span><span class="sxs-lookup"><span data-stu-id="2beba-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="2beba-116">转到 **项目管理和会计** > **项目** > **项目合同**。</span><span class="sxs-lookup"><span data-stu-id="2beba-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2beba-117">选择要更新的记录，然后在 **项目合同** 选项卡上，选择 **显示默认会计**。</span><span class="sxs-lookup"><span data-stu-id="2beba-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2beba-118">展开 **相关信息**，选择 **资金来源** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2beba-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="2beba-119">设置财务维度默认值。</span><span class="sxs-lookup"><span data-stu-id="2beba-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="2beba-120">请注意，财务维度默认来自客户帐户。</span><span class="sxs-lookup"><span data-stu-id="2beba-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="2beba-121">为项目合同子项设置财务维度</span><span class="sxs-lookup"><span data-stu-id="2beba-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="2beba-122">转到 **项目管理和会计** > **项目** > **项目合同**。</span><span class="sxs-lookup"><span data-stu-id="2beba-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2beba-123">选择要更新的记录，然后在 **项目合同** 选项卡上，选择 **显示默认会计**。</span><span class="sxs-lookup"><span data-stu-id="2beba-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2beba-124">展开 **相关信息**，选择 **合同子项** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2beba-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="2beba-125">设置财务维度默认值。</span><span class="sxs-lookup"><span data-stu-id="2beba-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="2beba-126">财务维度默认值适用，但只能用于固定价格（里程碑）合同子项。</span><span class="sxs-lookup"><span data-stu-id="2beba-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="2beba-127">这些默认值用于相关的项目分期付款交易和发票明细。</span><span class="sxs-lookup"><span data-stu-id="2beba-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="2beba-128">定义项目的默认财务维度</span><span class="sxs-lookup"><span data-stu-id="2beba-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="2beba-129">项目在 CDS 中创建和维护。</span><span class="sxs-lookup"><span data-stu-id="2beba-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="2beba-130">项目的会计属性在 Finance 中的 **项目管理和会计** 模块中设置。</span><span class="sxs-lookup"><span data-stu-id="2beba-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="2beba-131">转到 **项目管理和会计** > **项目** > **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="2beba-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="2beba-132">选择要更新的记录，然后在 **项目** 选项卡上，选择 **显示默认会计**。</span><span class="sxs-lookup"><span data-stu-id="2beba-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2beba-133">展开 **相关信息**，选择 **设置** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2beba-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="2beba-134">设置财务维度默认值。</span><span class="sxs-lookup"><span data-stu-id="2beba-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="2beba-135">请注意，财务维度默认来自客户帐户。</span><span class="sxs-lookup"><span data-stu-id="2beba-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="2beba-136">如果项目与具有多个项目合同客户的合同子项关联，主要客户将用于确定默认财务维度。</span><span class="sxs-lookup"><span data-stu-id="2beba-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="2beba-137">项目默认财务维度用于设置 **Project Operations 集成日记帐** 和相关项目发票明细上的时间、支出和费用交易的日记帐行默认值。</span><span class="sxs-lookup"><span data-stu-id="2beba-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]