---
title: 根据物料需求接收采购订单上的物料
description: 本主题介绍如何根据物料需求接收某一采购订单的物料。
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749640"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="5230f-103">根据物料需求接收采购订单上的物料</span><span class="sxs-lookup"><span data-stu-id="5230f-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5230f-104">本主题介绍如何根据物料需求接收某一采购订单的物料。</span><span class="sxs-lookup"><span data-stu-id="5230f-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="5230f-105">通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。</span><span class="sxs-lookup"><span data-stu-id="5230f-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="5230f-106">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="5230f-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5230f-107">在导航窗格中，转到**模块 > 项目管理与核算 > 项目 > 所有项目**。</span><span class="sxs-lookup"><span data-stu-id="5230f-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="5230f-108">在列表中，选择所需行中的链接。</span><span class="sxs-lookup"><span data-stu-id="5230f-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="5230f-109">在操作窗格上，选择**计划**。</span><span class="sxs-lookup"><span data-stu-id="5230f-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="5230f-110">选择**物料需求**。</span><span class="sxs-lookup"><span data-stu-id="5230f-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="5230f-111">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5230f-111">Select **New**.</span></span>
6. <span data-ttu-id="5230f-112">在新行的**物料编号**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5230f-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="5230f-113">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="5230f-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="5230f-114">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="5230f-114">Select **Save**.</span></span>
9. <span data-ttu-id="5230f-115">在操作窗格上，选择**管理**。</span><span class="sxs-lookup"><span data-stu-id="5230f-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="5230f-116">选择**功能**。</span><span class="sxs-lookup"><span data-stu-id="5230f-116">Select **Functions**.</span></span>
11. <span data-ttu-id="5230f-117">选择**创建采购订单**。</span><span class="sxs-lookup"><span data-stu-id="5230f-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="5230f-118">选中**全部包括**复选框。</span><span class="sxs-lookup"><span data-stu-id="5230f-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="5230f-119">在**供应商帐户**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5230f-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="5230f-120">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5230f-120">Select **OK**.</span></span>
15. <span data-ttu-id="5230f-121">在导航窗格中，转到**模块 > 应付帐款 > 采购订单 > 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="5230f-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="5230f-122">在列表中，选择所需行中的链接。</span><span class="sxs-lookup"><span data-stu-id="5230f-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="5230f-123">在操作窗格上，选择**采购**。</span><span class="sxs-lookup"><span data-stu-id="5230f-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="5230f-124">选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="5230f-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="5230f-125">在操作窗格上，选择**接收**。</span><span class="sxs-lookup"><span data-stu-id="5230f-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="5230f-126">选择**物料收货**。</span><span class="sxs-lookup"><span data-stu-id="5230f-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="5230f-127">在**产品收据**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5230f-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="5230f-128">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5230f-128">Select **OK**.</span></span>
