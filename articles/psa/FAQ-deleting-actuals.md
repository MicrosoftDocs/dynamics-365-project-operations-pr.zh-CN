---
title: 为什么我无法从实际值实体中删除记录?
description: 本文说明为何无法从实际值实体删除记录。
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925569"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>为什么我无法从实际值实体中删除记录?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) 不允许删除实际值，因为实际值充当对下游系统（如总帐）存在财务影响的交易的事实来源。 如果可以删除实际值，则财务报表交易的完整性可能会有问题。 若要建立审核线索，客户应该使用日记帐创建补偿交易。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
