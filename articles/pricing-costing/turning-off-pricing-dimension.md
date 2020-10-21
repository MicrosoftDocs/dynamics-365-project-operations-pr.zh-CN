---
title: 关闭定价维度
description: 此主题介绍如何关闭定价维度。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896495"
---
# <a name="turning-off-a-pricing-dimension"></a>关闭定价维度

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

您可能需要每隔数年检查和更新自己的定价策略。 您进行的任何更新都可能会要求您关闭现有定价维度并创建一个新的。 例如，您可能以前按**角色**定价，但现在决定按**工作经验**定价。 这可能需要您关闭充当定价维度的**角色**，并创建**工作经验**充当新定价维度。 

开通过奖定价维度的**适用于成本**和**适用于销售**字段设置为**否**来关闭定价维度，无论该定价维度是自带的还是自定义的。

不过，当您执行此操作时，您可能会收到错误消息**如果有相关联的价格记录，则无法更新或删除定价维度**。

此错误消息说明存在已经为正在关闭的维度设置的定价记录。 必须先删除引用某个维度的所有**角色价格**和**角色价格加价**记录，才能将该维度的适用性设置为**否**。 此规则同时适用于自带定价维度和您可能已创建的任何自定义定价维度。 要执行此项验证的原因是每个**角色价格**记录都必须有唯一的维度组合。 例如，在名称为 **2018 年美国成本费率**的价目表中，有以下**角色价格**行。 

| 标准标题         | 部门    |单位   |价格  |货币  |
| -----------------------|-------------|-------|-------|----------|
| 系统工程师|Contoso US|Hour| 100|USD|
| 高级系统工程师|Contoso US|Hour| 150| USD|


关闭充当定价维度的**标准标题**，并且定价引擎搜索价格时，将仅使用输入上下文中的**部门**值。 如果输入上下文的**部门**为“Contoso US”，结果将不确定，因为两个行都将匹配。 为了避免出现这样的情况，在您创建**角色价格**记录时，系统会验证维度组合是否唯一。 如果在创建**角色价格**记录后关闭了维度，可能会违反此项约束。 因此，您需要在关闭维度之前删除已填充了维度值的所有**角色价格**和**角色价格加价**行。
