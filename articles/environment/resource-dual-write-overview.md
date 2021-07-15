---
title: Project Operations 双重写入集成
description: 本主题概述了 Project Operations 双重写入集成。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368420"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="ef3a8-103">Project Operations 双重写入集成概述</span><span class="sxs-lookup"><span data-stu-id="ef3a8-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="ef3a8-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ef3a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef3a8-105">Project Operations 使用[双重写入功能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)在 Microsoft Dataverse 和 Dynamics 365 Finance 之间同步数据 。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="ef3a8-106">下图显示了如何作为 Dataverse 和 Finance 之间集成的一部分同步数据。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations 数据流概述](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="ef3a8-108">Dataverse 上的 Project Operations 提供现代的用户界面 (UI)，并使用 Power Platform 功能提供简便的无代码/低代码可扩展性。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="ef3a8-109">项目经理、资源经理、项目团队成员和其他行政人员在 Dataverse 上的 Project Operations 中执行活动。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="ef3a8-110">Finance 中的 Project Operations 提供项目会计和收入确认支持。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="ef3a8-111">Project Operations 插入了 Finance 中的财务框架，用于销售税计算、货币汇率、财务维度报告等。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="ef3a8-112">项目会计体验主要在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="ef3a8-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="ef3a8-113">Project Operations 集成包括以下组件集成：</span><span class="sxs-lookup"><span data-stu-id="ef3a8-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="ef3a8-114">Project Operations 设置和配置数据集成</span><span class="sxs-lookup"><span data-stu-id="ef3a8-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="ef3a8-115">项目估计值和实际值</span><span class="sxs-lookup"><span data-stu-id="ef3a8-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="ef3a8-116">项目发票</span><span class="sxs-lookup"><span data-stu-id="ef3a8-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="ef3a8-117">支出管理</span><span class="sxs-lookup"><span data-stu-id="ef3a8-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="ef3a8-118">供应商发票</span><span class="sxs-lookup"><span data-stu-id="ef3a8-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
