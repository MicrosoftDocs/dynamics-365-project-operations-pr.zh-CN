---
title: 基于项目的报价单所特有的概念
description: 本文提供有关 Microsoft Dynamics 365 Project Operations 中的项目报价单的信息。
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824316"
---
# <a name="concepts-unique-to-project-based-quotes"></a>基于项目的报价单所特有的概念

_**适用于：** 面向资源/非库存场景的 Project Operations_

开始在 Microsoft Dynamics 365 Project Operations 中使用项目报价单之前，您应该了解以下关键概念。

## <a name="owning-company"></a>业主公司

负责公司代表负责项目交付的法律实体。 报价单上的客户应该是财务和运营应用中该法人的有效客户。 负责公司的货币与在基于项目的报价单上选择的合同签订部门的货币必须匹配。

## <a name="contracting-unit"></a>合同签订部门

合同签订部门代表负责项目交付的部门或惯例。 您可以为每个合同签订部门设置资源成本。 当您在合同签订部门中为资源指定资源成本时，您可以为向此合同签订部门借用的资源，或企业内的其他部门或惯例设置不同的成本费率。 这些成本费率称为转让价格、资源借入或交换价格。 设置从其他部门借入资源的成本时，您可以设置以借出部门的货币设置成本费率。

## <a name="cost-currency"></a>成本货币

Project Operations 中的成本货币是报告成本所使用的货币。 此货币源自报价单、合同和项目的 **合同签订部门** 字段所附的货币。 可以任何货币针对项目记录成本。 但是，存在从记录的成本货币到项目的成本货币的货币转换。

由于 Dataverse 平台中的汇率不能具有时效性，因此，如果您更新货币汇率，屏幕上的成本总计可能会随时间发生变化。 但是，数据库中记录的成本保持不变，因为金额以发生时所用的货币存储。

## <a name="sales-currency"></a>销售货币

Project Operations 中的销售货币是用于记录和显示预估和实际销售金额的货币。 它还是客户为交易开票所使用的货币。 对于项目报价单，默认销售货币根据客户记录进行设置，可以在创建报价单时进行更改。 但是，保存报价单后，将无法更改销售货币。 默认产品和项目价目表根据报价单的销售货币进行设置。

与成本不同，销售值 **只能** 以销售货币记录。

## <a name="billing-method"></a>计费方法

项目通常具有固定费用和基于使用的合同签订模型。 在 Project Operations 中，项目的合同模式由计费方法表示。 计费方法有两个值：时间和材料以及固定价格。

- **时间和材料** - 这是一个基于使用的合同模型，其中，每个发生的成本都由相应的收入支持。 随着您估算或产生更多成本，相应的估计销售额和实际销售额也将增加。 您可以在具有此计费方法的报价单明细上指定上限。 这样，您可以设定实际收入上限。 估计收入不受上限的影响。
- **固定价格** - 一个固定费用合同模式，其中，销售值将独立于所发生的成本。 销售值是固定的，不会随着您估算或产生更多成本而改变。

## <a name="project-price-lists"></a>项目价目表

项目价目表是用于输入与时间、支出和其他项目相关组件的默认价格（不是成本费率）的价目表。 可以有多个价目表，每个价目表对于每个项目报价单可以有其自己的时效。 Project Operations 不支持项目价目表的重叠日期有效性。

## <a name="product-price-lists"></a>产品价目表

产品价目表是用于输入报价单中基于产品的行的默认价格（不是成本费率）的价目表。 每个报价单只有一个产品价目表。

## <a name="transaction-classes"></a>交易类

Project Operations 支持四种交易类：

- 时间
- 支出
- 材料
- 费用

成本和销售价值可以在 **时间**、**支出** 和 **材料** 交易类别中估算和发生。 **费用** 是仅限收入的交易类别。

## <a name="work-entities-and-billing-entities"></a>工作实体和计费实体

项目和任务是代表工作的实体。 报价单明细和合同子项是代表计费的实体。 您可以通过将不同的工作实体与报价单明细或合同子项相关联来将其链接到计费选项。

## <a name="multi-customer-deals"></a>多客户交易

如果每张发票有多个客户，则会发生多客户交易。 以下是一些典型的示例：

- **原始设备制造商 (OEM) 企业及其合作伙伴** - 合作伙伴和经销商销售包括增值服务的产品。 在与客户进行交易期间，OEM 通常会提出要为项目的一部分提供资金。
- **公共事业项目** - 地方政府的多个部门同意为一个项目提供资金，并根据先前商定的拆分方式开票。 例如，学区和城市或地方政府部门同意为修建游泳池提供资金。

## <a name="invoice-schedules"></a>发票计划

发票计划特定于每个报价单明细，并且是可选的。 发票计划根据特定开始和完成日期以及开票频率创建。 配置自动发票创建流程后，在合同阶段使用这些计划。 在报价单阶段，发票计划是可选的。 如果在报价单阶段创建发票计划，它们会被复制到项目报价单赢单时创建的项目合同中。

## <a name="differences-from-dynamics-365-sales-quotes"></a>与 Dynamics 365 Sales 报价单的差异

Project Operations 报价单基于 Dynamics 365 Sales 报价单构建。 但是，应注意一些重要的功能差异：

- Project Operations 报价单有两种不同类型的明细：一个用于项目，一个用于产品。
- Project Operations 报价单具有自己的页面和用户界面 (UI) 元素、业务规则、插件中的业务逻辑以及客户端脚本，这些让它们区别于 Sales 报价单。
- 在 Sales 中，可以向一个销售报价单附加多个订单。 在 Project Operations 中，只能向一个项目报价单附加一个项目合同。
- 当您赢得销售报价单时，相关商机可以保持打开状态。 项目报价单赢单后将结束相关商机。
- 销售报价单中不包含项目报价单中所包含的一些字段和概念。 这些字段包括 **合同签订部门**、**客户经理** 和 **帐单邮寄地址联系人姓名**。
- 可以通过基于选项集的 **类型** 字段来识别销售报价单和项目报价单。 对于销售报价单，此字段的值 **基于物料**。 对于项目报价单，此值 **基于工作**。

由于存在这些差异，我们不建议您交替使用销售报价单和 Project Operations 报价单。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
