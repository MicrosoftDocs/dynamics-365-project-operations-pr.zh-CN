---
title: 定义项目日历
description: 此主题提供有关使用项目日历跟踪项目计划的信息。
author: ruhercul
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072778"
---
# <a name="define-project-calendars"></a>定义项目日历

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

若要创建项目计划，请创建一个项目日历模板，用于定义每天的工时数和节假日。 若要创建项目日历模板，请将工作模板与项目的 **日历模板** 字段关联。 执行以下步骤创建一个工作模板。

1. 在左侧导航窗格中选择 **资源** 。 
2. 在 **资源** 列表页中，打开一条用户记录，然后选择 **显示工时** 。

  > [!NOTE]
  > 确保浏览器页中允许弹出窗口。 这样您就可以查看为资源设置的工时。
  
3. 在 **月视图** 选项卡中，选择 **设置** 。 将显示三个选项的列表： 

  - 新建周计划
  - 一天的工作计划
  - 休息时间

4. 选择 **新建周计划** ，然后为此资源计划设置选项。 可设置定期周计划、日工时参数、节假日等。
5. 设置日期范围，选择 **保存** ，然后选择 **关闭** 。 
6. 回到 **资源** 列表页，然后选择要为其设置工时的资源。 
7. 选择 **日历设置为** 以设置工作模板。 
8. 在 **工作模板** 对话框中，输入工作模板的名称，然后选择 **应用** 。 

现在可将此工作模板与项目日历模板关联。
