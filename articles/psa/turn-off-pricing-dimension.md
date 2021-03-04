---
title: 关闭定价维度
description: 本主题介绍如何在 Project Service 解决方案中设置定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147282"
---
# <a name="turn-off-a-pricing-dimension"></a>关闭定价维度

[!include [banner](../includes/psa-now-project-operations.md)]

您可能需要每隔数年检查和更新自己的定价策略。 您进行的任何更新都可能会要求您关闭现有定价维度并创建一个新的。 例如，您可能以前按 **角色** 定价，但现在决定按 **工作经验** 定价。 这可能需要您关闭充当定价维度的 **角色**，并创建 **工作经验** 充当新定价维度。 

开通过奖定价维度的 **适用于成本** 和 **适用于销售** 字段设置为 **否** 来关闭定价维度，无论该定价维度是自带的还是自定义的。

但是，如果这样做，可能会收到以下错误消息。

![关闭定价维度时可能出现的业务流程错误](media/Business-Process-Error.png)


此错误消息说明存在已经为正在关闭的维度设置的定价记录。 必须先删除引用某个维度的所有 **角色价格** 和 **角色价格加价** 记录，才能将该维度的适用性设置为 **否**。 此规则同时适用于自带定价维度和您可能已创建的任何自定义定价维度。 要执行此项验证的原因是，Project Service 的一项约束要求每个 **角色价格** 记录都必须有唯一的维度组合。 例如，在名称为 **2018 年美国成本费率** 的价目表中，有以下 **角色价格** 行。 

| 标准标题         | 部门    |单位   |价格  |货币  |
| -----------------------|-------------|-------|-------|----------|
| 系统工程师|Contoso US|Hour| 100|USD|
| 高级系统工程师|Contoso US|Hour| 150| USD|


关闭充当定价维度的 **标准标题**，并且 Project Service 定价引擎搜索价格时，将仅使用输入上下文中的 **部门** 值。 如果输入上下文的 **部门** 为“Contoso US”，结果将不确定，因为两个行都将匹配。 为了避免出现这样的情况，在您创建 **角色价格** 记录时，Project Service 会验证维度组合是否唯一。 如果在创建 **角色价格** 记录后关闭了维度，可能会违反此项约束。 因此，您需要在关闭维度之前删除已填充了维度值的所有 **角色价格** 和 **角色价格加价** 行。



[!INCLUDE[footer-include](../includes/footer-banner.md)]