---
title: 内部公司开票概述
description: 本主题提供了有关内部公司项目开票的信息和示例。
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595431"
---
# <a name="intercompany-invoicing-overview"></a>内部公司开票概述

_**适用于：** 面向资源/非库存场景的 Project Operations_

您的组织可能具有多个为项目彼此转移产品和服务的分公司、附属机构和其他法人。 提供服务或产品的法律实体称为 *贷款法律实体*。 接收服务或产品的法律实体称为 *借款法律实体*。

下图显示了一个典型情形，其中有 Contoso Robotics USA（借款法律实体）和Contoso Robotics UK（贷款法律实体）这两个法律实体，它们共享资源来为 Adventure works 客户交付项目。 对于此情形，Contoso Robotics USA 已签约将工作交付给 Adventure Works。

![内部公司开票](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations 使用以下流来处理内部公司交易：

1. 贷款法律实体中的资源按贷款法律实体中项目的预定时间和支出来记录内部公司的时间或支出交易。
2. 使用借款公司的单位成本价目表将时间和支出成本记录在贷款公司中。
3. 使用借款公司的单位成本价目表将内部公司未记帐销售交易记录在贷款公司中。
4. 使用项目合同销售价目表将未记帐收入记录在借款公司中。 记录未记帐收入后，可以对客户进行计费。 客户不必等到内部公司账单处理完成。
5. 在贷款公司中定期创建内部公司客户账单。 账单是手动创建或使用定期自动流程创建的。 可以为每个借款法律实体创建单个账单，也可以按项目创建单独的账单。
6. 在贷款法律实体中过帐内部公司客户账单后，会在借款法律实体中创建相应的待定供应商账单。 过帐账单后，待定供应商账单中的成本将记录到项目子分类帐中。

下图说明了内部公司开票，因为它与会计事件和预期过帐到总帐有关。

![内部公司流](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>其他资源

- [配置内部公司开票](configure-intercompany-invoicing.md)
- [记录内部公司交易](create-intercompany-transactions.md)
- [创建内部公司客户和供应商账单](create-intercompany-customer-vendor-invoices.md)
