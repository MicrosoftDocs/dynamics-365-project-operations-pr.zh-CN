---
title: 提交资源请求
description: 可将生成的资源要求作为资源请求提交。 然后将请求发给资源经理处理。
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279127"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="e5e7f-104">提交资源请求</span><span class="sxs-lookup"><span data-stu-id="e5e7f-104">Submit a resource request</span></span>

<span data-ttu-id="e5e7f-105">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="e5e7f-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5e7f-106">可将生成的资源要求作为资源请求提交。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e5e7f-107">然后将请求发给资源经理处理。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e5e7f-108">在 Dynamics 365 Project Operations 的 **项目** 页中，选择 **团队** 选项卡查看可预订资源列表。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="e5e7f-109">从列表中选择具有资源要求的通用资源，然后单击 **提交请求**。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="e5e7f-110">通用团队成员的请求状态将更改为 **已提交**。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e5e7f-111">处理请求之后，如果资源经理通过预订指定资源处理请求，通用资源将替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="e5e7f-112">否则，如果资源经理建议指定资源，通用资源将留在团队中，请求状态将更改为 **需要审阅**。</span><span class="sxs-lookup"><span data-stu-id="e5e7f-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]