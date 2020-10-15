---
title: 结束报价单
description: 此主题提供有关在 Project Operations 中结束报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898880"
---
# <a name="close-a-quote"></a><span data-ttu-id="49180-103">结束报价单</span><span class="sxs-lookup"><span data-stu-id="49180-103">Close a quote</span></span>

<span data-ttu-id="49180-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="49180-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="49180-105">项目报价单可作为赢单或丢单结束。</span><span class="sxs-lookup"><span data-stu-id="49180-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="49180-106">由于 Microsoft Dynamics 365 Project Operations 中的报价单不支持“激活”和“修订”功能，因此您可以结束草稿报价单。</span><span class="sxs-lookup"><span data-stu-id="49180-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="49180-107">作为赢单结束报价单</span><span class="sxs-lookup"><span data-stu-id="49180-107">Close a quote as Won</span></span>

<span data-ttu-id="49180-108">将项目报价单作为赢单结束会将报价单的状态设置为**已结束**，将状态描述设置为**赢单**。</span><span class="sxs-lookup"><span data-stu-id="49180-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="49180-109">结束报价单会使其变为只读，并创建一个包含所有报价单信息的草稿项目合同。</span><span class="sxs-lookup"><span data-stu-id="49180-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="49180-110">由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。</span><span class="sxs-lookup"><span data-stu-id="49180-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="49180-111">从项目报价单创建的项目合同在 Project Operations 的项目管理和会计模块中也会变为可用。</span><span class="sxs-lookup"><span data-stu-id="49180-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="49180-112">如果项目合同未映射到其任何子项上的项目，此项目合同将作为停用项目合同提供，并在项目至少映射到其合同子项中的一项后即变为可用。</span><span class="sxs-lookup"><span data-stu-id="49180-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="49180-113">如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。</span><span class="sxs-lookup"><span data-stu-id="49180-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="49180-114">将报价单作为赢单结束的财务影响</span><span class="sxs-lookup"><span data-stu-id="49180-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="49180-115">如果在项目仍附在草稿报价单上时项目中记录了时间的实际值，将仅记录时间或支出成本。</span><span class="sxs-lookup"><span data-stu-id="49180-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="49180-116">当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。</span><span class="sxs-lookup"><span data-stu-id="49180-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="49180-117">应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。</span><span class="sxs-lookup"><span data-stu-id="49180-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="49180-118">如果成本实际值引用时间和材料合同子项，系统将自动为报价单结束和项目合同创建创建相应的未记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="49180-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="49180-119">如果成本实际值引用固定价格合同子项，应用程序将根据项目合同客户的拆分计费规则停止重新处理成本实际值。</span><span class="sxs-lookup"><span data-stu-id="49180-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="49180-120">所有重新处理的实际值均在项目管理和会计模块中提供，供项目会计查看、更新和过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="49180-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="49180-121">作为丢单结束报价单</span><span class="sxs-lookup"><span data-stu-id="49180-121">Close a quote as Lost</span></span>

<span data-ttu-id="49180-122">将项目报价单作为丢单结束会将状态设置为**已结束**，将状态描述设置为**丢单**。</span><span class="sxs-lookup"><span data-stu-id="49180-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="49180-123">结束报价单会使其变为只读。</span><span class="sxs-lookup"><span data-stu-id="49180-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="49180-124">由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。</span><span class="sxs-lookup"><span data-stu-id="49180-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="49180-125">如果作为丢单结束的项目报价单在其任意明细上引用了项目，该项目也将标记为“已结束”，那一天之后的所有资源预订都将取消。</span><span class="sxs-lookup"><span data-stu-id="49180-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="49180-126">在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。</span><span class="sxs-lookup"><span data-stu-id="49180-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
