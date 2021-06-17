---
title: 关闭报价单 - 精简
description: 此主题提供有关在 Project Operations 中结束报价单的信息。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994125"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="a13e5-103">关闭报价单 - 精简</span><span class="sxs-lookup"><span data-stu-id="a13e5-103">Close a quote - lite</span></span>

<span data-ttu-id="a13e5-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="a13e5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a13e5-105">项目报价单可作为赢单或丢单结束。</span><span class="sxs-lookup"><span data-stu-id="a13e5-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a13e5-106">草稿报价单可以结束，因为 Microsoft Dynamics 365 Project Operations 中不支持对报价单执行激活和修订操作。</span><span class="sxs-lookup"><span data-stu-id="a13e5-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a13e5-107">作为赢单结束报价单</span><span class="sxs-lookup"><span data-stu-id="a13e5-107">Close a quote as Won</span></span>

<span data-ttu-id="a13e5-108">当您作为赢单结束项目报价单时，状态将设置为“已结束”，状态描述为“赢单”。</span><span class="sxs-lookup"><span data-stu-id="a13e5-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="a13e5-109">结束报价单会使项目报价单成为只读，并创建一个包含报价单信息的草稿项目合同。</span><span class="sxs-lookup"><span data-stu-id="a13e5-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a13e5-110">由于无法重新开启已结束的报价单，确认对话将确认您的更改。</span><span class="sxs-lookup"><span data-stu-id="a13e5-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a13e5-111">如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。</span><span class="sxs-lookup"><span data-stu-id="a13e5-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a13e5-112">将报价单作为赢单结束的财务影响</span><span class="sxs-lookup"><span data-stu-id="a13e5-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a13e5-113">如果项目上有任何时间实际值仍附加在草稿报价单上，将仅记录时间或支出成本。</span><span class="sxs-lookup"><span data-stu-id="a13e5-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a13e5-114">当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。</span><span class="sxs-lookup"><span data-stu-id="a13e5-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a13e5-115">应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。</span><span class="sxs-lookup"><span data-stu-id="a13e5-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a13e5-116">如果成本实际值引用时间和物料合同子项，则会针对报价单结束和项目合同创建的情况创建相应的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="a13e5-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a13e5-117">如果成本实际值引用固定价格合同子项，应用程序将停止重新处理基于项目合同客户的已拆分记帐规则的成本实际值。</span><span class="sxs-lookup"><span data-stu-id="a13e5-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a13e5-118">作为丢单结束报价单：</span><span class="sxs-lookup"><span data-stu-id="a13e5-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a13e5-119">当您作为丢单结束项目报价单时，状态将设置为“已结束”，状态描述为“丢单”。</span><span class="sxs-lookup"><span data-stu-id="a13e5-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="a13e5-120">结束报价单会使项目报价单成为只读。</span><span class="sxs-lookup"><span data-stu-id="a13e5-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a13e5-121">由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。</span><span class="sxs-lookup"><span data-stu-id="a13e5-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a13e5-122">如果作为丢单结束的项目报价单引用其任何行中的项目，该项目也将标记为“已结束”。</span><span class="sxs-lookup"><span data-stu-id="a13e5-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="a13e5-123">从当一天之后的任何资源预订都会被取消。</span><span class="sxs-lookup"><span data-stu-id="a13e5-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a13e5-124">在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。</span><span class="sxs-lookup"><span data-stu-id="a13e5-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]