---
title: 取消以前批准的时间和支出条目
description: 此主题介绍如何取消已批准的项目时间和支出交易。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072779"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>取消以前批准的时间或支出条目

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 最新版本中，审批者可取消自己以前批准的时间或支出条目。

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>取消以前批准的时间或支出条目

执行以下步骤取消以前批准的时间或支出条目。

1. 转到 **项目** \> **我的工作** \> **审批** 。
2. 在 **审批** 列表页中，将视图更改为 **我过去的审批** 。 将显示您以前批准的时间和支出条目的列表。
3. 选择一个或多个条目，然后选择 **取消审批** 。 您将收到警告消息。
4. 选择 **确定** 取消审批。

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>了解取消时间和支出条目审批的影响

取消审批时，同时会产生运营影响和财务影响。

### <a name="operational-impact"></a>运营影响

在运营端，取消了一项审批时，记录的状态重置为 **草稿** ， **我过去的审批** 视图中不再显示这项审批。 而是在 **供审批的时间条目** 视图或 **供审批的支出条目** 视图中显示已取消的审批，具体取决于是时间条目还是支出条目。 此外，相关时间或支出条目的状态更改为 **已提交** ，以便让关联的条目与状态为 **草稿** 的审批一致。

作为审批者，您可以编辑状态为 **草稿** 的审批的一些字段。 这些字段包括 **记帐类型** 和 **时间条目的可记帐工时** 。 进行更改之后，可再次审批记录。 也可以拒绝此条目。 如果拒绝时间条目的审批，该条目的状态将更改为 **已返回** 。 如果拒绝支出条目的审批，该状态将更改为 **已拒绝** 。 在功能方面，已返回条目和已拒绝条目与状态为 **草稿** 的条目具有相同行为。 项目团队成员可以对条目进行所需的任何更改，然后重新提交进行审批，或完全删除条目。

### <a name="financial-impact"></a>财务影响

取消审批时，也会对项目造成财务影响。 首先，按照以下方式更新成本和销售额的相应实际值。

- 调整状态设置为 **已调整** 。
- 记帐状态设置为 **已取消** 。

接下来，在实际值表中创建冲销条目。 为了创建冲销条目，系统将复制并覆盖原始实际值的字段值。 唯一不复制覆盖的值为数量值。 而是冲销这些值。 将为实际 **成本** 和 **未记帐销售额** 创建冲销实际值。 已冲销实际值的 **调整状态** 字段设置为 **不可调整** ，而记帐状态设置为 **已取消** 。

进行这些更改之后，记录为已对项目使用的金额和项目的收入积压不再计入这些实际值表示的金额。
