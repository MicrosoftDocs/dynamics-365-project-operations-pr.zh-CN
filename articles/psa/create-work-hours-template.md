---
title: 创建工作时间模板
description: 本主题介绍如何在 Project Service 中创建工作时间模板。
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598937"
---
# <a name="create-a-work-hours-template-project-service"></a>创建工作时间模板 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

若要创建和管理项目，必须将日历模板应用于该项目。 日历模板定义以下项目属性：

- 工作时数，包括开始和结束时间
- 工作天数
- 日历例外（如非工作日）

应用于项目的日历模板是组织设置中定义的日历模板的副本。

> [!NOTE]
> 如果更改日历模板，这些更改不会传播到项目的工作时间。 要更改项目的工作时间，必须应用新的模板。

要为您的组织创建日历模板，有两个关键要求：

- 使用新的或现有的可预订资源定义模板的所需工作时间。
- 创建一个新的日历模板，将该模板与可预订资源相关联。

**定义模板的工作时间**

1. 转到 **资源**\>**资源**。
2. 创建要在日历模板中引用的新资源，或选择一个现有资源。
3. 选择资源的 **工作时间** 选项卡，完成[为资源设置工作时间](/dynamics365/field-service/set-work-hours-resource)中的说明配置日历规则。

**创建新的日历模板**

1. 转到 **设置** \> **日历模板**。
2. 选择 **新建**，输入名称、说明和模板资源。


> [!NOTE]
> 在日历模板中引用资源时，该资源的日历的副本将与日历模板相关联。 如果所复制模板的工作时间发生更改，这些更改不会传播到日历模板。


### <a name="see-also"></a>另请参阅  
 [设置资源](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
