---
title: 货币不匹配错误
description: 本主题提供有关保存特定记录类型时发生的货币不匹配错误的故障排除信息。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903349"
---
# <a name="currency-mismatch-error"></a>货币不匹配错误 

_**适用于：** 面向资源/非库存场景的 Project Operations_

当您保存项目、合同、报价单或可预订资源时，您可能会收到错误消息：**负责公司货币与合同单位货币不匹配。请选择其他负责公司或合同单位以继续**。 这是因为记录的合同单位货币与负责公司货币之间存在货币不匹配情况。


## <a name="resolution"></a>分辨率

若要解决此问题，请执行以下操作：
- 验证此记录的合同单位的货币。 您可以通过打开部门记录并验证 **常规** 选项卡上 **货币** 字段中的值来查看货币。
- 验证负责公司的货币。 您可以在公司记录中通过转到 **相关** > **日记帐** 来查看货币。 双击与公司关联的日记帐记录，并验证 **常规** 选项卡上 **记帐币种** 字段中的值。

如果合同单位中设置的货币与日记帐记录不匹配，请在保存记录时调整配置或选择其他值。 系统要求这些记录相匹配，以确保内部公司发票流正确无误。 有关内部公司配置的详细信息，请参阅[创建内部公司事务](../../project-accounting/create-intercompany-transactions.md)。

如果公司记录没有关联的日记帐记录，那么这表明在设置环境时缺少配置。 系统管理员必须更正此配置。 系统管理员必须转至 **双重写入配置**，停止然后重启 **日记帐双重写入映射**，并进行映射及其先决条件的初始同步。 有关详细信息，请参阅 [Project Operations 双重写入映射版本](../../environment/resource-dual-write-maps.md)。
