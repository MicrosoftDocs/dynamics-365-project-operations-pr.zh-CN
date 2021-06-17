---
title: 定义支出策略
description: 您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出策略。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001865"
---
# <a name="define-expense-policies"></a><span data-ttu-id="55eb6-103">定义支出策略</span><span class="sxs-lookup"><span data-stu-id="55eb6-103">Define expense policies</span></span>

<span data-ttu-id="55eb6-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="55eb6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55eb6-105">您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的策略。</span><span class="sxs-lookup"><span data-stu-id="55eb6-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="55eb6-106">实施支出策略可帮助您有效地管理支出。</span><span class="sxs-lookup"><span data-stu-id="55eb6-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="55eb6-107">例如，您可以为纽约市的酒店支出设置策略，规定每晚支出不得超过 250 美元。</span><span class="sxs-lookup"><span data-stu-id="55eb6-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="55eb6-108">如果工作人员提交的支出报表或出差申请中房间费率超过此金额，系统会通知</span><span class="sxs-lookup"><span data-stu-id="55eb6-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="55eb6-109">工作人员已超过支出的策略金额。</span><span class="sxs-lookup"><span data-stu-id="55eb6-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="55eb6-110">在定义策略时您可以配置工作人员</span><span class="sxs-lookup"><span data-stu-id="55eb6-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="55eb6-111">将收到的消息。</span><span class="sxs-lookup"><span data-stu-id="55eb6-111">define the policy.</span></span>      
        
<span data-ttu-id="55eb6-112">您可以定义三种类型的策略：</span><span class="sxs-lookup"><span data-stu-id="55eb6-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="55eb6-113">**警告**：允许工作人员提交支出报表或出差申请，但会向所有审批者以及以后的报告</span><span class="sxs-lookup"><span data-stu-id="55eb6-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="55eb6-114">标记此支出。</span><span class="sxs-lookup"><span data-stu-id="55eb6-114">for later reporting.</span></span>        

- <span data-ttu-id="55eb6-115">**错误**：需要工作人员在提交支出报表或出差申请之前修改支出以遵守策略。</span><span class="sxs-lookup"><span data-stu-id="55eb6-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="55eb6-116">**理由**：需要工作人员或经理在提交支出报表或出差申请之前，输入超过策略金额的理由。</span><span class="sxs-lookup"><span data-stu-id="55eb6-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="55eb6-117">策略提示</span><span class="sxs-lookup"><span data-stu-id="55eb6-117">Policy tips</span></span>
<span data-ttu-id="55eb6-118">在为支出管理创建新策略时，以下一些建议可以为您提供帮助：</span><span class="sxs-lookup"><span data-stu-id="55eb6-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="55eb6-119">策略是有时效的，这意味着在使用晚于支出发生日期的日期创建时，策略不会生效。</span><span class="sxs-lookup"><span data-stu-id="55eb6-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="55eb6-120">例如，您今天创建了一个新策略，来强制执行餐饮支出最多 50 美元。</span><span class="sxs-lookup"><span data-stu-id="55eb6-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="55eb6-121">在昨天以前输入的所有现有支出都不会根据此策略进行检查。</span><span class="sxs-lookup"><span data-stu-id="55eb6-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="55eb6-122">在为可细化的支出类别创建策略时，请考虑为支出行类型添加条件。</span><span class="sxs-lookup"><span data-stu-id="55eb6-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="55eb6-123">某些策略（如需要收据）在明细行中可能没有意义。</span><span class="sxs-lookup"><span data-stu-id="55eb6-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="55eb6-124">在此情况下，该策略仅应用于标题行或非明细行。</span><span class="sxs-lookup"><span data-stu-id="55eb6-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="55eb6-125">默认情况下，根据源实体评估支出管理策略。</span><span class="sxs-lookup"><span data-stu-id="55eb6-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="55eb6-126">对于内部公司场景，您可以改为针对目标实体（借款实体）设置要评估的策略。</span><span class="sxs-lookup"><span data-stu-id="55eb6-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="55eb6-127">要针对目标实体运行策略，请在 **功能管理** 工作区中打开 **针对借款法人评估支出政策** 功能。</span><span class="sxs-lookup"><span data-stu-id="55eb6-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="55eb6-128">评估策略的时间</span><span class="sxs-lookup"><span data-stu-id="55eb6-128">When to evaluate policies</span></span>

<span data-ttu-id="55eb6-129">在支出管理参数中，您可以选择在保存明细或提交支出报表时评估支出管理策略。</span><span class="sxs-lookup"><span data-stu-id="55eb6-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="55eb6-130">如果您选择在保存明细时进行评估，用户将提前了解到一次完成支出报表所需执行的操作。</span><span class="sxs-lookup"><span data-stu-id="55eb6-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="55eb6-131">或者，您可以在提交到工作流期间通过在最后进行验证来延后策略评估，从而节省时间。</span><span class="sxs-lookup"><span data-stu-id="55eb6-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]