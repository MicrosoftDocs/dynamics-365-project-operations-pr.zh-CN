---
title: 支出概述
description: 本主题提供有关 Project Operations 中的支出功能的信息。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764898"
---
# <a name="expense-home-page"></a>支出主页

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


Dynamics 365 Project Operations 支持处理支出功能。 通过使用可自定义的策略、交易类别和审批工作流，处理项目产生或不是项目产生的支出。

在 Project Operations 中，支持两种支出部署模型： 

- **完全**：完全部署可用于 **面向资源/非库存场景的 Project Operations** 或 **面向生产订单场景的 Project Operations**。
- **基本**：基本部署可用于 **面向资源/非库存场景的 Project Operations** 和 **精简部署 - 估价交易开票**。

## <a name="full"></a>完全 
完全支出部署提供完整的政策执行，包括创建政策功能，如：

  - 支出类别限制
  - 旅行
  - 每日
  - 信用卡导入
  - 收据光学字符识别

## <a name="basic"></a>Basic 
基本支出部署场景只允许您记录项目的基本支出。 

有关详细信息，请参阅[支出条目（精简）](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>确定支出部署
要确定您运行的是否是基本支出管理部署，请验证地址 URL 是否以 **.crm.dynamics.com** 结尾。 
