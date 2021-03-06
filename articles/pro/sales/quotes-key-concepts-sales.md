---
title: 项目报价单关键概念
description: 此主题提供有关在 Project Operations 中使用项目报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896270"
---
# <a name="project-quote-key-concepts"></a>项目报价单关键概念

_**适用于：** 精简部署 - 估价交易开票_


以下是在 Dynamics 365 Project Operations 中开始使用项目报价单之前要知道的关键概念：

## <a name="contracting-unit"></a>合同签订部门

合同签订部门代表负责项目交付的部门或惯例。 您可以为每个合同签订部门设置资源成本。 当您在合同签订部门中为资源指定资源成本时，您还可以为向此合同签订部门借用的资源，或企业内的其他部门或惯例设置不同的成本率。 这些称为转让价格、资源借入或交换价格。 设置从其他部门借入资源的成本时，您还可以选择以借出部门的货币设置这些成本率。

## <a name="cost-currency"></a>成本货币

Project Operations 中的成本货币是报告成本使用的货币。 此货币源自报价单、合同和项目的**合同签订部门**字段所附的货币。 可以任何货币针对项目记录成本。 但是，存在从记录的货币成本到项目的成本货币的货币转换。

由于 CDS 平台中的汇率不能具有时效性，因此，如果您更新货币汇率，屏幕上的成本总计可能会随时间发生变化。 但是，数据库中记录的成本保持不变，因为金额以发生时所用的货币存储。

## <a name="sales-currency"></a>销售货币

Project Operations 中的销售货币是用于记录和显示预估和实际销售金额的货币。 它还是客户为交易开票所使用的货币。 在项目报价单上，销售货币默认来自客户记录，可以在创建报价单时进行更改。 保存报价单后，将无法更改销售货币。 产品和项目价目表默认基于报价单的销售货币。

与成本不同，销售值只能以销售货币记录。

## <a name="billing-method"></a>计费方法

项目通常具有固定费用和基于使用的合同签订模型。 这在项 Project Operations 中以**计费方法**表示，其具有两个值：时间和材料与固定价格。

- **时间和材料：** 这是一个基于使用的合同模型，其中，每个发生的成本都由相应的收入支持。 随着您预估或产生更多成本，相应的预估销售额和实际销售额也将增加。 您可以在具有此计费方法的报价单明细上指定上限。 这会限制实际收入。 预估收入不受上限的影响。
- **固定价格：** 这是一个固定费用合同模型，指示销售值将独立于所产生的成本。 销售值是固定的，不会随着您预估或产生更多成本而改变。

## <a name="project-price-lists"></a>项目价目表

项目价目表是用于与时间、支出和其他项目相关组件的默认价格（不是成本率）的价目表。 可以有多个价目表，每个价目表对于每个项目报价单可以有其自己的时效。 Project Operations 不支持项目价目表上有重叠的有效期。

## <a name="product-price-lists"></a>产品价目表

产品价目表是用于报价单中基于产品的行的默认价格（不是成本率）的价目表。 每个报价单只有一个产品价目表。

## <a name="transaction-classes"></a>交易类

Project Operations 支持四种交易类：

- 时间
- 支出
- 材料
- 费用

成本和销售值可以基于时间、支出和材料交易类预估和生成。 费用属于仅收入交易类。

## <a name="work-entities-and-billing-entities"></a>工作实体和计费实体

代表工作的实体是“项目”和“任务”。 代表计费的实体是“报价单明细”和“合同子项”。 您可以通过将不同的工作实体与报价单或合同子项相关联来将其链接到计费选项。

## <a name="multi-customer-deals"></a>多客户交易

如果有多个客户要开票，则会发生多客户交易。 常见的示例包括：

- **OEM 企业及其合作伙伴：** 合作伙伴和经销商销售具有增值服务的产品。 这通常是在与客户进行特定交易期间，OEM 提供为项目的一部分提供资金时出现的场景。 

- **公共事业项目：** 地方政府的多个部门同意为一个项目提供资金，并根据先前商定的拆分方式开票。 例如，学区和城市或地方政府部门同意为修建游泳池提供资金。

## <a name="invoice-schedules"></a>发票计划

发票计划特定于每个报价单明细，也是可选的。 发票计划根据特定开始和完成日期以及开票频率创建。 在配置自动发票创建流程时，在合同阶段使用发票计划。 在报价单阶段，此计划是可选的。 在**报价单**阶段创建发票计划后，它们将被复制到报价单赢单时创建的项目合同中。

## <a name="changes-from-dynamics-365-sales-quote"></a>与 Dynamics 365 Sales 报价单的差异：

Project Operations 报价单基于 Dynamics 365 Sales 报价单构建。 但是，应注意一些重要的功能差异：

- 不支持**修订**和**激活**操作。
- Project Operations 报价单有两种不同类型的明细。 一种用于项目，另一种用于产品。
- Project Operations 报价单具有自己的窗体和 UI 元素、业务规则、插件中的业务逻辑以及客户端脚本，这些让它们区别于 Sales 报价单。

由于这些原因，建议不要交替使用 Sales 报价单和 Project Operations 报价单。
