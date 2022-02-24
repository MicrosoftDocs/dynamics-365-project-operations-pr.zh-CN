---
title: 支出报表的多人审批
description: 此主题提供有关需要多人审批的支出报表的信息。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271702"
---
# <a name="multiple-approvers-on-an-expense-report"></a>支出报表的多人审批

根据您组织的支出审核策略，可能需要多人审核由员工提交的支出报表。 在设置支出报表审批的工作流程时，您可以添加包含一个或多个支出报表审批者的任务或步骤的工作流元素。 例如，您可能需要所有支出报表首先由提交报表的员工经理审核，然后由应付帐款协调员进行审核。

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