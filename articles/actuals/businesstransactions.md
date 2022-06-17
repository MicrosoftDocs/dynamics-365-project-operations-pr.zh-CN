---
title: Project Operations 中的业务交易
description: 本文概括介绍了 Microsoft Dynamics 365 Project Operations 中的业务交易这个概念。
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923269"
---
# <a name="business-transactions-in-project-operations"></a>Project Operations 中的业务交易

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

在 Microsoft Dynamics 365 Project Operations 中，*业务交易* 是不能通过任何实体表示的抽象概念。 但是实体中的某些常用字段或流程应该采用业务交易概念。 以下实体使用此抽象概念：

- 报价单明细详细信息
- 合同子项详细信息
- 估算明细
- 日记帐行
- 实际

在这些实体中，报价单明细详细信息、合同子项详细信息和估算明细映射到项目生命周期中的 *估算阶段*。 日记帐行和实际值实体映射到项目生命周期中的 *执行阶段*。

Project Operations 将所有这五种实体中的记录视为业务交易。 唯一区别是实体中映射到估算阶段的记录（报价单明细详细信息、合同子项详细信息和估算明细）被视为 *财务预测*，而实体中映射到执行阶段的记录（日记帐行和实际值）则被视为已发生的 *财务结果*。

有关详细信息，请参阅[估算](../project-management/estimating-projects-overview.md)和[实际值](actuals-overview.md)。

## <a name="concepts-that-are-unique-to-business-transactions"></a>业务交易独有的概念

以下概念专属于业务交易：

- 交易类型
- 交易分类
- 交易来源
- 交易连接

### <a name="transaction-type"></a>交易类型

交易类型代表对项目的财务影响的时间安排和上下文。 其在 Project Operations 中通过具有以下支持值的选项集定义：

- 成本
- 项目合同
- 未记帐销售额
- 已记帐销售额
- 组织间销售额
- 资源单位成本

### <a name="transaction-class"></a>交易分类

交易分类代表项目中出现的不同类型的成本。 其在 Project Operations 中通过具有以下支持值的选项集定义：

- 时间
- 支出
- 材料
- 费用
- 里程碑
- 税款

> [!NOTE]
> 在 Project Operations 中，**里程碑** 值通常由固定价格记帐的业务逻辑使用。

### <a name="transaction-origin"></a>交易来源

交易来源是一个实体，用于存储每个业务交易的来源，以帮助进行报告和跟踪。 随着项目执行的开始，每个业务交易都会创建另一个业务交易，而该业务交易继而又会再创建业务交易，依此类推。

### <a name="transaction-connection"></a>交易连接

交易连接是一种实体，用于存储两个相似业务交易（如陈和关联的实际销售额）之间的关系，或记帐活动（如确认发票或更正发票）触发的交易冲销。

交易来源和交易连接实体可共同帮助您跟踪业务交易与导致创建特定业务交易的操作之间的关系。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
