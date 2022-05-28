---
title: 2021 年第 2 波抢先体验版 - Project Operations 精简部署中的新增功能
description: 本主题提供有关 2021 年第 2 波抢先体验发行版的 Project Operations 精简部署中提供的功能的信息。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723665"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>2021 年第 2 波抢先体验版 - Project Operations 精简部署中的新增功能

_适用范围：精简部署 - 估价交易开票_

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

  - Dataverse 环境中的 Project Operations 版本 4.23.0.4

仅当环境已[选择加入抢先体验](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates)，才应用此版本。

## <a name="features-included-in-this-release"></a>此版本中包括的功能

[分包合同管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - 此功能为项目工作的所有方面提供更好的可见性和控制。 分包合同管理预览版中包含以下功能：

  - 项目经理可以创建与供应商之间的分包合同。 默认情况下，附加到供应商记录的价目表用于分包合同。 供应商客户具有 **供应商** 或 **提供商** 关系类型。
  - 项目经理可以将所有采购作为分包合同的行项逐项列出。 分包合同子项可以用于时间、支出或产品。 分包合同子项的交易分类决定了子项所用于的内容。
  - 供应商客户经理和项目经理可以迭代分包合同。 可以在附加到分包合同的采购价目表中调整定价。
  - 在流程中，如果分包合同子项用于时间，则供应商客户经理可以将供应商联系人与每个分包合同子项相关联。 该关联向处理分包合同的项目经理提供信息。 当供应商联系人与分包合同子项关联时，如果可预订的资源尚不存在，系统会自动根据联系人创建可预订的资源。
  - 每个分包合同子项中的记帐方法可以是固定价格或时间和材料。 对于固定价格分包合同子项，将设置基于里程碑的发票计划。
