---
title: 在转换时迁移已完全开票的记帐里程碑
description: 本文说明如何迁移在上线日期之前已针对打开的项目合同向客户开票的固定价格记帐里程碑。
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912229"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>在转换时迁移已完全开票的记帐里程碑

_**适用于：** 面向资源/非库存场景的 Project Operations_

## <a name="scenario"></a>场景

Contoso 将与 Microsoft Dynamics 365 Project Operations 一起上线，用于资源/非库存场景。 作为转换活动的一部分，实施团队必须从旧系统迁移打开的项目合同。 有些项目合同包括使用固定价格记帐方法并且已向最终客户部分开票的合同子项。 实施团队必须将这些记帐里程碑作为 **客户发票已过帐** 迁移，因为它们必须包含在合同总值中用于收入确认目的。 但是，应收帐款和总帐中的客户余额不能受影响。

## <a name="solution"></a>解决方案

### <a name="prerequisites"></a>先决条件

- 必须安装 Dynamics 365 Finance 10.0.24 或更高版本。
- 将完成迁移步骤的环境必须处于维护模式。 迁移里程碑时不应执行任何其他活动。
- 迁移步骤必须完全按照此处所述进行，并且只能用于转换活动。 Microsoft 不支持将此功能用于其他用途。

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>创建 Project Operations 集成合同子项里程碑双写入映射的转换版本 

1. 确保 **Project Operations 集成合同子项里程碑** 实体的目标映射是最新的。 

    1. 在 Finance 中，转到 **数据管理**\>**数据实体**，选择 **Project Operations 集成合同子项里程碑** 实体。 
    2. 选择 **修改目标映射**。 
    3. 在 **将暂存映射到目标** 页面上，选择 **生成映射**，然后确认您要生成映射。

2. 停止并刷新 **Project Operations 集成合同子项里程碑** (**msdyn\_contractlinescheduleofvalues**) 双写入映射。 

    1. 转到 **数据管理**\>**双写入**，选择映射，打开它的详细信息。 
    2. 选择 **停止**，等待系统停止映射。 
    3. 选择 **刷新表**。

3. 为交易状态添加映射。

    1. 选择 **添加映射**。
    2. 在新行的 **财务和运营应用** 列中，选择 **TRANSSTATUS \[TRANSSTATUS\]** 字段。
    3. 在 **Microsoft Dataverse** 列中，选择 **msdyn\_invoicestatus \[发票状态\]**。
    4. 在 **映射类型** 列中，选择右箭头 (**\>**)。
    5. 在出现的对话框中，在 **同步方向** 字段中，选择 **Dataverse 到财务和运营应用**。
    6. 选择 **添加转换**。
    7. 在 **转换类型** 字段中，选择 **ValueMap**。
    8. 选择 **添加值映射**。
    9. 在左侧字段中，输入 **4**。 在右侧字段中，输入 **192350001**。 
    10. 选择 **保存**，然后关闭对话框。

4. 选择 **另存为** 保存双写入映射的版本。 
5. 在 **添加表** 窗格的 **发布者** 字段中，选择 **默认发布者**。
6. 在 **版本** 字段中，输入版本。
7. 在 **说明** 字段中，输入有关此映射转换版本的注释。 
8. 选择 **保存**。
9. 启动映射。

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>将已开票里程碑迁移到 Dataverse 环境

1. 在 Project Operations Dataverse 环境中，创建发票状态为 **已准备好开票** 的里程碑。 此时，不要迁移任何尚未开票的里程碑。

    > [!NOTE]
    > 在迁移记帐里程碑之前，请确保与项目合同子项相关的财务维度已按预期设置。 迁移完成后将无法编辑财务维度。

2. 迁移所有里程碑后，停止以下双写入映射：

    - Project Operations 集成合同子项里程碑 (msdyn\_contractlinescheduleofvalues)
    - Project Operations 集成实际值 (msdyn\_actuals)
    - 项目发票方案 V2（发票）

    要停止映射，请按照下列步骤操作：

    1. 在 Finance 中，转到 **数据管理**\>**双写入**，选择映射，打开它的详细信息。
    2. 选择 **停止**，等待系统停止映射。

3. 在 Project Operations Dataverse 环境中，为记帐里程碑创建并确认估价发票。 

    1. 在站点地图中，转到项目合同，选择合同，然后选择 **创建发票**。
    2. 创建发票后，从站点地图的 **发票** 菜单打开它们，然后选择 **确认**。

    此步骤在 Dataverse 环境中创建所需的记录。 但是，它不会影响财务和应收帐款，因为之前列出的双写入映射已停止。

4. 确认所有估价发票后，将所有双写入映射返回到初始状态。

    1. 将 **Project Operations 集成合同子项里程碑** (**msdyn\_contractlinescheduleofvalues**) 双写入映射的版本重新更新为原始版本。 
    2. 在映射列表中选择双写入映射，选择 **表映射版本**，然后选择表映射的原始版本。
    3. 选择 **保存**。
    4. 重新启动以下双写入映射：

        - Project Operations 集成合同子项里程碑 (msdyn\_contractlinescheduleofvalues)
        - Project Operations 集成实际值 (msdyn\_actuals)
        - 项目发票方案 V2（发票）

里程碑现已迁移，系统已准备好进行转换活动的后续步骤。
