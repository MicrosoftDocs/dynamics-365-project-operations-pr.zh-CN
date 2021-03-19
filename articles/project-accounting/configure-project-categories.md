---
title: 配置项目类别
description: 此主题提供有关设置项目类别的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287497"
---
# <a name="configure-project-categories"></a><span data-ttu-id="7c026-103">配置项目类别</span><span class="sxs-lookup"><span data-stu-id="7c026-103">Configure project categories</span></span>

<span data-ttu-id="7c026-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7c026-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7c026-105">Project Operations 提供强大的功能，可以对项目的收入和支出进行分类。</span><span class="sxs-lookup"><span data-stu-id="7c026-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="7c026-106">类别提供报告和分析项目交易以及推进向总帐过帐的能力。</span><span class="sxs-lookup"><span data-stu-id="7c026-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="7c026-107">下图说明了交易类别、共享类别和项目类别之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="7c026-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="7c026-108">交易类别是项目交易的基本分组。</span><span class="sxs-lookup"><span data-stu-id="7c026-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="7c026-109">在该分组中，存在一组可以在应用程序和模块之间共享的共享类别。</span><span class="sxs-lookup"><span data-stu-id="7c026-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="7c026-110">更深入地讲，项目类别是粒度级别最细的类别。</span><span class="sxs-lookup"><span data-stu-id="7c026-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="7c026-111">项目类别特定于法人、模块和应用程序。</span><span class="sxs-lookup"><span data-stu-id="7c026-111">Project categories are specific to legal entity, module, and application.</span></span>

![交易类别、共享类别和项目类别之间的相关性](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="7c026-113">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="7c026-113">Transaction categories</span></span>

<span data-ttu-id="7c026-114">交易类别代表项目交易的基本分组，不特定于公司或交易类型。</span><span class="sxs-lookup"><span data-stu-id="7c026-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="7c026-115">例如，Contoso Robotics 使用“设计”、“旅行”、“安装”和“服务交易”类别对项目交易进行分组。</span><span class="sxs-lookup"><span data-stu-id="7c026-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="7c026-116">交易类别在 Project Operations 模块中定义。</span><span class="sxs-lookup"><span data-stu-id="7c026-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="7c026-117">转到 **设置**\>**交易类别** 打开窗体。</span><span class="sxs-lookup"><span data-stu-id="7c026-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="7c026-118">通过选择 **新建** 或选择 **从 Excel 导入**，创建一个新交易类别。</span><span class="sxs-lookup"><span data-stu-id="7c026-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="7c026-119">共享类别</span><span class="sxs-lookup"><span data-stu-id="7c026-119">Shared categories</span></span>

<span data-ttu-id="7c026-120">Dynamics 365 使用“共享类别”概念对 Dynamics 365 Finance、Dynamics 365 Supply Chain 和 Dynamics 365 Project Operations 等不同应用程序中的费用进行分类。</span><span class="sxs-lookup"><span data-stu-id="7c026-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="7c026-121">对于创建的每个交易类别，Project Operations 会自动创建四个相关的共享类别：工时、支出、费用和项目。</span><span class="sxs-lookup"><span data-stu-id="7c026-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="7c026-122">您可以转到 **项目管理和会计** \> **设置** \> **类别** \> **共享类别** 查看和调整共享类别。</span><span class="sxs-lookup"><span data-stu-id="7c026-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="7c026-123">项目类别</span><span class="sxs-lookup"><span data-stu-id="7c026-123">Project categories</span></span>

<span data-ttu-id="7c026-124">项目类别代表类别配置的最细粒度级别，必须由项目会计单独为每个公司进行配置。</span><span class="sxs-lookup"><span data-stu-id="7c026-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="7c026-125">转到 **项目管理和会计** \> **设置** \> **类别** \> **项目类别**。</span><span class="sxs-lookup"><span data-stu-id="7c026-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="7c026-126">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7c026-126">Select **New**.</span></span>
3. <span data-ttu-id="7c026-127">选择在上一节中创建的共享类别的 **类别 ID**。</span><span class="sxs-lookup"><span data-stu-id="7c026-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="7c026-128">Project Operations 仅允许使用与交易类别关联的那些共享类别。</span><span class="sxs-lookup"><span data-stu-id="7c026-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="7c026-129">选择类别组。</span><span class="sxs-lookup"><span data-stu-id="7c026-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="7c026-130">类别组</span><span class="sxs-lookup"><span data-stu-id="7c026-130">Category groups</span></span>

<span data-ttu-id="7c026-131">类别组用于在相关项目类别之间共享属性，主要是过帐模板。</span><span class="sxs-lookup"><span data-stu-id="7c026-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="7c026-132">每个交易类型必须至少有一个类别组，并且为每个项目类别分配一个组。</span><span class="sxs-lookup"><span data-stu-id="7c026-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="7c026-133">Project Operations 中的过帐规范由项目成本和收入模板规则、项目类别以及类别组定义。</span><span class="sxs-lookup"><span data-stu-id="7c026-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="7c026-134">您可以转到 **项目管理和会计** \> **设置** \> **类别** \> **类别组** 设置类别组。</span><span class="sxs-lookup"><span data-stu-id="7c026-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]