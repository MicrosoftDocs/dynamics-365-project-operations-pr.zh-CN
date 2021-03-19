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
# <a name="define-skills-and-proficiencies"></a>定义技能和专长

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

技能是 Dynamics 365 Project Operations 与 Dynamics 365 Field Service（如果有）共享的资源特征。 

- 若要维护 Project Operations 中的技能存储库，请转到 **资源** \> **资源技能**。 

## <a name="use-proficiency-models-to-rate-resources"></a>使用熟练度模型为资源评级

资源的技能由熟练度模型评级。 各等级在熟练度模型中。 

1. 若要创建熟练度模型，请转到 **资源** \> **熟练度模型**，然后选择 **新建**。
2. 在新评级模型中，指定最小评级值，最大评级值和正在评级的实体。
3. 在 **评级值** 子网格中，可以定义最小到最大的不同评级值。


这些评级值在 **资源要求**、**日程安排板** 和 **日程安排助理** 筛选器中显示。


[!INCLUDE[footer-include](../includes/footer-banner.md)]