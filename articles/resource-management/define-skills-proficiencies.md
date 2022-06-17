---
title: 定义技能和专长
description: 本文提供有关如何设置熟练度模型以对资源进行评级的信息。
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 707a88b2f72c7324a6954a2e0cdce995b012ff48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915451"
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