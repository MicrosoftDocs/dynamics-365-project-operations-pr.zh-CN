---
title: 设置目录产品的成本和销售费率 - 精简
description: 此主题提供有关如何设置产品目录中各项的成本和销售费率的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764538"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>设置目录产品的成本和销售费率 - 精简

_**适用于：** 精简部署 - 估价交易开票_


在 Dynamics 365 Project Operations 中设置产品目录项目的定价与 Dynamics 365 Sales 中相同。

在 Project Operations 中，无法在项目中估计或使用产品，因此无需在项目价目表上为报价单和合同设置产品目录价格。

使用报价单、合同或客户的 **产品价格** 字段设置产品目录价格。 不要在项目价目表中设置产品目录价格。 项目价目表是 Project Operations 独有的。 特定于应用程序的业务逻辑将价目表从报价单复制到合同。 因此会生成特定于合同的项目价目表。 如果报价单上的项目价目表太大，复制操作可能会延迟报价单赢单流程。 不会复制产品价目表来在合同上创建自定义价目表。 因为不涉及复制，所以报价单流程的性能不会受到影响。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]