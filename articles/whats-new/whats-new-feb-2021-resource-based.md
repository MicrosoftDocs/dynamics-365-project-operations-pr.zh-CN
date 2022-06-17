---
title: 2021 年 2 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 2 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910620"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 2 月新增功能 - 面向资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 4.7.0.95
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.16 

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| **记帐和定价** | 2053736 | 现在可以通过转到 **发票** > **相关信息** 来访问发票明细详细信息。 |
| **记帐和定价** | 2122613 | **激活** 和 **停用** 操作已从 **价目表** 关联实体中删除。 |
| **记帐和定价** | 2128606 | 解决了 **GetEstimatesForProject** 插件中 **ullReferenceException** 存在的问题。 |
| **部署和配置** | 2139346 | 解决了导入非托管 **Dynamics365ProjectOperationsDualWrite** 解决方案存在的问题。 |
| **部署和配置** | 2140569 | 不能在 Dataverse Teams 环境中安装项目解决方案。 |
| **部署和配置** | 2086991 | 限制自定义 Web 资源的本地化。 |
| **商机管理** | 2136794 | 当 **确认发票** 或 **发票标记为已支付** 流程失败时，显示正确的错误消息。 |
| **商机管理** | 2139330 | 更改项目的项目经理不能将负责公司重置为默认值。 |
| **商机管理** | 2146376 | 非应计费实际值中的更正税金额从发票确认创建。 |
| **项目规划和跟踪** | 2099879 | Dataverse 环境部署必须创建具有静态 ID 的默认交易类别，而不能在每个环境中随机生成。 |
| **项目规划和跟踪** | 2128577 | 修复了更新资源分配上的交易类别的 Project Service 用户特权。 |
| **项目规划和跟踪** | 2164035 | 修复了 **复制项目** 功能存在的问题。 |
| **时间条目** | 2129161 | 应用了更严格的限制，以确保用户不能更改和更新已提交或批准的时间条目。 |
| **时间条目** | 2103572 | 非项目时间条目的时间审批不能查找项目审批者角色。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计 

有关 Dynamics 365 Finance 中的项目管理和会计的详细信息，请参阅[2021 年 1 月新增功能 - 基于资源/非库存场景的 Project Operations](whats-new-jan-2021-resource-based.md)。


## <a name="regulatory-updates"></a>法规更新

有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 了解法规更新的另一种方法是登录 Lifecycle Services(LCS)，然后使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../includes/footer-banner.md)]