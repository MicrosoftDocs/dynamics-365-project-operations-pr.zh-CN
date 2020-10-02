---
title: 创建和确认更正日记帐
description: 此主题提供有关如何创建和确认更正日记帐的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896945"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="0de6a-103">创建和确认更正日记帐</span><span class="sxs-lookup"><span data-stu-id="0de6a-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="0de6a-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="0de6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0de6a-105">有时，可能未正确输入时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="0de6a-106">例如，顾问在创建时间条目时可能会选择错误的日期，也可能会在输入支出时转置这些数字。</span><span class="sxs-lookup"><span data-stu-id="0de6a-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="0de6a-107">如果顾问无法更新提交的条目，则管理员可以直接更正项目的条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="0de6a-108">若要完成本主题中的过程，您将需要管理员权限。</span><span class="sxs-lookup"><span data-stu-id="0de6a-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="0de6a-109">更正已批准的时间条目</span><span class="sxs-lookup"><span data-stu-id="0de6a-109">Correct approved time entries</span></span>     

<span data-ttu-id="0de6a-110">完成以下步骤以更正项目的一个或多个时间条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="0de6a-111">在**销售**区域中，选择**交易**，然后选择**已批准的时间**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="0de6a-112">在**已批准的时间**列表中，找到并选择一个或多个要更正的已批准时间条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="0de6a-113">您可以使用筛选器来查找相关条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="0de6a-114">例如，您可以对项目 ID 进行筛选，然后选择具有该项目 ID 的所有已批准时间条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="0de6a-115">选择**更正条目**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-115">Select **Correct entries**.</span></span> <span data-ttu-id="0de6a-116">系统会自动创建已分配类型为**时间更正**的新更正日记帐。</span><span class="sxs-lookup"><span data-stu-id="0de6a-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="0de6a-117">您选择的条目会添加到日记帐中。</span><span class="sxs-lookup"><span data-stu-id="0de6a-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="0de6a-118">在**新建日记帐**页上，输入您的更正日记帐的**说明**，然后选择**时间条目更正**选项卡。</span><span class="sxs-lookup"><span data-stu-id="0de6a-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="0de6a-119">在**时间条目的新值**部分中，根据需要使用正确的信息更新字段。</span><span class="sxs-lookup"><span data-stu-id="0de6a-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="0de6a-120">例如，您可以更改指派的项目或可预订资源。</span><span class="sxs-lookup"><span data-stu-id="0de6a-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="0de6a-121">选择**预览**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-121">Select **Preview**.</span></span> <span data-ttu-id="0de6a-122">在对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="0de6a-123">在**日记帐行**选项卡上，您可以查看与已冲销的所选时间条目相关的原始实际值列表，以及已创建的所更正相应行。</span><span class="sxs-lookup"><span data-stu-id="0de6a-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="0de6a-124">如果需要进行其他更正，请重复步骤 5 和步骤 6。</span><span class="sxs-lookup"><span data-stu-id="0de6a-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="0de6a-125">所有已更正的实际值将与您在**时间条目的新值**部分中选择的值相同。</span><span class="sxs-lookup"><span data-stu-id="0de6a-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="0de6a-126">如果更正按预期方式显示，请选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="0de6a-127">在对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="0de6a-128">返回到**销售**区域，选择**项目**，然后打开刚刚更新时间条目所针对的项目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="0de6a-129">在**项目**页上的**实际值**选项卡中，查看所做的更改。</span><span class="sxs-lookup"><span data-stu-id="0de6a-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="0de6a-130">如果**实际值**选项卡不可见，请选择**相关** > **实际值**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="0de6a-131">在**实际关联视图**列表中，您可以看到仍然列出了已冲销的原始时间条目，以及相应的已更正时间条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="0de6a-132">例如，在下图中，有两个数量为 8.00 的行项，“金额”列中列出了其相应的借项。</span><span class="sxs-lookup"><span data-stu-id="0de6a-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="0de6a-133">此外，还有两个数量为 -8.00 的行项，这些行项在“金额”列中显示了贷项金额。</span><span class="sxs-lookup"><span data-stu-id="0de6a-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="0de6a-134">这些更正会将数量调为零。</span><span class="sxs-lookup"><span data-stu-id="0de6a-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="0de6a-135">更正已批准的支出条目</span><span class="sxs-lookup"><span data-stu-id="0de6a-135">Correct approved expense entries</span></span>

<span data-ttu-id="0de6a-136">完成以下步骤以更正一个或多个支出条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="0de6a-137">在**销售**区域左侧导航窗格中的**交易**下面，选择**已批准的支出**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="0de6a-138">在**已批准的支出**列表中，选择要更正的项目，然后选择**更正条目**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="0de6a-139">系统将自动创建已分配类型为**支出更正**的新更正日记帐。</span><span class="sxs-lookup"><span data-stu-id="0de6a-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="0de6a-140">在**新建日记帐**页上，输入有关更正的**说明**，然后在**支出更正**选项卡上的**支出的新值**部分中，选择要为所选支出行更正的数据字段。</span><span class="sxs-lookup"><span data-stu-id="0de6a-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="0de6a-141">例如，您可以将支出分配给其他**项目**，或者更正**支出类别**、**支出日期**或**可预订的资源**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="0de6a-142">选择**预览**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-142">Select **Preview**.</span></span> <span data-ttu-id="0de6a-143">在对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="0de6a-144">在**日记帐行**选项卡上验证更正。您可以查看与已冲销的所选支出条目相关的原始实际值列表，以及已创建的所更正相应行。</span><span class="sxs-lookup"><span data-stu-id="0de6a-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="0de6a-145">如果更正的值符合预期，请选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="0de6a-146">在对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="0de6a-147">如果这些值未按预期方式显示，请选择**取消**以返回到**已批准的支出**列表。</span><span class="sxs-lookup"><span data-stu-id="0de6a-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="0de6a-148">重复步骤 2 到步骤 5。</span><span class="sxs-lookup"><span data-stu-id="0de6a-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="0de6a-149">已更正的实际值将与您在**支出的新值**部分中选择的值相同。</span><span class="sxs-lookup"><span data-stu-id="0de6a-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="0de6a-150">在确认了更正日记帐之后，请导航回您更新的一个或一些项目，以查看所做的更改。</span><span class="sxs-lookup"><span data-stu-id="0de6a-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="0de6a-151">在项目页中的**实际值**选项卡上，查看**实际关联视图**。</span><span class="sxs-lookup"><span data-stu-id="0de6a-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="0de6a-152">系统会列出原始条目和已更正的条目。</span><span class="sxs-lookup"><span data-stu-id="0de6a-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="0de6a-153">下图显示了原始支出条目金额和相应的已更正支出条目金额。</span><span class="sxs-lookup"><span data-stu-id="0de6a-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


