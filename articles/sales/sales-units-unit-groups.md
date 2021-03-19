---
title: 计价单位和计价单位组
description: 本主题提供了有关如何在 Dynamics 365 Project Operations 中创建计价单位和计价单位组的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277327"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="796cf-103">计价单位和计价单位组</span><span class="sxs-lookup"><span data-stu-id="796cf-103">Units and unit groups</span></span>

<span data-ttu-id="796cf-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="796cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="796cf-105">计价单位是您销售产品或服务时使用的数量或测量单位。</span><span class="sxs-lookup"><span data-stu-id="796cf-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="796cf-106">例如，如果您销售园艺用品，您可以以包、盒和盘为单位销售种子。</span><span class="sxs-lookup"><span data-stu-id="796cf-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="796cf-107">计价单位组是这些不同单位的集合。</span><span class="sxs-lookup"><span data-stu-id="796cf-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="796cf-108">若要完成本主题中的步骤，请确保您已被分配了系统管理员或 Sales Professional 管理员角色或具有同等权限。</span><span class="sxs-lookup"><span data-stu-id="796cf-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="796cf-109">创建计价单位组</span><span class="sxs-lookup"><span data-stu-id="796cf-109">Create a unit group</span></span>

1. <span data-ttu-id="796cf-110">在站点地图中，选择 **计价单位**。</span><span class="sxs-lookup"><span data-stu-id="796cf-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="796cf-111">选择 **新建**，在 **创建计价单位组** 对话框中，输入计价单位名称。</span><span class="sxs-lookup"><span data-stu-id="796cf-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="796cf-112">在 **基本计价单位** 字段中，输入销售产品时所使用的最小的常用计价单位。</span><span class="sxs-lookup"><span data-stu-id="796cf-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="796cf-113">例如，您可以输入“件”或“盎司”。</span><span class="sxs-lookup"><span data-stu-id="796cf-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="796cf-114">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="796cf-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="796cf-115">将计价单位添加到计价单位组</span><span class="sxs-lookup"><span data-stu-id="796cf-115">Add units to a unit group</span></span>

1. <span data-ttu-id="796cf-116">打开一个计价单位组，在 **相关** 选项卡上选择 **计价单位**。</span><span class="sxs-lookup"><span data-stu-id="796cf-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="796cf-117">您将看到已经添加了基本计价单位。</span><span class="sxs-lookup"><span data-stu-id="796cf-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="796cf-118">选择 **添加新计价单位**，在 **快速创建: 计价单位** 页上的 **名称** 字段中，输入计价单位的名称。</span><span class="sxs-lookup"><span data-stu-id="796cf-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="796cf-119">在 **数量** 字段中，输入计价单位将所含的数量。</span><span class="sxs-lookup"><span data-stu-id="796cf-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="796cf-120">例如，如果一盒包含两件，则输入“2”。</span><span class="sxs-lookup"><span data-stu-id="796cf-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="796cf-121">在 **基础单位** 字段中，选择一个基础单位来建立计价单位的最小度量单位。</span><span class="sxs-lookup"><span data-stu-id="796cf-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="796cf-122">例如，您可以选择“件”。</span><span class="sxs-lookup"><span data-stu-id="796cf-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="796cf-123">选择 **保存**：</span><span class="sxs-lookup"><span data-stu-id="796cf-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]