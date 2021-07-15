---
title: 项目发票方案性能
description: 该主题提供了关于项目发票方案性能改进的信息。
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269779"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="8ce12-103">项目发票方案性能</span><span class="sxs-lookup"><span data-stu-id="8ce12-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ce12-104">创建新的发票方案时，由于项目数和子项目数增加，可能会遇到性能问题。</span><span class="sxs-lookup"><span data-stu-id="8ce12-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="8ce12-105">为了提高性能，提供了一项功能，可缩短为已过帐的项目交易创建新发票方案所需的时间。</span><span class="sxs-lookup"><span data-stu-id="8ce12-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="8ce12-106">启用项目发票方案性能增强</span><span class="sxs-lookup"><span data-stu-id="8ce12-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="8ce12-107">若要启用项目发票方案性能增强功能，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8ce12-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="8ce12-108">转到 **功能管理** > **所有**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="8ce12-109">在功能列表中，找到 **项目发票方案性能增强**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="8ce12-110">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="8ce12-111">刷新浏览器，然后创建一个新发票方案。</span><span class="sxs-lookup"><span data-stu-id="8ce12-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="8ce12-112">关闭项目发票方案性能增强</span><span class="sxs-lookup"><span data-stu-id="8ce12-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="8ce12-113">完成以下步骤以关闭项目发票方案性能增强。</span><span class="sxs-lookup"><span data-stu-id="8ce12-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="8ce12-114">转到 **功能管理** > **所有**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="8ce12-115">在功能列表中，找到 **项目发票方案性能增强**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="8ce12-116">选择 **禁用**。</span><span class="sxs-lookup"><span data-stu-id="8ce12-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="8ce12-117">刷新浏览器。</span><span class="sxs-lookup"><span data-stu-id="8ce12-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="8ce12-118">启用记帐规则后，无法应用发票方案性能。</span><span class="sxs-lookup"><span data-stu-id="8ce12-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="8ce12-119">在批量创建发票方案的流程中，无论您输入什么内容，子任务数都将基于具有可开票交易的合同数将任务拆分为最大数量。</span><span class="sxs-lookup"><span data-stu-id="8ce12-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="8ce12-120">例如，如果您在批量创建发票方案时输入的子任务数为 **3**，并且只有两个具有可开票交易的合同，则仅创建两个子任务。</span><span class="sxs-lookup"><span data-stu-id="8ce12-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
