---
title: 导入和维护信用卡交易记录
description: 此主题介绍如何导入和维护与支出相关的信用卡交易记录。 这些交易记录可以设置为对重复执行的计划自动导入或根据需要手动导入。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271567"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="703fe-104">导入和维护信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="703fe-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="703fe-105">可以设置与支出相关的信用卡交易记录，以将其自动导入到定期计划中。</span><span class="sxs-lookup"><span data-stu-id="703fe-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="703fe-106">或者，可以根据需要手动导入交易记录。</span><span class="sxs-lookup"><span data-stu-id="703fe-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="703fe-107">信用卡交易记录通过信用卡交易记录数据实体导入。</span><span class="sxs-lookup"><span data-stu-id="703fe-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="703fe-108">有关数据实体的详细信息，请参阅[数据实体](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)。</span><span class="sxs-lookup"><span data-stu-id="703fe-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="703fe-109">导入信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="703fe-109">Import credit card transactions</span></span>

1. <span data-ttu-id="703fe-110">在 **信用卡交易记录** 页上，选择 **导入交易记录**。</span><span class="sxs-lookup"><span data-stu-id="703fe-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="703fe-111">如果您是第一次打开数据管理，系统必须更新数据实体列表，然后才能继续。</span><span class="sxs-lookup"><span data-stu-id="703fe-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="703fe-112">在 **名称** 字段中，为导入作业输入唯一说明。</span><span class="sxs-lookup"><span data-stu-id="703fe-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="703fe-113">在 **源数据格式** 字段中，选择包含要导入的信用卡交易记录的文件的格式。</span><span class="sxs-lookup"><span data-stu-id="703fe-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="703fe-114">选择 **上载**，然后查找并选择要导入的文件。</span><span class="sxs-lookup"><span data-stu-id="703fe-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="703fe-115">上载文件后，通过选择磁贴上的 **查看映射** 链接，验证信用卡交易记录文件和信用卡交易记录数据实体的列的映射。</span><span class="sxs-lookup"><span data-stu-id="703fe-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="703fe-116">如果存在映射错误，或者您必须更改映射，请从 **映射可视化项** 选项卡或 **映射详细信息** 选项卡更改映射。</span><span class="sxs-lookup"><span data-stu-id="703fe-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="703fe-117">若要自动处理信用卡交易记录，请选择 **创建定期数据作业**。</span><span class="sxs-lookup"><span data-stu-id="703fe-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="703fe-118">然后，您可以设置定义应如何导入信用卡交易记录的定期计划。</span><span class="sxs-lookup"><span data-stu-id="703fe-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="703fe-119">在您完成时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="703fe-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="703fe-120">若要立即导入所选的文件，请选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="703fe-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="703fe-121">如果在导入过程中出现错误，您可以查看执行日志或暂存数据，来查看为帮助确保成功导入而必须修复的错误。</span><span class="sxs-lookup"><span data-stu-id="703fe-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="703fe-122">如果必须导入多个文件格式，必须为每个格式类型创建单独的导入作业。</span><span class="sxs-lookup"><span data-stu-id="703fe-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="703fe-123">重新分配已离职员工的信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="703fe-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="703fe-124">员工记录终止后，该员工的 Active Directory 域服务 (AD DS) 帐户将被禁用。</span><span class="sxs-lookup"><span data-stu-id="703fe-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="703fe-125">不过，可能存在仍需要支出和还款的活动信用卡交易记录。</span><span class="sxs-lookup"><span data-stu-id="703fe-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="703fe-126">在 **信用卡交易记录** 页上，您可以为已离职的关联员工的任何信用卡交易记录重新分配员工。</span><span class="sxs-lookup"><span data-stu-id="703fe-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="703fe-127">选择一个或多个信用卡交易记录，然后选择 **重新分配交易记录**。</span><span class="sxs-lookup"><span data-stu-id="703fe-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="703fe-128">然后，您可以选择要向其分配信用卡交易记录的另一名员工。</span><span class="sxs-lookup"><span data-stu-id="703fe-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="703fe-129">在信用卡交易记录重新分配后，可以选择将其用于支出报表，并通过通常的支出报表还款流程进行支付。</span><span class="sxs-lookup"><span data-stu-id="703fe-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]