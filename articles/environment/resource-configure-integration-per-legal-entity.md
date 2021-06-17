---
title: 配置每个法律实体的 Project Operations 集成
description: 此主题提供有关在 Project Operations 中按法人设置集成的信息。
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000065"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="77f99-103">配置每个法律实体的 Project Operations 集成</span><span class="sxs-lookup"><span data-stu-id="77f99-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="77f99-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="77f99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="77f99-105">本主题指导您完成为每个法律实体配置 Dynamics 365 Project Operations 所需执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="77f99-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="77f99-106">在 Dynamics 365 Finance 中启用功能键</span><span class="sxs-lookup"><span data-stu-id="77f99-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="77f99-107">完成以下步骤启用所需的功能。</span><span class="sxs-lookup"><span data-stu-id="77f99-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="77f99-108">在 Dynamics 365 Finance 中，转到 **功能管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="77f99-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="77f99-109">在 **功能列表** 中，找到并启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="77f99-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="77f99-110">**为项目启用多个合同子项**</span><span class="sxs-lookup"><span data-stu-id="77f99-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="77f99-111">**启用 Dynamics 365 Customer Engagement 上的 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="77f99-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="77f99-112">如果您看不到列出的 **功能键**，请验证您的 Finance 版本是否满足最低版本要求（应用所有高质量更新的应用程序版本 10.0.13 或更高版本）。</span><span class="sxs-lookup"><span data-stu-id="77f99-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="77f99-113">选择 **检查更新** 刷新功能列表。</span><span class="sxs-lookup"><span data-stu-id="77f99-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="77f99-114">定义法人的 Project Operations 部署方案</span><span class="sxs-lookup"><span data-stu-id="77f99-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="77f99-115">您可以在法人级别启用 Dynamics 365 Customer Engagement 上的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="77f99-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="77f99-116">您可以让一个法人使用 Dynamics 365 Customer Engagement 上的面向资源/非库存场景的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="77f99-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="77f99-117">在同一个环境中，您可以让另一个法人使用面向库存/生产订单场景的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="77f99-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="77f99-118">在 Dynamics 365 Finance 中，转到 **项目管理和会计** > **设置** > **全局项目管理和会计参数**。</span><span class="sxs-lookup"><span data-stu-id="77f99-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="77f99-119">在可用法人列表中，选择将启用多个合同子项和 Dynamics 365 Customer Engagement 上的 Project Operations 功能的实体。</span><span class="sxs-lookup"><span data-stu-id="77f99-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="77f99-120">不选择将使用面向库存/生产订单场景的 Project Operations 的法人。</span><span class="sxs-lookup"><span data-stu-id="77f99-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="77f99-121">只有当法人没有任何现有项目时，才可以选择该法人。</span><span class="sxs-lookup"><span data-stu-id="77f99-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="77f99-122">配置项目管理和会计参数</span><span class="sxs-lookup"><span data-stu-id="77f99-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="77f99-123">使用 Dynamics 365 Customer Engagement 上的 Project Operations 的每个法人都需要一组默认参数。</span><span class="sxs-lookup"><span data-stu-id="77f99-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="77f99-124">这些参数在 **项目管理和会计参数** 页上的 **Project Operations** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="77f99-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="77f99-125">参数包括：</span><span class="sxs-lookup"><span data-stu-id="77f99-125">The parameters are:</span></span>

  - <span data-ttu-id="77f99-126">**记帐类型默认值**：Project Operations 使用一组固定的记帐类型默认值，这些值必须映射到明细属性“财务”。</span><span class="sxs-lookup"><span data-stu-id="77f99-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="77f99-127">为每个记帐类型创建一条记录：**未指定**、**应计费**、**非应计费**、**免费** 和 **不可用**。</span><span class="sxs-lookup"><span data-stu-id="77f99-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="77f99-128">**项目类别默认值**：选择每个交易类型要使用的默认项目类别。</span><span class="sxs-lookup"><span data-stu-id="77f99-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="77f99-129">这些默认值将在 **Project Operations 集成日记帐** 以及未为项目实际值指定交易类别的估算中使用。</span><span class="sxs-lookup"><span data-stu-id="77f99-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="77f99-130">**预测**：选择要用于时间和支出估计的预测模型。</span><span class="sxs-lookup"><span data-stu-id="77f99-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]