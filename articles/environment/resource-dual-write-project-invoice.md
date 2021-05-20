---
title: 项目发票集成
description: 本主题提供有关客户开票的 Project Operations 双重写入集成的信息。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955711"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="c7e0c-103">项目发票集成</span><span class="sxs-lookup"><span data-stu-id="c7e0c-103">Project invoice integration</span></span>

<span data-ttu-id="c7e0c-104">本主题提供有关客户开票的 Project Operations 双重写入集成的信息。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="c7e0c-105">在 Project Operations 中，项目经理管理项目记帐积压，并在 Microsoft Dataverse 中为客户创建估价发票。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="c7e0c-106">根据此估价发票，应收帐款职员或项目会计创建面向客户的发票。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="c7e0c-107">双重写入集成可确保估价发票详细信息同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="c7e0c-108">过帐面向客户的发票后，系统会使用会计详细信息更新 Dataverse 中的相关项目实际值。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="c7e0c-109">下图提供了此集成的高级概念概述图。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![项目发票集成](./media/DW5Invoicing.png)

<span data-ttu-id="c7e0c-111">项目经理在 Dataverse 中确认估价发票后，估价发票标头信息将使用双重写入表映射 **项目发票方案 V2 (发票)** 同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="c7e0c-112">这是从 Dataverse 到 Finance and Operations 应用的单向集成。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="c7e0c-113">不支持直接在 Finance and Operations 应用中创建或删除项目发票方案。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="c7e0c-114">Dataverse 中的发票确认还会触发业务逻辑，来在 **实际值** 实体中创建与记帐相关的记录。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="c7e0c-115">这些记录将使用双重写入表映射 **Project Operations 集成实际值 (msdyn\_actuals)** 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="c7e0c-116">有关详细信息，请参阅[项目估计值和实际值](resource-dual-write-estimates-actuals.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="c7e0c-117">项目发票方案明细通过定期流程 **从暂存导入** 创建。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="c7e0c-118">此流程基于 **实际值暂存** 表中的已记帐实际销售额详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="c7e0c-119">有关详细信息，请参阅[管理项目发票方案](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)。</span><span class="sxs-lookup"><span data-stu-id="c7e0c-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
