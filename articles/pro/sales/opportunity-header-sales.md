---
title: 商机标题
description: 此主题介绍基于项目的交易和基于项目的商机明细的整体信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072532"
---
# <a name="opportunity-header"></a><span data-ttu-id="1b609-103">商机标题</span><span class="sxs-lookup"><span data-stu-id="1b609-103">Opportunity header</span></span>

<span data-ttu-id="1b609-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="1b609-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1b609-105">商机标题捕获将应用于基于项目的商机上所有明细的基于项目的交易的综合信息。</span><span class="sxs-lookup"><span data-stu-id="1b609-105">The Opportunity header captures the overall information about a project-based deal that applies to all the lines on the project-based opportunity.</span></span>

<span data-ttu-id="1b609-106">Dynamics 365 Project Operations 中基于项目的商机是 Dynamics 365 Sales 中商机的扩展。</span><span class="sxs-lookup"><span data-stu-id="1b609-106">Project-based opportunities in Dynamics 365 Project Operations are extensions of opportunities in Dynamics 365 Sales.</span></span> <span data-ttu-id="1b609-107">这些扩展提供特定于基于项目的商机以及这类商机所需的附加功能。</span><span class="sxs-lookup"><span data-stu-id="1b609-107">These extensions provide additional functionality that is specific to and required for project-based opportunities.</span></span> <span data-ttu-id="1b609-108">这些扩展可以包含基于项目的商机中可用的新字段和功能区操作。</span><span class="sxs-lookup"><span data-stu-id="1b609-108">These extensions can include new fields and ribbon actions available in project-based opportunities.</span></span> <span data-ttu-id="1b609-109">您可能会发现 Project Operations 中不可用但 Sales 中可用的一些字段、功能和默认设置逻辑。</span><span class="sxs-lookup"><span data-stu-id="1b609-109">You may find some fields, functionality, and defaulting logic that is available in Sales isn't available in Project Operations.</span></span>

<span data-ttu-id="1b609-110">下表包括基于项目的商机中的字段，这些字段是 Project Operations 所特有的，或具有对 Sales 中的商机的一些重要的行为更改。</span><span class="sxs-lookup"><span data-stu-id="1b609-110">The following table includes the fields in a project-based opportunity that are either unique to Project Operations or have some important changes in behavior from the Opportunities in Sales.</span></span>

