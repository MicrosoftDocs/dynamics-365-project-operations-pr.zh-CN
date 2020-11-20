---
title: 使用“复制项目”开发项目模板
description: 此主题提供有关如何使用“复制项目”自定义操作创建项目模板的信息。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131602"
---
# <a name="develop-project-templates-with-copy-project"></a>使用“复制项目”开发项目模板

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 支持复制项目以及将所有工作还原为代表角色的通用资源的功能。 客户可以使用此功能来构建基本项目模板。

选择 **复制项目** 时，目标项目的状态将更新。 使用 **状态描述** 可以确定复制操作完成的时间。 如果未在目标项目实体中检测到目标日期，选择 **复制项目** 还会将项目的开始日期更新为当前的开始日期。

## <a name="copy-project-custom-action"></a>“复制项目”自定义操作 

### <a name="name"></a>客户 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>输入参数
有三个输入参数：

| 参数          | Type   | 值                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 实体引用 | 源项目 |
| 目标             | 实体引用 | 目标项目 |


- **{"clearTeamsAndAssignments":true}**：Web 版本的 Project 的默认行为，将删除所有工作和团队成员。
- **{"removeNamedResources":true}** Project Operations 的默认行为，将工作还原为通用资源。

有关操作的更多默认行为，请参阅[使用 Web API 操作](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>指定要复制的字段 
当调用操作时，**复制项目** 将查看项目视图 **复制项目列**，以确定在复制项目时要复制哪些字段。
