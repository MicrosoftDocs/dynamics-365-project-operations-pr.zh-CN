---
title: 审批概述
description: 本主题提供有关在 Project Operations 中使用审批的信息。
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961155"
---
# <a name="approvals-overview"></a>审批概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

时间和支出提交通过审批工作流移动。 条目被批准后，将在实际值中记录交易或在计划中预订时间。

## <a name="approvals-workflow"></a>审批工作流
当您创建和提交时间或支出条目时，会创建一个审批条目。 项目审批者或您的经理将审核和审批您的条目。 如果条目与项目相关，在批准后，将创建实际值。 这样可以跟踪成本和计费。 

## <a name="approve-an-entry"></a>审批条目
通过**审批**窗体，您可以在不同的视图之间切换，查看不同类型的审批。
  
1. 转到**审批**窗体，选择**支出**、**时间**或**撤消**。
2. 查看每个审批，选择您要执行的审批。
3. 选择**批准**将批准选定的条目。
系统将处理这些条目并创建实际值或预订。

## <a name="reject-an-entry"></a>拒绝条目
作为项目审批者，您可能必须将条目发送回用户以进行更正。
  
1. 转到**审批**窗体，选择要拒绝的条目。 
2. 选择**拒绝**。
3. 可选 - 在**拒绝注释**对话框中添加注释，以告知用户条目为何被拒绝。
4. 选择**确定**。 此条目将返回给用户。
  
## <a name="recall-entries"></a>撤消条目
在某些时候，您可能需要撤消已提交的条目。 如果条目尚未被批准，将会立即退回。 但是，已批准的条目可能会影响材料。 为了撤消实际值中的交易，需要项目审批者批准撤消。

## <a name="specify-project-approvers"></a>指定项目审批者
每个项目有很多项目团队成员。 您还可以指定哪些团队成员同时也是项目审批者。

1. 转到**项目**窗体，从列表中打开项目。
2. 在**团队**选项卡上，选择将成为项目审批者的团队成员，然后选择**编辑**。
3. 将**项目审批者**字段设置为**是**。
4. 选择**保存**。
5. 重复步骤 2-4 添加其他项目审批者。

## <a name="configure-the-users-manager"></a>配置用户的经理

1. 转到**设置** > **安全** > **用户**。
2. 选择要向其分派经理的用户，然后在**组织信息**区域中，从列表中选择经理。 
3. 选择**保存**。


