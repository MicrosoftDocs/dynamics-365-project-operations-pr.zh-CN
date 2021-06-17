---
title: 创建时间条目
description: 此主题介绍如何创建时间条目。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999255"
---
# <a name="create-time-entries"></a>创建时间条目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 早期版本中，时间条目以周为基础输入。 在 Project Service Automation 版本 3 中，时间条目基于日输入。 但是，输入了一些时间条目之后，可以批量创建或复制。

## <a name="create-a-time-entry"></a>创建时间条目

执行以下步骤创建一个时间条目。

1. 在 **时间条目** 页上，选择 **新建**。
2. 在 **快速创建:时间条目** 对话框中，输入以分钟、小时或天为单位的时间条目持续时间。 持续时间必须采用下面的格式输入持续时间：*x* 分钟、*x* 小时或 *x* 天。 小时和天数也可以采用小数值输入；例如，*x.x* 小时或 *x.x* 天。
3. 选择时间条目的类型和输入的时间条目所属项目。
4. 在 **项目任务** 字段中，找到此时间条目的任务。

    > [!NOTE]
    > 如果要为尚未分派给用户的任务创建时间条目，请在 **项目任务** 字段中依次选择 **搜索** 按钮、**更改视图** 和 **所有可用的项目任务** 列出所有任务。

5. 如果需要描述，输入描述，然后选择 **保存并关闭**。

创建并保存时间条目之后，可以在时间条目网格中编辑。 时间条目网格支持两种格式：

- 可以输入 **hh:mm** 格式的时间条目。 然后会将此格式转换为小时数加小数部分。
- 也可以直接输入小时数加小数部分。

请注意，小时的小数部分不是分钟。 因此，1.5 小时指的是 1 小时 30 分钟。 同样的规则也适用于天的小数部分。 一天是 24 小时，所以 0.5 天是 12 小时。

## <a name="bulk-create-time-entries"></a>批量创建时间条目

创建一些时间条目之后，可以复制这些时间条目以批量创建更多时间条目。

1. 在 **时间条目** 页上，选择 **复制周**。
2. 在 **开始期间** 字段组的 **开始日期** 和 **结束日期** 字段中，定义要复制的时间条目所属日期范围。
3. 在 **目标期间** 字段组 **开始日期** 字段内，指定要为其创建时间条目的日期。
4. 选择 **复制** 创建与 **结束期间** 字段组中指定的星期几对应的时间条目的副本。 例如，将把上周星期一的时间条目复制到在 **结束期间** 字段组中指定的周的星期一。

## <a name="import-data-for-time-entries"></a>为时间条目导入数据

可以从项目预订和分派导入数据。 导入数据时，可以指定要导入的预订的日期范围，然后明确选择应该作为 **草稿** 时间条目创建的预订。

## <a name="group-by-sort-search-and-filter-capabilities"></a>分组依据、排序、搜索和筛选功能

可以按列中指定的维度对时间条目进行分组和筛选。 在 **分组依据** 字段中选择要用于筛选时间条目的维度。 也可以使用列标题中的排序箭头按升序或降序为时间条目记录排序。 此外，还可以显示或隐藏条目，方法是选择列标题中的 **筛选** 按钮，然后在 **搜索** 框中输入应该用于按项目名称、项目任务、时间条目或资源搜索时间条目的文本。


[!INCLUDE[footer-include](../includes/footer-banner.md)]