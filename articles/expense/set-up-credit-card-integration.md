---
title: 设置信用卡集成
description: 此主题介绍如何导入和维护与支出相关的信用卡交易记录。
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
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120847"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="3c461-103">设置信用卡集成</span><span class="sxs-lookup"><span data-stu-id="3c461-103">Set up credit card integration</span></span>

<span data-ttu-id="3c461-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="3c461-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3c461-105">可以设置与支出相关的信用卡交易记录，以将其自动导入到定期计划中。</span><span class="sxs-lookup"><span data-stu-id="3c461-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3c461-106">或者，可以根据需要手动导入交易记录。</span><span class="sxs-lookup"><span data-stu-id="3c461-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3c461-107">信用卡交易记录通过信用卡交易记录数据实体导入。</span><span class="sxs-lookup"><span data-stu-id="3c461-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3c461-108">导入信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="3c461-108">Import credit card transactions</span></span>

1. <span data-ttu-id="3c461-109">在 **信用卡交易记录** 页上，选择 **导入交易记录**。</span><span class="sxs-lookup"><span data-stu-id="3c461-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3c461-110">如果您是第一次打开数据管理，系统必须更新数据实体列表，然后才能继续。</span><span class="sxs-lookup"><span data-stu-id="3c461-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3c461-111">在 **名称** 字段中，为导入作业输入唯一说明。</span><span class="sxs-lookup"><span data-stu-id="3c461-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="3c461-112">在 **源数据格式** 字段中，选择包含要导入的信用卡交易记录的文件的格式。</span><span class="sxs-lookup"><span data-stu-id="3c461-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3c461-113">选择 **上载**，然后查找并选择要导入的文件。</span><span class="sxs-lookup"><span data-stu-id="3c461-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3c461-114">上载文件后，通过选择磁贴上的 **查看映射** 链接，验证信用卡交易记录文件和信用卡交易记录数据实体的列的映射。</span><span class="sxs-lookup"><span data-stu-id="3c461-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3c461-115">如果存在映射错误，或者您必须更改映射，请从 **映射可视化项** 选项卡或 **映射详细信息** 选项卡更改映射。</span><span class="sxs-lookup"><span data-stu-id="3c461-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3c461-116">若要自动处理信用卡交易记录，请选择 **创建定期数据作业**。</span><span class="sxs-lookup"><span data-stu-id="3c461-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3c461-117">然后，您可以设置定义应如何导入信用卡交易记录的定期计划。</span><span class="sxs-lookup"><span data-stu-id="3c461-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3c461-118">在您完成时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3c461-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3c461-119">若要立即导入所选的文件，请选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="3c461-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3c461-120">如果在导入过程中出现错误，您可以查看执行日志或暂存数据，来查看为帮助确保成功导入而必须修复的错误。</span><span class="sxs-lookup"><span data-stu-id="3c461-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3c461-121">如果必须导入多个文件格式，必须为每个格式类型创建单独的导入作业。</span><span class="sxs-lookup"><span data-stu-id="3c461-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3c461-122">重新分配已离职员工的信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="3c461-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3c461-123">员工记录终止后，该员工的 Active Directory 域服务 (AD DS) 帐户将被禁用。</span><span class="sxs-lookup"><span data-stu-id="3c461-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3c461-124">不过，可能存在仍需要支出和还款的活动信用卡交易记录。</span><span class="sxs-lookup"><span data-stu-id="3c461-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3c461-125">在 **信用卡交易记录** 页上，您可以为已离职的关联员工的任何信用卡交易记录重新分配员工。</span><span class="sxs-lookup"><span data-stu-id="3c461-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3c461-126">选择一个或多个信用卡交易记录，然后选择 **重新分配交易记录**。</span><span class="sxs-lookup"><span data-stu-id="3c461-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3c461-127">然后，您可以选择要向其分配信用卡交易记录的另一名员工。</span><span class="sxs-lookup"><span data-stu-id="3c461-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3c461-128">在信用卡交易记录重新分配后，可以选择将其用于支出报表，并通过通常的支出报表还款流程进行支付。</span><span class="sxs-lookup"><span data-stu-id="3c461-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
