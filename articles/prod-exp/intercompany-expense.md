---
title: 内部公司支出
description: 本主题提供有关如何使用内部公司支出将工作人员的支出分配给为其执行工作的法人的信息。
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684218"
---
# <a name="intercompany-expenses"></a>内部公司支出

由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。 您可以使用内部公司支出将工作人员的支出分配给为其执行工作的法人。 雇用该工作人员的法人称为借出方法人。 工作人员产生支出的法人称为“借款法人”。 

您必须先启用内部公司支出行，工作人员才能够创建和提交内部公司支出。 在借出法人中，在 **支出管理参数** 页上，选择 **允许内部公司支出行**。 

## <a name="tax-posting-for-intercompany-expenses"></a>内部公司支出的税金过帐

[!include [banner](../includes/banner.md)]

您必须先在“总帐销售税”设置中启用此功能，然后才可以在支出报表中使用与借出（来源）法人关联的税组，而不是借款（目标）法人。 当 **内部公司税款过帐法人** 参数设置为 **来源**，**应用销售税税收规则** 设置为 **否** 时，将使用借出法人的税收组合。 如果同一个参数设置为 **目标**，将使用借入方法人的税务组合。 对于美国的法人来说，如果此参数设置为 **源**，则还必须在新的 **分类帐过帐组** 页中配置 **应收销售税** 字段。 成本核算引擎将把此字段中的信息用于与税务有关的成本核算条目。   
无论是否有项目，此行为对过帐的支出行都一致。  

## <a name="new-expense-expression-builder"></a>新支出表达式生成器

新支出表达式生成器解决了使用项目的内部公司支出方案的问题。 此功能可确保在您创建内部公司支出时，针对支出行上选择的项目正确验证支出策略，并且可以成功提交支出报表。

要使支出表达生成器功能正常工作，必须将其打开。 此外，还应设置具有项目 ID 的支出策略。

如果您已经配置了验证支出行上的项目 ID 的策略，则必须停用这些策略。 然后，您可以打开该功能并重新配置这些策略。

若要打开此功能，请执行以下步骤。

1. 转到 **工作区** \> **功能管理**。
2. 在列表中，选择 **用于解决使用项目的内部公司支出方案的问题的新支出表达式生成器**。 然后，选择 **立即启用**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
