---
title: 审阅项目和项目合同的开票积压
description: 此主题介绍如何审阅时间、支出和产品积压，以及如何将其标记为可开票。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bcdcc0cae06ce61bd582d56a8398e718051ff564
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123952"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>审阅项目和项目合同的开票积压

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

当交易准备就绪，可以创建和处理发票时，应该将该交易标记为 **可开票**。 此主题介绍可创建的交易类型。

## <a name="review-the-time-and-material-billing-backlog"></a>审阅时间和材料记帐积压

为项目提交和审批时间或支出条目时，PSA 将创建项目实际值。 如果将项目与交易分类的组合映射到时间和材料项目的合同子项，则批准了该条目时将创建两项实际值：

- 成本实际值 
- 未记帐实际销售额

未记帐实际销售额表示记帐积压，其记帐状态必须设置为 **可开票**。 创建项目发票时，将复制标记为 **可开票** 的未记帐实际销售额并替换发票明细详细信息。

若要审阅时间和材料的记帐积压，请转到 **Sales** \> **记帐** \> **时间和材料记帐积压**。 选择可开票的所有未记帐实际销售额，然后选择 **可开票**。 这些实际值的记帐状态将更改为 **可开票**。

![时间和材料记帐积压](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>审阅产品记帐积压

在 PSA 中，当项目合同中包含基于产品的合同子项时，只要为项目合同创建发票，都将考虑为这些明细开票。 将把具有标记为 **可开票** 的合同子项的所有产品作为项目发票明细复制到项目发票。

若要审阅产品的记帐积压，请转到 **Sales** \> **记帐** \> **产品记帐积压**。 选择可开票的所有基于产品的合同子项，然后选择 **可开票**。 这些明细的记帐状态将更改为 **可开票**。

![产品记帐积压](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>审阅固定价格合同的记帐里程碑

每项采用固定价格记帐方法的项目合同子项都必须定义合同里程碑。 这些合同里程碑只有在带有 **可开票** 标记时，才可以开票。 

若要审阅记帐里程碑，请转到 **Sales** \> **记帐** \> **固定价格里程碑**。 选择可开票的里程碑，然后选择 **可开票**。 这些里程碑的记帐状态将更改为 **可开票**。

![固定价格里程碑](media/FPBacklog.png)
