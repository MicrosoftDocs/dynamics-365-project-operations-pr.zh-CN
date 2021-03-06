---
title: 商机标题
description: 此主题介绍基于项目的交易和基于项目的商机明细的整体信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906087"
---
# <a name="opportunity-header"></a>商机标题

_**适用于：** 精简部署 - 估价交易开票_

商机标题捕获将应用于基于项目的商机上所有明细的基于项目的交易的综合信息。

Dynamics 365 Project Operations 中基于项目的商机是 Dynamics 365 Sales 中商机的扩展。 这些扩展提供特定于基于项目的商机以及这类商机所需的附加功能。 这些扩展可以包含基于项目的商机中可用的新字段和功能区操作。 您可能会发现 Project Operations 中不可用但 Sales 中可用的一些字段、功能和默认设置逻辑。

下表包括基于项目的商机中的字段，这些字段是 Project Operations 所特有的，或具有对 Sales 中的商机的一些重要的行为更改。

| **字段** | **位置** | **关联性、用途和指导** | **下游影响** |
| --- | --- | --- | --- |
| Type | “常规”选项卡（隐藏） | 此选项集字段具有以下选项：</br>- 基于工作（仅通过 Project Operations 提供）</br>- 基于项目（仅在安装了 Project Operations 和 Sales 时可用）</br>- 基于服务维护（安装 Field Service 后可用） | 当您使用 Project Operations 时，此字段值会自动设置为**基于工作**，将商机分类为基于项目。 商机应该基于项目，以在此交易的下游销售流程中启用所有项目特定的扩展和功能。 |
| 联系人​​ | “常规”选项卡 | 对此交易的客户主要联系人的引用。 | |
| 帐户​​ | “常规”选项卡 | 对客户的公司或客户记录的引用。 | |
| 客户经理 | “常规”选项卡 | 此基于项目的商机的客户经理的姓名。 | 客户经理负责在此项目完成之前管理与客户的关系。 根据与客户经理关联的可预订资源记录，默认设置合同签订部门。 |
| 合同签订部门 | “常规”选项卡 | 负责交付与此交易关联的一个或多个项目的部门。 | 合同签订部门是在交易完成后完成项目的公司部门。 每个合同签订部门都有一种货币，此货币用于报告项目中产生的预估成本和实际成本。 |

商机的**摘要**选项卡上的所有其他字段和部分，请参阅[创建或编辑商机（Sales 和销售中心）](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
