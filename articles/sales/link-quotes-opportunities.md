---
title: 从商机创建项目报价单
description: 此主题提供有关从商机创建项目报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898521"
---
# <a name="create-project-quotes-from-opportunities"></a>从商机创建项目报价单

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

可通过以下方法从项目商机创建报价单：

- 从**项目商机**页上的**报价单**选项卡
- 从商机销售流程
- 通过更新现有报价单上的商机引用

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>从“项目商机”页上的“报价单”选项卡

要从商机创建项目报价单，请完成以下步骤。

1. 打开**项目商机**页，然后选择**报价单**选项卡。 
2. 在**报价单**子网格中，选择 **+** 基于商机创建新项目报价单。 所有商机明细和相关的项目价目表都将从商机复制到新报价单。

## <a name="from-the-opportunity-sales-process-flow"></a>从商机销售流程

要从商机销售流程创建报价单，请完成以下步骤。

1. 从商机销售流程，打开商机。
2. 选择**授予资格**阶段。 
3. 选择**下一步**，然后选择 **+ 创建**创建新报价单。 此新报价单的**摘要**选项卡上的大多数信息默认来自商机。 
4. 在**摘要**选项卡上输入缺少的所有必需信息，或根据需要更新默认值，
5. 选择**保存**。 新报价单将创建并与商机关联。 现在，您可以在**商机**页的**报价单**选项卡上查看报价单信息。 

   商机销售流程将移至下一阶段**建议**。


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>通过更新现有报价单上的商机引用

现有报价单可以链接到商机。 完成以下步骤更新现有报价单上的商机信息。

1. 打开**报价单**页，选择**摘要**选项卡。
2. 在**商机**字段中，选择要链接到报价单的商机。 您可以在商机的**报价单**网格中查看报价单。 
3. 使用商机销售流程，可以将商机移到下一阶段**建议**。 

   当您将商机移到此阶段时，您可以从与此商机关联的报价单列表中选择此报价单。 选择此报价单表示您正在继续处理它。

   所有与商机关联的其他报价单仍可使用并处于可用状态，直到其中一个赢单。 您可以将销售流程移回上一阶段**授予资格**，然后选择另一个报价单继续处理。
