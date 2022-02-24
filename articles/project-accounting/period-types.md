---
title: 期间类型
description: 本主题提供有关如何为收入估算设置期间类型的信息。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531371"
---
# <a name="period-types"></a>期间类型

_**适用于：** 面向资源/非库存场景的 Project Operations_

期间类型定义项目收入的估计频率。 本主题提供有关如何为收入估算设置期间类型的信息。 

## <a name="create-and-work-with-period-types"></a>创建和使用期间类型
若要创建和使用期间类型，请完成以下步骤：

1. 在您的 Dynamics 365 Finance 环境中，转到 **项目管理和会计** > **设置** > **估计** > **期间类型**。
2. 选择 **新建** 以创建新期间类型。 输入名称和说明。
3. 在 **频率** 字段中选择值：

    - 如果选择 **周**、**双周**、**半月**、**月**、**日**、**季度** 或 **年**，则日历将用于生成期间。 
    - 如果选择 **分类帐期间**，则总帐配置中的分类帐期间将用于生成期间。
    - 如果选择 **无限**，则可以指定自定义期间。
4. 选择期间类型记录，然后选择 **生成期间** 以为期间类型创建期间。 根据所选的期间频率，您可以选择指定开始日期或要生成期间数。
5. 选择 **期间** 以查看生成的期间。

