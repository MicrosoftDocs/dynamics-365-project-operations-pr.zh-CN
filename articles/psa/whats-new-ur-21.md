---
title: Project Service Automation V3 更新版本 21 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 21 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072555"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="57354-103">Project Service Automation V3 更新版本 21</span><span class="sxs-lookup"><span data-stu-id="57354-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="57354-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="57354-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="57354-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="57354-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="57354-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="57354-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="57354-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="57354-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="57354-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="57354-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="57354-109">本主题列出了 Project Service Automation V3 更新版本 21 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="57354-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="57354-110">该版本的内部版本号为 V 3.10.32.50，并且在 2020 年 6 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="57354-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="57354-111">更新发布 21</span><span class="sxs-lookup"><span data-stu-id="57354-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="57354-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="57354-112">Bug fixes</span></span>

<span data-ttu-id="57354-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="57354-113">**Time and Expense**</span></span>

<span data-ttu-id="57354-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="57354-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="57354-115">在仪表板中托管 **时间条目网格控件** 时，网格不会利用仪表板网格容器的整个宽度。</span><span class="sxs-lookup"><span data-stu-id="57354-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="57354-116">对于特定时区， **时间条目** 网格控件不会显示记录。</span><span class="sxs-lookup"><span data-stu-id="57354-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="57354-117">晚上 9:00 之后的时间条目会在错误的日期出现。</span><span class="sxs-lookup"><span data-stu-id="57354-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="57354-118">如果 **需要支出收据** 支出类别没有值，用户将无法提交支出。</span><span class="sxs-lookup"><span data-stu-id="57354-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="57354-119">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="57354-119">**Resource Management**</span></span>

<span data-ttu-id="57354-120">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="57354-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="57354-121">**对帐** 视图中显示了停用的预订。</span><span class="sxs-lookup"><span data-stu-id="57354-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="57354-122">常规资源履行缺少验证，无法确保存在有效的预订状态。</span><span class="sxs-lookup"><span data-stu-id="57354-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="57354-123">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="57354-123">**Project Management**</span></span>

<span data-ttu-id="57354-124">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="57354-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="57354-125">即使项目不是活动状态， **项目** 窗体网格（ **资源分配** 、 **任务** 、 **对帐** 视图、 **支出估算** ）仍可编辑。</span><span class="sxs-lookup"><span data-stu-id="57354-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="57354-126">重复的客户无法与链接到已确认的项目合同的客户进行合并。</span><span class="sxs-lookup"><span data-stu-id="57354-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="57354-127">如果添加的资源无有效日历，则系统不会返回用户友好消息。</span><span class="sxs-lookup"><span data-stu-id="57354-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="57354-128">当项目链接到 **Microsoft Project 加载项** 后，会启用任务网格上的 **添加任务** 按钮。</span><span class="sxs-lookup"><span data-stu-id="57354-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="57354-129">将某种类别的任务分配给资源并且为资源角色定义了成本价时，工作量将失控增长。</span><span class="sxs-lookup"><span data-stu-id="57354-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="57354-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="57354-130">**Sales**</span></span>

<span data-ttu-id="57354-131">我们进行了以下增强：</span><span class="sxs-lookup"><span data-stu-id="57354-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="57354-132">已将 **发票频率** 和 **记帐开始时间** 移至 **发票计划** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="57354-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="57354-133">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="57354-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="57354-134">即使 **角色** 的总销售价不为零， **类别** 的 **总销售价** 也会为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="57354-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="57354-135">当另一个自定义流程正在更新其他字段时，客户无法将 **发票状态** 字段的值更改为 **准备好开发票** 。</span><span class="sxs-lookup"><span data-stu-id="57354-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="57354-136">如果重复选择 **刷新发票行** 按钮，则会创建多个重复行。</span><span class="sxs-lookup"><span data-stu-id="57354-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="57354-137">**更新价格** 按钮不适用于 **快速视图** 窗体中的 **角色价格** 子网格。</span><span class="sxs-lookup"><span data-stu-id="57354-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="57354-138">**销售价目表解析** 逻辑未正确处理时区，从而导致价目表选择错误。</span><span class="sxs-lookup"><span data-stu-id="57354-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="57354-139">批准单个时间条目后，项目的 **实际总费用** 可能会减少一部分。</span><span class="sxs-lookup"><span data-stu-id="57354-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="57354-140">如果 **检索的角色价格** 在 **基本计价单位** 和 **以基本计价单位表示的价格** 字段中没有值，则 **价格解析** 逻辑不会提供用户友好的错误消息。</span><span class="sxs-lookup"><span data-stu-id="57354-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
