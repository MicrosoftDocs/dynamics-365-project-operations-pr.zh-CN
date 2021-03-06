---
title: 管理项目报价单上的多个客户
description: 本主题提供处理涉及多个将为项目提供资金的客户的报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907928"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>管理项目报价单上的多个客户

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

项目报价单支持方案涉及多个将为交易提供资金的客户的场景。 报价单的**摘要**选项卡具有**潜在客户**字段，此字段标识交易的主要客户。 交易的其他客户可以在项目报价单的**客户**选项卡上设置。

项目报价单的**客户**选项卡上的所有报价单客户默认为为报价单创建的任何**新**的基于项目的报价单明细上的报价单明细客户。 任何现有的基于项目的报价单明细都不会继承在它们之后创建的新报价单客户记录。

在报价单赢单之前，报价单客户和报价单明细客户可以随时添加、更新或删除。 报价单上的有效客户必须在**客户**页上设置为业主公司或法人中的客户。 法人在 Dynamics 365 Project Operations 的**项目管理和会计**模块中设置，在 Project Operations 的**项目销售和交付**模块中作为公司出现。

## <a name="concept-of-a-primary-customer"></a>主要客户概念

在项目报价单的**摘要**选项卡上列为潜在客户的客户是报价单的主要客户。 如果您尝试从报价单上的客户列表中删除主要客户，将收到错误，指示无法删除报价单上的主要客户记录。

主要客户不应从报价单上的客户列表更新。 但是，您可以通过在报价单的**摘要**选项卡上更改潜在客户来影响主要客户。 当在**报价单摘要**上更新此字段时，新选择的潜在客户将被添加为新的报价单客户，并设置了**主要**标志。 之前的潜在客户仍会是报价单上的客户。

## <a name="create-update-or-delete-a-quote-customer-record"></a>创建、更新或删除报价单客户记录

报价单客户可以从**报价单**页上的**报价单客户**选项卡创建、更新或删除。 下表中列出的字段位于项目报价单的报价单客户记录中。

| **字段** | **位置** | **关联性、用途和指导** | **下游影响** |
| --- | --- | --- | --- |
| 帐户​​ | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 列出所有活动客户。 此字段在创建记录后将被锁定。 如果要更新，请删除该记录，然后重新创建字段。 如果您记录了所有实际值，或者报价单客户记录是主要客户，则可以删除该记录。 | 报价单客户在创建报价单明细时作为报价单明细客户复制。 当报价单赢单时，报价单客户还会复制到项目合同客户中。 |
| 计费拆分百分比 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 表示将归因于此报价单客户的每笔未计费销售交易的百分比。 | 复制到已创建的新报价单明细和项目合同客户。 |
| 帐单邮寄地址联系人姓名 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 这是一个文本字段，应该用于标识此客户的发票联系人。 这些值默认来自相关客户记录 | 当报价单赢单时复制到项目合同客户，然后依次复制到为此客户生成的发票上的“帐单邮寄地址联系人姓名”字段。 |
| 帐单邮寄地址名称 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 此文本字段应该用于标识此客户的发票联系人。 | 当报价单赢单时复制到项目合同客户，然后依次复制到为此客户生成的发票上的**帐单邮寄地址联系人姓名**字段。 |
| 付款方式 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 这是一个选项集，其中的值默认来自相关客户记录。 | 当报价单赢单时复制到项目合同客户，然后依次复制到为此客户生成的发票上的**帐单邮寄地址联系人姓名**字段。 |
| 舍入 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 指示此客户是否为此次交易的默认舍入客户。 | 当报价单赢单时复制到项目合同客户。 |
| 业主公司 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | **项目管理和会计**模块中设置了此客户的法人。 此字段为只读字段，设置为报价单本身的业主公司。 要在**客户**字段中添加的客户列表已在 Project Operations 的**项目管理和会计**模块中筛选出此业主公司的列表。 | 业主公司等同于 Project Operations 的**项目管理和会计**模块中的法人概念。 此项目产生的所有成本和收入均计入业主公司的总帐， |
| 上限 | **报价单客户**选项卡上的可编辑网格以及报价单客户的**主要**和**快速创建**窗体。 | 指示针对此协定向此客户开票的总金额是否有商定的限额或上限。 | 当报价单赢单时复制到项目合同客户。 |

## <a name="editing-billing-split-percentages"></a>编辑计费拆分百分比

您可以使用内嵌网格编辑体验来编辑计费拆分百分比。 如果计费拆分百分比总计不是 100%，将出现错误。 更新计费拆分百分比后，刷新页面以清除错误。

您还可以尝试在报价单客户的子网格上选择**平均分配**。 此操作会将计费拆分分配给所有报价单客户。 如果有任何舍入系数，将添加到舍入客户。 其中一个报价单客户始终标记为舍入客户。 这意味着报价单客户记录的**舍入**标志设置为**是**。 这通常是报价单的主要客户，但可以更改。