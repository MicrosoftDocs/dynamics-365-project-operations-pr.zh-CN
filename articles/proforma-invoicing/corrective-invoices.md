---
title: 更正发票
description: 本主题提供有关更正发票的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072772"
---
# <a name="corrected-invoices"></a>更正发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

可以编辑已确认的发票。 编辑已确认的发票时，将创建更正发票的草稿。 因为假设您希望冲销原始发票中的所有交易和数量，所以此更正发票中包含原始发票中的所有交易，并且其中的所有数量均为零 (0)。

当交易不需要更正时，可以将其从草稿纠正发票中删除。 若要仅冲销或返回部分数量，可以编辑明细详细信息中的“数量”字段。 如果打开发票明细详细信息，可以看到原始发票数量。 然后可以编辑当前发票数量，使其比原始发票数量少或多。

确认纠正发票时，将撤消原始已记帐实际销售额，并创建新的已记帐实际销售额。 如果减少了数量，差额将导致也创建一项新的未记帐实际销售额。 例如，如果原始已记帐销售额是八小时的，并且更正发票明细详细信息的减少后数量为六小时，将冲销原始已记帐销售明细，并创建两项新的实际值：

- 六小时的已记帐实际销售额。
- 其余两小时的未记帐实际销售额。 以后可为此交易记帐或标记为非应计费，具体取决于与客户的协商结果。
