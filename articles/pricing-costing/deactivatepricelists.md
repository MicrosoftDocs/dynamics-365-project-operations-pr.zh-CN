---
title: 停用价目表
description: 此主题说明如何停用或删除未使用或旧的价目表。
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001325"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="d826e-103">停用价目表</span><span class="sxs-lookup"><span data-stu-id="d826e-103">Deactivate price lists</span></span> 

<span data-ttu-id="d826e-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="d826e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d826e-105">若要从 Dynamics 365 Project Operations 中删除旧价目表或未使用的价目表，您必须完成两个步骤。</span><span class="sxs-lookup"><span data-stu-id="d826e-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="d826e-106">从特定页面移除或删除价目表。</span><span class="sxs-lookup"><span data-stu-id="d826e-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="d826e-107">停用或删除 **价目表** 页上“可用价目表”中的价目表。</span><span class="sxs-lookup"><span data-stu-id="d826e-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="d826e-108">您必须完成这两个步骤，才能完整移除价目表。</span><span class="sxs-lookup"><span data-stu-id="d826e-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="d826e-109">仅执行步骤 2（直接从“可用价目表”视图中删除或停用价目表）是不够的。</span><span class="sxs-lookup"><span data-stu-id="d826e-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="d826e-110">还必须从步骤 1 中提及的所有位置删除此价目表的关联。</span><span class="sxs-lookup"><span data-stu-id="d826e-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="d826e-111">从特定页面删除价目表</span><span class="sxs-lookup"><span data-stu-id="d826e-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="d826e-112">若要从 Project Operations 中删除价目表，请转到以下页面：</span><span class="sxs-lookup"><span data-stu-id="d826e-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="d826e-113">**项目参数** 页面 > **价目表** 选项卡</span><span class="sxs-lookup"><span data-stu-id="d826e-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="d826e-114">**部门** 页面 > **价目表** 网格</span><span class="sxs-lookup"><span data-stu-id="d826e-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="d826e-115">**客户** 页面 > **项目价目表** 网格</span><span class="sxs-lookup"><span data-stu-id="d826e-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="d826e-116">**项目报价单** 页面 > **项目价目表** 网格：这适用于所有可用的项目报价单。</span><span class="sxs-lookup"><span data-stu-id="d826e-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="d826e-117">**项目合同** 页面 > **项目价目表** 网格：这适用于所有可用的项目合同。</span><span class="sxs-lookup"><span data-stu-id="d826e-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="d826e-118">对于每个页面，您需要选择要删除的价目表，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="d826e-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="d826e-119">删除或停用“价目表”页中的价目表</span><span class="sxs-lookup"><span data-stu-id="d826e-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="d826e-120">若要从可用价目表中删除价目表，请转到 **销售** > **客户** > **价目表**。</span><span class="sxs-lookup"><span data-stu-id="d826e-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="d826e-121">选择要删除的价目表，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="d826e-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="d826e-122">只要在任何现有交易中引用了价目表，则将无法删除该价目表。</span><span class="sxs-lookup"><span data-stu-id="d826e-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="d826e-123">如果出现这种情况，您可以停用价目表，以便价目表不会显示在任何视图中。</span><span class="sxs-lookup"><span data-stu-id="d826e-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="d826e-124">若要停用价目表，请再次选择价目表，然后选择 **停用**。</span><span class="sxs-lookup"><span data-stu-id="d826e-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
