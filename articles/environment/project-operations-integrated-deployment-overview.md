---
title: 面向资源/非库存场景的 Project Operations 部署概述
description: 此主题提供有关面向资源/非库存场景的 Project Operations 部署类型的信息。
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca8c0894dff1a74b532f8262278fb20400f097c5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001235"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="b0c4a-103">面向资源/非库存场景的 Project Operations 部署概述</span><span class="sxs-lookup"><span data-stu-id="b0c4a-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="b0c4a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b0c4a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0c4a-105">面向资源/非库存场景的 Dynamics 365 Project Operations 部署类型具有以下适用于基于项目的公司的功能：</span><span class="sxs-lookup"><span data-stu-id="b0c4a-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="b0c4a-106">使用 Web 版本的 Microsoft Project 进行项目规划</span><span class="sxs-lookup"><span data-stu-id="b0c4a-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="b0c4a-107">劳动力资源的多维定价和成本核算</span><span class="sxs-lookup"><span data-stu-id="b0c4a-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="b0c4a-108">支出类别基于类别的定价</span><span class="sxs-lookup"><span data-stu-id="b0c4a-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="b0c4a-109">使用 Dynamics 365 Sales 功能的基于项目的销售管理</span><span class="sxs-lookup"><span data-stu-id="b0c4a-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="b0c4a-110">与其他应用程序（如 Dynamics 365 Field Service 和 Dynamics 365 Customer Service）集成的 Universal Resource Scheduling</span><span class="sxs-lookup"><span data-stu-id="b0c4a-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="b0c4a-111">项目进度和时间跟踪</span><span class="sxs-lookup"><span data-stu-id="b0c4a-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="b0c4a-112">包括使用 OCR 功能捕获收据在内的项目和非项目支出的基本和完整支出管理体验</span><span class="sxs-lookup"><span data-stu-id="b0c4a-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="b0c4a-113">从估价扩展到面向客户的开票，由企业级销售税和有时效性的汇率系统提供支持。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="b0c4a-114">可配置项目成本、收入模板和进行中工作 (WIP) 的会计和应计规则</span><span class="sxs-lookup"><span data-stu-id="b0c4a-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="b0c4a-115">项目收入确认</span><span class="sxs-lookup"><span data-stu-id="b0c4a-115">Project revenue recognition</span></span>
- <span data-ttu-id="b0c4a-116">通过 Power Platform 进行扩展</span><span class="sxs-lookup"><span data-stu-id="b0c4a-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="b0c4a-117">此部署类型提供对 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 应用程序提供的功能的扩展。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="b0c4a-118">如果您预期 Project Operations 将在整个项目生命周期内使用，应选择此部署类型，包括以下要求：</span><span class="sxs-lookup"><span data-stu-id="b0c4a-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="b0c4a-119">能够使用 Sales 应用程序中的功能管理基于项目的销售及其他类型的销售。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="b0c4a-120">一个集成的项目管理系统，管理从项目销售到会计的用于计划和财务的内部收费项目。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="b0c4a-121">一个支出管理系统，包含用于跟踪项目和非项目支出的政策执行和偿还。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="b0c4a-122">需要一个功能丰富的企业级销售税和汇率引擎，用于为项目生成面向客户的发票。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="b0c4a-123">符合国际财务报告标准 (IFRS) 的项目会计和收入确认系统。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="b0c4a-124">Finance 或 Supply Chain Management 应用程序，以及集成基于项目的交易。</span><span class="sxs-lookup"><span data-stu-id="b0c4a-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]