---
title: 2021 年 2 月新增功能 - Project Operations 精简部署
description: 此主题提供有关 2021 年 2 月版本的 Project Operations 精简部署中推出的质量更新的信息。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: df6490d3d9c28b095efd5ef856064de4b1517055
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272152"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a><span data-ttu-id="5bf1a-103">2021 年 2 月新增功能 - Project Operations 精简部署</span><span class="sxs-lookup"><span data-stu-id="5bf1a-103">What's new February 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="5bf1a-104">此主题适用于以下 Dynamics 365 Project Operations 组件和版本：</span><span class="sxs-lookup"><span data-stu-id="5bf1a-104">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="5bf1a-105">Dataverse 环境中的 Project Operations 版本 4.7.0.95</span><span class="sxs-lookup"><span data-stu-id="5bf1a-105">Project Operations on Dataverse environment version 4.7.0.95</span></span>

## <a name="quality-updates"></a><span data-ttu-id="5bf1a-106">质量更新</span><span class="sxs-lookup"><span data-stu-id="5bf1a-106">Quality updates</span></span>

| <span data-ttu-id="5bf1a-107">**功能区域**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-107">**Feature Area**</span></span> | <span data-ttu-id="5bf1a-108">**参考编号**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-108">**Reference number**</span></span> | <span data-ttu-id="5bf1a-109">**质量更新**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-109">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5bf1a-110">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-110">**Billing and Pricing**</span></span> | <span data-ttu-id="5bf1a-111">2053736</span><span class="sxs-lookup"><span data-stu-id="5bf1a-111">2053736</span></span> | <span data-ttu-id="5bf1a-112">现在可以通过转到 **发票** > **相关信息** 来访问发票明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-112">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="5bf1a-113">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-113">**Billing and Pricing**</span></span> | <span data-ttu-id="5bf1a-114">2122613</span><span class="sxs-lookup"><span data-stu-id="5bf1a-114">2122613</span></span> | <span data-ttu-id="5bf1a-115">**激活** 和 **停用** 操作已从 **价目表** 关联实体中删除。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-115">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="5bf1a-116">**记帐和定价**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-116">**Billing and Pricing**</span></span> | <span data-ttu-id="5bf1a-117">2128606</span><span class="sxs-lookup"><span data-stu-id="5bf1a-117">2128606</span></span> | <span data-ttu-id="5bf1a-118">解决了 **GetEstimatesForProject** 插件中 **ullReferenceException** 存在的问题。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-118">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="5bf1a-119">**部署和配置**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-119">**Deployment and configuration**</span></span> | <span data-ttu-id="5bf1a-120">2140569</span><span class="sxs-lookup"><span data-stu-id="5bf1a-120">2140569</span></span> | <span data-ttu-id="5bf1a-121">不能在 Dataverse Teams 环境中安装项目解决方案。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-121">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="5bf1a-122">**部署和配置**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-122">**Deployment and configuration**</span></span> | <span data-ttu-id="5bf1a-123">2086991</span><span class="sxs-lookup"><span data-stu-id="5bf1a-123">2086991</span></span> | <span data-ttu-id="5bf1a-124">限制自定义 Web 资源的本地化。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-124">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="5bf1a-125">**商机管理**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-125">**Opportunity Management**</span></span> | <span data-ttu-id="5bf1a-126">2136794</span><span class="sxs-lookup"><span data-stu-id="5bf1a-126">2136794</span></span> | <span data-ttu-id="5bf1a-127">当 **确认发票** 或 **发票标记为已支付** 流程失败时，显示正确的错误消息，</span><span class="sxs-lookup"><span data-stu-id="5bf1a-127">Display correct error message when **Confirm invoice** or **Mark invoice as paid** process fails,</span></span> |
| <span data-ttu-id="5bf1a-128">**商机管理**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-128">**Opportunity Management**</span></span> | <span data-ttu-id="5bf1a-129">2146376</span><span class="sxs-lookup"><span data-stu-id="5bf1a-129">2146376</span></span> | <span data-ttu-id="5bf1a-130">非应计费实际值中的更正税金额从发票确认创建。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-130">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="5bf1a-131">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-131">**Project Planning and Tracking**</span></span> | <span data-ttu-id="5bf1a-132">2099879</span><span class="sxs-lookup"><span data-stu-id="5bf1a-132">2099879</span></span> | <span data-ttu-id="5bf1a-133">Dataverse 环境部署必须创建具有静态 ID 的默认交易类别，而不能在每个环境中随机生成。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-133">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="5bf1a-134">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-134">**Project Planning and Tracking**</span></span> | <span data-ttu-id="5bf1a-135">2128577</span><span class="sxs-lookup"><span data-stu-id="5bf1a-135">2128577</span></span> | <span data-ttu-id="5bf1a-136">修复了更新资源分配上的交易类别的 Project Service 用户特权。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-136">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="5bf1a-137">**项目规划和跟踪**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-137">**Project Planning and Tracking**</span></span> | <span data-ttu-id="5bf1a-138">2164035</span><span class="sxs-lookup"><span data-stu-id="5bf1a-138">2164035</span></span> | <span data-ttu-id="5bf1a-139">修复了 **复制项目** 功能存在的问题。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-139">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="5bf1a-140">**时间条目**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-140">**Time entry**</span></span> | <span data-ttu-id="5bf1a-141">2129161</span><span class="sxs-lookup"><span data-stu-id="5bf1a-141">2129161</span></span> | <span data-ttu-id="5bf1a-142">应用了更严格的限制，以确保用户不能更改和更新已提交或批准的时间条目。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-142">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="5bf1a-143">**时间条目**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-143">**Time entry**</span></span> | <span data-ttu-id="5bf1a-144">2103572</span><span class="sxs-lookup"><span data-stu-id="5bf1a-144">2103572</span></span> | <span data-ttu-id="5bf1a-145">非项目时间条目的时间审批不能查找项目审批者角色。</span><span class="sxs-lookup"><span data-stu-id="5bf1a-145">Time approval for non-project time entries must not be looking for project approver role.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]