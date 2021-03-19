---
title: 撤消以前批准的时间或支出条目
description: 此主题介绍如何撤消以前批准的时间或支出交易。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283447"
---
# <a name="recall-approved-time-or-expense-entries"></a>撤消以前批准的时间或支出条目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

提交时间或支出条目的项目团队成员或其他人可以在该条目已被批准后将其撤消。 撤消已批准时间或支出条目的流程分两步：

1. 提交者请求撤消。
2. 审批者批准撤消。

## <a name="request-a-recall"></a>请求撤消

执行以下步骤请求撤消已批准的时间或支出条目。

1. 对于时间条目，请转到 **项目** \> **我的工作** \> **时间条目**。

    –或–

    对于支出条目，请转到 **项目** \> **我的工作** \> **支出条目**。

2. 对于时间条目，选择项目和任务特定组合的所有时间条目。 也可以在网格中选择特定项目特定日期的时间的单个单元格。

    –或–

    对于支出条目，选择要撤消的支出条目的行。

3. 选择 **撤消**。 出现确认对话框。 如果已批准了所选时间和支出条目，系统将提示您输入撤消原因。
4. 输入撤消原因，然后选择 **确定** 确认操作。 系统将向条目的审批者发送有关批准撤消的请求。

> [!NOTE]
> 虽然可以撤消已批准的时间和支出条目，如果已经对客户为批准的时间或支出条目条目开票，则不能创建撤消请求。 尝试创建撤消请求的用户将收到消息，说明不能撤消时间或支出，因为已为其开票。

## <a name="approve-or-reject-a-recall-request"></a>批准或拒绝撤消请求

可执行以下步骤批准或拒绝撤消请求。

1. 转到 **项目** \> **我的工作** \> **审批**。
2. 在 **审批** 列表页中，将视图更改为 **撤消待审批的请求**。 将显示提交的撤消请求的列表。
3. 选择一个或多个条目，然后选择 **批准** 或 **拒绝**。
4. 如果选择的是 **批准**，将收到警告消息，介绍批准的影响。 选择 **确定** 确认操作。 将批准撤消请求。

    –或–

    如果选择的是 **拒绝**，将拒绝撤消请求。

> [!NOTE]
> 请求撤消时，如果批准了撤消，系统将检查时间或支出条目的任何开票活动。 如果已经为条目开票，或者已经属于草稿发票，审批者将收到错误消息，说明不能批准撤消该时间或支持，因为已为其开票。

## <a name="impact-of-a-recall-request"></a>撤消请求的影响

撤消审批时，同时会产生运营影响和财务影响。

### <a name="operational-impact"></a>运营影响

如果批准了撤消请求，将把审批记录标记为 **已拒绝**。 条目的状态将更改为 **已返回** 或 **已拒绝**，具体取决于是时间条目还是支出条目。

项目团队成员可以查看条目，编辑条目再重新提交，或完全删除条目。

如果拒绝了撤消请求，条目的状态仍然为 **已批准**，并且项目团队成员或项目审批者不能编辑该条目。

### <a name="financial-impact"></a>财务影响

如果批准了撤消请求，将按照以下方式更新成本和销售额的相应实际值：

- **调整状态** 字段更新为 **已调整**。
- **记帐状态** 字段更新为 **已取消**。

接下来，在实际值表中创建冲销条目。 为了创建冲销条目，系统将复制并覆盖原始实际值的字段值。 唯一不复制覆盖的值为数量值。 而是冲销这些值。 将为实际 **成本** 和 **未记帐销售额** 创建冲销实际值。 已冲销实际值的 **调整状态** 字段设置为 **不可调整**，而 **记帐状态** 字段设置为 **已取消**。 由于这些更改，记录的项目开销和收入积压不再计入这些实际值表示的金额。

如果拒绝了撤消请求，则不存在对项目的财务影响。

## <a name="changes-to-time-entry-records"></a>对时间条目记录的更改

下图显示撤销了已批准时间条目时发生的更改。

![时间条目状态转换](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>对支出条目记录的更改

下图显示撤销了已批准支出条目时发生的更改。

![支出条目状态转换](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]