---
title: 项目发票方案性能
description: 该主题提供了关于项目发票方案性能改进的信息。
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999480"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="4f934-103">项目发票方案性能</span><span class="sxs-lookup"><span data-stu-id="4f934-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f934-104">创建新的发票方案时，由于项目数和子项目数增加，可能会遇到性能问题。</span><span class="sxs-lookup"><span data-stu-id="4f934-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="4f934-105">为了提高性能，提供了一项功能，可缩短为已过帐的项目交易创建新发票方案所需的时间。</span><span class="sxs-lookup"><span data-stu-id="4f934-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4f934-106">启用项目发票方案性能增强</span><span class="sxs-lookup"><span data-stu-id="4f934-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4f934-107">若要启用项目发票方案性能增强功能，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4f934-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="4f934-108">转到 **功能管理** > **所有**。</span><span class="sxs-lookup"><span data-stu-id="4f934-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4f934-109">在功能列表中，找到 **项目发票方案性能增强**。</span><span class="sxs-lookup"><span data-stu-id="4f934-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4f934-110">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="4f934-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="4f934-111">刷新浏览器，然后创建一个新发票方案。</span><span class="sxs-lookup"><span data-stu-id="4f934-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4f934-112">关闭项目发票方案性能增强</span><span class="sxs-lookup"><span data-stu-id="4f934-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4f934-113">完成以下步骤以关闭项目发票方案性能增强。</span><span class="sxs-lookup"><span data-stu-id="4f934-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="4f934-114">转到 **功能管理** > **所有**。</span><span class="sxs-lookup"><span data-stu-id="4f934-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4f934-115">在功能列表中，找到 **项目发票方案性能增强**。</span><span class="sxs-lookup"><span data-stu-id="4f934-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4f934-116">选择 **禁用**。</span><span class="sxs-lookup"><span data-stu-id="4f934-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="4f934-117">刷新浏览器。</span><span class="sxs-lookup"><span data-stu-id="4f934-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4f934-118">启用记帐规则或运行批处理过程时，无法应用发票方案性能。</span><span class="sxs-lookup"><span data-stu-id="4f934-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
