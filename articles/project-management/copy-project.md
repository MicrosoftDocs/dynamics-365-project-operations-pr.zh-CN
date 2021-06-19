---
title: 复制项目
description: 本主题提供有关在 Dynamics 365 Project Operations 中复制项目的信息。
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091243"
---
# <a name="copy-a-project"></a>复制项目

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

使用 Dynamics 365 Project Operations，可以通过选择 **项目** 窗体上的 **复制项目** 快速生成新项目。 若要复制项目，请打开要复制的项目，然后选择 **复制项目**。 该操作将复制以下内容：

- 项目属性 
- 工作分解结构
- 项目团队成员
- 项目估算
- 项目支出估计值
- 项目材料估算

## <a name="project-properties"></a>项目属性

在复制项目时，会复制以下字段中的值：

- 客户
- 描述
- 客户
- 日历模板
- 货币
- 合同签订部门
- 项目经理
- 状态 
- 总体项目状态
- 注释 
- 估计值
- 预计开始日期：这是利用副本创建项目的日期。
- 预计完成日期：此日期根据从副本制作的新项目的开始日期进行调整。
- 工作量(小时)
- 估算人工成本
- 估算支出成本
- 估算材料成本

> [!NOTE]
> 复制项目是一项长期操作。 项目记录、它们的相关属性和许多相关实体也会被复制。 由于操作的长期性，复制开始后，目标项目页面被锁定以进行编辑，直到复制操作完成为止。

## <a name="work-breakdown-structure"></a>工作分解结构

复制项目时，会复制整个已加载资源的工作分解结构。 指定资源将替换为通用资源。 如果指定资源与通用资源没有相同的工作时间，则将重新计算计划，任务持续时间可能会更改。

## <a name="project-team-members"></a>项目团队成员

从源项目复制项目团队时，将复制通用资源。 通用资源分派也与源项目中一样进行维护。 指定资源将转换为通用团队成员。

## <a name="estimates"></a>估计值

复制项目时，将从源项目复制资源、支出和材料估算行。 

有关如何以编程方式访问“复制项目”的信息，请参阅[使用“复制项目”开发项目模板](dev-copy-project.md)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
