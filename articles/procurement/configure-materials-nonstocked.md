---
title: 配置非库存材料以及待定供应商发票
description: 本文介绍如何启用非库存材料和待定供应商发票。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913747"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>配置非库存材料以及待定供应商发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

## <a name="minimum-version-requirement"></a>最低版本要求

对于 Dynamics 365 Project Operations 非库存/基于资源场景使用非库存材料和待定供应商发票需要以下版本：

Dynamics 365 Dataverse 解决方案：

- Project Operations – 4.9.0.221 或更高版本
- 双重写入应用程序业务流程解决方案 - 2.2.2.23 或更高版本

Dynamics 365 Finance：
- 10.0.18 (10.0.793.52) 或更高版本。 确保您的 Finance 环境是最新的，并且已应用所有质量更新以满足最低版本要求。

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>运行非库存材料与供应商发票集成的双重写入映射

本节提供有关非库存材料以及供应商发票所需的具体映射的信息。 验证[预配新环境](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps)一文中列出的先决条件映射是否在您的环境中运行。

1. 转到 Lifecycle Services (LCS)，导航到 LCS 项目，然后转到 **环境详细信息** 页。
2. 在 **Common Data Service 环境信息** 部分，选择 **链接到面向应用程序的 CDS**。 选择链接后，您将被重定向到映射中的实体列表。
3. 确保以下映射正在运行。 如果未运行，启动并确保包括所有相关的表映射。

    - CDS 发布的独特产品（产品）
    - 供应商 v2 (msdyn_vendors)
    - 用于材料估算的 Project Operations 表 (msdyn_estimatelines)
    - Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices)
    - Project Operations 集成项目供应商发票明细导出实体 (msdyn_projectvendorinvoicelines)
    - Project Operations 集成实际值 (msdyn_actuals)。 确保您运行的是映射版本 1.0.0.14 或更高版本。 您可以在 **双重写入** 页的 **版本** 列中看到映射的活动版本。 您可以通过选择 **表映射版本** 然后保存所选版本来激活映射的新版本。

如果您使用的是标准演示数据，可能还需要通过初始同步来停止并重新启动以下实体映射：
  - 付款天数 CDS V2 (msdyn_paymentdays)
  - 付款计划 (msdyn_paymentschedules)
  - 付款条款 (msdyn_paymentterms)
  - 供应商组 (msdyn_vendorgroups)
  - 单位 (uom)

> [!NOTE]
> 供应商组和单位的初始同步可能会因现有演示数据集中的一些记录而失败。 您可以忽略这些失败，因为它们不会阻止您在 Project Operations 中使用演示数据。

## <a name="configure-prerequisites-in-dataverse"></a>在 Dataverse 中配置先决条件

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>激活工作流以基于供应商实体创建客户

双重写入业务流程解决方案提供[供应商主集成](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping)。 作为此功能的先决条件，必须在 **客户** 实体中创建供应商数据。 激活模板工作流流程，在 **客户** 表中创建供应商，如[在供应商设计之间切换](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch)中所述。

### <a name="set-products-to-be-created-as-active"></a>将产品设置为以活动状态创建

非库存材料必须在 Finance 中配置为 **已发布产品**。 双重写入业务流程解决方案提供现成的[已发布产品与 Dataverse 产品集成目录](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping)。 默认情况下，Finance 中的产品在草稿状态下同步到 Dataverse。 要将产品同步到活动状态，以可以将其直接用于材料使用文档或待定供应商发票，转到 **系统** > **管理** > **系统管理** > **系统设置**，在 **销售** 选项卡上，将 **创建处于活动状态的产品** 设置为 **是**。

## <a name="configure-prerequisites-in-finance"></a>在 Finance 中配置先决条件

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>为待定供应商发票启用功能键

完成以下步骤，启用在待定供应商发票明细中添加项目详细信息的功能。

1. 在 Finance 中，转到 **功能管理** 工作区。
2. 在功能列表中，找到 **为基于资源/非库存场景启用 Project Operations 上的待定供应商发票** 功能，选择 **启用**。

### <a name="define-category-groups-and-project-categories-for-items"></a>为物料定义类别组和项目类别

为 **物料** 交易类型配置至少一个类别组，并使用此组至少配置一个项目类别。 有关详细信息，请参阅[配置项目类别](../project-accounting/configure-project-categories.md#category-groups)。

查看项目成本和收入配置文件，并为物料交易配置分类帐过帐设置。 有关详细信息，请参阅[配置收费项目会计](../project-accounting/configure-accounting-billable-projects.md)。

### <a name="set-up-a-write-in-product"></a>设置目录外产品

在 Project Operations 中，您可以记录已发布产品目录中配置的目录产品和目录外产品的材料估算和使用情况。 使用目录外产品需要为此目的在 Finance 中配置的一个已发布产品。 请完成以下步骤配置目录外产品。 在将 Project Operations 用于资源/非库存场景的每个法人中重复这些步骤。

1. 在 Finance 中，转到 **产品信息管理** > **产品** > **已发布产品**，选择 **新建**。
2. 在 **产品类型** 字段中，选择 **物料**，在 **产品子类型** 字段中，选择 **产品**。
3. 输入产品编号 (WRITEIN) 和产品名称（目录外产品）。
4. 选择物料模型组。 确保您选择的物料模型组将 **库存策略库存产品** 字段设置为 **False**。
5. 在 **物料组**、**存储维度组** 和 **跟踪维度组** 字段中选择值。 仅将 **存储维度** 用于 **站点**，然后在 **跟踪维度** 字段中，选择 **无**。
6. 在 **库存单位**、**采购单位** 和 **销售单位** 字段中选择值，然后保存更改。
7. 在 **计划** 选项卡中，设置默认订单设置，在 **库存** 选项卡上，设置默认的站点和仓库。
8. 转到 **项目管理和会计** > **设置** > **项目管理和会计参数**，打开 **Dynamics 365 Dataverse 上的 Project Operations**。 
9. 在 **材料** 选项卡上的 **目录外产品** 字段中，选择您创建的产品。
10. 在您的 Dataverse 环境中，在站点地图中，打开 **产品** 实体，查找目录外产品记录。 
11. 打开记录详细信息，将产品状态设置为 **已停用**。 此产品状态可防止任何人意外地在材料估算和使用文档中直接使用此记录。

### <a name="set-up-a-procurement-integration-account"></a>设置采购集成帐户

过帐具有属于项目的明细的待定供应商发票时，采购集成帐户将用作清算帐户。

当系统过帐待定供应商发票时，此帐户将用于项目成本金额。 供应商发票详细信息在 Dataverse 中处理，并将创建相应的项目实际值。 项目实际值的信息将被添加到 Project Operations 集成日记帐中。 过帐集成日记帐时，将从采购集成帐户中清除金额并将其记录到项目成本中。

1. 要设置采购集成帐户，转到 **项目管理和会计** > **设置** > **项目管理和会计参数**，打开 **Dynamics 365 Dataverse 上的 Project Operations**。 
2. 选择 **材料** 选项卡，然后在 **采购集成帐户** 字段中选择一个值。

#### <a name="set-up-project-category-defaults-for-an-item"></a>为物料设置项目类别默认值

1. 在 Finance 中，转到 **项目管理和会计** > **设置** > **项目管理和会计参数**，打开 **Dynamics 365 Dataverse 上的 Project Operations**。 
2. 在 **项目类别默认值** 选项卡上的 **物料** 字段中，选择一个值。 如果未在项目实际值记录中设置项目类别，此项目类别将用于材料交易。
