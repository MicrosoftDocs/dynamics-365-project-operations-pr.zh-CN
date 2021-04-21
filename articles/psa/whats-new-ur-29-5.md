---
title: Project Service Automation 更新版本 29.5 修补程序 V3 中的新增功能或更改
description: 本主题列出了 Project Service Automation 更新版本 29.5 修补程序 V3 中推出的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715647"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="5389e-103">Project Service Automation V3 更新版本 29.5 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="5389e-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="5389e-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="5389e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5389e-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="5389e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5389e-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="5389e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5389e-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="5389e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5389e-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="5389e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5389e-109">本主题列出了 Project Service Automation V3 更新版本 29.5 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="5389e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="5389e-110">该版本的内部版本号为 V3.10.47.150，并且在 2021 年 1 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="5389e-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="5389e-111">更新发布 29.5</span><span class="sxs-lookup"><span data-stu-id="5389e-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5389e-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="5389e-112">Bug fixes</span></span>


<span data-ttu-id="5389e-113">**销售**</span><span class="sxs-lookup"><span data-stu-id="5389e-113">**Sales**</span></span>

<span data-ttu-id="5389e-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="5389e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="5389e-115">当以赢单形式结束报价单并且该报价单没有价目表时，**ContractLineMapHelper.UpdateContractLineDetailPriceListReference** 中存在可能为 null 的引用异常。</span><span class="sxs-lookup"><span data-stu-id="5389e-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
