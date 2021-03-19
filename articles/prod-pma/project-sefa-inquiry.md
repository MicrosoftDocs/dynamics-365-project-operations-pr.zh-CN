---
title: 联邦奖励支出计划查询
description: 此主题提供有关联邦奖励支出计划查询的信息。
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288953"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="7bb49-103">联邦奖励支出计划查询</span><span class="sxs-lookup"><span data-stu-id="7bb49-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb49-104">根据 Office of Management and Budget Circular A-133，接收联邦资金的机构需要遵守审计要求，也称为单一审计。</span><span class="sxs-lookup"><span data-stu-id="7bb49-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="7bb49-105">审计流程用于定期报告联邦赠予的收入和支出。</span><span class="sxs-lookup"><span data-stu-id="7bb49-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="7bb49-106">单一审计报告的其中一部分是联邦奖励支出计划 (SEFA)。</span><span class="sxs-lookup"><span data-stu-id="7bb49-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="7bb49-107">联邦奖励支出计划查询包括“联邦国家补助目录 (CFDA)”标题和编号、赠予编号、赠予年份、提供资金的联邦机构的名称以及转赠实体的名称。</span><span class="sxs-lookup"><span data-stu-id="7bb49-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="7bb49-108">此查询针对特定期间。</span><span class="sxs-lookup"><span data-stu-id="7bb49-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="7bb49-109">通常，该期间与财务报表期间相同，即会计年度。</span><span class="sxs-lookup"><span data-stu-id="7bb49-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="7bb49-110">此查询包括在所选日期范围内具有预测日期的赠予。</span><span class="sxs-lookup"><span data-stu-id="7bb49-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="7bb49-111">查询的 **赠予机构** 列显示赠予客户或赠予机构（对于间接赠予）。</span><span class="sxs-lookup"><span data-stu-id="7bb49-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="7bb49-112">对于间接赠予，**中间机构** 列显示赠予客户。</span><span class="sxs-lookup"><span data-stu-id="7bb49-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="7bb49-113">如果不是间接赠予，**中间机构** 列为空白。</span><span class="sxs-lookup"><span data-stu-id="7bb49-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="7bb49-114">设置 CFDA 群集</span><span class="sxs-lookup"><span data-stu-id="7bb49-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="7bb49-115">您必须设置可与联邦奖励支出计划查询中的 CFDA 编号关联的 CFDA 群集。</span><span class="sxs-lookup"><span data-stu-id="7bb49-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="7bb49-116">转到 **项目管理和会计 \> 设置 \> 赠予 \> 联邦国家补助目录群集**。</span><span class="sxs-lookup"><span data-stu-id="7bb49-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="7bb49-117">选择 **新建** 创建 CFDA 群集。</span><span class="sxs-lookup"><span data-stu-id="7bb49-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="7bb49-118">输入群集名称。</span><span class="sxs-lookup"><span data-stu-id="7bb49-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="7bb49-119">选择 **保存** 以保存您所做的更改。</span><span class="sxs-lookup"><span data-stu-id="7bb49-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="7bb49-120">设置 CFDA 编号</span><span class="sxs-lookup"><span data-stu-id="7bb49-120">Set up CFDA numbers</span></span>

