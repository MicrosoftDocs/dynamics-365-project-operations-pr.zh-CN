---
title: 项目发票方案性能
description: 该主题提供了关于项目发票方案性能改进的信息。
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920291"
---
# <a name="project-invoice-proposal-performance"></a>项目发票方案性能

[!include [banner](../includes/banner.md)]

创建新的发票方案时，由于项目数和子项目数增加，可能会遇到性能问题。 为了提高性能，提供了一项功能，可缩短为已过帐的项目交易创建新发票方案所需的时间。

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>启用项目发票方案性能增强
若要启用项目发票方案性能增强功能，请完成以下步骤。

1.  转到 **功能管理** > **所有**。 在功能列表中，找到 **项目发票方案性能增强**。
2.  选择 **立即启用**。
3.  刷新浏览器，然后创建一个新发票方案。

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>关闭项目发票方案性能增强
完成以下步骤以关闭项目发票方案性能增强。

1.  转到 **功能管理** > **所有**。 在功能列表中，找到 **项目发票方案性能增强**。
2.  选择 **禁用**。
3.  刷新浏览器。

> [!NOTE]
> 启用记帐规则或运行批处理过程时，无法应用发票方案性能。
