---
title: 预订与分配
description: 此主题提供有关资源预订和资源分配之间的区别的信息。
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591255"
---
# <a name="bookings-vs-assignments"></a>预订与分配

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

预订是将资源硬性或软性分配给项目。 硬预订占用资源的产能。 预订表示团队的组织概念，让他们可以了解如何在各个项目中投放资源。 Dynamics 365 Project Operations 将预订视为项目级概念。 

与预订不同，分配是资源对项目计划中的项目任务的承诺。 资源可以是指定的或通用的。  从项目任务分配获取资源要求时，Project Operations 使用资源分配的工作量信息来构建资源要求详细信息的信息。 但是，不会保留对资源分配的引用。 对从资源要求派生的预订的更新不会更新任何资源分配。

通常，资源的预订总和等于一项或多项任务中资源分配的总和。 但是，Project Operations 不强制执行此共识。 **协调** 视图为项目经理显示资源的预订和分配不一致的位置。




[!INCLUDE[footer-include](../includes/footer-banner.md)]