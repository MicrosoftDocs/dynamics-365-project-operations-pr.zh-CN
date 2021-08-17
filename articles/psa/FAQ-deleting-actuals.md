---
title: 为什么我无法从实际值实体中删除记录?
description: 本主题说明为何无法从实际值实体删除记录。
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002860"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>为什么我无法从实际值实体中删除记录?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) 不允许删除实际值，因为实际值充当对下游系统（如总帐）存在财务影响的交易的事实来源。 如果可以删除实际值，则财务报表交易的完整性可能会有问题。 若要建立审核线索，客户应该使用日记帐创建补偿交易。



[!INCLUDE[footer-include](../includes/footer-banner.md)]