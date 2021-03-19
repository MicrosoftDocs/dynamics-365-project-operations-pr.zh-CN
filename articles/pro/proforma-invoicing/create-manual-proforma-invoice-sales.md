---
title: 创建手动估价发票 - 精简
description: 此主题提供在 Project Operations 中创建手动估价发票的信息。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274177"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="76c1e-103">创建手动估价发票 - 精简</span><span class="sxs-lookup"><span data-stu-id="76c1e-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="76c1e-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="76c1e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76c1e-105">在 Dynamics 365 Project Operations 中，可以根据需要手动创建估价发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="76c1e-106">您可以从 **项目合同** 列表页或 **项目合同** 详细信息页手动创建估价发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="76c1e-107">项目合同列表页</span><span class="sxs-lookup"><span data-stu-id="76c1e-107">Project Contracts list page</span></span>

<span data-ttu-id="76c1e-108">在 **项目合同** 列表页上，选择一个或多个项目合同，然后为所有选定记录创建发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="76c1e-109">系统将检查所选的项目合同中哪些合同有日期在当天日期之前的 **可开票** 积压。</span><span class="sxs-lookup"><span data-stu-id="76c1e-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="76c1e-110">从这些合同，系统会创建草稿估价发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="76c1e-111">如果项目合同有多个客户，可能会为每个客户创建一个发票，每个项目合同有多个发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="76c1e-112">所有创建的项目发票都在 **销售** 区域 **记帐** 部分的 **发票** 页上提供。</span><span class="sxs-lookup"><span data-stu-id="76c1e-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="76c1e-113">项目合同详细信息页</span><span class="sxs-lookup"><span data-stu-id="76c1e-113">Project Contract details page</span></span>

<span data-ttu-id="76c1e-114">估价发票也可以从 **项目合同** 详细信息页面创建。</span><span class="sxs-lookup"><span data-stu-id="76c1e-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="76c1e-115">系统将验证项目合同是否有日期在当天日期之前的 **可开票** 积压。</span><span class="sxs-lookup"><span data-stu-id="76c1e-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="76c1e-116">从这些合同，系统会基于每个合同子项上的客户数量创建草稿估价发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="76c1e-117">创建了单个估价发票时，**发票** 页将打开。</span><span class="sxs-lookup"><span data-stu-id="76c1e-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="76c1e-118">如果为该项目合同创建了多个发票，将打开 **发票** 列表页以显示所有已创建的发票。</span><span class="sxs-lookup"><span data-stu-id="76c1e-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]