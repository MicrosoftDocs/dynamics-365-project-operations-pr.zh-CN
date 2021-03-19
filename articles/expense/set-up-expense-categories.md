---
title: 设置支出类别
description: 此主题提供有关如何为支出报表设置支出类别和共享类别的信息。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276112"
---
# <a name="set-up-expense-categories"></a>设置支出类别

_**适用于：** 面向资源/非库存场景的 Project Operations_

员工在创建支出报表时，其记录的每项支出都必须与支出类别关联。 支出类别派生自可在组织中的法人之间共享的共享类别。 根据您的组织的定义方式，这些支出类别还可以在其他区域中共享。 根据组织的定义和实施团队的指导，您必须确定支出管理中使用的类别是仅在支出管理中使用还是应在其他区域共享。

> [!NOTE]
> 这些类别可以在项目管理与会计和支出管理之间共享，也可以在项目管理与会计和生产之间共享。 但是，不能在支出管理和生产之间共享。

在开始设置过程之前，每个支出类别必须确定以下方面：

- 什么是支出类别？ 示例包括航班、酒店或里程类别。
- 支出类别是否还可以用于项目管理和会计？ 如果可以，您还必须确定以下方面：

    - 哪些成本科目将用于以下支出？

        - 成本
        - 工资分配
        - WIP-成本值
        - 成本-项
        - WIP-成本值-项
        - 应计损失
        - WIP-应计损失

    - 哪些收入科目将用于以下收入来源？

        - 已开票收入
        - 应计收入-销售值
        - WIP-销售值
        - 应计收入生产
        - WIP-生产
        - 应计收入-利润
        - WIP-利润
        - 应计收入-预订
        - WIP-预订

- 什么是支出类型？
- 支出类别的默认付款方式是什么？
- 支出类别中的支出是否必须细化？
- 支出类别的主要默认科目是什么？
- 支出类别的默认项销售税组是什么？
- 是否允许对支出类别使用其他付款方式？ 如果允许，有哪些？
- 此支出类别是否有子类别？ 如果有子类别，您还必须确定以下方面：

    - 是否将任何子类别排除在退税之外？
    - 子类别的项目销售税组是什么？


[!INCLUDE[footer-include](../includes/footer-banner.md)]