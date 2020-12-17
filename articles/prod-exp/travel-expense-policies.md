---
title: 设置支出策略
description: 您可以在 Microsoft Dynamics 365 Finance 中设置您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出策略。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650083"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="e2c79-103">设置支出策略</span><span class="sxs-lookup"><span data-stu-id="e2c79-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2c79-104">您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的策略。</span><span class="sxs-lookup"><span data-stu-id="e2c79-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="e2c79-105">实施支出策略可帮助您有效地管理支出。</span><span class="sxs-lookup"><span data-stu-id="e2c79-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="e2c79-106">例如，您可以为纽约市的酒店支出设置策略，规定每晚支出不得超过 250 美元。</span><span class="sxs-lookup"><span data-stu-id="e2c79-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="e2c79-107">如果员工提交的支出报表或出差申请中的房费超过了此金额，系统将通知</span><span class="sxs-lookup"><span data-stu-id="e2c79-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="e2c79-108">工作人员已超过支出的策略金额。</span><span class="sxs-lookup"><span data-stu-id="e2c79-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="e2c79-109">在定义策略时您可以配置工作人员</span><span class="sxs-lookup"><span data-stu-id="e2c79-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="e2c79-110">将收到的消息。</span><span class="sxs-lookup"><span data-stu-id="e2c79-110">define the policy.</span></span>      
        
<span data-ttu-id="e2c79-111">您可以定义三种类型的策略：</span><span class="sxs-lookup"><span data-stu-id="e2c79-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="e2c79-112">警告 – 允许工作人员提交支出报表或出差申请，但将为所有审核人和最新报表</span><span class="sxs-lookup"><span data-stu-id="e2c79-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="e2c79-113">标记此支出。</span><span class="sxs-lookup"><span data-stu-id="e2c79-113">for later reporting.</span></span>        

- <span data-ttu-id="e2c79-114">错误 – 在提交支出报表或出差申请前，要求工作人员修改该支出以符合该策略。</span><span class="sxs-lookup"><span data-stu-id="e2c79-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="e2c79-115">调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出策略金额的调整。</span><span class="sxs-lookup"><span data-stu-id="e2c79-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="e2c79-116">策略提示</span><span class="sxs-lookup"><span data-stu-id="e2c79-116">Policy tips</span></span>
<span data-ttu-id="e2c79-117">下面是一些在为支出管理新建策略时可以帮助您的建议。</span><span class="sxs-lookup"><span data-stu-id="e2c79-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="e2c79-118">策略有生效日期，如果创建策略时不为其设置支出产生后的日期，策略不会生效。</span><span class="sxs-lookup"><span data-stu-id="e2c79-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="e2c79-119">例如，如果今天创建新策略以实施最大餐费 50 美元，则不会针对此策略检查截止昨天的任何现有支出。</span><span class="sxs-lookup"><span data-stu-id="e2c79-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="e2c79-120">在为可细化的支出类别创建策略时，请考虑为支出行类型添加条件。</span><span class="sxs-lookup"><span data-stu-id="e2c79-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="e2c79-121">某些策略（如索取收据）可能对明细化行无意义，只应该应用于标题行或非明细化行。</span><span class="sxs-lookup"><span data-stu-id="e2c79-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="e2c79-122">默认情况下，根据源实体评估支出管理策略。</span><span class="sxs-lookup"><span data-stu-id="e2c79-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="e2c79-123">对于内部公司场景，您可以改为针对目标实体（借款实体）设置要评估的策略。</span><span class="sxs-lookup"><span data-stu-id="e2c79-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="e2c79-124">若要针对目标法人运行策略，请在 **功能管理** 工作区中开启“根据借入方法人评估策略”。</span><span class="sxs-lookup"><span data-stu-id="e2c79-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="e2c79-125">评估策略的时间</span><span class="sxs-lookup"><span data-stu-id="e2c79-125">When to evaluate policies</span></span>

<span data-ttu-id="e2c79-126">支出管理参数中有一个选项，用于在保存行时或在提交支出报表时评估支出管理策略。</span><span class="sxs-lookup"><span data-stu-id="e2c79-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="e2c79-127">如果选择在保存行时评估，这将确保用户可以查看需要执行哪些操作才能一次性完成所有支出报表。</span><span class="sxs-lookup"><span data-stu-id="e2c79-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="e2c79-128">否则，如果要在结束时向工作流提交期间进行验证，可以推迟策略评估并节约时间。</span><span class="sxs-lookup"><span data-stu-id="e2c79-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
