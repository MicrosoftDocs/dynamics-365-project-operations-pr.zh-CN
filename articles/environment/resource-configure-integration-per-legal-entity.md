---
title: 配置每个法律实体的 Project Operations 集成
description: 本文提供有关在 Project Operations 中按法人设置集成的信息。
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914667"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>配置每个法律实体的 Project Operations 集成 

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文将引导您完成按法人配置 Dynamics 365 Project Operations 所需的步骤。

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>在 Dynamics 365 Finance 中启用功能键

完成以下步骤启用所需的功能。

1. 在 Dynamics 365 Finance 中，转到 **功能管理** 工作区。
2. 在 **功能列表** 中，找到并启用以下功能：
  
    - **为项目启用多个合同子项**
    - **启用 Dynamics 365 Customer Engagement 上的 Project Operations**

> [!NOTE]
> 如果您看不到列出的 **功能键**，请验证您的 Finance 版本是否满足最低版本要求（应用所有高质量更新的应用程序版本 10.0.13 或更高版本）。 选择 **检查更新** 刷新功能列表。

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>定义法人的 Project Operations 部署方案

您可以在法人级别启用 Dynamics 365 Customer Engagement 上的 Project Operations。 对于基于资源/非库存场景，您可以有一个使用 Dynamics 365 Customer Engagement 上的 Project Operations 的法人。 在同一个环境中，您可以让另一个法人使用面向库存/生产订单场景的 Project Operations。

1. 在 Dynamics 365 Finance 中，转到 **项目管理和会计** > **设置** > **全局项目管理和会计参数**。
2. 在可用法人列表中，选择将启用多个合同子项和 Dynamics 365 Customer Engagement 上的 Project Operations 功能的实体。 不选择将使用面向库存/生产订单场景的 Project Operations 的法人。

> [!NOTE]
> 只有当法人没有任何现有项目时，才可以选择该法人。

## <a name="configure-project-management-and-accounting-parameters"></a>配置项目管理和会计参数

使用 Dynamics 365 Customer Engagement 上的 Project Operations 的每个法人都需要一组默认参数。 这些参数在 **项目管理和会计参数** 页上的 **Project Operations** 选项卡上配置。 参数包括：

  - **记帐类型默认值**：Project Operations 使用一组固定的记帐类型默认值，这些值必须映射到明细属性“财务”。 为每个记帐类型创建一条记录：**未指定**、**应计费**、**非应计费**、**免费** 和 **不可用**。
  - **项目类别默认值**：选择每个交易类型要使用的默认项目类别。 这些默认值将在 **Project Operations 集成日记帐** 以及未为项目实际值指定交易类别的估算中使用。
  - **预测**：选择要用于时间和支出估计的预测模型。


[!INCLUDE[footer-include](../includes/footer-banner.md)]