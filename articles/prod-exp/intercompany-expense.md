---
title: 内部公司支出
description: 本主题提供有关如何使用内部公司支出将工作人员的支出分配给为其执行工作的法人的信息。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271522"
---
# <a name="intercompany-expenses"></a>内部公司支出

由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。 您可以使用内部公司支出将工作人员的支出分配给为其执行工作的法人。 雇用该工作人员的法人称为借出方法人。 工作人员产生支出的法人称为“借款法人”。 

您必须先启用内部公司支出行，工作人员才能够创建和提交内部公司支出。 在借出法人中，在 **支出管理参数** 页上，选择 **允许内部公司支出行**。 

## <a name="tax-posting-for-intercompany-expenses"></a>内部公司支出的税金过帐

[!include [banner](../includes/banner.md)]

您必须先在“总帐销售税”设置中启用此功能，然后才可以在支出报表中使用与借出（来源）法人关联的税组，而不是借款（目标）法人。 当 **内部公司税款过帐法人** 参数设置为 **来源**，**应用销售税税收规则** 设置为 **否** 时，将使用借出法人的税收组合。 如果同一个参数设置为 **目标**，将使用借入方法人的税务组合。 对于美国的法人来说，如果此参数设置为 **源**，则还必须在新的 **分类帐过帐组** 页中配置 **应收销售税** 字段。 成本核算引擎将把此字段中的信息用于与税务有关的成本核算条目。   
无论是否有项目，此行为对过帐的支出行都一致。  


[!INCLUDE[footer-include](../includes/footer-banner.md)]