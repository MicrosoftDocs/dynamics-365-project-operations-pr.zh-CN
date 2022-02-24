---
title: 使用待定供应商发票购买非库存材料
description: 本主题说明如何记录待定供应商发票。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993770"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>使用待定供应商发票购买非库存材料

_**适用于：** 面向资源/非库存场景的 Project Operations_

当公司为项目采购非库存材料时，可以立即针对项目记录成本。 

例如，Contoso Robotics US 正在执行设备更新项目，需要软件许可证。 这些许可证是从第三方供应商购买的。  使用 Dynamics 365 Finance，应付帐款职员记录待定供应商发票单据，并将许可证成本直接归于设备更新项目。 

> [!IMPORTANT]
> 在使用本主题所述的功能之前，请查看并应用所需的配置。 有关详细信息，请参阅[启用非库存材料和待定供应商发票](configure-materials-nonstocked.md)。 

## <a name="post-a-project-related-pending-vendor-invoice"></a>过帐与项目相关的待定供应商发票 

待定供应商发票可以在 **待定供应商发票** 页上记录（**应付帐款** > **发票** > **待定供应商发票**）。 完成以下步骤过帐与项目相关的待定供应商发票：

1. 转到 **应付帐款** > **发票**，选择 **新建**。 
2. 在 **发票客户** 字段中，选择一个供应商，在 **编号** 字段中，输入供应商发票标识。
3. 在供应商发票上添加明细，然后在 **物料编号** 字段中，选择从供应商处购买的非库存物料。 

    > [!NOTE]
    > 基于采购类别的供应商发票明细无法针对项目记录。 
    
5. 添加购买的数量。 系统将基于非库存物料价格配置填充单价。 
6. 验证明细上的总金额和其他所需详细信息。
7. 在明细详细信息的 **项目** 选项卡上，选择将要向其记录此物料的项目的 ID。
8. （可选）选择活动编号，更新项目类别和明细属性。
9. 过帐待定供应商发票。 过帐发票时，系统将记录：
    
    - 供应商余额金额。
    - 销售税金额。
    - 项目的成本将记录到采购集成帐户中。
    - Dataverse 中的项目实际值交易。 此交易将使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)进一步处理。 过帐此日记帐会将金额从采购集成帐户转移到项目成本帐户。
