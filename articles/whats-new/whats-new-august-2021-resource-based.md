---
title: 2021 年 8 月新增功能 - 适用于基于资源/非库存场景的 Project Operations
description: 本主题提供有关适用于基于资源/非库存场景的 2021 年 8 月发行版本的 Project Operations 中提供的质量更新的信息。
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594153"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 8 月新增功能 - 适用于基于资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

   - Microsoft Dataverse 环境中的 Project Operations 版本 4.13.0.152。
   - Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.20。

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- **审批集**：审批集将时间、支出或材料用量审批请求组合在一起，构成较小的操作子集。 此分组允许项目按特定顺序处理审批，并允许重试和排序。 对于大量审批来说，组合请求可以提升审批处理的可靠性和可跟踪性。 有关详细信息，请参阅[审批集](../approvals/approval-sets.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。

有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在 **版本** 列中的 **双重写入** 页面上查看映射的活动版本。 通过选择 **表映射版本**，选择最新版本，然后保存选定版本，激活映射的新版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果在启动映射时遇到问题，请按照双重写入故障排除指南中[映射上缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2295625 | 必须将里程碑名称从发票计划复制到发票行明细。 |
| 计费和定价 | 2316323 | Project Operations 中基于资源的方案的估价发票中的折扣不应可编辑。 |
|   商机管理 | 2338619 | 只能通过页面调用 **商机** 和 **报价单** 业务规则。 |
| 资源管理 | 2316523 | 使用来自附加了角色的资源要求的 **发送请求** 时，不应显示错误。 |
| 资源管理 | 2326885 | 通过项目创建资源要求不应显示错误。 |
| 时间和支出 | 2335584 | 时间条目中已弃用的任务流。 |
| 时间和支出 | 2336884 | **复制周** 时间条目按钮必须不仅支持当前用户。 |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 出差和支出 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 从信用卡交易记录创建支出时，过帐的供应商交易记录和销售税交易记录金额不正确。 |
| 出差和支出 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 错误结算是生成付款日记帐时创建的行。 |
| 出差和支出 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 从信用卡交易记录创建支出时，过帐的销售税交易记录金额不正确。 |
| 出差和支出 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 删除支出行可能需要很长时间。 |
| 项目会计 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | 应用 KB 4619395 之后过帐预估时，系统不支持设置连续编号规则。 |
| 项目会计 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 过帐供应商发票可能失败，错误消息为：“凭证中的交易记录没有按 5/17/2021 平衡。 （会计币种：0.00 - 申报币种：0.01）” |
