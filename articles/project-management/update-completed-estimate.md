---
title: 更新完工估算
description: 此主题提供有关更新项目的工作量预估的信息。
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072787"
---
# <a name="update-estimate-at-completion"></a>更新完工估算

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

项目经理经常修订任务的原始估算。 项目重新预估是项目经理基于项目当前状态对估算的感知。 但是，建议项目经理不要更改基准数字，因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。

项目经理可通过两种方法重新预估任务的工作量：

- 将默认的要完成的估算 (ETC) 替换为任务的实际剩余工作量新估算。 
- 将默认进度百分比替换为项目真实进度新估算。

这些方法都会导致重新计算任务的 ETC、完工估算 (EAC)、进度百分比，以及任务的预估工作量偏差。 将会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。
