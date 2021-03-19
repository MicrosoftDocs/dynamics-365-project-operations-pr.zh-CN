---
title: 开票流程概述
description: 本主题提供在面向资源/非库存场景的 Project Operations 中开票的流程概述。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275796"
---
# <a name="invoicing-process-overview"></a><span data-ttu-id="1972a-103">开票流程概述</span><span class="sxs-lookup"><span data-stu-id="1972a-103">Invoicing process overview</span></span>

<span data-ttu-id="1972a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="1972a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1972a-105">面向资源/非库存场景的 Project Operations 提供了量身定制的全面功能，可以满足项目经理和应收帐款业务员/项目会计的需求。</span><span class="sxs-lookup"><span data-stu-id="1972a-105">Project Operations for resource/non-stocked based scenarios offers comprehensive capabilities tailored to fit the needs of both Project manager and Accounts receivable clerk/project accountant.</span></span> <span data-ttu-id="1972a-106">对于开票流程，项目经理管理项目记帐积压，应收帐款业务员/项目会计创建合规且准确的面向客户的发票单据。</span><span class="sxs-lookup"><span data-stu-id="1972a-106">For the invoicing process, the Project manager manages the project billing backlog and the Accounts receivable clerk/project accountant creates a compliant and accurate customer-facing invoice document.</span></span>

![开票流关系图](./media/invoicing-flow.png)

<span data-ttu-id="1972a-108">项目合同子项定义关联的项目交易的记帐方法。</span><span class="sxs-lookup"><span data-stu-id="1972a-108">The project contract line defines the billing method for associated project transactions.</span></span> <span data-ttu-id="1972a-109">当项目经理批准时间和支出交易时，系统会将交易记录在 **项目实际值** 实体中，并将信息发送到 Dynamics 365 Finance 中的 **项目管理和会计** 模块。</span><span class="sxs-lookup"><span data-stu-id="1972a-109">When the Project manager approves time and expense transactions, the system records the transactions in the **Project Actuals** entity and sends the information to the **Project management and accounting** module in Dynamics 365 Finance.</span></span> <span data-ttu-id="1972a-110">项目会计然后使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)来审核和过帐记录。</span><span class="sxs-lookup"><span data-stu-id="1972a-110">The Project accountant then reviews and posts the records using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="1972a-111">此日记帐包含项目实际值的重要会计详细信息，如记帐、销售税组、记帐物料销售税组和财务维度。</span><span class="sxs-lookup"><span data-stu-id="1972a-111">This journal includes important accounting details for project actuals, such as billing, sales tax group, billing item sales tax group, and financial dimensions.</span></span>

<span data-ttu-id="1972a-112">项目经理可以使用[时间和材料记帐积压](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)和[固定价格里程碑](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)中的时间和材料记帐方法审核未记帐的销售交易。</span><span class="sxs-lookup"><span data-stu-id="1972a-112">The Project manager can review unbilled sales transactions using the time and material billing method in the [Time and material billing backlog](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) and fixed price billing in [Fixed price milestones](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones).</span></span> <span data-ttu-id="1972a-113">这些视图让您可以筛选和选择下一个计费周期中需要包括的交易，然后将其标记为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="1972a-113">These views allow you to filter and select transactions that need to be included in the next billing cycle and then mark them as **Ready to Invoice**.</span></span>

<span data-ttu-id="1972a-114">您可以[手动创建估价发票](../proforma-invoicing/create-manual-proforma-invoice.md)或使用[定期流程](../proforma-invoicing/configure-automated-invoice-creation.md)。</span><span class="sxs-lookup"><span data-stu-id="1972a-114">You can [manually create a proforma invoice](../proforma-invoicing/create-manual-proforma-invoice.md) or use a [periodic process](../proforma-invoicing/configure-automated-invoice-creation.md).</span></span> <span data-ttu-id="1972a-115">项目经理可以根据需要[调整草稿估价发票](../proforma-invoicing/manage-proforma-invoice.md)，然后确认。</span><span class="sxs-lookup"><span data-stu-id="1972a-115">The Project manager can [adjust a draft proforma invoice](../proforma-invoicing/manage-proforma-invoice.md) as needed and then confirm it.</span></span>

<span data-ttu-id="1972a-116">确认的估价发票将发送到 Finance 中的 **项目管理和会计** 模块。</span><span class="sxs-lookup"><span data-stu-id="1972a-116">The confirmed proforma invoice is sent to the **Project management and accounting** module in Finance.</span></span> <span data-ttu-id="1972a-117">项目会计将设置项目发票方案的格式并更新，然后发布和打印文档。</span><span class="sxs-lookup"><span data-stu-id="1972a-117">The Project accountant formats and updates the project invoice proposal, and then posts and prints the document.</span></span> <span data-ttu-id="1972a-118">发布后的项目发票记录在总帐以及客户和项目分类帐中。</span><span class="sxs-lookup"><span data-stu-id="1972a-118">Posted project invoices are recorded in the General ledger, as well as the Customer and Project subledgers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]