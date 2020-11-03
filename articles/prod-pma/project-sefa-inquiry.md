---
title: 联邦奖励支出计划查询
description: 此主题提供有关联邦奖励支出计划查询的信息。
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072588"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>联邦奖励支出计划查询

[!include [banner](../includes/banner.md)]

根据 Office of Management and Budget Circular A-133，接收联邦资金的机构需要遵守审计要求，也称为单一审计。 审计流程用于定期报告联邦赠予的收入和支出。 单一审计报告的其中一部分是联邦奖励支出计划 (SEFA)。

联邦奖励支出计划查询包括“联邦国家补助目录 (CFDA)”标题和编号、赠予编号、赠予年份、提供资金的联邦机构的名称以及转赠实体的名称。 此查询针对特定期间。 通常，该期间与财务报表期间相同，即会计年度。

此查询包括在所选日期范围内具有预测日期的赠予。 查询的 **赠予机构** 列显示赠予客户或赠予机构（对于间接赠予）。 对于间接赠予， **中间机构** 列显示赠予客户。 如果不是间接赠予， **中间机构** 列为空白。

## <a name="set-up-the-cfda-clusters"></a>设置 CFDA 群集

您必须设置可与联邦奖励支出计划查询中的 CFDA 编号关联的 CFDA 群集。

1. 转到 **项目管理和会计 \> 设置 \> 赠予 \> 联邦国家补助目录群集** 。
2. 选择 **新建** 创建 CFDA 群集。
3. 输入群集名称。
4. 选择 **保存** 以保存您所做的更改。

## <a name="set-up-cfda-numbers"></a>设置 CFDA 编号

您必须设置可以添加到赠予中并包含在联邦奖励支出计划查询中的 CFDA 编号。

1. 转到 **项目管理和会计 \> 设置 \> 赠予 \> 联邦国家补助目录编号** 。
2. 选择 **新建** 创建 CFDA 编号。
3. 在 **编号** 列中，输入 CFDA 编号。
4. 按 **Tab** 键。
5. 在 **说明** 列中，输入 CFDA 标题。
6. 按 **Tab** 键。
7. 可选：在 **计划群集** 字段中，添加适当的 CFDA 群集。
8. 选择 **保存** 以保存您所做的更改。

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>设置赠予以针对联邦奖励支出计划查询进行报告

1. 转到 **项目管理和会计 \> 赠予 \> 赠予** ，选择现有赠予。
2. 在 **设置** 快速选项卡上的 **联邦国家补助目录** 字段中，分配 CFDA 编号。 赠予上的 CFDA 编号确定用于报告的 CFDA 群集。
3. 在 **联系信息** 快速选项卡上，按照以下步骤输入赠予方信息：

    1. 在 **赠予客户** 字段中，输入负责赠予的客户。 对于现有赠予，可能已经输入了此信息。
    2. 指明赠予客户是否是出资者。 如果赠予客户是出资者，保留 **间接** 复选框不选。 如果另一个客户是出资者，赠予客户负责使用和跟踪资金，则选中 **间接** 复选框。

4. 如果您在上一步中选择了 **间接** 复选框，在 **赠予机构** 字段中，输入提供赠予的客户。 赠予机构和赠予客户不能是同一客户。

下面是一个间接赠予的示例：

联邦政府资助了某个州的一个基础设施项目。 联邦政府将资金交给该州来使用。 在此例中，联邦政府是赠予机构，该州为赠予客户。

> [!NOTE] 
> 当您第一次启用此功能时，将使用赠予上的现有编号输入初始 CFDA 编号。

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>基于赠予类型从 SEFA 报告中排除赠予

1. 转到 **项目管理和会计 \> 设置 \> 赠予 \> 赠予类型** 。
2. 在 **默认信息** 快速选项卡上，选择 **从联邦奖励支出计划中排除** 复选框。
3. 选择 **保存** 以保存您所做的更改。

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>运行联邦奖励支出计划查询

1. 转到 **项目管理和会计 \> 查询和报表 \> 赠予查询 \> 联邦奖励支出计划** 。
2. 在 **参数** 部分，执行以下步骤：

    1. 在 **日期间隔** 字段中，选择日期间隔的代码。 或者，在 **起始日期** 和 **截止日期** 字段中，定义日期间隔。
    2. 可选：若要仅将已记帐交易作为收入包括在查询中，请将 **仅包括已记帐收入** 选项设置为 **是** 。

## <a name="columns"></a>列数

联邦奖励支出计划查询包括以下列：

- 联邦国家补助目录的群集名称
- 赠予机构
- 中间机构
- 赠予名称
- 赠予 ID
- 赠予申请 ID
- 联邦国家补助目录
- 收据
- 支出
