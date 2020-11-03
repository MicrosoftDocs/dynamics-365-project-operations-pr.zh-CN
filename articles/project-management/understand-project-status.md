---
title: 了解项目状态
description: 此主题提供有关 Dynamics 365 Project Operations 中分配给项目的状态的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072476"
---
# <a name="understand-project-status"></a>了解项目状态

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


 **项目实体** 页上的 **状态** 部分提供基于成本和工作量的项目运行状况摘要。


## <a name="status-summary-fields"></a>“状态摘要”字段

-  **总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。 此字段使用颜色编码（如绿色、黄色和红色）来指示上升的风险。 
- 项目经理可使用 **注释** 字段输入有关状态的特定注释。 
-  **状态更新日期** 字段不可编辑。 此字段中的值是指示状态上次更新时间的时间戳。
-  **计划绩效** 和 **成本绩效** 字段从跟踪网格设置。 如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，这些字段将更新为 **提前** 。 如果根节点的计划与成本偏差为负，这些字段将设置为 **落后** 。
