---
title: 定义支出策略
description: 您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出策略。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896630"
---
# <a name="define-expense-policies"></a>定义支出策略

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的策略。         
实施支出策略可帮助您有效地管理支出。         

例如，您可以为纽约市的酒店支出设置策略，规定每晚支出不得超过 250 美元。       
如果工作人员提交的支出报表或出差申请中房间费率超过此金额，系统会通知         
工作人员已超过支出的策略金额。 在定义策略时您可以配置工作人员        
将收到的消息。      
        
您可以定义三种类型的策略：         
        
- **警告**：允许工作人员提交支出报表或出差申请，但会向所有审批者以及以后的报告         
  标记此支出。        

- **错误**：需要工作人员在提交支出报表或出差申请之前修改支出以遵守策略。        
 
 - **理由**：需要工作人员或经理在提交支出报表或出差申请之前，输入超过策略金额的理由。        

## <a name="policy-tips"></a>策略提示
在为支出管理创建新策略时，以下一些建议可以为您提供帮助： 

- 策略是有时效的，这意味着在使用晚于支出发生日期的日期创建时，策略不会生效。 例如，您今天创建了一个新策略，来强制执行餐饮支出最多 50 美元。 在昨天以前输入的所有现有支出都不会根据此策略进行检查。
- 在为可细化的支出类别创建策略时，请考虑为支出行类型添加条件。 某些策略（如需要收据）在明细行中可能没有意义。 在此情况下，该策略仅应用于标题行或非明细行。 
- 默认情况下，根据源实体评估支出管理策略。 对于内部公司场景，您可以改为针对目标实体（借款实体）设置要评估的策略。 要针对目标实体运行策略，请在**功能管理**工作区中打开**针对借款法人评估支出政策**功能。

## <a name="when-to-evaluate-policies"></a>评估策略的时间

在支出管理参数中，您可以选择在保存明细或提交支出报表时评估支出管理策略。 如果您选择在保存明细时进行评估，用户将提前了解到一次完成支出报表所需执行的操作。 或者，您可以在提交到工作流期间通过在最后进行验证来延后策略评估，从而节省时间。
