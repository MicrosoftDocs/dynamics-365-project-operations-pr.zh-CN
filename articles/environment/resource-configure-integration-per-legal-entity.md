---
title: 配置每个法律实体的 Project Operations 集成
description: 此主题提供有关在 Project Operations 中按法人设置集成的信息。
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096741"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="0d83a-103">配置每个法律实体的 Project Operations 集成</span><span class="sxs-lookup"><span data-stu-id="0d83a-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="0d83a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0d83a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d83a-105">此主题将指导您完成按法人配置 Dynamics 365 Project Operations 所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="0d83a-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="0d83a-106">在 Dynamics 365 Finance 中启用功能键</span><span class="sxs-lookup"><span data-stu-id="0d83a-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="0d83a-107">完成以下步骤启用所需的功能。</span><span class="sxs-lookup"><span data-stu-id="0d83a-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="0d83a-108">在 Dynamics 365 Finance 中，转到 **功能管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="0d83a-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="0d83a-109">在 **功能列表** 中，找到并启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="0d83a-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="0d83a-110">**为项目启用多个合同子项**</span><span class="sxs-lookup"><span data-stu-id="0d83a-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="0d83a-111">**启用 Dynamics 365 Customer Engagement 上的 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="0d83a-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="0d83a-112">如果您看不到列出的 **功能键** ，请验证您的 Finance 版本是否满足最低版本要求（应用所有高质量更新的应用程序版本 10.0.13 或更高版本）。</span><span class="sxs-lookup"><span data-stu-id="0d83a-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="0d83a-113">选择 **检查更新** 刷新功能列表。</span><span class="sxs-lookup"><span data-stu-id="0d83a-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="0d83a-114">定义法人的 Project Operations 部署方案</span><span class="sxs-lookup"><span data-stu-id="0d83a-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="0d83a-115">您可以在法人级别启用 Dynamics 365 Customer Engagement 上的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="0d83a-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="0d83a-116">您可以让一个法人使用 Dynamics 365 Customer Engagement 上的面向资源/非库存场景的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="0d83a-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="0d83a-117">在同一个环境中，您可以让另一个法人使用面向库存/生产订单场景的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="0d83a-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="0d83a-118">在 Dynamics 365 Finance 中，转到 **项目管理和会计** > **设置** > **全局项目管理和会计参数** 。</span><span class="sxs-lookup"><span data-stu-id="0d83a-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="0d83a-119">在可用法人列表中，选择将启用多个合同子项和 Dynamics 365 Customer Engagement 上的 Project Operations 功能的实体。</span><span class="sxs-lookup"><span data-stu-id="0d83a-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="0d83a-120">不选择将使用面向库存/生产订单场景的 Project Operations 的法人。</span><span class="sxs-lookup"><span data-stu-id="0d83a-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="0d83a-121">只有当法人没有任何现有项目时，才可以选择该法人。</span><span class="sxs-lookup"><span data-stu-id="0d83a-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="0d83a-122">配置项目管理和会计参数</span><span class="sxs-lookup"><span data-stu-id="0d83a-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="0d83a-123">使用 Dynamics 365 Customer Engagement 上的 Project Operations 的每个法人都需要一组默认参数。</span><span class="sxs-lookup"><span data-stu-id="0d83a-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="0d83a-124">这些参数在 **项目管理和会计参数** 页上的 **Project Operations** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="0d83a-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="0d83a-125">参数包括：</span><span class="sxs-lookup"><span data-stu-id="0d83a-125">The parameters are:</span></span>

  - <span data-ttu-id="0d83a-126">**记帐类型默认值** ：Project Operations 使用一组固定的记帐类型默认值，这些值必须映射到明细属性“财务”。</span><span class="sxs-lookup"><span data-stu-id="0d83a-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="0d83a-127">为每个记帐类型创建一条记录： **未指定** 、 **应计费** 、 **非应计费** 、 **免费** 和 **不可用** 。</span><span class="sxs-lookup"><span data-stu-id="0d83a-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="0d83a-128">**项目类别默认值** ：选择每个交易类型要使用的默认项目类别。</span><span class="sxs-lookup"><span data-stu-id="0d83a-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="0d83a-129">这些默认值将在 **Project Operations 集成日记帐** 以及未为项目实际值指定交易类别的估算中使用。</span><span class="sxs-lookup"><span data-stu-id="0d83a-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="0d83a-130">**预测** ：选择要用于时间和支出估计的预测模型。</span><span class="sxs-lookup"><span data-stu-id="0d83a-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
