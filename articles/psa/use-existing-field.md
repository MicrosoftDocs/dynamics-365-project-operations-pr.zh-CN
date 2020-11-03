---
title: 将 Project Service 中的现有字段用作定价维度
description: 此主题介绍如何将现有 Project Service 字段用作定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072682"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>将 Project Service 中的现有字段用作定价维度

Project Service Automation (PSA) 在 **实际值** 实体中有大量字段，可在项目组织中用作基于资源的定价的定价维度。 例如，一个常用字段为 **可预订资源** 。 可记帐资源少于 20-30 个的小型公司可能会发现采用特定于每个资源的记帐费率和成本费率这种方法更简单。 但是，随着可记帐员工数量增多，这可能变得不现实，因为随着资源升级，经验增多或获得其他技能集，资源成本和记帐费率会开始变化。 因为这种方法仍然适用于一定规模的公司，所以请参阅[将可预订资源用作定价维度](bookable-resource-pricing-dimension.md)了解如何将现有 Project Service 字段用作定价维度。

另一个示例是交易类别的。 客户和实施者已在 PSA 中使用交易类别为工作分类和使用此字段根据工作类别定价和设置成本。 有关详细信息，请参阅[将交易类别用作定价维度](transaction-category-pricing-dimension.md)。
