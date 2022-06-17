---
title: 审批概述
description: 本文提供有关在 Project Operations 中使用审批的信息。
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: d5b5c93dc948992505054ef7b17579aafcdf8f8d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924695"
---
# <a name="approvals-overview"></a>审批概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

时间、支出和材料使用提交将经历审批工作流。 条目被批准后，将在实际值中记录交易或在计划中预订时间。

## <a name="approvals-workflow"></a>审批工作流
创建并提交时间、支出或材料使用条目时，将创建审批记录。 项目审批者或经理将审核并批准该条目。 如果此条目与项目相关，则将在审批后创建实际值。 这样可以跟踪成本和计费。

## <a name="approve-an-entry"></a>审批条目
 **审批** 页使您能够在不同的视图之间切换，以便可以查看不同类型的审批。
  
1. 转到 **审批** 页并选择 **支出**、**时间**、**材料使用** 或 **撤消**。
2. 查看每个审批，选择您要执行的审批。
3. 选择 **批准** 将批准选定的条目。
系统将处理这些条目并创建实际值。

## <a name="reject-an-entry"></a>拒绝条目
作为项目审批者，您可能必须将条目发送回用户以进行更正。
  
1. 转到 **审批** 页面，选择要拒绝的条目。 
2. 选择 **拒绝**。
3. （可选）请在 **拒绝注释** 对话框中添加注释，以通知用户拒绝该条目的原因。
4. 选择 **确定**。 此条目将返回给用户。
  
## <a name="cancel-approval"></a>取消审批
在某些情况下，您可能需要取消以前批准的条目。 取消之前批准的条目将影响财务。 

## <a name="approving-recall-requests"></a>审批撤消请求
在某些情况下，顾问可能需要撤消之前批准的条目。 取消之前批准的条目将影响财务。 项目审批者需要批准撤消以撤消实际值中的交易。

## <a name="specify-project-approvers"></a>指定项目审批者
每个项目有很多项目团队成员。 您还可以指定哪些团队成员同时也是项目审批者。

1. 转到 **项目** 页，并从列表中打开项目。
2. 在 **团队** 选项卡上，选择将成为项目审批者的团队成员，然后选择 **编辑**。
3. 将 **项目审批者** 字段设置为 **是**。
4. 选择 **保存**。
5. 重复步骤 2-4 添加其他项目审批者。

## <a name="configure-the-users-manager"></a>配置用户的经理

1. 转到 **设置** > **安全** > **用户**。
2. 选择要向其分派经理的用户，然后在 **组织信息** 区域中，从列表中选择经理。 
3. 选择 **保存**。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
