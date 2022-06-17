---
title: 将日程安排板配置为显示合同工和分包产能
description: 本文介绍如何将 Microsoft Dynamics 365 Project Operations 中的日程安排板配置为在为项目资源要求配备人员时显示分包资源产能。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919819"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>将日程安排板配置为显示合同工和分包产能 

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Microsoft Dynamics 365 Project Operations 中的日程安排板可以通过两种方式搜索资源：

- 常规资源搜索，没有任何基于项目的特定资源要求的上下文。
- 要求特定的资源搜索，其中项目要求将提供有关建议的资源的上下文。

若要将分包资源产能和合同工通知给日程安排板，您需要更新日程安排板设置。 这些更新包括： 
- 为常规资源搜索更新日程安排板设置。
- 为基于要求的资源搜索更新日程安排板设置。

## <a name="update-schedule-board-settings-for-general-resource-search"></a>为常规资源搜索更新日程安排板设置
### <a name="update-filters-for-general-resource-search"></a>更新常规资源搜索的筛选器
在搜索资源时，应更新日程安排板上可用的筛选器，以便也可以通过指定以下任意或所有内容来搜索外部资源：
  - 工作人员类型，无论显示的资源应为合同工还是员工。
  - 资源应该属于的供应商公司。
  - 属于特定分包合同或分包合同子项的资源。
    
### <a name="update-retrieve-resource-query"></a>更新检索资源查询
还应该更新用于搜索的查询，以使用这些附加的筛选器属性。 使用以下步骤为常规资源搜索更新日程安排板配置：  
1. 打开特定日程安排板的 **日程安排板设置**。
2. 打开 **常规设置** 选项卡，然后滚动到 **其他设置**。
3. 在本节内的设置列表中，将 **筛选器布局** 更新为 **Project Operations Lite 的默认筛选器布局**。
4. 将 **检索资源查询** 更新为 **Project Operations Lite 的默认检索资源查询**。

![为常规资源搜索更新日程安排板设置](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>为基于要求的资源搜索更新日程安排板设置
### <a name="update-filters-for-requirement-specific-resource-search"></a>更新要求特定资源搜索的筛选器 
在搜索资源时，应更新日程安排板上可用的筛选器，以便也可以通过指定以下任意或所有内容来搜索外部资源：
 - 工作人员类型，无论显示的资源应为合同工还是员工。
 - 资源应该属于的供应商公司。
 - 属于特定分包合同或分包合同子项的资源。

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>更新要求特定资源搜索的检索资源查询 
还应该更新用于搜索的查询，以使用这些附加的筛选器属性。 使用以下步骤为基于要求的资源搜索更新日程安排板配置：

1. 打开特定日程安排板的 **日程安排板设置**，然后选择 **打开默认设置**，以打开特定于要求的搜索的设置。
2. 打开 **常规设置** 选项卡，然后滚动到 **其他设置**。
3. 在本节内的设置列表中，将 **筛选器布局** 更新为 **Project Operations Lite 的默认筛选器布局**。
4. 将 **检索资源查询** 更新为 **Project Operations Lite 的默认检索资源查询**。
5. 打开 **日程安排类型** 选项卡并转到 **项目**。
6. 在 **项目** 设置下，将 **日程安排助理检索资源查询** 更新为 **Project Operations 精简版的默认检索资源查询**，将 **日程安排助理检索约束查询** 更新为 **Project Operations Lite 的默认检索约束查询**。

![为基于要求的资源搜索更新日程安排板设置](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
