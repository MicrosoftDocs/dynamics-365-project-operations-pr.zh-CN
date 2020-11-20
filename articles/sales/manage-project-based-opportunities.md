---
title: 管理基于项目的商机
description: 此主题提供有关如何处于与项目相关的商机的信息。
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118462"
---
# <a name="manage-project-based-opportunities"></a>管理基于项目的商机

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

基于项目的公司通常将业务交付分布在多个国家和地区。 项目执行和交付的成本可能因管理交付的地理位置或部门而异。 这继而会影响交易的利润。 交付基于项目的服务通常涉及大量的人事资源时间、大量出差支出、材料成本和其他支出。

Dynamics 365 Project Operations 中基于项目的商机在设计加入了对 Dynamics 365 Sales 的扩展。 此主题将详细介绍基于项目的公司在管理基于项目的商机时所需的其他功能中包含的不同字段和业务逻辑。

## <a name="view-all-project-based-opportunities"></a>查看所有基于项目的商机

可在 **商机** 列表页查看所有基于项目的商机的列表。 

1. 转到 **销售** > **商机**。
2. 使用 **视图切换器** 选择商机的其他筛选视图。 您可以使用自定义筛选条件创建您自己的视图，来配置这些视图和导航选项。

可从此列表页或详细信息页面创建或删除项目商机。

## <a name="business-process-flow-for-project-based-deals"></a>基于项目的交易的业务流程

Project Operations 中基于项目的交易支持以下业务流程：

- 潜在顾客转化为商机业务流程
- 商机销售流程

### <a name="lead-to-opportunity-business-process"></a>潜在顾客转化为商机业务流程 
潜在顾客转化为商机业务流程支持以下阶段：

| 阶段 | 映射实体 | 功能 |
| --- | --- | --- |
| 授予资格 | 潜在顾客 | 授予潜在顾客创建客户、联系人和商机的资格。 |
| 制定 | 商机​​ | 开发商机以添加有关所涉及的工作、关键利益干系人和竞争的更多信息。 |
| 建议 | 商机​​ | 制定方案并获得内部审查团队的批准。 |
| 结束 | 商机​​ | 赢得商机以达成交易。 |

### <a name="opportunity-sales-process"></a>商机销售流程
Project Operations 的商机销售流程是 Sales 应用程序中商机销售流程业务流程的扩展。 此业务流程设计为开箱即用，可以在基于项目的商机中支持以下阶段。

| 阶段 | 映射实体 | 功能 |
| --- | --- | --- |
| 授予资格 | 商机​​ | 授予潜在顾客创建客户、联系人和商机的资格。 |
| 建议 | 报价单 | 使用项目报价单制定方案并获得内部审查团队的批准。 |
| 合同 | 项目合同 | 赢得报价单以创建合同并开始项目的执行和交付。 |
| 结束 | 项目合同 | 成功完成工作并关闭项目合同。 |

> [!NOTE]
> 如果基于项目的交易从潜在顾客开始，潜在顾客转化为商机业务流程优先。
>
> 如果基于项目的交易从商机开始，商机销售流程优先。

您可以编辑产品业务流程或创建您自己的业务流程，来根据需要跟踪销售流程。 有关业务流程的详细信息，请参阅[业务流程概述](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)。
