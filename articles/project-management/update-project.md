---
title: 创建并更新项目
description: 本文提供有关在 Project Operations 中更新项目的信息。
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911079"
---
# <a name="create-and-update-a-project"></a>创建并更新项目

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

以下是创建项目后可以对项目更新的字段的摘要。 这还包括基于这些更新的任何适用影响。

## <a name="project-detail-fields"></a>项目详细信息字段

- **名称**：项目的标题。
- **说明**：项目的概述。
- **客户**：要向其交付项目的公司。
- **日历模板**：项目的工作时间。 当字段更改时，将重新计算整个计划。
- **货币**：项目的货币。 此字段的默认值基于在合同签订部门中定义的货币。 当合同签订部门更新时，此字段也会更新。
- **合同签订部门**：代表主要负责赢得销售和管理对客户的工作和服务交付的公司组或部门的部门。  未定义项目经理的部门时，此字段将默认为项目参数中定义的值。
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
