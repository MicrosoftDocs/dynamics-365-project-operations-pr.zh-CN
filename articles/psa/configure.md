---
title: 配置 Project Service Automation
description: 配置 Project Service 的步骤
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129172"
---
# <a name="configure-project-service"></a><span data-ttu-id="deeac-103">配置 Project Service</span><span class="sxs-lookup"><span data-stu-id="deeac-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="deeac-104">在可以使用 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]自动化功能管理您的客户、项目和资源之前，您需要完成一些配置步骤以确保[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]解决方案满足您组织的需求。</span><span class="sxs-lookup"><span data-stu-id="deeac-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="deeac-105">这些步骤包括：</span><span class="sxs-lookup"><span data-stu-id="deeac-105">These steps include:</span></span>  
  
-   <span data-ttu-id="deeac-106">[设置时间单位](../psa/set-up-time-units.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="deeac-107">在将用作项目计划和计费的基础的产品目录中配置时间单位。</span><span class="sxs-lookup"><span data-stu-id="deeac-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="deeac-108">[设置货币和汇率](../psa/set-up-currencies-exchange-rates.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="deeac-109">设置为项目使用的货币。</span><span class="sxs-lookup"><span data-stu-id="deeac-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="deeac-110">[创建部门](../psa/create-organizational-units.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="deeac-111">设置您的公司用于划分其业务的组，不论是按地域、业务功能还是其他逻辑分类。</span><span class="sxs-lookup"><span data-stu-id="deeac-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="deeac-112">[设置发票频率](../psa/set-up-invoice-frequencies.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="deeac-113">设置要为您的客户计费使用的时间段。</span><span class="sxs-lookup"><span data-stu-id="deeac-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="deeac-114">[配置交易类别](../psa/configure-transaction-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="deeac-115">设置您的顾问可以向其收取可记帐和不可记帐费用的交易类别。</span><span class="sxs-lookup"><span data-stu-id="deeac-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="deeac-116">[配置支出类别](../psa/configure-expense-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="deeac-117">设置您的顾问可以向其收取可记帐和不可记帐费用的类别。</span><span class="sxs-lookup"><span data-stu-id="deeac-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="deeac-118">[创建产品目录项](../psa/create-product-catalog-items.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="deeac-119">添加所销售的产品（例如软件许可证）到产品目录。</span><span class="sxs-lookup"><span data-stu-id="deeac-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="deeac-120">[创建价目表](../psa/create-price-list.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="deeac-121">根据您想要向客户收取的他们项目需要的每个角色的费用配置不同价目表。</span><span class="sxs-lookup"><span data-stu-id="deeac-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="deeac-122">[设置资源](../psa/set-up-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="deeac-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="deeac-123">添加您的项目需要的技能、专长、资源角色以及其他资源信息。</span><span class="sxs-lookup"><span data-stu-id="deeac-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="deeac-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="deeac-124">See Also</span></span>  
 <span data-ttu-id="deeac-125">[Project Service Automation 概述](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="deeac-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="deeac-126">[配置 Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="deeac-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="deeac-127">[客户经理指南](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="deeac-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="deeac-128">[项目经理指南](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="deeac-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="deeac-129">[资源经理指南](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="deeac-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="deeac-130">时间、费用和协作指南</span><span class="sxs-lookup"><span data-stu-id="deeac-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
