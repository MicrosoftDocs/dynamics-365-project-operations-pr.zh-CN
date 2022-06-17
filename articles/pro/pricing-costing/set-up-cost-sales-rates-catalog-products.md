---
title: 设置目录产品的成本和销售费率 - 精简
description: 本文提供有关如何设置产品目录中的项目的成本和销售费率的信息。
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917381"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>设置目录产品的成本和销售费率 - 精简

_**适用于：** 精简部署 - 估价交易开票_


在 Dynamics 365 Project Operations 中设置产品目录项目的定价与 Dynamics 365 Sales 中相同。

在 Project Operations 中，无法在项目中估计或使用产品，因此无需在项目价目表上为报价单和合同设置产品目录价格。

使用报价单、合同或客户的 **产品价格** 字段设置产品目录价格。 不要在项目价目表中设置产品目录价格。 项目价目表是 Project Operations 独有的。 特定于应用程序的业务逻辑将价目表从报价单复制到合同。 因此会生成特定于合同的项目价目表。 如果报价单上的项目价目表太大，复制操作可能会延迟报价单赢单流程。 不会复制产品价目表来在合同上创建自定义价目表。 因为不涉及复制，所以报价单流程的性能不会受到影响。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]