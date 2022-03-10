---
title: 项目发票方案性能
description: 该主题提供了关于项目发票方案性能改进的信息。
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005695"
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
> 启用记帐规则后，无法应用发票方案性能。
> 
> 在批量创建发票方案的流程中，无论您输入什么内容，子任务数都将基于具有可开票交易的合同数将任务拆分为最大数量。 例如，如果您在批量创建发票方案时输入的子任务数为 **3**，并且只有两个具有可开票交易的合同，则仅创建两个子任务。
