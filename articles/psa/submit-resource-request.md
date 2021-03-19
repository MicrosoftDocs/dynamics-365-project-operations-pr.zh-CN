---
title: 提交资源请求
description: 此主题介绍如何提交针对项目资源的请求。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282232"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="78d4d-103">提交资源请求</span><span class="sxs-lookup"><span data-stu-id="78d4d-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78d4d-104">可将生成的资源要求作为资源请求提交。</span><span class="sxs-lookup"><span data-stu-id="78d4d-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="78d4d-105">然后将请求发给资源经理处理。</span><span class="sxs-lookup"><span data-stu-id="78d4d-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="78d4d-106">在 Project Service Automation (PSA) 的 **项目** 页中，单击 **团队** 选项卡查看可预订资源列表。</span><span class="sxs-lookup"><span data-stu-id="78d4d-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="78d4d-107">从列表中选择具有资源要求的通用资源，然后单击 **提交请求**。</span><span class="sxs-lookup"><span data-stu-id="78d4d-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![提交资源请求](media/RM-how-to-18.png)

<span data-ttu-id="78d4d-109">通用团队成员的请求状态将更改为 **已提交**。</span><span class="sxs-lookup"><span data-stu-id="78d4d-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="78d4d-110">资源经理处理请求之后，如果资源经理使用指定资源的预订处理请求之后，通用资源将替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="78d4d-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="78d4d-111">否则，如果资源经理已建议指定资源，通用资源将留在团队中，而请求状态则更改为 **需要审阅**。</span><span class="sxs-lookup"><span data-stu-id="78d4d-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]