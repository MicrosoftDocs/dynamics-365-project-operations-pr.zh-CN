---
title: 从日程安排板创建项目预订
description: 此主题介绍如何从日程安排板创建项目预订。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146517"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>从日程安排板创建项目预订

[!include [banner](../includes/psa-now-project-operations.md)]

您可以直接在项目的 **团队** 选项卡上，或通过从通用团队成员分派生成资源要求，然后使用项目团队成员来满足生成的要求，来将资源预订到项目。

您还可以直接从日程安排板将资源预订到项目。 可通过三种方法执行此操作：

- **从已生成的资源要求预订：** 可以在创建通用资源并在项目内分派任务之后生成资源要求。

- **从主要要求预订：** 主要要求在日程安排板的 **项目** 选项卡中显示。 

- **从新资源要求预订：** 可以从头开始创建资源要求并将其与项目关联。 在日程安排板上，此资源要求显示在 **未解决的要求** 选项卡上。

## <a name="book-from-a-generated-resource-requirement"></a>从已生成的资源要求预订

您可以在项目内创建通用资源并向其分派一项或多项任务。 然后，您可以从通用团队成员生成资源要求。 

1.  在日程安排板上，此资源将显示在 **未解决的要求** 选项卡上。如果您有很多未解决的要求，您可能需要在网格上使用列筛选器。 

    ![日程安排板上的“未解决的要求”选项卡](media/FAQ-Project-Booking-Schedule-Board-1.png "预订和分派表的屏幕截图")

2. 选择此要求。 **查找可用性** 选项卡将显示在所选行的顶部。
 
3. 选择此选项卡时，将打开日程安排板的日程安排助理模式，然后筛选满足资源要求的可用资源。 之后，可以预订资源。

4. 您还可以将选定行从日程安排的底部拖放到上面网格中的资源单元格中。 当您放下要求时，它将在右侧打开 **创建资源预订** 面板。

    选择 **预订** 将资源预订到项目团队中。

![“创建资源预订”面板](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>从主要要求预订

在 Project Service 中创建项目将自动创建名为“主要要求”的资源要求。 这是用于通过日程安排板快速预订资源的空要求，既不生成要求，也不从头创建要求。 由于要求是空的，您将需要指定日期以及分配方法和时数（如果适用）。 

1. 若要使用“主要要求”预订资源，在日程安排板上选择 **项目** 选项卡。如果您有很多项目，您可能需要使用 **项目** 列的列筛选器。

   ![日程安排板上的列筛选器](media/FAQ-Project-Booking-Schedule-Board-2.png "预订和分派表的屏幕截图")

2. 选择仅将项目名称作为其名称且持续时间为零 (0) 的要求。

3. 选择行上显示的 **查找可用性** 选项卡。 这会让日程安排板进入“日程安排助理模式”，并显示可以预订到项目的可用资源。

4. 由于 **主要要求** 是持续时间为零 (0) 的空要求，您需要在选择和预订资源时在 **创建资源预订** 面板上设置持续时间。

5. 您还可以在日程安排板底部选择 **项目主要要求**，并将其拖放到资源上以进行预订。
 
    由于 **主要要求** 是持续时间为零 (0) 的空要求，所以您需要在选择和预订资源时在 **创建资源预订** 面板上设置持续时间。
 
    在通过日程安排板上的 **主要要求** 预订资源时，您将其添加到项目团队，而无需进行任何分派。
 
## <a name="book-from-a-new-resource-requirement"></a>从新资源要求预订
完成以下步骤从新资源要求预订。 

1. 转到 **资源要求**，然后选择 **新建** 创建新的资源要求。

2. 在 **项目** 选项卡上，选择一个项目以关联该项目的要求。
 
    在日程安排上，这个新要求显示为您可以满足的 **未解决的要求**。

3. 预订资源以将其添加到项目团队。

4. 现在资源已经预订，您必须手动分派任务。



[!INCLUDE[footer-include](../includes/footer-banner.md)]