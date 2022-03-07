---
title: 记录分包组件的时间、支出和材料使用情况
description: 本主题说明 Microsoft Dynamics 365 Project Operations 如何跟踪分包组件项目中记录的时间、费用和材料使用情况。
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902815"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>记录分包组件项目中的时间、支出和材料使用情况

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

本主题说明 Microsoft Dynamics 365 Project Operations 如何跟踪分包组件项目中记录的时间、费用和材料使用情况。

## <a name="costing-for-subcontractor-time-on-projects"></a>分包商项目时间成本估算
在 Project Operations 中，合同工可以像员工一样记录项目时间。 当输入项目和/或项目任务的时间时，合同工可以选择特定的分包合同和分包合同子项。

当合同工提交的时间获得批准时，系统会使用在分包合同采购价目表的 **角色价格** 部分中为该合同工资源设置的单位成本费率来记录项目成本。

## <a name="costing-for-subcontracted-expenses-on-projects"></a>项目分包支出成本估算
当输入项目产生的支出时，您可以为支出条目选择分包合同和分包合同子项。 

提交并批准此支出条目后，系统将根据在分包合同采购价目表的 **类别价格** 部分中为该交易类别设置的单位成本在项目中记录支出成本。

## <a name="costing-for-subcontracted-materials-on-projects"></a>项目分包材料成本估算
当输入项目材料用量时，您可以在材料使用日志中选择分包合同和分包合同子项。 提交并批准此材料使用日志后，系统将根据在分包合同价目表的 **价目表项** 部分中为该产品设置的单位成本在项目中记录材料成本。

也可以在项目中记录目录外产品的材料使用情况。 此类型的材料使用情况也可链接到分包合同和分包合同子项。 在记录目录外产品的材料使用情况时，您需要输入目录外产品的单位成本。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
