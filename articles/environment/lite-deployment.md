---
title: 部署 Project Operations - 精简
description: 此主题提供有关如何安装“Project Operations 精简部署 - 估价交易开票”的信息。
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995520"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="e0268-103">部署 Project Operations - 精简</span><span class="sxs-lookup"><span data-stu-id="e0268-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="e0268-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="e0268-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e0268-105">Project Operations 支持多个部署模型。</span><span class="sxs-lookup"><span data-stu-id="e0268-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="e0268-106">若要确定最佳部署模型，请参阅[部署类型](determine-deployment-type.md)。</span><span class="sxs-lookup"><span data-stu-id="e0268-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="e0268-107">此部署（精简部署 – 估价交易开票）引发 **Common Data Service - 仅 Project Operations 部署**。</span><span class="sxs-lookup"><span data-stu-id="e0268-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="e0268-108">将 Project Operations 安装到新的 CDS 环境中</span><span class="sxs-lookup"><span data-stu-id="e0268-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="e0268-109">安装到现有 CD 环境中</span><span class="sxs-lookup"><span data-stu-id="e0268-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="e0268-110">将 Project Operations 安装到新的 CDS 环境中</span><span class="sxs-lookup"><span data-stu-id="e0268-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="e0268-111">作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)创建一个新的 CDS 环境。</span><span class="sxs-lookup"><span data-stu-id="e0268-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="e0268-112">确保 **CDS 数据库** 和 **Dynamics 365 应用** 已启用。</span><span class="sxs-lookup"><span data-stu-id="e0268-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="e0268-113">已启用，请参阅[在 Power Platform 管理中心创建和管理环境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。</span><span class="sxs-lookup"><span data-stu-id="e0268-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="e0268-114">从 Dynamics 365 应用的部署列表中选择 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="e0268-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="e0268-115">将 Project Operations 安装到现有 CDS 环境中</span><span class="sxs-lookup"><span data-stu-id="e0268-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="e0268-116">作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)中找到要安装 Project Operations 的环境。</span><span class="sxs-lookup"><span data-stu-id="e0268-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="e0268-117">安装 Dynamics 365 应用的部署列表中的 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="e0268-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="e0268-118">有关详细信息，请参阅[管理 Dynamics 365 应用](/power-platform/admin/manage-apps)。</span><span class="sxs-lookup"><span data-stu-id="e0268-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]