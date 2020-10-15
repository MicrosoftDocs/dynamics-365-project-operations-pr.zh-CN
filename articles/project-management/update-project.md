---
title: 更新项目
description: 此主题提供有关在 Project Operations 中更新项目的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897801"
---
# <a name="update-a-project"></a>更新项目

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

以下是创建项目后可以在项目中更新的字段的摘要，以及更新的所有适用含义。

## <a name="project-detail-fields"></a>项目详细信息字段

- **名称**：项目的标题。
- **说明**：项目的概述。
- **客户**：要向其交付项目的公司。
- **日历模板**：项目的工作时间。 当字段更改时，将重新计算整个计划。
- **货币**：项目的货币。 此字段的默认值基于在合同签订部门定义的货币。 当合同签订部门更新时，此字段也会更新。
- **合同签订部门**：代表主要负责赢得销售和管理对客户的工作和服务交付的公司组或部门的部门。 
- **项目经理**：有权审阅和审批时间条目和支出的项目团队成员。

## <a name="estimate-fields"></a>预估字段

- **预估开始日期**：项目将开始的日期。 更新此字段后，项目上的所有任务都会按新的开始日期按比例移动。
- **完成日期**：项目计划结束的日期。
- **工作量**：项目的预估工作量。 在项目中添加任务后，此字段不能再进行编辑。
- **预估人工成本**：项目的估计人工成本。 在项目中添加人工成本后，此字段不能再进行编辑。
- **预估支出**：项目的估计支出。 在项目中添加支出后，此字段不能再进行编辑。

## <a name="project-actual-fields"></a>项目实际值字段
- **实际开始时间**：项目开始的日期。
- **实际完成时间**：在项目完成时更新。

## <a name="project-status-fields"></a>项目状态字段

- **总体项目状态**：项目经理提供的总体项目运行状况。
- **注释**：项目经理提供的有关当前项目运行状况的叙述。

