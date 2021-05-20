---
title: Project Service Automation V3 更新版本 14 中的新增功能或更改
description: 本主题介绍 Project Service Automation V3 更新版本 14 中的新增功能。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949357"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="3b85e-103">Project Service Automation V3 更新版本 14</span><span class="sxs-lookup"><span data-stu-id="3b85e-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3b85e-104">我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。</span><span class="sxs-lookup"><span data-stu-id="3b85e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3b85e-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="3b85e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b85e-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="3b85e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b85e-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="3b85e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3b85e-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="3b85e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b85e-109">本主题列出了 PSA V3 更新版本 14 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="3b85e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="3b85e-110">此版本的内部版本号为 V3.10.4.21，并且按以下计划提供：</span><span class="sxs-lookup"><span data-stu-id="3b85e-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="3b85e-111">**公开发布（自行更新）：** 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="3b85e-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="3b85e-112">**自动更新：** 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="3b85e-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="3b85e-113">更新发布 14</span><span class="sxs-lookup"><span data-stu-id="3b85e-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="3b85e-114">增强功能</span><span class="sxs-lookup"><span data-stu-id="3b85e-114">Enhancements</span></span>

- <span data-ttu-id="3b85e-115">Sales</span><span class="sxs-lookup"><span data-stu-id="3b85e-115">Sales</span></span>

     - <span data-ttu-id="3b85e-116">当报价单更新为 **作为赢单结束** 时，**报价单明细详细信息** 中的自定义字段值会复制到 **项目合同子项详细信息** 中。</span><span class="sxs-lookup"><span data-stu-id="3b85e-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="3b85e-117">已确认的项目可以 **作为赢单结束**。</span><span class="sxs-lookup"><span data-stu-id="3b85e-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="3b85e-118">资源管理</span><span class="sxs-lookup"><span data-stu-id="3b85e-118">Resource Management</span></span>

     - <span data-ttu-id="3b85e-119">在扩展预订时，系统将用确认对话框提示用户汇总预订结果并提供指向“维护预订”的链接。</span><span class="sxs-lookup"><span data-stu-id="3b85e-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="3b85e-120">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="3b85e-120">Bug fixes</span></span>

- <span data-ttu-id="3b85e-121">时间和支出</span><span class="sxs-lookup"><span data-stu-id="3b85e-121">Time and Expense</span></span>

     - <span data-ttu-id="3b85e-122">已修复：在用户尚未选择任何要更正的条目的情况下改善了用户体验。</span><span class="sxs-lookup"><span data-stu-id="3b85e-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="3b85e-123">资源管理</span><span class="sxs-lookup"><span data-stu-id="3b85e-123">Resource Management</span></span>

     - <span data-ttu-id="3b85e-124">已修复：多次预订资源会使可预订资源的名称溢出。</span><span class="sxs-lookup"><span data-stu-id="3b85e-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="3b85e-125">Sales</span><span class="sxs-lookup"><span data-stu-id="3b85e-125">Sales</span></span>

     - <span data-ttu-id="3b85e-126">已修复：在用户还输入项目的支出估计成本价之前，不会计算总销售价。</span><span class="sxs-lookup"><span data-stu-id="3b85e-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="3b85e-127">已修复：如果关联的项目合同未处于 **草稿** 状态，则以 **赢得** 形式结束报价单将会失败。</span><span class="sxs-lookup"><span data-stu-id="3b85e-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]