---
title: 支出条目（精简）
description: 此主题提供有关如何在精简部署中使用支出条目的信息。
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590935"
---
# <a name="expense-entry-lite"></a>支出条目（精简）

_**适用于：** 精简部署 - 估价交易开票_

基本或精简支出管理是一项记录简单支出的功能。 您可以记录一个项目的支出，然后项目审批者将对其进行审核和审批。

有关 Dynamics 365 Project Operations 中的费用功能的详细信息，请参阅[费用概述](expense-overview.md)。

## <a name="capture-a-basic-expense"></a>捕获基本支出

您可以捕获支出，以将其提交给审批者。

1. 转到 **支出**，选择 **新建**。
2. 在 **新支出** 页上，输入所需的支出信息，然后选择 **保存**。

## <a name="submit-a-basic-expense"></a>提交基本支出

完成所有支出的捕获并准备好将其进行审批后，必须提交。

1. 转到 **支出**，选择一项支出。 或者，使用标题上的复选框选择所有支出。
2. 选择 **提交**。 系统将处理选定的条目，然后创建支出审批请求。

## <a name="add-an-attachment"></a>添加附件

您可能需要向审批人提供有关您的费用的其他文档。 您可以在支出条目的时间线中附加收据。 选择 **编辑**，然后在 **时间线** 部分中，选择回形针图标以附加收据。

## <a name="recall-a-basic-expense"></a>撤消基本支出

当您误提交支出时，可以撤消。 撤消支出条目所需的时间取决于其审批阶段。  如果审批者尚未审批条目，可以立即撤消。 但是，如果条目已经完成审批，则会要求审批者批准撤消，从而撤消交易。

1. 转到 **支出**，然后在支出列表中，选择要撤消的支出。
2. 选择 **撤消**。 如果支出条目尚未审批，系统会立即将其撤消。 如果支出条目已完成审批，将创建一个撤消请求，通知审批者您要撤消支出。 然后，审批者将确认可以撤消，条目将退回。

## <a name="delete-a-basic-expense"></a>刪除基本支出

尚未提交的支出可以删除。 若要删除已提交的支出，必须先将其撤消。

## <a name="see-also"></a>另请参阅

- [审批概述](../approvals/approvals-overview.md)
