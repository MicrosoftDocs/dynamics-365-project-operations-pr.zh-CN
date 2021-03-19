---
title: 设置支出策略
description: 您可以在 Microsoft Dynamics 365 Finance 中设置您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出策略。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271252"
---
# <a name="set-up-expense-policies"></a>设置支出策略

您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的策略。         
实施支出策略可帮助您有效地管理支出。         

例如，您可以为纽约市的酒店支出设置策略，规定每晚支出不得超过 250 美元。       
如果员工提交的支出报表或出差申请中的房费超过了此金额，系统将通知        
工作人员已超过支出的策略金额。 在定义策略时您可以配置工作人员        
将收到的消息。      
        
您可以定义三种类型的策略：         
        
- 警告 – 允许工作人员提交支出报表或出差申请，但将为所有审核人和最新报表        
  标记此支出。        

- 错误 – 在提交支出报表或出差申请前，要求工作人员修改该支出以符合该策略。       
 
 - 调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出策略金额的调整。        

## <a name="policy-tips"></a>策略提示
下面是一些在为支出管理新建策略时可以帮助您的建议。 
* 策略有生效日期，如果创建策略时不为其设置支出产生后的日期，策略不会生效。 例如，如果今天创建新策略以实施最大餐费 50 美元，则不会针对此策略检查截止昨天的任何现有支出。
* 在为可细化的支出类别创建策略时，请考虑为支出行类型添加条件。 某些策略（如索取收据）可能对明细化行无意义，只应该应用于标题行或非明细化行。 
* 默认情况下，根据源实体评估支出管理策略。 对于内部公司场景，您可以改为针对目标实体（借款实体）设置要评估的策略。 若要针对目标法人运行策略，请在 **功能管理** 工作区中开启“根据借入方法人评估策略”。

## <a name="when-to-evaluate-policies"></a>评估策略的时间

支出管理参数中有一个选项，用于在保存行时或在提交支出报表时评估支出管理策略。 如果选择在保存行时评估，这将确保用户可以查看需要执行哪些操作才能一次性完成所有支出报表。 否则，如果要在结束时向工作流提交期间进行验证，可以推迟策略评估并节约时间。


[!INCLUDE[footer-include](../includes/footer-banner.md)]