---
title: 产品目录定价
description: 此主题介绍 Dynamics 365 Project Service Automation (PSA) 中的产品目录定价工作原理。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3fb9b51d58cbe3b0db6dad902461b90ac04cc42f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151197"
---
# <a name="product-catalog-pricing"></a>产品目录定价 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


价目表和价目表明细实体支持产品目录定价。 此功能通常用于项目报价单和项目合同中基于目录的明细。

对于基于项目的明细，合同在赢单后表示交易。 由于协商流程通常在赢单前，所以始终将附加到报价单的定价照原样复制到新价目表和附加到合同。 新价目表的更改不能超出合同的范围。 此项限制有助于保护从基础价目表中进行的任何价格更改协商而来的费率卡。

应该设置产品，以使其在产品目录中具有默认成本和价目表。 必须使用价目表、标准成本和当前成本来配置默认成本和价目表。 仅当系统在报价单或项目合同的产品价目表中找不到该产品的价目表明细时，才为报价单明细或项目合同子项使用默认价目表。

报价单之间可以更改产品目录明细的价目表。 这种功能非常重要，因为如果不能准确跟踪成本，则不能确定项目协定的运营利润。 默认情况下，产品的标准成本用作成本费。 但是，如果该报价单有其他成本费，则可以更新报价单明细中的默认成本费。

## <a name="price-list-items"></a>价目表项

可将产品目录中的产品添加到不同价目表中。 产品的价目表明细始终引用特定单位。 可以将价目表项中的产品的定价配置为货币金额。 也可以将其配置为定价、当前成本或标准成本的函数。

PSA 支持在将价格配置为定价、标准成本或当前成本时使用各种舍入选项。 除了利用多种定价方法和舍入选项，还可以将折扣表与价目表项关联。 

> ![将目录中的产品添加到不同价目表中](media/basic-guide-16.png)

通过选择 **项目报价单** 页中的 **创建自定义报价** 为报价单创建新的自定义价目表时，PSA 将创建该价目表的备份，并将新价目表标头中的 **实体** 字段设置为 **销售实体**。 将为新价目表的名称追加报价单名称和时间戳。 也可以在自定义工作流中使用新价目表的名称和报价单的名称对使用自定义定价的报价单触发额外审阅和审批。

 
## <a name="default-product-price-list"></a>默认产品价目表
每个客户记录都有一个 **默认价目表** 字段，可在其中指定与客户的货币匹配的价目表。 在 PSA 中，不会在此字段中自动输入默认值。 如果有与特定客户达成的自定义定价协议，可使用此字段为该客户关联价目表。

商机、报价单和项目合同实体按照以下顺序输入默认产品价目表。 项目价目表也采用相同的顺序。

1.  报价单
2.  商机
3.  客户
4.  PSA 的全局设置

默认情况下，报价单明细中的 **产品** 字段列出报价单的产品价目表中的所有可用产品。 如果已停用某个产品，或者该产品是草稿产品，则不列出该产品，即使价目表中有此产品。 

产品目录明细作为发票明细添加到为项目合同创建的第一份发票中。 在草稿发票中，可以删除这些发票明细。 在此情况下想，这些发票将在后续发票中出现，直到为其开票或将发票发给客户。 在 PSA 中，不能为产品发票明细的部分数量开票。 为项目合同中的产品明细开票时，将创建实际值。 但是，不将这些实际值链接到相关项目实体。 换句话说，基于产品的项目合同明细独立于任何基于项目的使用。 PSA 不跟踪项目的材料消耗。


[!INCLUDE[footer-include](../includes/footer-banner.md)]