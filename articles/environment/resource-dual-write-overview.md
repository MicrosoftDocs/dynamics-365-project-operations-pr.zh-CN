---
title: Project Operations 双重写入集成
description: 本主题概述了 Project Operations 双重写入集成。
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582745"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations 双重写入集成概述

_**适用于：** 面向资源/非库存场景的 Project Operations_

Project Operations 使用[双写入功能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)跨 Microsoft Dataverse 和 Dynamics 365 Finance 同步数据。

下图显示了如何作为 Dataverse 和 Finance 之间集成的一部分同步数据。

![Project Operations 数据流概述。](./media/ProjectOperationsFlows.jpg)

Dataverse 上的 Project Operations 提供现代的用户界面 (UI)，并使用 Power Platform 功能提供简便的无代码/低代码可扩展性。 项目经理、资源经理、项目团队成员和其他行政人员在 Dataverse 上的 Project Operations 中执行活动。

Finance 中的 Project Operations 提供项目会计和收入确认支持。 Project Operations 插入了 Finance 中的财务框架，用于销售税计算、货币汇率、财务维度报告等。 项目会计体验主要在 Finance 中。

Project Operations 集成包括以下组件集成：


- [Project Operations 设置和配置数据集成](resource-dual-write-setup-integration.md) 
- [项目估计值和实际值](resource-dual-write-estimates-actuals.md)
- [项目发票](resource-dual-write-project-invoice.md)
- [支出管理](resource-dual-write-expense.md)
- [供应商发票](resource-dual-write-vendor-invoice.md)
