---
title: 提交资源请求
description: 可将生成的资源要求作为资源请求提交。 然后将请求发给资源经理处理。
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961686"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="536d8-104">提交资源请求</span><span class="sxs-lookup"><span data-stu-id="536d8-104">Submit a resource request</span></span>

<span data-ttu-id="536d8-105">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="536d8-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="536d8-106">可将生成的资源要求作为资源请求提交。</span><span class="sxs-lookup"><span data-stu-id="536d8-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="536d8-107">然后将请求发给资源经理处理。</span><span class="sxs-lookup"><span data-stu-id="536d8-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="536d8-108">在 Dynamics 365 Project Operations 的**项目**页中，选择**团队**选项卡查看可预订资源列表。</span><span class="sxs-lookup"><span data-stu-id="536d8-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="536d8-109">从列表中选择具有资源要求的通用资源，然后单击**提交请求**。</span><span class="sxs-lookup"><span data-stu-id="536d8-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="536d8-110">通用团队成员的请求状态将更改为**已提交**。</span><span class="sxs-lookup"><span data-stu-id="536d8-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="536d8-111">处理请求之后，如果资源经理通过预订指定资源处理请求，通用资源将替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="536d8-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="536d8-112">否则，如果资源经理建议指定资源，通用资源将留在团队中，请求状态将更改为**需要审阅**。</span><span class="sxs-lookup"><span data-stu-id="536d8-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
