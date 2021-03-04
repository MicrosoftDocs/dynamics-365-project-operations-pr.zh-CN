---
title: 创建手动估价发票 - 精简
description: 此主题提供在 Project Operations 中创建手动估价发票的信息。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764492"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>创建手动估价发票 - 精简

_**适用于：** 精简部署 - 估价交易开票_

在 Dynamics 365 Project Operations 中，可以根据需要手动创建估价发票。 您可以从 **项目合同** 列表页或 **项目合同** 详细信息页手动创建估价发票。

##  <a name="project-contracts-list-page"></a>项目合同列表页

在 **项目合同** 列表页上，选择一个或多个项目合同，然后为所有选定记录创建发票。

系统将检查所选的项目合同中哪些合同有日期在当天日期之前的 **可开票** 积压。 从这些合同，系统会创建草稿估价发票。 如果项目合同有多个客户，可能会为每个客户创建一个发票，每个项目合同有多个发票。

所有创建的项目发票都在 **销售** 区域 **记帐** 部分的 **发票** 页上提供。

## <a name="project-contract-details-page"></a>项目合同详细信息页

估价发票也可以从 **项目合同** 详细信息页面创建。 系统将验证项目合同是否有日期在当天日期之前的 **可开票** 积压。 从这些合同，系统会基于每个合同子项上的客户数量创建草稿估价发票。

创建了单个估价发票时，**发票** 页将打开。 如果为该项目合同创建了多个发票，将打开 **发票** 列表页以显示所有已创建的发票。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]