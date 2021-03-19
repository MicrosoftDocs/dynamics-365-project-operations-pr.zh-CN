---
title: Project Service Automation V3 更新版本 28 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 28 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280207"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="83945-103">Project Service Automation V3 更新版本 28 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="83945-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="83945-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="83945-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="83945-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="83945-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="83945-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="83945-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="83945-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="83945-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="83945-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="83945-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="83945-109">此主题列出了作为 Project Service Automation V3 更新版 28 的新增或更改功能的功能或修补程序。此版本的版本号为 V3.10.46.32，通过 2021 年 1 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="83945-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="83945-110">更新发布 28</span><span class="sxs-lookup"><span data-stu-id="83945-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="83945-111">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="83945-111">Bug fixes</span></span>

<span data-ttu-id="83945-112">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="83945-112">**Time and Expense**</span></span>

<span data-ttu-id="83945-113">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="83945-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="83945-114">用户可以使用 **批量编辑** 来更新已批准和提交的时间条目。</span><span class="sxs-lookup"><span data-stu-id="83945-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="83945-115">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="83945-115">**Project Management**</span></span>

<span data-ttu-id="83945-116">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="83945-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="83945-117">在将任务 GUID 解释为数字的情况下，无法使用 **工作分解结构** 页上功能区中的 **编辑任务** 打开任务进行编辑。</span><span class="sxs-lookup"><span data-stu-id="83945-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="83945-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="83945-118">**Sales**</span></span>

<span data-ttu-id="83945-119">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="83945-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="83945-120">调用 **GetEstimatesForProject** 插件时，生成 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="83945-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="83945-121">除了已更新的 **InvoiceStatus** 属性外，里程碑网格上的 **标记为已准备好开票** 仅部分更新了属性。</span><span class="sxs-lookup"><span data-stu-id="83945-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]