---
title: 定义技能和专长
description: 此主题提供有关如何设置熟练度模型来对资源进行评级的信息。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279667"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="8a893-103">定义技能和专长</span><span class="sxs-lookup"><span data-stu-id="8a893-103">Define skills and proficiencies</span></span>

<span data-ttu-id="8a893-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="8a893-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a893-105">技能是 Dynamics 365 Project Operations 与 Dynamics 365 Field Service（如果有）共享的资源特征。</span><span class="sxs-lookup"><span data-stu-id="8a893-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="8a893-106">若要维护 Project Operations 中的技能存储库，请转到 **资源** \> **资源技能**。</span><span class="sxs-lookup"><span data-stu-id="8a893-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="8a893-107">使用熟练度模型为资源评级</span><span class="sxs-lookup"><span data-stu-id="8a893-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="8a893-108">资源的技能由熟练度模型评级。</span><span class="sxs-lookup"><span data-stu-id="8a893-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="8a893-109">各等级在熟练度模型中。</span><span class="sxs-lookup"><span data-stu-id="8a893-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="8a893-110">若要创建熟练度模型，请转到 **资源** \> **熟练度模型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="8a893-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="8a893-111">在新评级模型中，指定最小评级值，最大评级值和正在评级的实体。</span><span class="sxs-lookup"><span data-stu-id="8a893-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="8a893-112">在 **评级值** 子网格中，可以定义最小到最大的不同评级值。</span><span class="sxs-lookup"><span data-stu-id="8a893-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="8a893-113">这些评级值在 **资源要求**、**日程安排板** 和 **日程安排助理** 筛选器中显示。</span><span class="sxs-lookup"><span data-stu-id="8a893-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]