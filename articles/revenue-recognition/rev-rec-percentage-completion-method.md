---
title: 固定价格收入估算项目
description: 本主题提供有关项目中固定价格收入的信息。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006415"
---
# <a name="fixed-price-revenue-estimate-projects"></a>固定价格收入估算项目 

_**适用于：** 面向资源/非库存场景的 Project Operations_

当您在 Microsoft Dataverse 上的 Dynamics 365 Project Operations 中创建具有以下属性的项目合同子项时，系统会自动创建固定价格收入估算项目。 此项目中的信息基于以下内容：

  - 固定价格记帐方法。
  - 关联的项目。
  - **项目合同子项** 页上 **账单计划** 选项卡上定义的至少一个里程碑。

## <a name="review-fixed-price-revenue-estimates-projects"></a>查看固定价格收入估算项目
要查看固定价格收入估算项目，请完成以下步骤：

1. 在 Dynamics 365 Finance 环境中，转到 **项目管理和会计** > **项目** > **固定价格收入估算项目**。
2. 选择要查看的项目，并双击 **估算项目 ID**，以打开记录并查看项目的详细信息。
3. 展开 **项目** 选项卡。您将在 **选定的项目** 网格中看到一个项目。 系统使用此项目作为默认项目，因为它是与项目合同子项关联的项目。 
4. 若要更改此关联，请选择其他项目并将其添加到 **选定的项目** 网格中。 如果在此网格中选择了多个项目，则所有选定项目的项目完成百分比和收入估算将一起计算。

  可以手动设置项目成本、收入模板、成本模板和期间代码。 如果未手动设置它们，则使用为项目成本和收入配置文件配置的规则在首次计算项目估算期间默认这些值。



[!INCLUDE[footer-include](../includes/footer-banner.md)]