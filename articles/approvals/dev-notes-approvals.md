---
title: 审批开发人员注释
description: 此主题提供有关处理审批的其他开发人员信息。
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991655"
---
# <a name="developer-notes-for-approvals"></a>审批开发人员注释

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 包含确保通过审批阶段正确进行记录转换的验证逻辑。 正确的记录转换确保： 

  - 所有支持行全部在相关表中创建，如日记帐和实际值。
  - 在继续之前，审批者在项目中将标记为 **项目审批者**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]