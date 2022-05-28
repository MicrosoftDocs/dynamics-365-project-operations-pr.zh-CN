---
title: 将采购类别用于项目采购订单和待定供应商发票
description: 本主题介绍如何配置可用于项目采购订单和待定供应商发票的采购类别。
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613247"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>将采购类别用于项目采购订单和待定供应商发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

采购专业人员可以创建和维护可用于项目采购订单和待定供应商发票的物料和服务的目录。 [采购目录](/dynamics365/supply-chain/procurement/procurement-catalogs)让您可以轻松地对采购进行分类，而无需配置和使用已发布产品目录。 每个采购类别都可以映射到时间、支出或物料交易的项目类别。 过帐使用采购类别的待定供应商发票后，系统将创建时间、支出或材料项目实际值、项目交易记录和子分类帐条目。

## <a name="minimum-version-requirements"></a>最低版本要求

需要以下版本来将采购类别用于 Microsoft Dynamics 365 Project Operations 非库存/基于资源场景的项目采购订单：

- Project Operations Dataverse 解决方案版本 4.41.0.45 或更高版本
- Finance and Operations 环境版本 10.0.26 或更高版本

## <a name="run-dual-write-maps-for-procurement-category-support"></a>为采购类别支持运行双写入映射

确保 **Project Operations integration project vendor invoice line export entity msdyn\_projectvendorinvoicelines** 的映射使用版本 1.0.0.4 或更高版本。

## <a name="enable-the-feature-key-for-procurement-categories"></a>为采购类别启用功能键

按照以下步骤启用将采购类别用于项目采购订单的功能。

1. 在 Dynamics 365 Finance 中，打开 **功能管理** 工作区。
1. 在功能列表中，找到 **在 Project Operations 中为基于资源/非库存场景使用采购类别** 功能，然后选择 **启用**。

> [!IMPORTANT]
> 作为先决条件，您还必须启用 **在 Project Operations 中为基于资源/非库存场景启用待定供应商发票** 功能。

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>在采购类别层次结构中映射项目类别

按照以下步骤将项目类别映射到 **采购类别** 层次结构中的采购类别：

1. 转到 **采购 \> 采购目录**。
1. 选择 **编辑类别层次结构**。
1. 选择所需的类别层次结构节点，然后在 **分配项目类别** 选项卡上，将该节点与 **时间**、支出**或 **物料项目** 类别（即 **默认时间** 或 **默认支出** 类别）中的项目类别相关联。
1. 选择 **保存**。
1. 关闭该页面。

> [!NOTE]
> 将采购类别映射到项目类别是可选的。 如果采购类别未映射，系统将使用 **项目管理与核算参数** 页面 **Dynamics 365 Customer engagement 上的 Project Operations** 选项卡上 **项目类别默认值** 部分的 **物料** 字段中设置的值。
