---
title: Project Service Automation V3 更新版本 31 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 31 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945524"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="2d20c-103">Project Service Automation V3 更新版本 31 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="2d20c-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2d20c-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="2d20c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2d20c-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="2d20c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2d20c-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="2d20c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2d20c-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="2d20c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2d20c-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="2d20c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2d20c-109">本主题列出了 Project Service Automation V3 更新版本 31 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="2d20c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="2d20c-110">此版本的内部版本号为 V3.10.52.77，通过 2021 年 5 月的自我更新正式发布。</span><span class="sxs-lookup"><span data-stu-id="2d20c-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="2d20c-111">更新发布 31</span><span class="sxs-lookup"><span data-stu-id="2d20c-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2d20c-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="2d20c-112">Bug fixes</span></span>

<span data-ttu-id="2d20c-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="2d20c-113">**Time and Expense**</span></span>

<span data-ttu-id="2d20c-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="2d20c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d20c-115">**可预订资源** 页上的时间条目控件命令按钮令人迷惑。</span><span class="sxs-lookup"><span data-stu-id="2d20c-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="2d20c-116">审批时间条目时，**Project.SetTrackingFields** 中生成了 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="2d20c-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="2d20c-117">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="2d20c-117">**Resource Management**</span></span>

<span data-ttu-id="2d20c-118">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="2d20c-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d20c-119">**创建团队成员** 未正确显示 **默认预订已提交状态** 的预订设置元数据设置。</span><span class="sxs-lookup"><span data-stu-id="2d20c-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="2d20c-120">从 PSA 1.X 升级到 3.X 时，升级流程在 **UpgradeResourceRequirements** 处失败。</span><span class="sxs-lookup"><span data-stu-id="2d20c-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="2d20c-121">**销售**</span><span class="sxs-lookup"><span data-stu-id="2d20c-121">**Sales**</span></span>

<span data-ttu-id="2d20c-122">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="2d20c-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d20c-123">实际收入将金额转换为跟踪网格中的项目货币。</span><span class="sxs-lookup"><span data-stu-id="2d20c-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="2d20c-124">在组织的基础货币与项目货币不同的情况下创建日记帐行、报价单明细和合同子项时，货币默认值不清楚。</span><span class="sxs-lookup"><span data-stu-id="2d20c-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="2d20c-125">**挂起的更正日记帐验证** 查询未按项目筛选。</span><span class="sxs-lookup"><span data-stu-id="2d20c-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="2d20c-126">剩余销售额在项目上的计算不正确。</span><span class="sxs-lookup"><span data-stu-id="2d20c-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="2d20c-127">基于联系人的报价单在创建时如果没有价目表将失败。</span><span class="sxs-lookup"><span data-stu-id="2d20c-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="2d20c-128">处理微调框在您选择 **确认发票** 时未显示。</span><span class="sxs-lookup"><span data-stu-id="2d20c-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="2d20c-129">处理微调框在您选择 **创建发票** 时未显示。</span><span class="sxs-lookup"><span data-stu-id="2d20c-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="2d20c-130">作为丢单结束报价单时未取消预订。</span><span class="sxs-lookup"><span data-stu-id="2d20c-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







