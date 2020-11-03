---
title: 为什么我无法从实际值实体中删除记录?
description: 本主题说明为何无法从实际值实体删除记录。
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072730"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="06aa3-103">为什么我无法从实际值实体中删除记录?</span><span class="sxs-lookup"><span data-stu-id="06aa3-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="06aa3-104">Project Service Automation (PSA) 不允许删除实际值，因为实际值充当对下游系统（如总帐）存在财务影响的交易的事实来源。</span><span class="sxs-lookup"><span data-stu-id="06aa3-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="06aa3-105">如果可以删除实际值，则财务报表交易的完整性可能会有问题。</span><span class="sxs-lookup"><span data-stu-id="06aa3-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="06aa3-106">若要建立审核线索，客户应该使用日记帐创建补偿交易。</span><span class="sxs-lookup"><span data-stu-id="06aa3-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

