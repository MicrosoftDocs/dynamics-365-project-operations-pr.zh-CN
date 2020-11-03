---
title: 内部公司支出
description: 由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。 在此情况下，您可以使用内部公司支出功能来将工作人员的支出分配到执行该工作的法人。
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072755"
---
# <a name="intercompany-expenses"></a>内部公司支出

[!include [banner](../includes/banner.md)]

由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。 在此情况下，您可以使用内部公司支出功能来将工作人员的支出分配到执行该工作的法人。 雇用该工作人员的法人称为借出方法人。 工作人员产生支出的法人称为“借款法人”。 

在工作人员可以为不同的法人执行工作的创建和提交支出之前，必须在借出法人中的 **支出管理参数** 页选择 **允许内部公司支出行** 选项。 

## <a name="tax-posting-for-intercompany-expenses"></a>内部公司支出的税金过帐

[!include [banner](../includes/banner.md)]

如果要在支出报表中使用与借出方（源）法人而不是借入方（目标）法人 关联的税组，需要在设置总帐销售税时配置此设置。 如果总帐参数 **内部公司税金过帐的法人** 设置为 **源** ，并且 **应用应用销售税纳税规则** 设置为 **否** 时，将使用借出方法人的税务组合。 如果同一个参数设置为 **目标** ，将使用借入方法人的税务组合。 对于美国的法人来说，如果此参数设置为 **源** ，则还必须在新的 **分类帐过帐组** 页中配置 **应收销售税** 字段。 成本核算引擎将把此字段中的信息用于与税务有关的成本核算条目。   
无论是否有项目，此行为对过帐的支出行都一致。  
