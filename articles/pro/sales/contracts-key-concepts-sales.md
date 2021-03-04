---
title: 项目合同 - 关键概念 - 精简
description: 此主题提供有关项目合同的关键概念的信息。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3381707457ef35ff604c716592afd8382b98ad5d
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643027"
---
# <a name="project-contracts---key-concepts---lite"></a>项目合同 - 关键概念 - 精简

_**适用于：** 精简部署 - 估价交易开票_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题提供了在 Dynamics 365 Project Operations 中开始使用项目合同之前要了解的关键概念：

## <a name="contracting-unit"></a>合同签订部门

合同签订部门代表负责项目交付的部门或惯例。 您可以为每个合同签订部门设置资源成本。 当您指定资源的资源成本时，您还可以为资源设置不同成本费率。 此合同签订部门借用来自企业内其他部门或惯例的这些资源。 资源的成本费率称为转让价格、资源借入或交换价格。 设置从其他部门借入资源的成本费率时，应使用借出部门的货币。

## <a name="cost-currency"></a>成本货币

成本货币是在屏幕上报告成本使用的货币。 此货币源自合同和项目的 **合同签订部门** 字段所附的货币。 可以任何货币针对项目记录成本。 但是，在屏幕上显示时，存在从记录的货币成本到项目的成本货币的货币转换。

由于 Common Data Service (CDS) 平台中的汇率不能具有时效性，因此，如果您更新货币汇率，屏幕上的成本总计可能会随时间发生变化。 但是，数据库中记录的成本保持不变，因为金额以发生时所用的货币存储。

## <a name="sales-currency"></a>销售货币

Project Operations 中的销售货币是用于记录和显示预估和实际销售金额的货币。 销售货币还是客户为交易开票所使用的货币。 在项目合同上，销售货币默认来自客户记录，可以在创建合同时进行更改。 当通过作为赢单结束报价单创建合同时，合同中的货币会默认为报价单上的货币。

当您从头创建项目合同时，**销售货币** 字段无法编辑。 产品和项目价目表默认基于合同上的此货币。

与成本不同，销售值只能以销售货币记录。

## <a name="billing-method"></a>记帐方法

通常，项目的合同签订模型有两种：固定费用和基于使用。 在 Project Operations 中，这些模型表示为具有两个可能值的计费方法：

- 时间和材料：基于使用的合同签订模型，其中，每个发生的成本都由相应的收入支持。 随着您估算或产生更多成本，相应的估计销售额和实际销售额也将增加。 在具有此限定实际收入的计费方法的合同子项上指定上限。 估计收入不受上限的影响。
- 固定价格：一个固定费用合同签订模型，指示销售值将独立于所产生的成本。 销售值是固定的，不会随着您估算或产生更多成本而改变。

## <a name="project-price-lists"></a>项目价目表

项目价目表用于提供时间、支出和其他项目相关组件的默认价格（不是成本费率）。 可以有多个价目表。 每个价目表对每个项目合同有自己的时效。 Project Operations 不支持项目价目表上有重叠的有效期。

当通过赢得项目报价单创建项目合同时，将复制项目价目表，其中包含合同名称和日期。 复制此信息将构成此项目合同上项目组件的自定义定价。

## <a name="product-price-lists"></a>产品价目表

产品价目表用于提供合同中基于产品的明细的默认价格（不是成本费率）。 每个合同只有一个产品价目表。

## <a name="transaction-classes"></a>交易类

Project Operations 支持四种交易类：

- 时间
- 支出
- 材料
- 费用

成本和销售值可以基于时间、支出和材料交易类预估和生成。 费用属于仅收入交易类。

## <a name="work-entities-and-billing-entities"></a>工作实体和计费实体

代表工作的实体是项目和任务。 代表计费方面的实体是合同子项。 您可以通过将不同的工作实体与合同子项相关联来将其与计费选项关联。

## <a name="multi-customer-deals"></a>多客户交易

多客户交易在一个交易中有多个客户要开票。 常见示例包括：

- OEM 企业及其合作伙伴：合作伙伴和经销商销售包含一些增值服务的产品，通常涉及与客户的特定交易。 OEM 提出要为项目的一部分提供资金。 

- 公共事业项目：地方政府的多个部门同意为一个项目提供资金，并根据先前商定的拆分方式开票。 例如，学区和地方政府同意为修建游泳池提供资金。

## <a name="invoice-schedules"></a>发票计划

发票计划特定于每个合同子项，是使用自动开票的必需条件。 发票计划根据特定开始和完成日期以及开票频率创建。 在配置自动发票创建流程时，在合同阶段使用此计划。 从报价单创建项目合同时，会将发票计划从报价单复制到项目合同。

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Dynamics 365 Sales 合同的更改

Project Operations 合同基于 Dynamics 365 Sales 合同构建。 但是，应注意一些重要的功能偏差和差异：

- Project Operations 合同有两种不同类型的明细，一个用于项目，一个用于产品。
- Project Operations 合同具有自己的窗体和 UI 元素、业务规则、插件中的业务逻辑以及客户端脚本，这些让它们区别于 Sales 合同。

出于这些原因，您不应该交换使用销售合同和项目合同。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]