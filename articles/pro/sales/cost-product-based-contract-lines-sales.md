---
title: 基于产品的合同子项成本核算 - 精简
description: 此主题提供有关创建的信息
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997325"
---
# <a name="cost-product-based-contract-lines---lite"></a>基于产品的合同子项成本核算 - 精简

_**适用于：** 精简部署 - 估价交易开票_


Dynamics 365 Project Operations 中基于产品的合同子项包括 **成本费** 字段，该字段存储产品的成本费以用于下游利润率计算。

为目录产品创建基于产品的合同子项时，合同子项的成本默认来自产品目录中的 **标准成本** 字段。 产品目录中的 **标准成本** 字段以组织的基础货币设置。 当单位成本默认为合同子项上的值时，它将转换为合同中的销售币种。

## <a name="unit-cost-on-a-product-based-contract-line"></a>基于产品的合同子项中的单位成本

在基于产品的合同子项中提供单位成本可以让一个单位的每个销售显示不同的产品成本。 虽然不是总是有必要这样做，但在某些情况下供应商可能会为客户提供打折的产品成本。 考虑以下情况：

Fabrikam Robotics 正在 Adatum Corporation 的装配线上安装机械臂。 Fabrikam 提供安装服务，但机械臂来自 Trey Research。 如果在 Adatum Corporation 安装机械臂为 Trey Research 开辟了一个新的行业类别，那么他们可能为这笔交易向 Fabrikam 提供特殊折扣。 在这种情况下，Fabrikam 为机械臂创建了基于产品的合同子项。 然后为此合同输入了单位成本。 此成本与 Trey Research 机械臂的成本不同。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]