<span data-ttu-id="7bb49-121">您必须设置可以添加到赠予中并包含在联邦奖励支出计划查询中的 CFDA 编号。</span><span class="sxs-lookup"><span data-stu-id="7bb49-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="7bb49-122">转到 **项目管理和会计 \> 设置 \> 赠予 \> 联邦国家补助目录编号**。</span><span class="sxs-lookup"><span data-stu-id="7bb49-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="7bb49-123">选择 **新建** 创建 CFDA 编号。</span><span class="sxs-lookup"><span data-stu-id="7bb49-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="7bb49-124">在 **编号** 列中，输入 CFDA 编号。</span><span class="sxs-lookup"><span data-stu-id="7bb49-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="7bb49-125">按 **Tab** 键。</span><span class="sxs-lookup"><span data-stu-id="7bb49-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="7bb49-126">在 **说明** 列中，输入 CFDA 标题。</span><span class="sxs-lookup"><span data-stu-id="7bb49-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="7bb49-127">按 **Tab** 键。</span><span class="sxs-lookup"><span data-stu-id="7bb49-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="7bb49-128">可选：在 **计划群集** 字段中，添加适当的 CFDA 群集。</span><span class="sxs-lookup"><span data-stu-id="7bb49-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="7bb49-129">选择 **保存** 以保存您所做的更改。</span><span class="sxs-lookup"><span data-stu-id="7bb49-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="7bb49-130">设置赠予以针对联邦奖励支出计划查询进行报告</span><span class="sxs-lookup"><span data-stu-id="7bb49-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="7bb49-131">转到 **项目管理和会计 \> 赠予 \> 赠予**，选择现有赠予。</span><span class="sxs-lookup"><span data-stu-id="7bb49-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="7bb49-132">在 **设置** 快速选项卡上的 **联邦国家补助目录** 字段中，分配 CFDA 编号。</span><span class="sxs-lookup"><span data-stu-id="7bb49-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="7bb49-133">赠予上的 CFDA 编号确定用于报告的 CFDA 群集。</span><span class="sxs-lookup"><span data-stu-id="7bb49-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="7bb49-134">在 **联系信息** 快速选项卡上，按照以下步骤输入赠予方信息：</span><span class="sxs-lookup"><span data-stu-id="7bb49-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="7bb49-135">在 **赠予客户** 字段中，输入负责赠予的客户。</span><span class="sxs-lookup"><span data-stu-id="7bb49-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="7bb49-136">对于现有赠予，可能已经输入了此信息。</span><span class="sxs-lookup"><span data-stu-id="7bb49-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="7bb49-137">指明赠予客户是否是出资者。</span><span class="sxs-lookup"><span data-stu-id="7bb49-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="7bb49-138">如果赠予客户是出资者，保留 **间接** 复选框不选。</span><span class="sxs-lookup"><span data-stu-id="7bb49-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="7bb49-139">如果另一个客户是出资者，赠予客户负责使用和跟踪资金，则选中 **间接** 复选框。</span><span class="sxs-lookup"><span data-stu-id="7bb49-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="7bb49-140">如果您在上一步中选择了 **间接** 复选框，在 **赠予机构** 字段中，输入提供赠予的客户。</span><span class="sxs-lookup"><span data-stu-id="7bb49-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="7bb49-141">赠予机构和赠予客户不能是同一客户。</span><span class="sxs-lookup"><span data-stu-id="7bb49-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="7bb49-142">下面是一个间接赠予的示例：</span><span class="sxs-lookup"><span data-stu-id="7bb49-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="7bb49-143">联邦政府资助了某个州的一个基础设施项目。</span><span class="sxs-lookup"><span data-stu-id="7bb49-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="7bb49-144">联邦政府将资金交给该州来使用。</span><span class="sxs-lookup"><span data-stu-id="7bb49-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="7bb49-145">在此例中，联邦政府是赠予机构，该州为赠予客户。</span><span class="sxs-lookup"><span data-stu-id="7bb49-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="7bb49-146">当您第一次启用此功能时，将使用赠予上的现有编号输入初始 CFDA 编号。</span><span class="sxs-lookup"><span data-stu-id="7bb49-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="7bb49-147">基于赠予类型从 SEFA 报告中排除赠予</span><span class="sxs-lookup"><span data-stu-id="7bb49-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="7bb49-148">转到 **项目管理和会计 \> 设置 \> 赠予 \> 赠予类型**。</span><span class="sxs-lookup"><span data-stu-id="7bb49-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="7bb49-149">在 **默认信息** 快速选项卡上，选择 **从联邦奖励支出计划中排除** 复选框。</span><span class="sxs-lookup"><span data-stu-id="7bb49-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="7bb49-150">选择 **保存** 以保存您所做的更改。</span><span class="sxs-lookup"><span data-stu-id="7bb49-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="7bb49-151">运行联邦奖励支出计划查询</span><span class="sxs-lookup"><span data-stu-id="7bb49-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="7bb49-152">转到 **项目管理和会计 \> 查询和报表 \> 赠予查询 \> 联邦奖励支出计划**。</span><span class="sxs-lookup"><span data-stu-id="7bb49-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="7bb49-153">在 **参数** 部分，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="7bb49-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="7bb49-154">在 **日期间隔** 字段中，选择日期间隔的代码。</span><span class="sxs-lookup"><span data-stu-id="7bb49-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="7bb49-155">或者，在 **起始日期** 和 **截止日期** 字段中，定义日期间隔。</span><span class="sxs-lookup"><span data-stu-id="7bb49-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="7bb49-156">可选：若要仅将已记帐交易作为收入包括在查询中，请将 **仅包括已记帐收入** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="7bb49-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="7bb49-157">列数</span><span class="sxs-lookup"><span data-stu-id="7bb49-157">Columns</span></span>

<span data-ttu-id="7bb49-158">联邦奖励支出计划查询包括以下列：</span><span class="sxs-lookup"><span data-stu-id="7bb49-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="7bb49-159">联邦国家补助目录的群集名称</span><span class="sxs-lookup"><span data-stu-id="7bb49-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="7bb49-160">赠予机构</span><span class="sxs-lookup"><span data-stu-id="7bb49-160">Grantor agency</span></span>
- <span data-ttu-id="7bb49-161">中间机构</span><span class="sxs-lookup"><span data-stu-id="7bb49-161">Pass-through agency</span></span>
- <span data-ttu-id="7bb49-162">赠予名称</span><span class="sxs-lookup"><span data-stu-id="7bb49-162">Grant name</span></span>
- <span data-ttu-id="7bb49-163">赠予 ID</span><span class="sxs-lookup"><span data-stu-id="7bb49-163">Grant ID</span></span>
- <span data-ttu-id="7bb49-164">赠予申请 ID</span><span class="sxs-lookup"><span data-stu-id="7bb49-164">Grant application ID</span></span>
- <span data-ttu-id="7bb49-165">联邦国家补助目录</span><span class="sxs-lookup"><span data-stu-id="7bb49-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="7bb49-166">收据</span><span class="sxs-lookup"><span data-stu-id="7bb49-166">Receipts</span></span>
- <span data-ttu-id="7bb49-167">支出</span><span class="sxs-lookup"><span data-stu-id="7bb49-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]