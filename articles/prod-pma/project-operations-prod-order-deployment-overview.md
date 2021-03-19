---
title: 面向库存/生产订单场景的 Project Operations 部署概述
description: 此主题提供有关面向库存/生产订单场景的 Project Operations 部署类型的信息。
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ffbcb326e5cd86c49b3b3b27ce7d68404a6842b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289223"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="24d20-103">面向库存/生产订单场景的 Project Operations 部署概述</span><span class="sxs-lookup"><span data-stu-id="24d20-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="24d20-104">_**适用范围：** 面向库存/生产订单场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="24d20-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="24d20-105">此部署类型具有以下适用于基于项目的公司的功能：</span><span class="sxs-lookup"><span data-stu-id="24d20-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="24d20-106">使用[工作分解结构](work-breakdown-structures.md)的项目规划</span><span class="sxs-lookup"><span data-stu-id="24d20-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="24d20-107">为项目采购和使用存货库存</span><span class="sxs-lookup"><span data-stu-id="24d20-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="24d20-108">使用 Dynamics 365 Finance and Operations 应用中的 **销售和市场营销** 模块管理基于项目的销售</span><span class="sxs-lookup"><span data-stu-id="24d20-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="24d20-109">使用 Finance and Operations 应用中的成本费率和帐单费率配置进行项目定价和成本核算</span><span class="sxs-lookup"><span data-stu-id="24d20-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="24d20-110">Finance and Operations 应用中的项目资源管理</span><span class="sxs-lookup"><span data-stu-id="24d20-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="24d20-111">Finance and Operations 应用中的项目进度和时间跟踪</span><span class="sxs-lookup"><span data-stu-id="24d20-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="24d20-112">使用 OCR 功能捕获收据的项目和非项目支出的支出管理体验</span><span class="sxs-lookup"><span data-stu-id="24d20-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="24d20-113">使用企业级销售税和有时效性的汇率系统的开票</span><span class="sxs-lookup"><span data-stu-id="24d20-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="24d20-114">用于 WIP 会计和应计的可配置项目组</span><span class="sxs-lookup"><span data-stu-id="24d20-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="24d20-115">项目收入确认</span><span class="sxs-lookup"><span data-stu-id="24d20-115">Project revenue recognition</span></span>

<span data-ttu-id="24d20-116">此部署类型还提供对 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 应用程序提供的功能的扩展。</span><span class="sxs-lookup"><span data-stu-id="24d20-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="24d20-117">选择此部署类型以在整个项目生命周期内使用 Dynamics 365 Project Operations，包括以下关键要求：</span><span class="sxs-lookup"><span data-stu-id="24d20-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="24d20-118">一个广泛的项目管理系统，管理用于计划和财务的内部收费项目的库存项目和作业/生产订单成本核算。</span><span class="sxs-lookup"><span data-stu-id="24d20-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="24d20-119">已经有 Dynamics 365 Finance 或 Dynamics 365 Supply Chain and Manufacturing 应用以及集成的基于项目的交易的组织将简化数据访问和报告需求。</span><span class="sxs-lookup"><span data-stu-id="24d20-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="24d20-120">一个功能齐全的支出管理系统，包含用于跟踪项目和非项目支出的政策执行和偿还。</span><span class="sxs-lookup"><span data-stu-id="24d20-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="24d20-121">一个企业级销售税和汇率引擎，用于为项目生成面向客户的发票。</span><span class="sxs-lookup"><span data-stu-id="24d20-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="24d20-122">符合国际财务报告标准 (IFRS) 的项目会计和收入确认系统。</span><span class="sxs-lookup"><span data-stu-id="24d20-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]