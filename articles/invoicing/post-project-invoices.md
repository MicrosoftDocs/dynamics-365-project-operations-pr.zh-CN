---
title: 开票流程概述
description: 本主题提供在面向资源/非库存场景的 Project Operations 中开票的流程概述。
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582699"
---
# <a name="invoicing-process-overview"></a>开票流程概述

_**适用于：** 面向资源/非库存场景的 Project Operations_

面向资源/非库存场景的 Project Operations 提供了量身定制的全面功能，可以满足项目经理和应收帐款业务员/项目会计的需求。 对于开票流程，项目经理管理项目记帐积压，应收帐款业务员/项目会计创建合规且准确的面向客户的发票单据。

![开票流关系图。](./media/invoicing-flow.png)

项目合同子项定义关联的项目交易的记帐方法。 当项目经理批准时间和支出交易时，系统会将交易记录在 **项目实际值** 实体中，并将信息发送到 Dynamics 365 Finance 中的 **项目管理和会计** 模块。 项目会计然后使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)来审核和过帐记录。 此日记帐包含项目实际值的重要会计详细信息，如记帐、销售税组、记帐物料销售税组和财务维度。

项目经理可以使用[时间和材料记帐积压](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)和[固定价格里程碑](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)中的时间和材料记帐方法审核未记帐的销售交易。 这些视图让您可以筛选和选择下一个计费周期中需要包括的交易，然后将其标记为 **可开票**。

您可以[手动创建估价发票](../proforma-invoicing/create-manual-proforma-invoice.md)或使用[定期流程](../proforma-invoicing/configure-automated-invoice-creation.md)。 项目经理可以根据需要[调整草稿估价发票](../proforma-invoicing/manage-proforma-invoice.md)，然后确认。

确认的估价发票将发送到 Finance 中的 **项目管理和会计** 模块。 项目会计将设置项目发票方案的格式并更新，然后发布和打印文档。 发布后的项目发票记录在总帐以及客户和项目分类帐中。


[!INCLUDE[footer-include](../includes/footer-banner.md)]