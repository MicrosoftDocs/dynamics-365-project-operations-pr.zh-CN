---
title: 设置目录产品的成本和销售费率 - 精简
description: 此主题提供有关如何设置产品目录中各项的成本和销售费率的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176690"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>设置目录产品的成本和销售费率 - 精简

_**适用于：** 精简部署 - 估价交易开票_


在 Dynamics 365 Project Operations 中为产品目录项设置定价与在 Dynamics 365 Sales 中相同。

由于无法在 Project Operations 中的项目中估算或使用产品，因此无需在报价单和合同的项目价目表中设置产品目录价格。

应在报价单、合同或客户的 **产品价格** 字段中设置产品目录价格。 不要在这些实体的项目价目表中设置产品目录价格。 项目价目表是 Project Operations 独有的。 存在将价目表从报价单复制到合同的特定于应用程序的业务逻辑。 因此会生成特定于合同的项目价目表。 如果报价单上的项目价目表太大，复制操作可能会延迟报价单赢单流程。 不会复制产品价目表来在合同上创建自定义价目表。 这意味着产品价目表不会影响报价单赢单流程的性能。
