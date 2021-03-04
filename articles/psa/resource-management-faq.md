---
title: 资源管理常见问题
description: 此主题提供资源管理常见问题的解答。
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144357"
---
# <a name="resource-management-faq"></a><span data-ttu-id="7de6e-103">资源管理常见问题</span><span class="sxs-lookup"><span data-stu-id="7de6e-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="7de6e-104">团队成员与资源要求之间有何区别？</span><span class="sxs-lookup"><span data-stu-id="7de6e-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="7de6e-105">项目团队成员可以分派给任务，预订或超额预订，以及设置为审批者。</span><span class="sxs-lookup"><span data-stu-id="7de6e-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="7de6e-106">资源要求不能作为需求的草稿说明独立于项目团队成员存在。</span><span class="sxs-lookup"><span data-stu-id="7de6e-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="7de6e-107">建议工时与软预订工时之间有何区别？</span><span class="sxs-lookup"><span data-stu-id="7de6e-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="7de6e-108">建议工时和软预订工时在可视化方面不同。</span><span class="sxs-lookup"><span data-stu-id="7de6e-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="7de6e-109">建议工时仅对资源经理和使用资源请求发起需求的项目经理显示。</span><span class="sxs-lookup"><span data-stu-id="7de6e-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="7de6e-110">软预订工时对可访问日程安排板的任何人显示。</span><span class="sxs-lookup"><span data-stu-id="7de6e-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="7de6e-111">如何查看为项目软预订的资源工时？</span><span class="sxs-lookup"><span data-stu-id="7de6e-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="7de6e-112">当您预订资源要求时，可进行软预订。</span><span class="sxs-lookup"><span data-stu-id="7de6e-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="7de6e-113">为项目团队软预订的资源显示为具有软预订工时的团队成员。</span><span class="sxs-lookup"><span data-stu-id="7de6e-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="7de6e-114">也在日程安排板中显示。</span><span class="sxs-lookup"><span data-stu-id="7de6e-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="7de6e-115">如何更改我预订的资源（通用资源或指定资源）的所需工时和开始日期与结束日期？</span><span class="sxs-lookup"><span data-stu-id="7de6e-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="7de6e-116">预订资源之后，选择 **维护预订** 以进行所需任何更改。</span><span class="sxs-lookup"><span data-stu-id="7de6e-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="7de6e-117">Project Service Automation 支持哪些资源类型？</span><span class="sxs-lookup"><span data-stu-id="7de6e-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="7de6e-118">Dynamics 365 Project Service Automation 中仅支持 **用户** 和 **联系人** 资源类型。</span><span class="sxs-lookup"><span data-stu-id="7de6e-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="7de6e-119">虽然可以创建其他类型的资源（例如，**设备** 和 **组**），但是它们不支持端到端用例。</span><span class="sxs-lookup"><span data-stu-id="7de6e-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="7de6e-120">分派与预订之间有何区别？</span><span class="sxs-lookup"><span data-stu-id="7de6e-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="7de6e-121">分派是将资源分派给项目计划中的项目任务。</span><span class="sxs-lookup"><span data-stu-id="7de6e-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7de6e-122">资源可以是实际资源，也可以是通用资源。</span><span class="sxs-lookup"><span data-stu-id="7de6e-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="7de6e-123">预订是将资源硬性或软性分配给项目。</span><span class="sxs-lookup"><span data-stu-id="7de6e-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7de6e-124">硬预订占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="7de6e-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7de6e-125">理想情况下，实际资源、预订和分派应一致，因为它们没有区别。</span><span class="sxs-lookup"><span data-stu-id="7de6e-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="7de6e-126">但是，PSA 不强制执行此共识。</span><span class="sxs-lookup"><span data-stu-id="7de6e-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="7de6e-127">“协调”视图为项目经理显示资源的预订和分派不一致的位置。</span><span class="sxs-lookup"><span data-stu-id="7de6e-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
