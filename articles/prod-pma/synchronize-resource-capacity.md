---
title: 同步资源产能
description: 此主题介绍如何在日历与项目之间同步资源的产能。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997500"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="bc3ba-103">同步资源产能</span><span class="sxs-lookup"><span data-stu-id="bc3ba-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc3ba-104">资源同步流程帮助确保日历和基础日历信息深入到项目资源计划。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="bc3ba-105">如果更改日历，流程对项目资源计划进行所需的更新。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="bc3ba-106">因为日历的资源信息提前同步，这些流程还有助于改进性能。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="bc3ba-107">因此，资源计划信息的更新更快。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="bc3ba-108">我们建议您批量计划流程，而不是一次计划一个。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="bc3ba-109">否则，某些员工可能忘记上次同步信息的起迄日期。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="bc3ba-110">如果不使用起迄日期，可能在日期同步时发生间隔。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![日历同步](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="bc3ba-112">同步资源产能汇总</span><span class="sxs-lookup"><span data-stu-id="bc3ba-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="bc3ba-113">同步流程被设计为同步所有资源日历信息。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="bc3ba-114">此信息包括有关对项目的资源日历产能表进行的任何更改的基本日历信息。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="bc3ba-115">如果在项目中添加新的资源，同步可以帮助确保更新的日历信息可用。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="bc3ba-116">此同步随时都可以进行。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="bc3ba-117">我们建议您使用批次执行。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-117">We recommend that you use a batch.</span></span> <span data-ttu-id="bc3ba-118">选项在同步产能预留中可用。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="bc3ba-119">选择 **项目管理与核算** &gt; **定期** &gt; **产能同步** &gt; **同步资源产能汇总**。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="bc3ba-120">设置下表中的选项。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="bc3ba-121">选项</span><span class="sxs-lookup"><span data-stu-id="bc3ba-121">Option</span></span>      | <span data-ttu-id="bc3ba-122">描述</span><span class="sxs-lookup"><span data-stu-id="bc3ba-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="bc3ba-123">期间代码</span><span class="sxs-lookup"><span data-stu-id="bc3ba-123">Period code</span></span> | <span data-ttu-id="bc3ba-124">选择性地选择总帐日期间隔代码，以设置资源产能汇总的同步流程的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="bc3ba-125">开始日期</span><span class="sxs-lookup"><span data-stu-id="bc3ba-125">Start date</span></span>  | <span data-ttu-id="bc3ba-126">输入资源产能汇总的同步流程的开始日期。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="bc3ba-127">结束日期</span><span class="sxs-lookup"><span data-stu-id="bc3ba-127">End date</span></span>    | <span data-ttu-id="bc3ba-128">输入资源产能汇总的同步流程的结束日期。</span><span class="sxs-lookup"><span data-stu-id="bc3ba-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="bc3ba-129">[![同步流程](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="bc3ba-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]