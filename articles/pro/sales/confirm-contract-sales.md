---
title: 确认项目合同
description: 此主题提供如何在 Project Operations 中确认合同的信息。
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003665"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="b6e25-103">确认项目合同</span><span class="sxs-lookup"><span data-stu-id="b6e25-103">Confirm a project contract</span></span>

<span data-ttu-id="b6e25-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b6e25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b6e25-105">Dynamics 365 Project Operations 中的项目合同可以由于 **已确认** 的原因而处于活动状态，或者由于 **丢失** 的原因而处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="b6e25-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="b6e25-106">在确认项目合同时，状态将从 **草稿** 更新为 **有效**，状态描述为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="b6e25-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="b6e25-107">有效或关闭的合同无法编辑或重新打开。</span><span class="sxs-lookup"><span data-stu-id="b6e25-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="b6e25-108">确认项目合同的财务影响</span><span class="sxs-lookup"><span data-stu-id="b6e25-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="b6e25-109">确认项目合同后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重新计算成本。</span><span class="sxs-lookup"><span data-stu-id="b6e25-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="b6e25-110">然后根据关联项目合同子项的计费方法处理新的成本实际值。</span><span class="sxs-lookup"><span data-stu-id="b6e25-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="b6e25-111">如果成本实际值引用时间和材料合同子项，应用程序会自动重新创建相应的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="b6e25-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="b6e25-112">如果成本实际值引用固定价格合同子项，应用程序将停止重新处理成本实际值。</span><span class="sxs-lookup"><span data-stu-id="b6e25-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="b6e25-113">实际值中的上限、应计费设置以及定价和成本核算将在确认过程中评估，然后更新。</span><span class="sxs-lookup"><span data-stu-id="b6e25-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="b6e25-114">作为丢单关闭项目合同</span><span class="sxs-lookup"><span data-stu-id="b6e25-114">Close a project contract as lost</span></span>

<span data-ttu-id="b6e25-115">当作为丢单关闭项目合同时，合同状态将更新为 **已关闭**，状态描述为 **丢单**。</span><span class="sxs-lookup"><span data-stu-id="b6e25-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="b6e25-116">项目合同将变为只读。</span><span class="sxs-lookup"><span data-stu-id="b6e25-116">The project contract becomes read-only.</span></span> <span data-ttu-id="b6e25-117">在完成更改之前，会提供确认对话框，因为您无法重新打开已关闭的项目合同。</span><span class="sxs-lookup"><span data-stu-id="b6e25-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="b6e25-118">如果作为丢单关闭的项目合同在其子项上引用了项目，该项目也会标记为关闭。</span><span class="sxs-lookup"><span data-stu-id="b6e25-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="b6e25-119">从当一天之后的任何资源预订都会被取消。</span><span class="sxs-lookup"><span data-stu-id="b6e25-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="b6e25-120">发票上尚未包含的项目合同上的任何未记帐实际销售额都将被冲销。</span><span class="sxs-lookup"><span data-stu-id="b6e25-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="b6e25-121">在 Dynamics 365 Project Operations中，以丢单形式结束项目合同不会影响相关商机的状态。</span><span class="sxs-lookup"><span data-stu-id="b6e25-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="b6e25-122">商机仍保持开启状态，必须手动结束。</span><span class="sxs-lookup"><span data-stu-id="b6e25-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]