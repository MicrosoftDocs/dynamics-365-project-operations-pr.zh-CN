---
title: 设置支出管理工作流
description: 您可以设置用于审核和审批出差和支出文档的工作流程。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072631"
---
# <a name="set-up-workflows-for-expense-management"></a>设置支出管理工作流

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

您可以设置用来审核和审批出差和支出文档的工作流程。 您可以为支出报表、出差申请和预付现金请求定义工作流。

工作流表示一个业务流程，定义文档在系统中的流动方式。 工作流还指示必须完成任务或审批文档的人员。 在组织中使用工作流系统具有以下几项好处：

- **一致的流程** ：您可以为特定文档（如采购申请和支出报表）定义审批流程。 使用工作流系统有助于确保以一致且有效的方式处理和审批文档。
- **流程可见** ：可以跟踪特定工作流实例的状态、历史记录和性能指标。 这可以帮助您确定是否应对工作流进行更改以提高效率。
- **集中式工作列表** ：用户可以查看集中式工作列表，来查看分配给他们的工作流任务和审批。 

## <a name="workflow-types"></a>工作流类型

下表列出了您可以在 **支出管理** 中创建的工作流的类型。


|              <strong>类型</strong>              |                   <strong>使用此类型可以</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>支出报表自动审批</strong> |            为支出报表创建审批工作流。             |
|  <strong>支出报表自动发布</strong>   |        为支出报表创建自动发布工作流。        |
|       <strong>支出明细项目</strong>        |     为支出报表中的明细项目创建审批工作流。      |
| <strong>支出明细项目自动发布</strong> | 为支出报表中的明细项目创建自动发布工作流。 |
|       <strong>出差申请</strong>       |          为出差申请创建审批工作流。           |
|      <strong>预付现金请求</strong>      |         为预付现金请求创建审批工作流。          |
|        <strong>增值税退税</strong>        | 为增值税 (VAT) 退税创建审批工作流。  |
