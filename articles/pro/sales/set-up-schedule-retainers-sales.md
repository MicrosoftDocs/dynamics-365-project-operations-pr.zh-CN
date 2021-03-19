---
title: 设置保留款计划
description: 此主题提供有关如何在 Project Operations 中设置保留款计划的信息。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272242"
---
# <a name="set-up-a-retainer-schedule"></a><span data-ttu-id="abc16-103">设置保留款计划</span><span class="sxs-lookup"><span data-stu-id="abc16-103">Set up a retainer schedule</span></span>

<span data-ttu-id="abc16-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="abc16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abc16-105">保留款计划在 Dynamics 365 Project Operations 中的 **项目合同** 页设置。</span><span class="sxs-lookup"><span data-stu-id="abc16-105">Retainer schedules are set up on the **Project Contract** page in Dynamics 365 Project Operations.</span></span>

1. <span data-ttu-id="abc16-106">在 **项目合同** 页上的 **预付款和保留款** 选项卡上，选择 **设置保留款计划**。</span><span class="sxs-lookup"><span data-stu-id="abc16-106">On the **Project Contract** page, on the **Advances and Retainers** tab, select **Set up retainer schedule**.</span></span>
2. <span data-ttu-id="abc16-107">在打开的对话页面上，将显示下表中列出的字段。</span><span class="sxs-lookup"><span data-stu-id="abc16-107">On the dialog page that opens, the fields listed in the following table are shown.</span></span> <span data-ttu-id="abc16-108">此表显示了输入值会怎样影响将要创建的保留款计划。</span><span class="sxs-lookup"><span data-stu-id="abc16-108">The table gives an idea on how the entered values impact or influence the retainer schedule that will be created.</span></span>

| <span data-ttu-id="abc16-109">字段</span><span class="sxs-lookup"><span data-stu-id="abc16-109">Field</span></span> | <span data-ttu-id="abc16-110">描述</span><span class="sxs-lookup"><span data-stu-id="abc16-110">Description</span></span> | <span data-ttu-id="abc16-111">下游影响</span><span class="sxs-lookup"><span data-stu-id="abc16-111">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="abc16-112">项目合同客户</span><span class="sxs-lookup"><span data-stu-id="abc16-112">Project Contract Customer</span></span> | <span data-ttu-id="abc16-113">将就此保留款或预付款为其开票的合同中的客户。</span><span class="sxs-lookup"><span data-stu-id="abc16-113">The customer on the contract who will be invoiced for this retainer or advance.</span></span> | <span data-ttu-id="abc16-114">如果您在合同中有多个客户，您需要为每个客户的特定保留款或预付款金额开票，请为每个客户手动创建一个发票。</span><span class="sxs-lookup"><span data-stu-id="abc16-114">If you have multiple customers on the contract, and if you need to invoice each of them for a specific retainer or advance amount, manually create one invoice for each customer.</span></span> |
| <span data-ttu-id="abc16-115">保留款计划开始</span><span class="sxs-lookup"><span data-stu-id="abc16-115">Retainer Schedule Start</span></span> | <span data-ttu-id="abc16-116">输入保留款计划的开始日期。</span><span class="sxs-lookup"><span data-stu-id="abc16-116">Enter the start date of the retainer schedule.</span></span> | <span data-ttu-id="abc16-117">此日期不能是创建第一个保留款或预付款的日期。</span><span class="sxs-lookup"><span data-stu-id="abc16-117">This date may not be the date on which the first retainer or advance is created.</span></span> <span data-ttu-id="abc16-118">创建第一个保留款或预付款的日期，此日期还受发票频率的影响。</span><span class="sxs-lookup"><span data-stu-id="abc16-118">The date on which the first retainer or advance is created, is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="abc16-119">保留款计划结束</span><span class="sxs-lookup"><span data-stu-id="abc16-119">Retainer Schedule End</span></span> | <span data-ttu-id="abc16-120">输入保留款计划的结束日期。</span><span class="sxs-lookup"><span data-stu-id="abc16-120">Enter the end date of the retainer schedule.</span></span> | <span data-ttu-id="abc16-121">此日期不能是创建最后一个保留款或预付款的日期。</span><span class="sxs-lookup"><span data-stu-id="abc16-121">This date may not be the date on which the last retainer or advance is created.</span></span> <span data-ttu-id="abc16-122">创建最后一个保留款或预付款的日期还受发票频率的影响。</span><span class="sxs-lookup"><span data-stu-id="abc16-122">The date on which the last retainer or advance is created is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="abc16-123">要创建的保留款数量</span><span class="sxs-lookup"><span data-stu-id="abc16-123">Number of Retainers to Create</span></span> | <span data-ttu-id="abc16-124">当您输入要创建的保留款数量时，系统将使用开始日期和频率在此字段中创建数量。</span><span class="sxs-lookup"><span data-stu-id="abc16-124">When you enter the number of retainers to create, the system uses the start date and frequency to create the number in this field.</span></span> | <span data-ttu-id="abc16-125">当手动更新此字段时，系统会忽略 **保留款计划结束** 字段中的值，而是创建特定的保留款或预付款数量。</span><span class="sxs-lookup"><span data-stu-id="abc16-125">When this field is manually updated, the system ignores the value in the **Retainer Schedule End** field and instead creates the specific number of retainers or advances.</span></span> |
| <span data-ttu-id="abc16-126">账单频率</span><span class="sxs-lookup"><span data-stu-id="abc16-126">Invoice Frequency</span></span> | <span data-ttu-id="abc16-127">应用程序创建保留款和预付款的频率。</span><span class="sxs-lookup"><span data-stu-id="abc16-127">How often the application will create retainers and advances.</span></span> | <span data-ttu-id="abc16-128">此值直接影响保留款和预付款的数量和创建日期。</span><span class="sxs-lookup"><span data-stu-id="abc16-128">This value directly influences the number of retainers and advances and the created dates.</span></span> |
| <span data-ttu-id="abc16-129">总金额</span><span class="sxs-lookup"><span data-stu-id="abc16-129">Total Amount</span></span> | <span data-ttu-id="abc16-130">总金额是拆分为将要创建的各个保留款或预付款的金额。</span><span class="sxs-lookup"><span data-stu-id="abc16-130">The total amount is the amount that is split into the individual retainer or advance payments that will be created.</span></span> | <span data-ttu-id="abc16-131">此字段没有下游影响。</span><span class="sxs-lookup"><span data-stu-id="abc16-131">There's no downstream impact for this field.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]