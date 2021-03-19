---
title: “升级”主页
description: 此主题介绍何处可以找到有关 Dynamics 365 Project Service Automation 中的新功能和更新功能和用于升级到最新版本的流程的重要信息。
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 838eecb1229ea20106c7d5487dc37a81e8df501b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281692"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="96390-103">“升级”主页</span><span class="sxs-lookup"><span data-stu-id="96390-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="96390-104">从 PSA 版本 2.x 或 1.x 升级到版本 3.x</span><span class="sxs-lookup"><span data-stu-id="96390-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="96390-105">新实例</span><span class="sxs-lookup"><span data-stu-id="96390-105">New instances</span></span>

<span data-ttu-id="96390-106">从 2019 年 5 月 17 日开始，如果在配置新实例期间选择 Project Service Automation，将默认安装版本 3.x。</span><span class="sxs-lookup"><span data-stu-id="96390-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="96390-107">现有实例</span><span class="sxs-lookup"><span data-stu-id="96390-107">Existing instances</span></span>

<span data-ttu-id="96390-108">以前，已有 PSA 版本 2.x 实例，但需要更新到版本 3.x（此版本是基于统一客户端接口 (UCI) 的 PSA 版本）的客户必须联系 Microsoft 支持部门，并提供自己实例的详细信息，支持人员才能让该实例升级到版本 3.x。</span><span class="sxs-lookup"><span data-stu-id="96390-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="96390-109">从 2020 年 3 月 1 日起，有 PSA 版本 2.x 实例并需要升级到版本 3.x 的客户可以直接从管理门户升级其实例，无需联系 Microsoft 支持部门。</span><span class="sxs-lookup"><span data-stu-id="96390-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="96390-110">PSA 版本 3.x 中有一些重大更改。</span><span class="sxs-lookup"><span data-stu-id="96390-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="96390-111">其基于统一接口框架，可帮助提供改进的用户体验。</span><span class="sxs-lookup"><span data-stu-id="96390-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="96390-112">这款经过重新设计的应用程序提供一致、统一的用户界面 (UI)，该界面采用了响应式设计理念，非常适合在任何屏幕尺寸或设备上查看。</span><span class="sxs-lookup"><span data-stu-id="96390-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="96390-113">整个应用程序还有其他一些更改。</span><span class="sxs-lookup"><span data-stu-id="96390-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="96390-114">已更改的一些领域包括定价、预订和分派资源、时间、支出与审批。</span><span class="sxs-lookup"><span data-stu-id="96390-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="96390-115">建议在开始升级流程之前完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="96390-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="96390-116">验证确定的实例中是否已同时安装了 Dynamics 365 Field Service 和 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="96390-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="96390-117">如果已安装了这两个解决方案，应计划在恢复正常使用此解决方案之前升级这两个解决方案。</span><span class="sxs-lookup"><span data-stu-id="96390-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="96390-118">请仔细阅读以下主题。</span><span class="sxs-lookup"><span data-stu-id="96390-118">Carefully review the following topics.</span></span> <span data-ttu-id="96390-119">注意和了解版本之间的变化有助于完成升级流程。</span><span class="sxs-lookup"><span data-stu-id="96390-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="96390-120">这些主题介绍 PSA 中的主要更改，以及计划升级到版本 3.x 之前的注意事项和建议。</span><span class="sxs-lookup"><span data-stu-id="96390-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="96390-121">Project Service Automation 版本 3 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="96390-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="96390-122">升级注意事项 - Project Service Automation 版本 2.x 或 1.x 到版本 3</span><span class="sxs-lookup"><span data-stu-id="96390-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="96390-123">升级生产实例之前，升级沙盒实例，以便评估实施中的更改。</span><span class="sxs-lookup"><span data-stu-id="96390-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="96390-124">阅读前面介绍的主题并准备好升级到 PSA 版本 3.x 或基于 UCI 的版本之后，向 Microsoft 支持提交请求，以便从管理中心获取升级。</span><span class="sxs-lookup"><span data-stu-id="96390-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="96390-125">在请求中提供实例的详细信息。</span><span class="sxs-lookup"><span data-stu-id="96390-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="96390-126">新建实例中的旧 PSA 版本（PSA 版本 2.x）</span><span class="sxs-lookup"><span data-stu-id="96390-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="96390-127">从 2019 年 5 月 17 日开始，所有新实例都采用 UCI 作为默认客户端。</span><span class="sxs-lookup"><span data-stu-id="96390-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="96390-128">为了与此项更改保持一致，将默认设置 PSA 版本 3.x 和 Field Service 版本 8.x，因为这些版本设计为支持 UCI 客户端。</span><span class="sxs-lookup"><span data-stu-id="96390-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="96390-129">从 2020 年 3 月 1 日开始，Dynamics PSA 的客户不能再使用较旧版本的 PSA（例如，PSA 版本 2.x 或更低版本）创建新环境。</span><span class="sxs-lookup"><span data-stu-id="96390-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="96390-130">任何新环境都将仅获取 PSA 版本 3.x。</span><span class="sxs-lookup"><span data-stu-id="96390-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="96390-131">若要在使用 Field Service 和 PSA 应用程序的旧版本时获得最佳体验，请转到 **系统设置** 页，为 **仅使用新的统一接口(推荐)** 字段选择 **否**，因为这些版本未设计为可在 UCI 中正确加载。</span><span class="sxs-lookup"><span data-stu-id="96390-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="96390-132">关闭 UCI 之后，可使用旧 Web 客户端打开和运行这些 Field Service 和 PSA 版本。</span><span class="sxs-lookup"><span data-stu-id="96390-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]