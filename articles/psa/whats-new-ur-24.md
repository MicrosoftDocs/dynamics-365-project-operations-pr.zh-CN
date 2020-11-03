---
title: Project Service Automation V3 更新版本 24 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 24 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072556"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="c240a-103">Project Service Automation V3 更新版本 24</span><span class="sxs-lookup"><span data-stu-id="c240a-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="c240a-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="c240a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c240a-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="c240a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c240a-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="c240a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c240a-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="c240a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c240a-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="c240a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c240a-109">本主题列出了 Project Service Automation V3 更新版本 24 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="c240a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="c240a-110">该版本的内部版本号为 V 3.10.42.43，并且在 2020 年 10 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="c240a-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="c240a-111">更新发布 24</span><span class="sxs-lookup"><span data-stu-id="c240a-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c240a-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="c240a-112">Bug fixes</span></span>

<span data-ttu-id="c240a-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c240a-113">**Sales**</span></span>

<span data-ttu-id="c240a-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="c240a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c240a-115">设置默认产品价目表时出现问题。</span><span class="sxs-lookup"><span data-stu-id="c240a-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="c240a-116">由于嵌入的价目表和角色价格记录副本，报价单赢单的性能很慢。</span><span class="sxs-lookup"><span data-stu-id="c240a-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="c240a-117">**项目合同/销售中心** > **产品明细项目/订单行数量** 将自动舍入到最接近的整数。</span><span class="sxs-lookup"><span data-stu-id="c240a-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="c240a-118">在读取价目表时提升为系统特权。</span><span class="sxs-lookup"><span data-stu-id="c240a-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="c240a-119">将客户地址字段 **address1_freighttermscode** 和 **address1_shippingmethodcode** 复制到报价单/订单。</span><span class="sxs-lookup"><span data-stu-id="c240a-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="c240a-120">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="c240a-120">**Time and Expense**</span></span>

<span data-ttu-id="c240a-121">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="c240a-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="c240a-122">**时间条目网格** 不支持 **仅限日期** 时间行为。</span><span class="sxs-lookup"><span data-stu-id="c240a-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="c240a-123">**时间条目** 不能自动刷新。</span><span class="sxs-lookup"><span data-stu-id="c240a-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="c240a-124">需要手动刷新。</span><span class="sxs-lookup"><span data-stu-id="c240a-124">A manual refresh is required.</span></span>
- <span data-ttu-id="c240a-125">资源的工作中有工间休息时间（0 小时）时，无法从工作导入时间条目。</span><span class="sxs-lookup"><span data-stu-id="c240a-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="c240a-126">创建时间条目时，将开始日期设置为与 **msdyn_date** 相同的值。</span><span class="sxs-lookup"><span data-stu-id="c240a-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="c240a-127">为时间条目重新启用批量编辑。</span><span class="sxs-lookup"><span data-stu-id="c240a-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="c240a-128">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="c240a-128">**Resource Management**</span></span>

<span data-ttu-id="c240a-129">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="c240a-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="c240a-130">尝试在无要求的情况下更新日间预订状态会引发 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="c240a-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="c240a-131">加载 **协调视图** 时出错。</span><span class="sxs-lookup"><span data-stu-id="c240a-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="c240a-132">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="c240a-132">**Project Management**</span></span>

<span data-ttu-id="c240a-133">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="c240a-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="c240a-134">在 **项目计划** 中，从 **手动** 更改为 **自动** 时，无法完成自动保存。</span><span class="sxs-lookup"><span data-stu-id="c240a-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="c240a-135">不应针对 **项目跟踪网格** 上的差异计算支出成本。</span><span class="sxs-lookup"><span data-stu-id="c240a-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="c240a-136">加载期间 **估算标记** 列的行为与更改 **时间分段** 类型的行为不一致。</span><span class="sxs-lookup"><span data-stu-id="c240a-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="c240a-137">项目中的实际成本无法反映 **实际值** 中的总计。</span><span class="sxs-lookup"><span data-stu-id="c240a-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="c240a-138">**摘要** 选项卡上的 **估计完成日期** 与 **WBS 计划** 不匹配。</span><span class="sxs-lookup"><span data-stu-id="c240a-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="c240a-139">升级中的 **更新实际时数** 不能正常工作。</span><span class="sxs-lookup"><span data-stu-id="c240a-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="c240a-140">根 **BU** 之外的项目经理无法创建项目。</span><span class="sxs-lookup"><span data-stu-id="c240a-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="c240a-141">对 **支出估算** 中的任务或类别的更改不会保留。</span><span class="sxs-lookup"><span data-stu-id="c240a-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="c240a-142">**合同副本** 复制发票计划和运行状态。</span><span class="sxs-lookup"><span data-stu-id="c240a-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="c240a-143">**刷新实际值** 按钮无法正确计算摘要任务。</span><span class="sxs-lookup"><span data-stu-id="c240a-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="c240a-144">Microsoft Project 加载项：如果有任何团队成员具有空资源单位，则修复 null 引用错误。</span><span class="sxs-lookup"><span data-stu-id="c240a-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

