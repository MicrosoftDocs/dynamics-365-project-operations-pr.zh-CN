---
title: 技能和熟练度模型
description: 此主题介绍如何使用技能和熟练度模型。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124177"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="37f08-103">技能和熟练度模型</span><span class="sxs-lookup"><span data-stu-id="37f08-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="37f08-104">技能是 Dynamics 365 Project Service Automation 与 Dynamics 365 Field Service（如果有）共享的资源特征。</span><span class="sxs-lookup"><span data-stu-id="37f08-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="37f08-105">若要维护 Project Service Automation 中的技能存储库，请转到 **资源** \> **资源技能**。</span><span class="sxs-lookup"><span data-stu-id="37f08-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![资源技能](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="37f08-107">使用熟练度模型为资源评级</span><span class="sxs-lookup"><span data-stu-id="37f08-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="37f08-108">资源的技能由熟练度模型评级。</span><span class="sxs-lookup"><span data-stu-id="37f08-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="37f08-109">各等级在熟练度模型中。</span><span class="sxs-lookup"><span data-stu-id="37f08-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="37f08-110">若要创建熟练度模型，请转到 **资源** \> **熟练度模型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="37f08-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="37f08-111">在新评级模型中，指定最小评级值，最大评级值和正在评级的实体。</span><span class="sxs-lookup"><span data-stu-id="37f08-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="37f08-112">在 **评级值** 子网格中，可以定义最小到最大的不同评级值。</span><span class="sxs-lookup"><span data-stu-id="37f08-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![定义了最小和最大评级](media/Resource-Management-image85.png)

<span data-ttu-id="37f08-114">这些评级值在 **资源要求**、**日程安排板** 和 **日程安排助理** 筛选器中显示。</span><span class="sxs-lookup"><span data-stu-id="37f08-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
