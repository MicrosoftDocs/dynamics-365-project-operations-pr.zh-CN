---
title: Project Service Automation V3 更新版本 30 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 30 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852833"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="bf6bb-103">Project Service Automation V3 更新版本 30 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="bf6bb-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bf6bb-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bf6bb-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bf6bb-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bf6bb-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bf6bb-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bf6bb-109">本主题列出了 Project Service Automation V3 更新版本 30 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="bf6bb-110">此版本的内部版本号为 V3.10.51.61，通常可通过 2021 年 4 月的自我更新获得。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="bf6bb-111">更新发布 30</span><span class="sxs-lookup"><span data-stu-id="bf6bb-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bf6bb-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="bf6bb-112">Bug fixes</span></span>

<span data-ttu-id="bf6bb-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="bf6bb-113">**Time and Expense**</span></span>

<span data-ttu-id="bf6bb-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="bf6bb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bf6bb-115">如果删除了 **角色** 字段，则在 **快速创建** 页上创建和保存时间条目时将出错。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="bf6bb-116">“时间条目”筛选器应用了错误的筛选器运算符。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="bf6bb-117">在时间条目控件中选择 **复制周** 时，不会自动显示复制的时间表。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="bf6bb-118">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="bf6bb-118">**Resource Management**</span></span>

<span data-ttu-id="bf6bb-119">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="bf6bb-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="bf6bb-120">在扩展预订时，分派给硬预订的预订状态不正确。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="bf6bb-121">扩展预订操作会考虑预订设置元数据中定义为 **已提交** 的预订状态。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="bf6bb-122">如果未指定有效的预订状态，则不会正确本地化错误消息。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="bf6bb-123">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="bf6bb-123">**Project Management**</span></span>

<span data-ttu-id="bf6bb-124">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="bf6bb-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="bf6bb-125">项目不能用一种货币来创建，但却包含另一种货币的相关任务。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="bf6bb-126">**销售**</span><span class="sxs-lookup"><span data-stu-id="bf6bb-126">**Sales**</span></span>

<span data-ttu-id="bf6bb-127">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="bf6bb-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="bf6bb-128">复制价目表时，不会更新价格。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="bf6bb-129">当成本明细具有来源值时，以赢单形式结束报价单将失败。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="bf6bb-130">在 **项目任务** 实体中，**估计成本** 已重命名为 **计划成本(基础货币)**。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="bf6bb-131">创建或删除发票时会生成 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="bf6bb-131">A null reference exception is generated when invoices are created or deleted.</span></span>
