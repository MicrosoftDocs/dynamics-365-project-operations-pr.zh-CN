---
title: 支出报表和多人审批
description: 此主题提供有关需要多人审批的支出报表的信息。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002045"
---
# <a name="expense-reports-and-multiple-approvers"></a>支出报表和多人审批

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

根据您的组织的支出审批政策，可能必须由多个人员审批提交的支出报表。 在设置支出报表审批的工作流程时，您可以添加包含一个或多个支出报表审批者的任务或步骤的工作流元素。 例如，您可能需要所有支出报表由两名单独的人员（提交报表的员工的经理和应付帐款协调员）审批。

如果您决定需要多个支出报表审批者，可以采用以下任一方式添加工作流元素：

- 添加一个具有一个步骤的审批元素。 例如，该步骤可能要求将支出报表分配给某个用户组，并由该用户组成员的 50% 进行审批。
- 添加一个具有多个步骤的审批元素。 例如，审批元素可能包括以下步骤：

    1. 提交支出报表的员工的经理审批报表。
    2. 应付帐款职员验证收据和支出报表项。
    3. 预算负责人审批支出报表。

- 添加多个审批元素，每个元素包含一个步骤。 例如，您可以为下列每个步骤添加单独的审批元素：

    1. 员工的经理审批支出报表。
    2. 预算负责人审批支出报表。


[!INCLUDE[footer-include](../includes/footer-banner.md)]