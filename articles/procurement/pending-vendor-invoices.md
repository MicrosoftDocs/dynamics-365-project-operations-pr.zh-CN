---
title: 使用待定供应商发票采购非库存材料或采购类别
description: 本文介绍如何记录待定供应商发票。
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921981"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>使用待定供应商发票采购非库存材料或采购类别

_**适用于：** 面向资源/非库存场景的 Project Operations_

当公司为项目采购非库存材料或采购类别时，可以立即对照项目记录成本。 

例如，Contoso Robotics US 正在执行设备续订项目，并且需要软件许可证。 这些许可证是从第三方供应商购买的。  使用 Dynamics 365 Finance，应付帐款职员记录待定的供应商发票文档，并将许可证成本直接划归到设备续订项目。 

> [!IMPORTANT]
> 在使用本文中描述的功能之前，请查看并应用所需的配置。 有关详细信息，请参阅[启用非库存材料以及待定供应商发票](configure-materials-nonstocked.md)和[将采购类别用于项目采购订单和待定供应商发票](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>过帐与项目相关的待定供应商发票 

待定供应商发票可以在 **待定供应商发票** 页上记录（**应付帐款** > **发票** > **待定供应商发票**）。 完成以下步骤过帐与项目相关的待定供应商发票：

1. 转到 **应付帐款** > **发票**，选择 **新建**。 
1. 在 **发票客户** 字段中，选择供应商，然后在 **编号** 字段中输入供应商发票标识。
1. 在供应商发票中添加一行，然后在 **物料编号** 字段中，选择从供应商处购买的非库存物料。 或者，在 **采购类别** 字段中，选择从供应商处采购的采购类别。   
1. 添加采购的数量。 系统会根据非库存物料价格配置填充单价。 
1. 验证明细上的总金额和其他所需详细信息。
1. 在明细详细信息中，在 **项目** 选项卡上，选择将记录此物料的项目的 ID。
1. 可选：选择活动编号，并更新项目类别和明细属性。
1. 过帐待定供应商发票。 过帐发票时，系统会记录以下信息：
    
    - 供应商余额金额。
    - 销售税金额。
    - 项目的成本将记录到采购集成帐户中。
    - Dataverse 中的项目实际成本交易。  此交易将使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)进一步处理。 过帐此日记帐会将金额从采购集成帐户转移到项目成本帐户。 
    - 使用时间和材料记帐方法向项目客户记帐的购买。 此外，还会在 Dataverse 中为购买创建未记帐的销售交易。 Dataverse 中的产品价目表用于未记帐销售交易的销售价格和金额。