| <span data-ttu-id="1b609-111">**字段**</span><span class="sxs-lookup"><span data-stu-id="1b609-111">**Field**</span></span> | <span data-ttu-id="1b609-112">**位置**</span><span class="sxs-lookup"><span data-stu-id="1b609-112">**Location**</span></span> | <span data-ttu-id="1b609-113">**关联性、用途和指导**</span><span class="sxs-lookup"><span data-stu-id="1b609-113">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="1b609-114">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="1b609-114">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="1b609-115">Type</span><span class="sxs-lookup"><span data-stu-id="1b609-115">Type</span></span> | <span data-ttu-id="1b609-116">“常规”选项卡（隐藏）</span><span class="sxs-lookup"><span data-stu-id="1b609-116">General tab (hidden)</span></span> | <span data-ttu-id="1b609-117">此选项集字段具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="1b609-117">This option set field has the following options:</span></span></br><span data-ttu-id="1b609-118">- 基于工作（仅通过 Project Operations 提供）</span><span class="sxs-lookup"><span data-stu-id="1b609-118">- Work-based (available only with Project Operations)</span></span></br><span data-ttu-id="1b609-119">- 基于项目（仅在安装了 Project Operations 和 Sales 时可用）</span><span class="sxs-lookup"><span data-stu-id="1b609-119">- Item-based (available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="1b609-120">- 基于服务维护（安装 Field Service 后可用）</span><span class="sxs-lookup"><span data-stu-id="1b609-120">- Service maintenance-based (available when Field Service is installed)</span></span> | <span data-ttu-id="1b609-121">当您使用 Project Operations 时，此字段值会自动设置为 **基于工作** ，将商机分类为基于项目。</span><span class="sxs-lookup"><span data-stu-id="1b609-121">When you use Project Operations, this field value is automatically set to **Work-based** which classifies the Opportunity as project-based.</span></span> <span data-ttu-id="1b609-122">商机应该基于项目，以在此交易的下游销售流程中启用所有项目特定的扩展和功能。</span><span class="sxs-lookup"><span data-stu-id="1b609-122">An Opportunity should be project-based to enable all project-specific extensions and functionality in the downstream sales process for this deal.</span></span> |
| <span data-ttu-id="1b609-123">联系人​​</span><span class="sxs-lookup"><span data-stu-id="1b609-123">Contact</span></span> | <span data-ttu-id="1b609-124">“常规”选项卡</span><span class="sxs-lookup"><span data-stu-id="1b609-124">General tab</span></span> | <span data-ttu-id="1b609-125">对此交易的客户主要联系人的引用。</span><span class="sxs-lookup"><span data-stu-id="1b609-125">Reference to the customer's primary contact for this deal.</span></span> | |
| <span data-ttu-id="1b609-126">帐户​​</span><span class="sxs-lookup"><span data-stu-id="1b609-126">Account</span></span> | <span data-ttu-id="1b609-127">“常规”选项卡</span><span class="sxs-lookup"><span data-stu-id="1b609-127">General tab</span></span> | <span data-ttu-id="1b609-128">对客户的公司或客户记录的引用。</span><span class="sxs-lookup"><span data-stu-id="1b609-128">Reference to the customer's company or account record.</span></span> | |
| <span data-ttu-id="1b609-129">客户经理</span><span class="sxs-lookup"><span data-stu-id="1b609-129">Account Manager</span></span> | <span data-ttu-id="1b609-130">“常规”选项卡</span><span class="sxs-lookup"><span data-stu-id="1b609-130">General tab</span></span> | <span data-ttu-id="1b609-131">此基于项目的商机的客户经理的姓名。</span><span class="sxs-lookup"><span data-stu-id="1b609-131">The name of the Account manager for this project-based opportunity.</span></span> | <span data-ttu-id="1b609-132">客户经理负责在此项目完成之前管理与客户的关系。</span><span class="sxs-lookup"><span data-stu-id="1b609-132">The Account manager is responsible for managing the relationship with the customer through the completion of this project.</span></span> <span data-ttu-id="1b609-133">根据与客户经理关联的可预订资源记录，默认设置合同签订部门。</span><span class="sxs-lookup"><span data-stu-id="1b609-133">Based on the bookable resource record tied to the Account manager, the contracting unit is defaulted.</span></span> |
| <span data-ttu-id="1b609-134">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="1b609-134">Contracting Unit</span></span> | <span data-ttu-id="1b609-135">“常规”选项卡</span><span class="sxs-lookup"><span data-stu-id="1b609-135">General tab</span></span> | <span data-ttu-id="1b609-136">负责交付与此交易关联的一个或多个项目的部门。</span><span class="sxs-lookup"><span data-stu-id="1b609-136">The Organization unit that is responsible for the delivery of the project or projects associated with this deal.</span></span> | <span data-ttu-id="1b609-137">合同签订部门是在交易完成后完成项目的公司部门。</span><span class="sxs-lookup"><span data-stu-id="1b609-137">The contracting unit is the division of the company that will complete the project(s) after the deal is closed.</span></span> <span data-ttu-id="1b609-138">每个合同签订部门都有一种货币，此货币用于报告项目中产生的预估成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="1b609-138">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |

<span data-ttu-id="1b609-139">商机的 **摘要** 选项卡上的所有其他字段和部分，请参阅[创建或编辑商机（Sales 和销售中心）](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)</span><span class="sxs-lookup"><span data-stu-id="1b609-139">For all the other fields and sections on the **Summary** tab of the opportunity, see [Create or edit opportunities (Sales and Sales hub)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)</span></span>