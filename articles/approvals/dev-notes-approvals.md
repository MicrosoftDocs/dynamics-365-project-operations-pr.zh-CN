---
title: 审批开发人员注释
description: 本文提供有关处理审批的其他开发人员信息。
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924741"
---
# <a name="developer-notes-for-approvals"></a>审批开发人员注释

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 包含确保通过审批阶段正确进行记录转换的验证逻辑。 正确的记录转换确保： 

  - 所有支持行全部在相关表中创建，如日记帐和实际值。
  - 在继续之前，审批者在项目中将标记为 **项目审批者**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]