---
title: 更新完工估算
description: 此主题提供有关更新项目的工作量预估的信息。
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286417"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="4d53c-103">更新完工估算</span><span class="sxs-lookup"><span data-stu-id="4d53c-103">Update estimate at completion</span></span>

<span data-ttu-id="4d53c-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="4d53c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d53c-105">项目经理经常修订任务的原始估算。</span><span class="sxs-lookup"><span data-stu-id="4d53c-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="4d53c-106">项目重新预估是项目经理基于项目当前状态对估算的感知。</span><span class="sxs-lookup"><span data-stu-id="4d53c-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="4d53c-107">但是，建议项目经理不要更改基准数字，因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。</span><span class="sxs-lookup"><span data-stu-id="4d53c-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="4d53c-108">项目经理可通过两种方法重新预估任务的工作量：</span><span class="sxs-lookup"><span data-stu-id="4d53c-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="4d53c-109">将默认的要完成的估算 (ETC) 替换为任务的实际剩余工作量新估算。</span><span class="sxs-lookup"><span data-stu-id="4d53c-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="4d53c-110">将默认进度百分比替换为项目真实进度新估算。</span><span class="sxs-lookup"><span data-stu-id="4d53c-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="4d53c-111">这些方法都会导致重新计算任务的 ETC、完工估算 (EAC)、进度百分比，以及任务的预估工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="4d53c-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="4d53c-112">将会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="4d53c-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]