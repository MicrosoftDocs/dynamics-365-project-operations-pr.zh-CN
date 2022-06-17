---
title: 技能和熟练度模型
description: 本文介绍如何使用技能和熟练度模型。
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 27a9668c3a0d6a2323fb4797a29f6c7d3d146c57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925293"
---
# <a name="skills-and-proficiency-models"></a>技能和熟练度模型

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

技能是 Dynamics 365 Project Service Automation 与 Dynamics 365 Field Service（如果有）共享的资源特征。 

若要维护 Project Service Automation 中的技能存储库，请转到 **资源** \> **资源技能**。 

> ![资源技能。](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>使用熟练度模型为资源评级

资源的技能由熟练度模型评级。 各等级在熟练度模型中。 

1. 若要创建熟练度模型，请转到 **资源** \> **熟练度模型**，然后选择 **新建**。
2. 在新评级模型中，指定最小评级值，最大评级值和正在评级的实体。
3. 在 **评级值** 子网格中，可以定义最小到最大的不同评级值。

> ![定义了最小和最大评级。](media/Resource-Management-image85.png)

这些评级值在 **资源要求**、**日程安排板** 和 **日程安排助理** 筛选器中显示。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
