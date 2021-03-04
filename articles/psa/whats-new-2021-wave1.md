---
title: Project Service Automation 2021 年提前访问第 1 波 V3 的新增或变更功能
description: 本主题列出了 Project Service Automation 2021 年提前访问第 1 波 V3 中推出的功能和修补程序。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2021
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
ms.openlocfilehash: 3895f06c6a401f200cf832940ef85eaa8d66fbb2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151152"
---
# <a name="whats-new-or-changed-in-project-service-automation-early-access-wave-1-2021-v3"></a><span data-ttu-id="befc6-103">Project Service Automation 2021 年提前访问第 1 波 V3 的新增或变更功能</span><span class="sxs-lookup"><span data-stu-id="befc6-103">What's new or changed in Project Service Automation Early Access Wave 1 2021, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

## <a name="project-service-automation-early-access-wave-1-2021-v3"></a><span data-ttu-id="befc6-104">Project Service Automation 2021 年提前访问第 1 波 V3</span><span class="sxs-lookup"><span data-stu-id="befc6-104">Project Service Automation Early Access Wave 1 2021, V3</span></span>

<span data-ttu-id="befc6-105">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="befc6-105">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="befc6-106">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="befc6-106">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="befc6-107">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="befc6-107">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="befc6-108">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="befc6-108">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="befc6-109">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="befc6-109">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="befc6-110">本主题列出了 Project Service Automation V3 2021 年提前访问第 1 波中新增或变更的功能和修补程序。</span><span class="sxs-lookup"><span data-stu-id="befc6-110">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Early Access Wave 1 2021.</span></span> <span data-ttu-id="befc6-111">此版本的内部版本号为 V3.10.49.3，通过 2021 年 2 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="befc6-111">This version has a build number of V3.10.49.3 and is generally available through a self-update in February 2021.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="befc6-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="befc6-112">Bug fixes</span></span>

<span data-ttu-id="befc6-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="befc6-113">**Time and Expense**</span></span>

<span data-ttu-id="befc6-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="befc6-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="befc6-115">如果持续时间为空，在创建时间条目时将自动填充结束日期。</span><span class="sxs-lookup"><span data-stu-id="befc6-115">End dates auto-populate when a time entry is created if the duration is null.</span></span>
- <span data-ttu-id="befc6-116">用户可以更改已批准或已提交的时间条目中的任务。</span><span class="sxs-lookup"><span data-stu-id="befc6-116">Users can change the task on a time entry that has been approved or submitted.</span></span>
