---
title: 使用待定供应商发票购买非库存材料
description: 本主题说明如何记录待定供应商发票。
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880624"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="6661a-103">使用待定供应商发票购买非库存材料</span><span class="sxs-lookup"><span data-stu-id="6661a-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="6661a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6661a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6661a-105">当公司为项目采购非库存材料时，可以立即针对项目记录成本。</span><span class="sxs-lookup"><span data-stu-id="6661a-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="6661a-106">例如，Contoso Robotics US 正在执行设备更新项目，需要软件许可证。</span><span class="sxs-lookup"><span data-stu-id="6661a-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="6661a-107">这些许可证是从第三方供应商购买的。</span><span class="sxs-lookup"><span data-stu-id="6661a-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="6661a-108">使用 Dynamics 365 Finance，应付帐款职员记录待定供应商发票单据，并将许可证成本直接归于设备更新项目。</span><span class="sxs-lookup"><span data-stu-id="6661a-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="6661a-109">在使用本主题所述的功能之前，请查看并应用所需的配置。</span><span class="sxs-lookup"><span data-stu-id="6661a-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="6661a-110">有关详细信息，请参阅[启用非库存材料和待定供应商发票](configure-materials-nonstocked.md)。</span><span class="sxs-lookup"><span data-stu-id="6661a-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="6661a-111">过帐与项目相关的待定供应商发票</span><span class="sxs-lookup"><span data-stu-id="6661a-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="6661a-112">待定供应商发票可以在 **待定供应商发票** 页上记录（**应付帐款** > **发票** > **待定供应商发票**）。</span><span class="sxs-lookup"><span data-stu-id="6661a-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="6661a-113">完成以下步骤过帐与项目相关的待定供应商发票：</span><span class="sxs-lookup"><span data-stu-id="6661a-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="6661a-114">转到 **应付帐款** > **发票**，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6661a-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="6661a-115">在 **发票客户** 字段中，选择一个供应商，在 **编号** 字段中，输入供应商发票标识。</span><span class="sxs-lookup"><span data-stu-id="6661a-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="6661a-116">在供应商发票上添加明细，然后在 **物料编号** 字段中，选择从供应商处购买的非库存物料。</span><span class="sxs-lookup"><span data-stu-id="6661a-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="6661a-117">基于采购类别的供应商发票明细无法针对项目记录。</span><span class="sxs-lookup"><span data-stu-id="6661a-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="6661a-118">添加购买的数量。</span><span class="sxs-lookup"><span data-stu-id="6661a-118">Add the quantity purchased.</span></span> <span data-ttu-id="6661a-119">系统将基于非库存物料价格配置填充单价。</span><span class="sxs-lookup"><span data-stu-id="6661a-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="6661a-120">验证明细上的总金额和其他所需详细信息。</span><span class="sxs-lookup"><span data-stu-id="6661a-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="6661a-121">在明细详细信息的 **项目** 选项卡上，选择将要向其记录此物料的项目的 ID。</span><span class="sxs-lookup"><span data-stu-id="6661a-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="6661a-122">（可选）选择活动编号，更新项目类别和明细属性。</span><span class="sxs-lookup"><span data-stu-id="6661a-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="6661a-123">过帐待定供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6661a-123">Post pending vendor invoice.</span></span> <span data-ttu-id="6661a-124">过帐发票时，系统将记录：</span><span class="sxs-lookup"><span data-stu-id="6661a-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="6661a-125">供应商余额金额。</span><span class="sxs-lookup"><span data-stu-id="6661a-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="6661a-126">销售税金额。</span><span class="sxs-lookup"><span data-stu-id="6661a-126">The sales tax amount.</span></span>
    - <span data-ttu-id="6661a-127">项目的成本将记录到采购集成帐户中。</span><span class="sxs-lookup"><span data-stu-id="6661a-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="6661a-128">Dataverse 中的项目实际值交易。</span><span class="sxs-lookup"><span data-stu-id="6661a-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="6661a-129">此交易将使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)进一步处理。</span><span class="sxs-lookup"><span data-stu-id="6661a-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="6661a-130">过帐此日记帐会将金额从采购集成帐户转移到项目成本帐户。</span><span class="sxs-lookup"><span data-stu-id="6661a-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
