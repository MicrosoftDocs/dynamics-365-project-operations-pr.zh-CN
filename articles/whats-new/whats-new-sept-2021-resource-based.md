---
title: 2021 年 9 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 9 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923361"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 9 月新增功能 - 基于资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

   - Microsoft Dataverse 环境中的 Project Operations 版本 4.14.0.99。
   - Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.20。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在 **版本** 列中的 **双重写入** 页面上查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 时间和支出 | 1811407 | 调整了支出条目审批的项目审批人安全角色。 |
| 时间和支出 | 1811438 | 调整了项目审批人安全角色以取消时间条目审批。 |
| 时间和支出 | 2370126 | 更新了 **时间条目** 实体中的 **项目任务** 和 **角色** 图标。 |
| 时间和支出 | 2379879 | 在使用适用于手机的 Dynamics 365 时，更正了时间条目中的 **复制周** 函数。 |
| 计费和定价 | 2371906 | 对于基于资源的部署，不得在 Project Operations 中调整形式发票总额。 |
| 计费和定价 | 2385802 | 修复了刷新项目总计时出现实际小时数为负的错误。 |
| 计费和定价 | 2389675 | 改进形式发票确认行为。 长期作业实体必须考虑为会计编写确认结果所需的活动。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 出差和支出 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 从信用卡交易创建的支出中过帐的供应商和销售税交易金额不正确。 |
| 出差和支出 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 生成付款日记帐后会创建错误的结算行。 |
| 出差和支出 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 从信用卡交易创建的支出中过帐的销售税交易金额不正确。 |
| 出差和支出 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 删除支出行可能需要很长时间。 |
| 项目会计 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | 应用 KB 4619395 后，不支持将编号序列更改为 **连续**，并且当您发布估算值时，会出现以下错误：“系统不支持设置‘连续’的编号序列 Proj_X”。 |
| 项目会计 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 过帐供应商发票可能会失败，并显示以下错误消息：“凭证上的交易按照 2021 年 5 月 17 日结余。 （会计币种：0.00 - 申报币种：0.01）”。 |
