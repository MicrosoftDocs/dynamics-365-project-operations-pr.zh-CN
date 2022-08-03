---
title: 里程碑的供应商发票明细
description: 本文说明如何在分包合同上创建里程碑的供应商发票明细。
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931319"
---
# <a name="vendor-invoice-lines-for-milestones"></a>里程碑的供应商发票明细

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Microsoft Dynamics 365 Project Operations 中的供应商发票可以包含在分包合同子项上定义的里程碑的供应商发票明细。 项目经理可以使用里程碑的供应商发票明细将采购的服务成本记录为为项目采购的服务或产品所产生的基于里程碑的成本。

里程碑的供应商发票明细必须始终引用具有固定价格记帐方法的分包合同子项。 当里程碑的供应商发票明细引用分包合同子项时，项目经理能够将引用该分包合同子项的时间、支出或材料的基本成本与供应商开票的里程碑进行匹配和验证。

下表提供了有关里程碑的供应商发票明细中的字段的信息。

| 字段 | 说明  | 功能影响 |
| --- | --- | --- |
| Name | 供应商发票明细的名称，帮助进行识别。 | 此名称将在基于供应商发票明细的所有查找中显示为第一列。 |
| 说明  | 供应商发票明细中由供应商开票的服务的简要说明。 | None |
| 分包合同 | 最初订购服务依据的分包合同。 | 当为供应商发票选择分包合同时，供应商发票上的所有明细都将继承该选择。 供应商发票不能有引用不同分包合同的供应商发票明细。 |
| 分包合同子项 | 订购服务依据的分包合同子项。 可以选择的分包合同子项的列表仅限于所选分包合同上的明细。 | 在里程碑的供应商发票明细上选择分包合同子项时，**角色** 和 **交易类别** 字段以及产品相关字段不相关且不可用。 **数量**、**单位** 和 **单位组** 字段也与基于里程碑的供应商发票明细不相关。 |
| 交易日期 | 供应商发票明细的实际成本将在项目中记录的日期。 | None |
| 交易分类 | 选择 **里程碑** 记录在分包合同子项中定义的已完成里程碑的供应商发票。 | None |
| 里程碑 | 选择在标记为 **可开票** 的相关分包合同子项上定义的里程碑。 | 可以在供应商发票明细上选择状态为 **可开票** 的分包合同子项里程碑。 |
| 集成 | 使用正在开票的服务的项目的名称。 | 此字段为必填项，不能留空。 |
| 任务 | 使用正在开票的服务的项目任务的名称。 此字段仅在选择项目时可用。 选择项目任务是可选的。 | 如果此字段留空，项目经理可以将供应商发票明细与项目任何任务中记录的相关分包合同子项上的交易类别进行匹配。 如果供应商发票明细不引用分包合同子项，并且此字段留空，由供应商发票明细创建的实际成本将不会链接到任何未记帐实际销售额。 在这种情况下，如果设置了基于任务的记帐，成本可能无法向最终客户开票。 |
| 里程碑金额 | 输入在可以开票的分包合同子项上定义的里程碑的值。 | None |
| 销售税 | 输入销售税金额。 | None |
| 总金额 | 供应商发票明细的总金额，包括税款。 此字段的计算方法是 *里程碑金额* + *销售税*。 | None |

> [!NOTE]
> 创建引用分包合同子项里程碑的供应商发票明细时，分包合同里程碑的状态将更新为 **已创建供应商发票**。 然后，当确认该供应商发票时，分包合同子项里程碑的状态将更新为 **已确认供应商发票**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]