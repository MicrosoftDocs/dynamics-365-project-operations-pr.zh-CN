---
title: 软预订要求
description: 本主题提供有关如何软预订要求的信息。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147372"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="8a886-103">软预订要求</span><span class="sxs-lookup"><span data-stu-id="8a886-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8a886-104">资源要求可以是硬预订的。</span><span class="sxs-lookup"><span data-stu-id="8a886-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="8a886-105">硬预订会创建占用资源产能的建议。</span><span class="sxs-lookup"><span data-stu-id="8a886-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="8a886-106">然后会将该建议发回给请求者进行审批。</span><span class="sxs-lookup"><span data-stu-id="8a886-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="8a886-107">软预订将资源暂时添加到项目团队，并且在日程安排板中具有不同状态，但是不会占用该资源的产能。</span><span class="sxs-lookup"><span data-stu-id="8a886-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="8a886-108">若要从日程安排板软预订资源，请将 **预订状态** 字段设置为 **软性**。</span><span class="sxs-lookup"><span data-stu-id="8a886-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![预订状态设置为“软性”](media/Resource-Management-image77.png)

<span data-ttu-id="8a886-110">当 **团队** 选项卡位于 **指定的团队成员** 视图中时，将在此处显示该资源。</span><span class="sxs-lookup"><span data-stu-id="8a886-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="8a886-111">将在 **软预订工时数** 列中显示软预订的工时数。</span><span class="sxs-lookup"><span data-stu-id="8a886-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![“指定的团队成员”视图中的“软预订工时数”](media/Resource-Management-image78.png)

<span data-ttu-id="8a886-113">软预订的团队成员可以分派给任务。</span><span class="sxs-lookup"><span data-stu-id="8a886-113">Soft-booked team members can be assigned to tasks.</span></span>

![软预订的团队成员已分派给任务](media/Resource-Management-image79.png)

<span data-ttu-id="8a886-115">在 **协调** 选项卡上，不显示软预订资源的预订，因为 **协调** 选项卡仅考虑硬预订。</span><span class="sxs-lookup"><span data-stu-id="8a886-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![“协调”选项卡上无预订的软预订资源](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="8a886-117">不能从基于通用团队成员生成的要求软预订资源。</span><span class="sxs-lookup"><span data-stu-id="8a886-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="8a886-118">在日程安排板中，将为资源的软预订使用其他颜色。</span><span class="sxs-lookup"><span data-stu-id="8a886-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![日程安排板中的软预订](media/Resource-Management-image81.png)

<span data-ttu-id="8a886-120">若要将软预订转换为硬预订，请在日程安排板中右键单击软预订，然后选择 **更改状态** \> **硬预订** \> **硬性**。</span><span class="sxs-lookup"><span data-stu-id="8a886-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![将预订状态更改为“硬性”](media/Resource-Management-image82.png)

<span data-ttu-id="8a886-122">将更改预订，并且更改日程安排板中的状态。</span><span class="sxs-lookup"><span data-stu-id="8a886-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="8a886-123">因为预订状态现在为 **硬性**，所以资源显示为已预订，并且已调整了其产能和可用性。</span><span class="sxs-lookup"><span data-stu-id="8a886-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="8a886-124">可使用相同的方法从日程安排板取消硬预订或软预订。</span><span class="sxs-lookup"><span data-stu-id="8a886-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="8a886-125">若要在项目的 **团队** 选项卡上将软预订资源转换为硬预订，请选择该资源，然后选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="8a886-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![确认命令](media/Resource-Management-image83.png)
