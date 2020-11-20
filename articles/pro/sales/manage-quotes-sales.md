---
title: 管理项目报价单
description: 此主题提供有关项目报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177815"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="0c171-103">管理项目报价单</span><span class="sxs-lookup"><span data-stu-id="0c171-103">Manage project quotes</span></span>

<span data-ttu-id="0c171-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="0c171-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c171-105">在 Dynamics 365 Project Operations 中，项目报价单专门用于帮助构建项目工作方案。</span><span class="sxs-lookup"><span data-stu-id="0c171-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="0c171-106">Project Operations 中项目报价单的结构针对具有以下组件的项目方案构造：</span><span class="sxs-lookup"><span data-stu-id="0c171-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="0c171-107">标识将显示为高级组件的独立工作组件的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="0c171-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="0c171-108">标识和估计每个高级组件或报价单明细的工作的报价单明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="0c171-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="0c171-109">与报价单明细关联的工作的计划或日期估计和财务方面信息。</span><span class="sxs-lookup"><span data-stu-id="0c171-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="0c171-110">为每个报价单明细设置合同签订模型和应计费组件。</span><span class="sxs-lookup"><span data-stu-id="0c171-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="0c171-111">此设置帮助估计每个报价单明细和整个报价单的收入、花费和利润率的传播。</span><span class="sxs-lookup"><span data-stu-id="0c171-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="0c171-112">查看所有基于项目的报价单</span><span class="sxs-lookup"><span data-stu-id="0c171-112">View all project-based quotes</span></span>

<span data-ttu-id="0c171-113">可以从 **报价单** 列表页查看所有项目报价单的列表。</span><span class="sxs-lookup"><span data-stu-id="0c171-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="0c171-114">转到 **销售** > **报价单**。</span><span class="sxs-lookup"><span data-stu-id="0c171-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="0c171-115">包含您在系统中的所有项目报价单的列表将显示。</span><span class="sxs-lookup"><span data-stu-id="0c171-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="0c171-116">使用 **视图切换器** 选择报价单的其他筛选视图。</span><span class="sxs-lookup"><span data-stu-id="0c171-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="0c171-117">使用自定义筛选条件，您可以配置自己的视图和导航选项。</span><span class="sxs-lookup"><span data-stu-id="0c171-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="0c171-118">可以从此列表页或详细信息页面创建或删除报价单。</span><span class="sxs-lookup"><span data-stu-id="0c171-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
