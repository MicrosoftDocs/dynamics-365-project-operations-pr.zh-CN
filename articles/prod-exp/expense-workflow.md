---
title: 支出管理工作流
description: 此主题介绍如何使用 Microsoft Dynamics 365 Finance 中的工作流系统在支出管理中设置支出报表审核流程。
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001285"
---
# <a name="expense-management-workflow"></a>支出管理工作流

可使用工作流系统设置“支出管理”中支出报表的审核流程。 您可以设置使用以下条件确定由谁审核支出报表的工作流：

- 员工报告层次结构和预定义的审核限制
- 支持临时审核人和最终审核人的多级审核
- 财务维度和项目责任
- 给特定用户或用户组的分配

工作流审核可为支出报表、出差申请、预付现金和增值税 (VAT) 还原而创建。

**示例**

以下流程是针对某一支出报表的出差支出管理工作流程示例。

1. 员工创建和保存支出报表。
2. 员工提交支出报表以供审核。 审核人根据工作流设置后定义的规则标识。
3. 审核人接收支出报表可供审核的通知。 审核人审核支出报表并验证是否满足以下条件：

    - 支出不违反任何支出策略。 如果支出违反策略，审核人验证支出报表中是否包括有效的业务理由。
    - 电子收据是否附加到支出报表。

4. 审核人审核整个支出报表。
5. 将支出报表分配给应付账款协调员以供过帐。
6. 发生以下步骤之一，具体取决于是否配置自动过帐：

    - 如果配置自动过帐，则对支出报表进行付款处理，并且更新支出报表的状态。
    - 如果没有配置自动过帐，应付账款协调员验证所有原始收据已提交，并且收货与支出报表上的成本相符。 还必须验证支出报表上的所有税码是否正确。

在验证这些需求后，将支出报表过帐。

在支出报表过帐后，对支出报表授权付款，并且员工获得补偿。


[!INCLUDE[footer-include](../includes/footer-banner.md)]