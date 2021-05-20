---
title: Project Service Automation V3 更新版本 19 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 19 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949128"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="39205-103">Project Service Automation V3 更新版本 19</span><span class="sxs-lookup"><span data-stu-id="39205-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="39205-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="39205-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="39205-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="39205-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="39205-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="39205-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="39205-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="39205-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="39205-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="39205-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="39205-109">本主题列出了 PSA V3 更新版本 19 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="39205-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="39205-110">该版本的内部版本号为 V3.10.30.41，并且在 2020 年 5 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="39205-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="39205-111">更新发布 19</span><span class="sxs-lookup"><span data-stu-id="39205-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="39205-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="39205-112">Bug fixes</span></span>

<span data-ttu-id="39205-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="39205-113">**Time and Expense**</span></span>

<span data-ttu-id="39205-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="39205-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="39205-115">不能正确显示导入时间条目产生的错误。</span><span class="sxs-lookup"><span data-stu-id="39205-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="39205-116">“时间条目”网格不支持 **仅限日期** 字段行为。</span><span class="sxs-lookup"><span data-stu-id="39205-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="39205-117">项目资源无法为项目创建支出。</span><span class="sxs-lookup"><span data-stu-id="39205-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="39205-118">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="39205-118">**Project Management**</span></span>

<span data-ttu-id="39205-119">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="39205-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="39205-120">在完成 (EAC) 计算期间孙任务导致工作量估算不正确。</span><span class="sxs-lookup"><span data-stu-id="39205-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="39205-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="39205-121">**Sales**</span></span>

<span data-ttu-id="39205-122">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="39205-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="39205-123">**重新计算** 操作不支持支出合同子项详细信息或报价单明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="39205-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="39205-124">费用估算缺少 **更新价格**。</span><span class="sxs-lookup"><span data-stu-id="39205-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="39205-125">客户无法从 **项目合同** 页面选择自定义合同状态描述。</span><span class="sxs-lookup"><span data-stu-id="39205-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="39205-126">客户在通过报价单创建自定义价目表时遇到了性能下降。</span><span class="sxs-lookup"><span data-stu-id="39205-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="39205-127">客户遇到了 **报价单明细详细信息** 与 **合同子项详细信息** 页中 **计价单位** 默认值不一致。</span><span class="sxs-lookup"><span data-stu-id="39205-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="39205-128">向应计费合同子项添加非应计费交易类别项不采用交易类别的 **非应计费** 记帐类型。</span><span class="sxs-lookup"><span data-stu-id="39205-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="39205-129">客户在以前创建的合同中不能使用新添加的角色和类别。</span><span class="sxs-lookup"><span data-stu-id="39205-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="39205-130">客户在 PreValidateProjectTeamMemberUpdate.cs 中进行不必要的检索时遇到性能下降</span><span class="sxs-lookup"><span data-stu-id="39205-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="39205-131">不应将 **资源类别** 列表中设置为不应计费的角色作为项目合同子项中的 **不应计费** 添加到 **应计费角色** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="39205-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="39205-132">客户在创建项目时可能遇到性能下降，因为 **GetBookableResourceIdFromUser** 检索所有可预订资源列，而不是仅检索主 ID。</span><span class="sxs-lookup"><span data-stu-id="39205-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="39205-133">**TransactionType** 实体缺少用于防止输入对交易类型无效的 **计价单位** 和 **计价单位组** 的前期验证更新插件。</span><span class="sxs-lookup"><span data-stu-id="39205-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="39205-134">**删除** 步骤在导入时间条目时无效。</span><span class="sxs-lookup"><span data-stu-id="39205-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]