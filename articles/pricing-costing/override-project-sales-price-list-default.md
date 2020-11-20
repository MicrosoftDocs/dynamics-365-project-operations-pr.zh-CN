---
title: 替代项目销售价目表
description: 此主题提供有关创建自定义销售价目表的信息。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130837"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="e0110-103">替代项目销售价目表</span><span class="sxs-lookup"><span data-stu-id="e0110-103">Override project sales price lists</span></span>

<span data-ttu-id="e0110-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="e0110-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="e0110-105">特定于客户的项目价目表</span><span class="sxs-lookup"><span data-stu-id="e0110-105">Customer-specific project price lists</span></span>

<span data-ttu-id="e0110-106">在 Dynamics 365 Project Operations 中，特定于客户的价格协议可以设置为客户记录中的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="e0110-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="e0110-107">若要设置特定于客户的项目价目表，在 **销售** 区域，导航到客户记录。</span><span class="sxs-lookup"><span data-stu-id="e0110-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="e0110-108">打开 **客户** 列表页。</span><span class="sxs-lookup"><span data-stu-id="e0110-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="e0110-109">找到并双击客户记录打开 **客户** 详细信息页。</span><span class="sxs-lookup"><span data-stu-id="e0110-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="e0110-110">在 **项目价目表** 选项卡上，选择 \*\*+ 新建项目价目表^^。</span><span class="sxs-lookup"><span data-stu-id="e0110-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="e0110-111">在 **新建项目价目表** 页上，从下拉列表中选择一个价目表。</span><span class="sxs-lookup"><span data-stu-id="e0110-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="e0110-112">仅包含将上下文设置为 **销售** 且其货币与客户货币匹配的价目表。</span><span class="sxs-lookup"><span data-stu-id="e0110-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="e0110-113">为关联命名，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e0110-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="e0110-114">特定于客户的项目价目表已创建。</span><span class="sxs-lookup"><span data-stu-id="e0110-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="e0110-115">此价目表将用于设定为此客户创建的报价单或项目合同的创建日期在价目表有效期内的项目报价单或合同上的默认项目价格。</span><span class="sxs-lookup"><span data-stu-id="e0110-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="e0110-116">项目报价单上的自定义定价</span><span class="sxs-lookup"><span data-stu-id="e0110-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="e0110-117">在项目报价单上，您可以使用从默认值来自客户或项目参数的默认标准价目表开始的项目定价。</span><span class="sxs-lookup"><span data-stu-id="e0110-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="e0110-118">当您需要为特定报价单上的项目相关工作进行自定义定价时，可以从与项目价目表关联的实体获取自定义定价。</span><span class="sxs-lookup"><span data-stu-id="e0110-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="e0110-119">完成以下步骤，设置特定于报价单的项目定价。</span><span class="sxs-lookup"><span data-stu-id="e0110-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="e0110-120">打开项目报价单，选择 **项目价目表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e0110-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="e0110-121">在子网格中，选择 **创建自定义定价**。</span><span class="sxs-lookup"><span data-stu-id="e0110-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="e0110-122">附加到报价单的所有项目价目表都将复制到新价目表中。</span><span class="sxs-lookup"><span data-stu-id="e0110-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="e0110-123">新价目表的名称将反映报价单的名称，其中包含创建这些价目表的日期时间戳。</span><span class="sxs-lookup"><span data-stu-id="e0110-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="e0110-124">您可以使用其中的每个价目表，并可以对人工（角色价格）和支出（类别价格）价格进行更新。</span><span class="sxs-lookup"><span data-stu-id="e0110-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="e0110-125">这些价格仅适用于此项目报价单。</span><span class="sxs-lookup"><span data-stu-id="e0110-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="e0110-126">项目合同上的价目表</span><span class="sxs-lookup"><span data-stu-id="e0110-126">Price lists on a project contract</span></span>

<span data-ttu-id="e0110-127">在项目合同上，项目定价始终默认为具有合同名称并且创建日期时间戳附加到名称中的自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="e0110-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="e0110-128">无论是在报价单赢单时创建合同，还是从头创建合同，都是如此。</span><span class="sxs-lookup"><span data-stu-id="e0110-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="e0110-129">如果需要，您可以删除与自定义价目表的这一关联，然后将标准价目表与项目合同关联。</span><span class="sxs-lookup"><span data-stu-id="e0110-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="e0110-130">当您将标准价目表与报价单或合同上的项目价目表关联时，对价目表中的价格所作的任何更改都将影响使用该价目表的所有报价单和合同。</span><span class="sxs-lookup"><span data-stu-id="e0110-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>