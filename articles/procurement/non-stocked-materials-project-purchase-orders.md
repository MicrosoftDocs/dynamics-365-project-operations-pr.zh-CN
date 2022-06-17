---
title: 使用项目采购订单为项目采购非库存材料
description: 本文说明如何使用项目采购订单为项目采购非库存材料。
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929801"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>使用项目采购订单为项目订购采购类别或非库存材料

_**适用于：** 面向资源/非库存场景的 Project Operations_

贵组织中的采购部门可以使用[销售订单](/dynamics365/supply-chain/procurement/purchase-order-overview)来跟踪产品和服务订单。 采购类别或非库存村料的采购订单可属于项目。 如果为这些销售订单开发票，则将记录项目的成本。

## <a name="prerequisites"></a>先决条件
完成以下步骤以启用项目采购订单功能。

1. 在 Dynamics 365 Finance 中，转到 **功能管理** 工作区。
2. 在功能列表中，查找并选择以下功能：**对基于资源/非库存场景在 Project Operations 上启用项目采购订单**。
3. 选择 **启用**。
4. 配置非库存材料和待定供应商发票，如[配置非库存材料及待定供应商发票](configure-materials-nonstocked.md)中所述。
5. 如[将采购类别用于项目采购订单和待定供应商发票](configure-procurement-categories.md)中所述配置采购类别。

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>创建项目采购订单列表中的项目采购订单

1. 在 Finance 中，转到 **项目管理和会计** > **项目** > **所有项目**，并选择一个项目。
2. 在操作窗格上 **管理** 选项卡的 **新建** 组中，选择 **物料任务** > **采购订单**。
3. 在 **创建采购订单** 页上，选择要向其下达采购订单的供应商，酌情输入其他信息，然后选择 **确定**。
4. 在 **采购订单** 页上的 **采购订单行** 网格中，选择 **添加行**。
5. 根据需要输入物料编号或采购类别、数量、单位、单价和其他信息。

    > [!NOTE]
    > 项目采购订单中只能使用采购类别、非库存物料和服务。 不支持库存物料。

6. 继续根据需要添加物料或采购类别并确认采购订单。

    可通过创建并发布产品收据来记录产品和服务收据。

    > [!NOTE]
    > 产品收据不会记录到 Microsoft Dataverse 中的项目实际值，并且不会影响项目子分类帐。

    供应商发送采购订单上的物料和服务的发票后，采购部门可以在操作窗格上转到 **发票** > **生成** > **发票**，从而为采购订单生成发票。 有关待定供应商发票的详细信息，请参阅[使用待定供应商发票购买非库存材料](pending-vendor-invoices.md)。
