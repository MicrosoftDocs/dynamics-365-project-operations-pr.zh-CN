---
title: 供应商发票集成
description: 此主题提供有关 Project Operations 中的供应商发票集成的信息。
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955714"
---
# <a name="vendor-invoice-integration"></a><span data-ttu-id="fef63-103">供应商发票集成</span><span class="sxs-lookup"><span data-stu-id="fef63-103">Vendor invoice integration</span></span>

<span data-ttu-id="fef63-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fef63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fef63-105">可以通过以下方法记录 Dynamics 365 Project Operations 中与项目相关的采购：转到 **应付帐款** > **发票** > **待定供应商发票**，使用待定供应商发票文档。</span><span class="sxs-lookup"><span data-stu-id="fef63-105">Project-related procurement in Dynamics 365 Project Operations can be recorded by going to **Accounts Payable** > **Invoices** > **Pending vendor invoices** and using a pending vendor invoice document.</span></span> <span data-ttu-id="fef63-106">有关详细信息，请参阅[使用待定供应商发票购买非库存材料](../procurement/pending-vendor-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="fef63-106">For more information, see [Purchase non-stocked materials using a pending vendor invoice](../procurement/pending-vendor-invoices.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fef63-107">在使用本主题所述的功能之前，请查看并应用所需的配置。</span><span class="sxs-lookup"><span data-stu-id="fef63-107">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="fef63-108">有关详细信息，请参阅[启用非库存材料和待定供应商发票](../procurement/configure-materials-nonstocked.md)。</span><span class="sxs-lookup"><span data-stu-id="fef63-108">For more information, see [Enable non-stocked materials and pending vendor invoices](../procurement/configure-materials-nonstocked.md).</span></span>

<span data-ttu-id="fef63-109">在 Project Operations 中，与项目相关的供应商发票将使用特殊过帐规则过帐：</span><span class="sxs-lookup"><span data-stu-id="fef63-109">In Project Operations, project-related vendor invoices are posted using special posting rules:</span></span>

- <span data-ttu-id="fef63-110">与项目相关的成本（包括非抵扣税）不会立即过帐到总帐中的项目成本帐户。</span><span class="sxs-lookup"><span data-stu-id="fef63-110">Project-related cost (including non-recoverable tax) isn't immediately posted to the project cost account in the general ledger.</span></span> <span data-ttu-id="fef63-111">成本会过帐到 **采购集成帐户**。</span><span class="sxs-lookup"><span data-stu-id="fef63-111">Instead, the cost is posted to the **Procurement integration account**.</span></span> <span data-ttu-id="fef63-112">此帐户在 **Dynamics 365 Customer engagement 上的 Project Operations** 选项卡上的 **项目管理和会计** > **设置** > **项目管理和会计参数** 中配置。</span><span class="sxs-lookup"><span data-stu-id="fef63-112">This account is configured in **Project management and accounting** > **Setup** > **Project management and accounting parameters** on the **Project Operations on Dynamics 365 Customer engagement** tab.</span></span>
- <span data-ttu-id="fef63-113">双重写入使用以下表映射将供应商发票详细信息同步到 Microsoft Dataverse：</span><span class="sxs-lookup"><span data-stu-id="fef63-113">Dual-write synchronizes vendor invoice details to Microsoft Dataverse using the following table maps:</span></span>

     - <span data-ttu-id="fef63-114">**Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices)**：此表映射同步供应商发票标头信息。</span><span class="sxs-lookup"><span data-stu-id="fef63-114">**Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)**: This table map synchronizes vendor invoice header information.</span></span> <span data-ttu-id="fef63-115">仅至少有一个包含项目 ID 的明细的供应商发票会同步到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="fef63-115">Only vendor invoices with at least one line that contains a project ID are synchronized to Dataverse.</span></span>
     - <span data-ttu-id="fef63-116">**Project Operations 集成项目供应商发票明细导出实体 (msdyn_projectvendorinvoicelines)**：此表映射同步供应商发票明细信息。</span><span class="sxs-lookup"><span data-stu-id="fef63-116">**Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)**: This table map synchronizes vendor invoice line information.</span></span> <span data-ttu-id="fef63-117">仅包含项目 ID 的明细会同步到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="fef63-117">Only lines that contain a project ID are synchronized to Dataverse.</span></span>

     > [!NOTE]
     > <span data-ttu-id="fef63-118">Dataverse 中的供应商发票详细信息不可编辑。</span><span class="sxs-lookup"><span data-stu-id="fef63-118">Vendor invoice details in Dataverse are not editable.</span></span>

<span data-ttu-id="fef63-119">过帐供应商发票时，税子分类帐、供应商子分类帐和其他财务过帐将在 Dynamics 365 Finance 中记录为适用。</span><span class="sxs-lookup"><span data-stu-id="fef63-119">Tax subledger, vendor subledger, and other financial postings are recorded as applicable in Dynamics 365 Finance when the vendor invoice is posted.</span></span>

![供应商发票集成](media/DW7VendorInvoice.png)

<span data-ttu-id="fef63-121">当记录被写入 Dataverse 中的 **供应商发票** 实体时，记录的自动审批流程将开始。</span><span class="sxs-lookup"><span data-stu-id="fef63-121">When records are written to a **Vendor invoice** entity in Dataverse, an automated approval process of the records begins.</span></span> <span data-ttu-id="fef63-122">如果需要，可以转到 **高级设置** > **系统** > **系统作业**，在 Dataverse 中查看自动审批流程的状态。</span><span class="sxs-lookup"><span data-stu-id="fef63-122">If needed, the automated approval process status can be reviewed in Dataverse by going to **Advanced settings** > **System** > **System jobs**.</span></span> <span data-ttu-id="fef63-123">审批完成后，系统将在 **实际值** 实体中创建材料交易类记录。</span><span class="sxs-lookup"><span data-stu-id="fef63-123">After the approval is complete, the system creates material transaction class records in the **Actuals** entity.</span></span>

<span data-ttu-id="fef63-124">然后使用双重写入表映射 **Project Operations 集成实际值(msdyn_actuals)** 处理与材料相关的实际值。</span><span class="sxs-lookup"><span data-stu-id="fef63-124">Material-related actuals are then processed using the dual-write table map, **Project Operations integration actuals (msdyn_actuals)**.</span></span> <span data-ttu-id="fef63-125">有关详细信息，请参阅[项目估计值和实际值](resource-dual-write-estimates-actuals.md)。</span><span class="sxs-lookup"><span data-stu-id="fef63-125">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span>

<span data-ttu-id="fef63-126">定期流程 **从暂存导入** 创建与供应商发票相关的 Project Operations 集成日记帐行。</span><span class="sxs-lookup"><span data-stu-id="fef63-126">The periodic process, **Import from staging** creates vendor invoice-related Project Operations integration journal lines.</span></span> <span data-ttu-id="fef63-127">抵销帐户默认为采购集成帐户。</span><span class="sxs-lookup"><span data-stu-id="fef63-127">The offset account defaults to the procurement integration account.</span></span> <span data-ttu-id="fef63-128">过帐集成日记帐时，将清除供应商发票交易的帐户余额，并将明细金额移至项目成本帐户。</span><span class="sxs-lookup"><span data-stu-id="fef63-128">When the integration journal is posted, the account balance is cleared for the vendor invoice transaction and the line amount is moved to the project cost account.</span></span> <span data-ttu-id="fef63-129">另外还将创建项目子分类帐交易记录，用于下游开票和收入确认目的。</span><span class="sxs-lookup"><span data-stu-id="fef63-129">Project subledger transactions are also created for downstream invoicing and revenue recognition purposes.</span></span>
