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
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072525"
---
# <a name="close-quotes"></a><span data-ttu-id="62adf-103">结束报价单</span><span class="sxs-lookup"><span data-stu-id="62adf-103">Close quotes</span></span> 

<span data-ttu-id="62adf-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="62adf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62adf-105">项目报价单可作为赢单或丢单结束。</span><span class="sxs-lookup"><span data-stu-id="62adf-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="62adf-106">Microsoft Dynamics 365 Project Operations 中不支持对报价单执行“激活”和“修订”操作，因此可以结束报价单草稿。</span><span class="sxs-lookup"><span data-stu-id="62adf-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="62adf-107">作为赢单结束报价单</span><span class="sxs-lookup"><span data-stu-id="62adf-107">Close a quote as Won</span></span>

<span data-ttu-id="62adf-108">将项目报价单作为赢单结束将结束报价单，并将状态设置为“已结束”，将状态描述设置为“赢单”。</span><span class="sxs-lookup"><span data-stu-id="62adf-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="62adf-109">结束报价单会使项目报价单成为只读，并创建一个包含报价单信息的草稿项目合同。</span><span class="sxs-lookup"><span data-stu-id="62adf-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="62adf-110">由于无法重新开启已结束的报价单，因此有一个确认对话框。由于无法重新开启已结束的报价单，并且更改不可逆，因此，在进行更改之前，会出现一个确认对话框。</span><span class="sxs-lookup"><span data-stu-id="62adf-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="62adf-111">如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。</span><span class="sxs-lookup"><span data-stu-id="62adf-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="62adf-112">将报价单作为赢单结束的财务影响</span><span class="sxs-lookup"><span data-stu-id="62adf-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="62adf-113">如果在项目仍附在草稿报价单上时项目中记录了时间的实际值，将仅记录时间或支出成本。</span><span class="sxs-lookup"><span data-stu-id="62adf-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="62adf-114">当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。</span><span class="sxs-lookup"><span data-stu-id="62adf-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="62adf-115">应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。</span><span class="sxs-lookup"><span data-stu-id="62adf-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="62adf-116">如果成本实际值引用时间和材料合同子项，系统将自动为报价单结束和项目合同创建创建相应的未记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="62adf-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="62adf-117">如果成本实际值引用固定价格合同子项，应用程序将根据项目合同客户的拆分计费规则停止重新处理成本实际值。</span><span class="sxs-lookup"><span data-stu-id="62adf-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="62adf-118">作为丢单结束报价单：</span><span class="sxs-lookup"><span data-stu-id="62adf-118">Closing a quote as lost:</span></span>

<span data-ttu-id="62adf-119">将项目报价单作为丢单结束会将状态设置为“已结束”，将状态描述设置为“丢单”。</span><span class="sxs-lookup"><span data-stu-id="62adf-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="62adf-120">结束报价单会使项目报价单成为只读。</span><span class="sxs-lookup"><span data-stu-id="62adf-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="62adf-121">由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。</span><span class="sxs-lookup"><span data-stu-id="62adf-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="62adf-122">如果作为丢单结束的项目报价单在其任意明细上引用了项目，该项目也将标记为“已结束”，那一天之后的所有资源预订都将取消。</span><span class="sxs-lookup"><span data-stu-id="62adf-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="62adf-123">在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。</span><span class="sxs-lookup"><span data-stu-id="62adf-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
