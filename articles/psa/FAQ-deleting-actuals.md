---
title: 为什么我无法从实际值实体中删除记录?
description: 本主题说明为何无法从实际值实体删除记录。
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286057"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="62a87-103">为什么我无法从实际值实体中删除记录?</span><span class="sxs-lookup"><span data-stu-id="62a87-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="62a87-104">Project Service Automation (PSA) 不允许删除实际值，因为实际值充当对下游系统（如总帐）存在财务影响的交易的事实来源。</span><span class="sxs-lookup"><span data-stu-id="62a87-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="62a87-105">如果可以删除实际值，则财务报表交易的完整性可能会有问题。</span><span class="sxs-lookup"><span data-stu-id="62a87-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="62a87-106">若要建立审核线索，客户应该使用日记帐创建补偿交易。</span><span class="sxs-lookup"><span data-stu-id="62a87-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]