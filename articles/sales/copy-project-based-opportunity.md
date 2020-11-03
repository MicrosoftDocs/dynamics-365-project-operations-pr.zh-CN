---
title: 复制基于项目的商机
description: 此主题提供有关如何在 Project Operations 中复制基于项目的商机的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072543"
---
# <a name="copy-project-based-opportunities"></a><span data-ttu-id="18a70-103">复制基于项目的商机</span><span class="sxs-lookup"><span data-stu-id="18a70-103">Copy project-based opportunities</span></span>

<span data-ttu-id="18a70-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="18a70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="18a70-105">项目商机可以轻松地复制来创建新的项目商机。</span><span class="sxs-lookup"><span data-stu-id="18a70-105">Project opportunities can easily be copied to create new project opportunities.</span></span> 

1. <span data-ttu-id="18a70-106">转到 **项目商机** 列表页，从列表中选择商机。</span><span class="sxs-lookup"><span data-stu-id="18a70-106">Go to the **Project Opportunities** list page and select an opportunity from the list.</span></span> <span data-ttu-id="18a70-107">或者，打开特定商机的详细信息页。</span><span class="sxs-lookup"><span data-stu-id="18a70-107">Or, open the details page of a specific opportunity.</span></span> 
2. <span data-ttu-id="18a70-108">在任一页面，选择 **复制** 。</span><span class="sxs-lookup"><span data-stu-id="18a70-108">From either page, select **Copy**.</span></span> <span data-ttu-id="18a70-109">将打开一个包含以下字段信息的对话页面。</span><span class="sxs-lookup"><span data-stu-id="18a70-109">A dialog page will open that contains the following field information.</span></span> <span data-ttu-id="18a70-110">根据在此对话中选择的值，复制过程可能会有变化。</span><span class="sxs-lookup"><span data-stu-id="18a70-110">Depending on the values selected in this dialog, the copy process may change.</span></span>

    | <span data-ttu-id="18a70-111">**字段**</span><span class="sxs-lookup"><span data-stu-id="18a70-111">**Field**</span></span> | <span data-ttu-id="18a70-112">**关联性、用途和指导**</span><span class="sxs-lookup"><span data-stu-id="18a70-112">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="18a70-113">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="18a70-113">**Downstream impact**</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="18a70-114">主题</span><span class="sxs-lookup"><span data-stu-id="18a70-114">Topic</span></span> | <span data-ttu-id="18a70-115">输入目标商机的相关主题。</span><span class="sxs-lookup"><span data-stu-id="18a70-115">Enter the relevant topic of the target opportunity.</span></span> <span data-ttu-id="18a70-116">当对话打开时，系统会将其设置为源商机的主题，并附加 **copy** 。</span><span class="sxs-lookup"><span data-stu-id="18a70-116">When the dialog opens, the system will set it to the topic of the source opportunity with **copy** appended to it.</span></span> | <span data-ttu-id="18a70-117">此字段没有下游影响。</span><span class="sxs-lookup"><span data-stu-id="18a70-117">There's no downstream impact for this field.</span></span> |
    | <span data-ttu-id="18a70-118">帐户​​</span><span class="sxs-lookup"><span data-stu-id="18a70-118">Account</span></span> | <span data-ttu-id="18a70-119">对客户的公司或客户记录的引用。</span><span class="sxs-lookup"><span data-stu-id="18a70-119">References the customer's company or account record.</span></span> <span data-ttu-id="18a70-120">当对话打开时，系统会将其设置为源商机上的客户。</span><span class="sxs-lookup"><span data-stu-id="18a70-120">Wen the dialog opens, the system will set it to the account on the source opportunity.</span></span> | <span data-ttu-id="18a70-121">此字段是商机上的主要客户。</span><span class="sxs-lookup"><span data-stu-id="18a70-121">This field is the primary customer on the opportunity.</span></span> |
    | <span data-ttu-id="18a70-122">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="18a70-122">Contracting Unit</span></span> | <span data-ttu-id="18a70-123">负责交付与此交易关联的项目的部门。</span><span class="sxs-lookup"><span data-stu-id="18a70-123">The organization unit responsible for the delivery of the projects associated with this deal.</span></span> <span data-ttu-id="18a70-124">当对话打开时，系统会将其设置为源商机的合同签订部门。</span><span class="sxs-lookup"><span data-stu-id="18a70-124">When the dialog opens, the system will set it to the contracting unit of the source opportunity.</span></span> | <span data-ttu-id="18a70-125">合同签订部门是在交易完成后执行项目的公司的部门。</span><span class="sxs-lookup"><span data-stu-id="18a70-125">The contracting unit is the division of the company that executes the projects after the deal is closed.</span></span> <span data-ttu-id="18a70-126">每个合同签订部门都有一种货币，此货币用于报告项目中产生的预估成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="18a70-126">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |
    | <span data-ttu-id="18a70-127">货币</span><span class="sxs-lookup"><span data-stu-id="18a70-127">Currency</span></span> | <span data-ttu-id="18a70-128">进行交易所使用的货币。</span><span class="sxs-lookup"><span data-stu-id="18a70-128">The currency that the deal is transacted in.</span></span> <span data-ttu-id="18a70-129">当对话页面打开时，系统会将其设置为源商机的货币。</span><span class="sxs-lookup"><span data-stu-id="18a70-129">When the dialog page opens, the system will set it to the currency of the source opportunity.</span></span> | <span data-ttu-id="18a70-130">货币用于确定默认价目表以及在报价单上生成财务估算值。</span><span class="sxs-lookup"><span data-stu-id="18a70-130">Currency is used to default a price list and build financial estimates on the quote.</span></span> <span data-ttu-id="18a70-131">最后，当交易赢单时，此货币用于向客户开票。</span><span class="sxs-lookup"><span data-stu-id="18a70-131">Eventually, the currency is used to invoice the customer when the deal is won.</span></span> |
    | <span data-ttu-id="18a70-132">复制定价</span><span class="sxs-lookup"><span data-stu-id="18a70-132">Copy pricing</span></span> | <span data-ttu-id="18a70-133">“是/否”值指示是否应从源商机复制商机上的定价。</span><span class="sxs-lookup"><span data-stu-id="18a70-133">A Yes/No value that indicates if the pricing on the opportunity should be copied from the source opportunity.</span></span> | <span data-ttu-id="18a70-134">如果选择 **是** ，价目表将从源商机复制到目标商机。</span><span class="sxs-lookup"><span data-stu-id="18a70-134">If **Yes** is selected, price lists are copied from the source to the target opportunity.</span></span> <span data-ttu-id="18a70-135">如果选择 **否** ，会根据设置的最新价目表确定默认价目表。</span><span class="sxs-lookup"><span data-stu-id="18a70-135">If **No** is selected, price lists are defaulted based on the latest price lists that were set up.</span></span> |

3. <span data-ttu-id="18a70-136">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="18a70-136">Select **OK**.</span></span> <span data-ttu-id="18a70-137">系统将根据选定的参数创建项目商机的副本，新项目商机将打开。</span><span class="sxs-lookup"><span data-stu-id="18a70-137">The system creates a copy of the project opportunity based on the selected parameters and the new project opportunity is opened.</span></span>
