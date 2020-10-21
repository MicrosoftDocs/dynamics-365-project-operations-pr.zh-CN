---
title: 计价单位和计价单位组
description: 此主题提供有关如何在 Dynamics 365 Project Operations 中创建计价单位和计价单位组的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898745"
---
# <a name="units-and-unit-groups"></a>计价单位和计价单位组

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

计价单位是您销售产品或服务时使用的数量或测量单位。 例如，如果您销售园艺用品，您可以以包、盒和盘为单位销售种子。 计价单位组是这些不同单位的集合。

若要完成本主题中的步骤，请确保您已被分配了系统管理员或 Sales Professional 管理员角色或具有同等权限。

## <a name="create-a-unit-group"></a>创建计价单位组

1. 在站点地图中，选择**计价单位**。
2. 选择**新建**，在**创建计价单位组**对话框中，输入计价单位名称。
3. 在**基本计价单位**字段中，输入销售产品时所使用的最小的常用计价单位。 例如，您可以输入“件”或“盎司”。
4. 选择**确定**。

## <a name="add-units-to-a-unit-group"></a>将计价单位添加到计价单位组

1. 打开一个计价单位组，在**相关**选项卡上选择**计价单位**。 您将看到已经添加了基本计价单位。
2. 选择**添加新计价单位**，在**快速创建: 计价单位**页上的**名称**字段中，输入计价单位的名称。
3. 在**数量**字段中，输入计价单位将所含的数量。 例如，如果一盒包含两件，则输入“2”。 
4. 在**基础单位**字段中，选择一个基础单位来建立计价单位的最小度量单位。 例如，您可以选择“件”。
5. 选择**保存**：
