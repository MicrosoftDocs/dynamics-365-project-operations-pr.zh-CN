---
title: 创建价目表
description: 如何在 Project Service 中创建价目表
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149442"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="34a76-103">创建价目表 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="34a76-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="34a76-104">价目表提供模板，供帐户管理员用于创建报价单和项目及确立项目的成本。</span><span class="sxs-lookup"><span data-stu-id="34a76-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="34a76-105">价目表提供角色和费用的明细项目列表以及您对每项收取的价格。</span><span class="sxs-lookup"><span data-stu-id="34a76-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="34a76-106">您可创建多个价目表，针对不同的销售地区或销售渠道维护单独的价格结构。</span><span class="sxs-lookup"><span data-stu-id="34a76-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="34a76-107">最好为要向客户收取的每种货币至少创建一个价目表。</span><span class="sxs-lookup"><span data-stu-id="34a76-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="34a76-108">要为将交付的工作创建财务预算，请确保每个项目都有所依托的成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="34a76-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="34a76-109">设置应用于组织中创建的所有项目的默认成本和销售价目表。</span><span class="sxs-lookup"><span data-stu-id="34a76-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="34a76-110">价目表依赖角色和费用类别，所以创建价目表之前，确保您已配置了要在创建价目表时使用的角色和费用类别。</span><span class="sxs-lookup"><span data-stu-id="34a76-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="34a76-111">转到 **Project Service > 价目表**。</span><span class="sxs-lookup"><span data-stu-id="34a76-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="34a76-112">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="34a76-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="34a76-113">在 **上下文** 中，选择此价目表针对 **成本**、**采购** 还是 **销售**。</span><span class="sxs-lookup"><span data-stu-id="34a76-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="34a76-114">在 **名称** 中，输入价目表的名称。</span><span class="sxs-lookup"><span data-stu-id="34a76-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="34a76-115">在 **货币** 中，选择记帐或成本所用货币。</span><span class="sxs-lookup"><span data-stu-id="34a76-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="34a76-116">在 **时间单位** 中，指定价格适用于的时间段（如天还是小时）</span><span class="sxs-lookup"><span data-stu-id="34a76-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="34a76-117">根据需要填写 **开始日期**、**结束日期** 和 **说明**。</span><span class="sxs-lookup"><span data-stu-id="34a76-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="34a76-118">单击 **保存** 创建记录，以便继续编辑。</span><span class="sxs-lookup"><span data-stu-id="34a76-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="34a76-119">要向价目表添加角色价格，单击 **角色价格** 下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="34a76-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="34a76-120">在 **角色价格** 窗格中，填写详细信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="34a76-121">根据需要继续添加角色价格。</span><span class="sxs-lookup"><span data-stu-id="34a76-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="34a76-122">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="34a76-123">要向价目表添加费用类别价格，单击 **类别价格** 下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="34a76-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="34a76-124">在 **交易类别价格** 窗格中，填写详细信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="34a76-125">根据需要继续添加类别价格。</span><span class="sxs-lookup"><span data-stu-id="34a76-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="34a76-126">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="34a76-127">要向价目表添加价目表项，单击 **价目表项** 下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="34a76-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="34a76-128">在 **价目表项** 窗格中，填写详细信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="34a76-129">根据需要继续添加价目表项。</span><span class="sxs-lookup"><span data-stu-id="34a76-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="34a76-130">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="34a76-131">要向价目表添加区域关系，单击 **区域关系** 下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="34a76-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="34a76-132">在 **新建连接** 窗口中，填写详细信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="34a76-133">根据需要继续添加区域关系。</span><span class="sxs-lookup"><span data-stu-id="34a76-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="34a76-134">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34a76-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="34a76-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34a76-135">See Also</span></span>  
 [<span data-ttu-id="34a76-136">配置 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="34a76-136">Configure Project Service Automation</span></span>](../psa/configure.md)
