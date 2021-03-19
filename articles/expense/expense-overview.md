---
title: 支出概述
description: 本主题提供有关 Project Operations 中的支出功能的信息。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276562"
---
# <a name="expense-home-page"></a><span data-ttu-id="59d89-103">支出主页</span><span class="sxs-lookup"><span data-stu-id="59d89-103">Expense home page</span></span>

<span data-ttu-id="59d89-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="59d89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="59d89-105">Dynamics 365 Project Operations 支持处理支出功能。</span><span class="sxs-lookup"><span data-stu-id="59d89-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="59d89-106">通过使用可自定义的策略、交易类别和审批工作流，处理项目产生或不是项目产生的支出。</span><span class="sxs-lookup"><span data-stu-id="59d89-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="59d89-107">在 Project Operations 中，支持两种支出部署模型：</span><span class="sxs-lookup"><span data-stu-id="59d89-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="59d89-108">**完全**：完全部署可用于 **面向资源/非库存场景的 Project Operations** 或 **面向生产订单场景的 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="59d89-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="59d89-109">**基本**：基本部署可用于 **面向资源/非库存场景的 Project Operations** 和 **精简部署 - 估价交易开票**。</span><span class="sxs-lookup"><span data-stu-id="59d89-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="59d89-110">完全</span><span class="sxs-lookup"><span data-stu-id="59d89-110">Full</span></span> 
<span data-ttu-id="59d89-111">完全支出部署提供完整的政策执行，包括创建政策功能，如：</span><span class="sxs-lookup"><span data-stu-id="59d89-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="59d89-112">支出类别限制</span><span class="sxs-lookup"><span data-stu-id="59d89-112">Expense category limits</span></span>
  - <span data-ttu-id="59d89-113">旅行</span><span class="sxs-lookup"><span data-stu-id="59d89-113">Travel</span></span>
  - <span data-ttu-id="59d89-114">每日</span><span class="sxs-lookup"><span data-stu-id="59d89-114">Per diem</span></span>
  - <span data-ttu-id="59d89-115">信用卡导入</span><span class="sxs-lookup"><span data-stu-id="59d89-115">Credit card imports</span></span>
  - <span data-ttu-id="59d89-116">收据光学字符识别</span><span class="sxs-lookup"><span data-stu-id="59d89-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="59d89-117">Basic</span><span class="sxs-lookup"><span data-stu-id="59d89-117">Basic</span></span> 
<span data-ttu-id="59d89-118">基本支出部署场景只允许您记录项目的基本支出。</span><span class="sxs-lookup"><span data-stu-id="59d89-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="59d89-119">有关详细信息，请参阅[支出条目（精简）](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="59d89-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="59d89-120">确定支出部署</span><span class="sxs-lookup"><span data-stu-id="59d89-120">Determine your Expense deployment</span></span>
<span data-ttu-id="59d89-121">要确定您运行的是否是基本支出管理部署，请验证地址 URL 是否以 **.crm.dynamics.com** 结尾。</span><span class="sxs-lookup"><span data-stu-id="59d89-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]