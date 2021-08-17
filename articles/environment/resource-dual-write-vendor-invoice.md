---
title: 供应商发票集成
description: 此主题提供有关 Project Operations 中的供应商发票集成的信息。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986480"
---
# <a name="vendor-invoice-integration"></a>供应商发票集成

_**适用于：** 面向资源/非库存场景的 Project Operations_

可以通过以下方法记录 Dynamics 365 Project Operations 中与项目相关的采购：转到 **应付帐款** > **发票** > **待定供应商发票**，使用待定供应商发票文档。 有关详细信息，请参阅[使用待定供应商发票购买非库存材料](../procurement/pending-vendor-invoices.md)。

> [!IMPORTANT]
> 在使用本主题所述的功能之前，请查看并应用所需的配置。 有关详细信息，请参阅[启用非库存材料和待定供应商发票](../procurement/configure-materials-nonstocked.md)。

在 Project Operations 中，与项目相关的供应商发票将使用特殊过帐规则过帐：

- 与项目相关的成本（包括非抵扣税）不会立即过帐到总帐中的项目成本帐户。 成本会过帐到 **采购集成帐户**。 此帐户在 **Dynamics 365 Customer engagement 上的 Project Operations** 选项卡上的 **项目管理和会计** > **设置** > **项目管理和会计参数** 中配置。
- 双重写入使用以下表映射将供应商发票详细信息同步到 Microsoft Dataverse：

     - **Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices)**：此表映射同步供应商发票标头信息。 仅至少有一个包含项目 ID 的明细的供应商发票会同步到 Dataverse。
     - **Project Operations 集成项目供应商发票明细导出实体 (msdyn_projectvendorinvoicelines)**：此表映射同步供应商发票明细信息。 仅包含项目 ID 的明细会同步到 Dataverse。

     > [!NOTE]
     > Dataverse 中的供应商发票详细信息不可编辑。

过帐供应商发票时，税子分类帐、供应商子分类帐和其他财务过帐将在 Dynamics 365 Finance 中记录为适用。

![供应商发票集成。](media/DW7VendorInvoice.png)

当记录被写入 Dataverse 中的 **供应商发票** 实体时，记录的自动审批流程将开始。 如果需要，可以转到 **高级设置** > **系统** > **系统作业**，在 Dataverse 中查看自动审批流程的状态。 审批完成后，系统将在 **实际值** 实体中创建材料交易类记录。

然后使用双重写入表映射 **Project Operations 集成实际值(msdyn_actuals)** 处理与材料相关的实际值。 有关详细信息，请参阅[项目估计值和实际值](resource-dual-write-estimates-actuals.md)。

定期流程 **从暂存导入** 创建与供应商发票相关的 Project Operations 集成日记帐行。 抵销帐户默认为采购集成帐户。 过帐集成日记帐时，将清除供应商发票交易的帐户余额，并将明细金额移至项目成本帐户。 另外还将创建项目子分类帐交易记录，用于下游开票和收入确认目的。
