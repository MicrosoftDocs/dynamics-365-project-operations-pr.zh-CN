---
title: 设置保留款计划
description: 此主题提供有关如何在 Project Operations 中设置保留款计划的信息。
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1c48f04aa47d50c9f3ab46031ef0d6cd68619d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574741"
---
# <a name="set-up-a-retainer-schedule"></a>设置保留款计划

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

保留款计划在 Dynamics 365 Project Operations 中的 **项目合同** 页设置。

1. 在 **项目合同** 页上的 **预付款和保留款** 选项卡上，选择 **设置保留款计划**。
2. 在打开的对话页面上，将显示下表中列出的字段。 此表显示了输入值会怎样影响将要创建的保留款计划。

| 字段 | 描述 | 下游影响 |
| --- | --- | --- |
| 项目合同客户 | 将就此保留款或预付款为其开票的合同中的客户。 | 如果您在合同中有多个客户，您需要为每个客户的特定保留款或预付款金额开票，请为每个客户手动创建一个发票。 |
| 保留款计划开始 | 输入保留款计划的开始日期。 | 此日期不能是创建第一个保留款或预付款的日期。 创建第一个保留款或预付款的日期，此日期还受发票频率的影响。 |
| 保留款计划结束 | 输入保留款计划的结束日期。 | 此日期不能是创建最后一个保留款或预付款的日期。 创建最后一个保留款或预付款的日期还受发票频率的影响。 |
| 要创建的保留款数量 | 当您输入要创建的保留款数量时，系统将使用开始日期和频率在此字段中创建数量。 | 当手动更新此字段时，系统会忽略 **保留款计划结束** 字段中的值，而是创建特定的保留款或预付款数量。 |
| 账单频率 | 应用程序创建保留款和预付款的频率。 | 此值直接影响保留款和预付款的数量和创建日期。 |
| 总金额 | 总金额是拆分为将要创建的各个保留款或预付款的金额。 | 此字段没有下游影响。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]