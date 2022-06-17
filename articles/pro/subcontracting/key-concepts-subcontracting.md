---
title: 合同分包中的关键概念
description: 本文解释了适用于 Microsoft Dynamics 365 Project Operations 中的合同分包的一些关键概念。
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927685"
---
# <a name="key-concepts-in-subcontracting"></a>合同分包中的关键概念

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

本文解释了在开始使用 Microsoft Dynamics 365 Project Operations 中的合同分包功能之前您应该了解的一些关键概念。

## <a name="contracting-unit-on-the-subcontract"></a>合同分包中的合同单位

合同单位代表负责最终项目交付的部门或 事务所。 合同单位也是与供应商建立合同关系的部门。

## <a name="purchase-currency"></a>采购货币

在 Project Operations 中，采购货币是创建分包合同所使用的货币。 它也是记录项目分包商成本所用的货币。 采购货币可以不同于项目货币，而项目货币也可以不同于销售货币。

## <a name="billing-methods-on-subcontract-lines"></a>分包合同子项中的记帐方法

对于项目，通常有固定费用和基于消费的合同承包模式。 Project Operations 支持在销售和购买环境中使用这些记帐方法。 对于购买，记帐方法的工作方式如下：

- **时间和材料** - 如果分包合同子项使用 **时间和材料** 记帐方法，那么当分包商处理该项目并记录时间时，会在项目上记录时间成本。 然后，分包商的这些成本交易与供应商发票上的行项匹配。 在此模型中，使用 Project Operations 的项目经理可以将供应商发票行与记录和批准的分包商时间进行匹配和验证。 验证完成后，批准后记录的先前成本实际值被撤销，并对项目创建基于供应商发票的新成本实际值。
- **固定价格** – 在这种固定费用合同模式下，供应商发票基于固定里程碑。 但是，分包商资源也可以报告时间。 然后由项目经理审查和批准该时间。 在获得批准后，Project Operations 会对项目创建临时成本实际值。 供应商发送里程碑发票后，项目经理可以将先前记录的成本实际值与里程碑进行匹配。 完成验证后，成本实际值被撤消，并记录基于里程碑的成本。

## <a name="project-price-lists-on-subcontracts"></a>分包合同中的项目价目表

项目价目表是用于设置时间、支出和其他项目相关组件的采购价格的价目表。 可以有多个价目表，每个价目表在 Project Operations 中都有自己的日期有效分包合同。 Project Operations 不支持分包合同项目价目表上有重叠的生效日期。

## <a name="transaction-classes-on-subcontracts"></a>分包合同中的交易分类

Project Operations 支持四种交易类：

- 时间
- 支出
- 材料
- 费用

只能按 **时间**、**费用** 和 **材料** 交易分类估算和产生购买成本。 **费用** 是一种纯收入性质的交易分类，在购买的内容中不可用。

## <a name="purchase-pricing-dimensions"></a>采购定价维度

定价维度允许您决定哪些属性用于时间交易的购买价格设置和违约。 在采购方面，Project Operations 仅支持用于购买价格设置和违约的固定维度集。 对于分包合同子项和分包时间交易的购买价格设置和违约，属性为 **角色** 和 **可预订资源**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
