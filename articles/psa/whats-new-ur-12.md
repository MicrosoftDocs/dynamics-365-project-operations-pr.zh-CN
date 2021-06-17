---
title: Project Service Automation V3 更新版本 12 中的新增功能或更改
description: 本主题介绍 Project Service Automation V3 更新版本 12 中的新增功能。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f29eaf7c471104ad3e319d8f4e1cbc70e44fc1ca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000335"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="7d19a-103">Project Service Automation V3 更新版本 12</span><span class="sxs-lookup"><span data-stu-id="7d19a-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7d19a-104">我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。</span><span class="sxs-lookup"><span data-stu-id="7d19a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="7d19a-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="7d19a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7d19a-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="7d19a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7d19a-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="7d19a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="7d19a-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="7d19a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7d19a-109">本主题列出了 Project Service Automation V3 更新版本 12 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="7d19a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="7d19a-110">该版本的内部版本号为 V3.10.2.34，并且在 2019 年 10 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="7d19a-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="7d19a-111">更新发布 12</span><span class="sxs-lookup"><span data-stu-id="7d19a-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7d19a-112">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="7d19a-112">Bug fixes</span></span>

- <span data-ttu-id="7d19a-113">时间和支出</span><span class="sxs-lookup"><span data-stu-id="7d19a-113">Time and Expense</span></span>

    - <span data-ttu-id="7d19a-114">已修复：已使用更相关的上下文更新了时间条目错误消息。</span><span class="sxs-lookup"><span data-stu-id="7d19a-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="7d19a-115">已修复：时间条目网格和计划在必要时会正确显示垂直滚动条。</span><span class="sxs-lookup"><span data-stu-id="7d19a-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="7d19a-116">已修复：可以批准提交的支出和时间条目。</span><span class="sxs-lookup"><span data-stu-id="7d19a-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="7d19a-117">已修复：“取消审批确认”对话框消息已更正，以在将 **已批准** 更改为 **已提交** 后反映审批状态。</span><span class="sxs-lookup"><span data-stu-id="7d19a-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="7d19a-118">已修复：在批准支出记录后，**价格**、**单位** 和 **数量** 字段现在在支出记录上已被锁定。</span><span class="sxs-lookup"><span data-stu-id="7d19a-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="7d19a-119">项目管理</span><span class="sxs-lookup"><span data-stu-id="7d19a-119">Project Management</span></span>

    - <span data-ttu-id="7d19a-120">已修复：已删除针对 **团队成员** 主窗体的 **新** 操作。</span><span class="sxs-lookup"><span data-stu-id="7d19a-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="7d19a-121">已修复：已更新资源分派以解决导致任务结束日期发生变化的不准确舍入错误。</span><span class="sxs-lookup"><span data-stu-id="7d19a-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="7d19a-122">已修复：在任务网格中，将向用户呈现相关的服务器端错误。</span><span class="sxs-lookup"><span data-stu-id="7d19a-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="7d19a-123">已修复：团队成员的名称现在呈现在任务人员选取器中，而不是呈现在职位名称中。</span><span class="sxs-lookup"><span data-stu-id="7d19a-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="7d19a-124">资源管理</span><span class="sxs-lookup"><span data-stu-id="7d19a-124">Resource Management</span></span>

    - <span data-ttu-id="7d19a-125">已修复：根据模板创建的项目的资源要求详细信息现在使用项目日历。</span><span class="sxs-lookup"><span data-stu-id="7d19a-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="7d19a-126">已修复：技能和资格现在从角色主数据默认为针对该角色创建的资源要求。</span><span class="sxs-lookup"><span data-stu-id="7d19a-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="7d19a-127">Sales</span><span class="sxs-lookup"><span data-stu-id="7d19a-127">Sales</span></span>

    - <span data-ttu-id="7d19a-128">已修复：在 **合同主** 窗体中发现重复的对象 ID。</span><span class="sxs-lookup"><span data-stu-id="7d19a-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="7d19a-129">已修复：已更新逻辑以使 **报价单分析** 选项卡可见，以便显示该选项卡的元数据设置。</span><span class="sxs-lookup"><span data-stu-id="7d19a-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="7d19a-130">已修复：实际记录上的会计日期现在来自时间/支出条目日期，而不是审批日期。</span><span class="sxs-lookup"><span data-stu-id="7d19a-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]