---
title: 支出明细
description: 本主题说明如何使用重构的“支出”工作区列出支出明细。
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944115"
---
# <a name="expense-itemization"></a>支出明细

[!include [banner](../includes/banner.md)]

_**适用于：** 面向资源/非库存场景的 Project Operations_

组织通常要求员工提供旅行期间产生的支出的详细明细。 例如，酒店对账单可能包含几条明细行，其中包含入住期间每天发生的房费、税费、停车费和其他杂项支出。 或者，对于餐费，您可能必须提供更详细的早餐、午餐或晚餐明细。 无论组织有何需求，都可以设置每个支出类别，以反映构成支出的子类别或行项目。 虽然 **支出管理** 中始终支持明细，但在启用 **能够快速列出经常性支出明细** 功能后，**重构的支出** 工作区可更高效地列出明细。  

## <a name="enable-quick-itemization"></a>启用快速明细 

您可以使用 **能够快速列出经常性支出明细** 功能快速列出经常性支出明细，同时无需在逗留期间每次都输入日常支出。 完成以下步骤以启用快速明细。

1. 转到 **功能管理** 工作区，在功能列表中，查找并选择 **重新打造支出报表**。 
2. 选择 **立即启用**。 
3. 在功能列表中，查找并选择 **能够快速列出经常性支出明细**。
4. 选择 **立即启用**。 

## <a name="itemization-grid"></a>明细网格 

如果支出类别具有构成该支出的子类别或者其他组件，则可以逐项列出。 若要列出支出明细，请选择支出报表内的支出行，在 **支出详细信息** 窗格中，选择 **操作** > **列出明细**。 **明细** 滑块显示了一个包含字段的网格。 下表提供的示例显示了网格中每个字段，以及该字段在支出报表中的呈现方式。 

|     字段          |     步骤                                                                                  |     示例              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     子类别    |     在 **酒店** 支出类别类型下面配置的子类别列表。             |     每日房费      |
|     开始日期     |     首次发生该支出项的日期。                                           |     2021 年 9 月 13 日           |
|     每日费率     |     支出项产生的金额。                                                    |     200                  |
|     数量       |     连续时间段内重复发生该费用的次数。                       |     3                    |

![列出支出明细。](media/Itemization%20screen%201.png)

保存明细时，您将看到“明细”网格中指定数量的单个明细行。 每行从网格中指定的日期开始。

![明细报表。](media/Itemization%20screen%202.png)
