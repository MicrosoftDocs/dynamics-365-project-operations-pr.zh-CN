---
title: 为项目安排资源
description: 如何在 Project Service 中为项目安排资源
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150432"
---
# <a name="schedule-resources-for-a-project-project-service"></a>为项目安排资源 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

可以检查资源可用性以概览资源的预订情况，也可以按技能、团队、位置和其他选项筛选视图。  
  
日程安排板显示资源列表及资源可用性。 选择视图模式将按 **小时**、**日**、**周** 或 **月** 显示可用性。  
  
使用日程安排板之前，请务必设置该板。 有关详细信息，请参阅[配置日程安排板（Field Service 或 Project Service Automation）](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board)。
  
如果在使用早期版本，并且需要了解资源可用性，请参阅[查看资源可用性](../psa/view-resource-availability.md)。  

> [!IMPORTANT]
>  若要使用日程安排板的预订功能、地理编码和位置服务，需要开启地图。  
> 
> 1. 在主菜单中，选择 **资源计划** > **管理**。  
> 2. 单击 **计划参数**。  
> 3. 打开记录，向下滚动到 **Resource Scheduling Optimization** 部分。  
> 4. 在 **连接到地图** 字段中，选择 **是**。  
> 5. 接受条款并保存记录。  
> 6. 在主菜单中，选择 **Project Service** > **日程安排板**。 可在此处通过多种方法手动安排预订要求。 选择适合您的方法。
  
## <a name="find-available-resources"></a>查找可用资源

1.  在 **预订要求** 列表中右键单击未安排的预订并选择以下选项之一：  
  
- 选择 **查找可用性 - 当前资源**，以便从日程安排板中的资源列表查找可用资源。  
- 选择 **查找可用性 - 所有资源**，以便从系统中的资源查找可用资源  
   > [!NOTE]
   >  执行此操作时，筛选器将显示所选预订要求的选项。  
  
2. 看到可用时隙时，在日程安排板中右键单击该时隙，然后选择 **在此处预订**。 或者将预订要求拖放到可用时隙。  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>使用日视图预订资源并查找已预订人员
  
1.  在日程安排板中，选择 **视图模式**，然后选择 **日**。  
  
    下面显示一个网格视图，该视图中是某个资源按天预订了多少小时，哪些天有空。  
  
2.  单击要预订的资源的名称，然后选择 **预订**。  
  
3.  在 **资源预订（创建）** 对话框中，选择要为其预订资源的项目，以及预订方法和开始及结束时间。  
  
4.  完成后，选择 **预订**。  
  
## <a name="view-to-the-schedule-board"></a>查看日程安排板
  
1.  从底部的列表中选择未安排的预订要求。  
  
2.  将预订要求拖到日程安排板中的可用资源/时隙。  
  
3.  完成后，选择 **预订**。  
  
### <a name="additional-resources"></a>其他资源  
 [资源经理指南](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]