---
title: Project Service Automation V3 更新版本 22 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 22 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150972"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="cf6e8-103">Project Service Automation V3 更新版本 22</span><span class="sxs-lookup"><span data-stu-id="cf6e8-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cf6e8-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cf6e8-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cf6e8-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cf6e8-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cf6e8-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cf6e8-109">本主题列出了 Project Service Automation V3 更新版本 22 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="cf6e8-110">该版本的内部版本号为 V 3.10.33.48，并且在 2020 年 6 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="cf6e8-111">更新发布 22</span><span class="sxs-lookup"><span data-stu-id="cf6e8-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cf6e8-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="cf6e8-112">Bug fixes</span></span>



<span data-ttu-id="cf6e8-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="cf6e8-113">**Time and Expense**</span></span>

<span data-ttu-id="cf6e8-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cf6e8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cf6e8-115">导入后，**时间条目** 不会自动添加到“时间条目”时间表中。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="cf6e8-116">**时间条目** 网格日期选择器无法识别用户的区域设置。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="cf6e8-117">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="cf6e8-117">**Resource Management**</span></span>

<span data-ttu-id="cf6e8-118">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cf6e8-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cf6e8-119">在手动模式下，生成 **资源要求** 时无法识别对 **资源分配** 等值线所做的更改。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="cf6e8-120">**资源请求** 不支持自定义请求状态。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="cf6e8-121">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="cf6e8-121">**Project Management**</span></span>

<span data-ttu-id="cf6e8-122">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cf6e8-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="cf6e8-123">在 EstimateGridControl 上使用双击不会正确分析荷兰格式的数字。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="cf6e8-124">在使用 Microsoft Project 桌面客户端加载项更改分配后，已分派的小时数未正确更新。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="cf6e8-125">当合同货币不同于客户货币并且组织被配置为显示货币代码而非货币符号时，“项目跟踪”和“估计”网格会显示不正确的销售货币代码。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="cf6e8-126">如果工作时间日程安排为每天 24 小时，则团队成员的完成日期将增加一天。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="cf6e8-127">在“项目日程安排”上，将事务类别添加到任务不会触发自动保存。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="cf6e8-128">将团队成员添加到项目模板时显示以下错误：“资源要求不能与项目模板相关联”。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="cf6e8-129">功能区规则脚本“msdyn.Approval.CanApproveOrReject”显示超时错误。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="cf6e8-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cf6e8-130">**Sales**</span></span>

<span data-ttu-id="cf6e8-131">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cf6e8-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="cf6e8-132">在“新建报价单项目价目表”窗体/实体上的“价目表”查找中选择“成本价目表”时，未显示验证错误消息。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="cf6e8-133">如果附加到报价单的 BPF 处于最后阶段，则以“赢单”形式结束报价单时，不会导航到创建的合同。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="cf6e8-134">在撤回时间条目后，用于冲销的 **未记帐销售额** 会链接到原始成本。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="cf6e8-135">选择 **确认** 按钮后，除非刷新发票，否则发票状态不会更改为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="cf6e8-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
