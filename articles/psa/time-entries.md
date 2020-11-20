---
title: 创建时间条目
description: 此主题介绍如何创建时间条目。
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131250"
---
# <a name="create-time-entries"></a><span data-ttu-id="45d08-103">创建时间条目</span><span class="sxs-lookup"><span data-stu-id="45d08-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45d08-104">在 Dynamics 365 Project Service Automation 早期版本中，时间条目以周为基础输入。</span><span class="sxs-lookup"><span data-stu-id="45d08-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="45d08-105">在 Project Service Automation 版本 3 中，时间条目基于日输入。</span><span class="sxs-lookup"><span data-stu-id="45d08-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="45d08-106">但是，输入了一些时间条目之后，可以批量创建或复制。</span><span class="sxs-lookup"><span data-stu-id="45d08-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="45d08-107">创建时间条目</span><span class="sxs-lookup"><span data-stu-id="45d08-107">Create a time entry</span></span>

<span data-ttu-id="45d08-108">执行以下步骤创建一个时间条目。</span><span class="sxs-lookup"><span data-stu-id="45d08-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="45d08-109">在 **时间条目** 页上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="45d08-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="45d08-110">在 **快速创建:时间条目** 对话框中，输入以分钟、小时或天为单位的时间条目持续时间。</span><span class="sxs-lookup"><span data-stu-id="45d08-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="45d08-111">持续时间必须采用下面的格式输入持续时间：*x* 分钟、*x* 小时或 *x* 天。</span><span class="sxs-lookup"><span data-stu-id="45d08-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="45d08-112">小时和天数也可以采用小数值输入；例如，*x.x* 小时或 *x.x* 天。</span><span class="sxs-lookup"><span data-stu-id="45d08-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="45d08-113">选择时间条目的类型和输入的时间条目所属项目。</span><span class="sxs-lookup"><span data-stu-id="45d08-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="45d08-114">在 **项目任务** 字段中，找到此时间条目的任务。</span><span class="sxs-lookup"><span data-stu-id="45d08-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45d08-115">如果要为尚未分派给用户的任务创建时间条目，请在 **项目任务** 字段中依次选择 **搜索** 按钮、**更改视图** 和 **所有可用的项目任务** 列出所有任务。</span><span class="sxs-lookup"><span data-stu-id="45d08-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="45d08-116">如果需要描述，输入描述，然后选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="45d08-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="45d08-117">创建并保存时间条目之后，可以在时间条目网格中编辑。</span><span class="sxs-lookup"><span data-stu-id="45d08-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="45d08-118">时间条目网格支持两种格式：</span><span class="sxs-lookup"><span data-stu-id="45d08-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="45d08-119">可以输入 **hh:mm** 格式的时间条目。</span><span class="sxs-lookup"><span data-stu-id="45d08-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="45d08-120">然后会将此格式转换为小时数加小数部分。</span><span class="sxs-lookup"><span data-stu-id="45d08-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="45d08-121">也可以直接输入小时数加小数部分。</span><span class="sxs-lookup"><span data-stu-id="45d08-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="45d08-122">请注意，小时的小数部分不是分钟。</span><span class="sxs-lookup"><span data-stu-id="45d08-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="45d08-123">因此，1.5 小时指的是 1 小时 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="45d08-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="45d08-124">同样的规则也适用于天的小数部分。</span><span class="sxs-lookup"><span data-stu-id="45d08-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="45d08-125">一天是 24 小时，所以 0.5 天是 12 小时。</span><span class="sxs-lookup"><span data-stu-id="45d08-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="45d08-126">批量创建时间条目</span><span class="sxs-lookup"><span data-stu-id="45d08-126">Bulk create time entries</span></span>

<span data-ttu-id="45d08-127">创建一些时间条目之后，可以复制这些时间条目以批量创建更多时间条目。</span><span class="sxs-lookup"><span data-stu-id="45d08-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="45d08-128">在 **时间条目** 页上，选择 **复制周**。</span><span class="sxs-lookup"><span data-stu-id="45d08-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="45d08-129">在 **开始期间** 字段组的 **开始日期** 和 **结束日期** 字段中，定义要复制的时间条目所属日期范围。</span><span class="sxs-lookup"><span data-stu-id="45d08-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="45d08-130">在 **目标期间** 字段组 **开始日期** 字段内，指定要为其创建时间条目的日期。</span><span class="sxs-lookup"><span data-stu-id="45d08-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="45d08-131">选择 **复制** 创建与 **结束期间** 字段组中指定的星期几对应的时间条目的副本。</span><span class="sxs-lookup"><span data-stu-id="45d08-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="45d08-132">例如，将把上周星期一的时间条目复制到在 **结束期间** 字段组中指定的周的星期一。</span><span class="sxs-lookup"><span data-stu-id="45d08-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="45d08-133">为时间条目导入数据</span><span class="sxs-lookup"><span data-stu-id="45d08-133">Import data for time entries</span></span>

<span data-ttu-id="45d08-134">可以从项目预订和分派导入数据。</span><span class="sxs-lookup"><span data-stu-id="45d08-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="45d08-135">导入数据时，可以指定要导入的预订的日期范围，然后明确选择应该作为 **草稿** 时间条目创建的预订。</span><span class="sxs-lookup"><span data-stu-id="45d08-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="45d08-136">分组依据、排序、搜索和筛选功能</span><span class="sxs-lookup"><span data-stu-id="45d08-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="45d08-137">可以按列中指定的维度对时间条目进行分组和筛选。</span><span class="sxs-lookup"><span data-stu-id="45d08-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="45d08-138">在 **分组依据** 字段中选择要用于筛选时间条目的维度。</span><span class="sxs-lookup"><span data-stu-id="45d08-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="45d08-139">也可以使用列标题中的排序箭头按升序或降序为时间条目记录排序。</span><span class="sxs-lookup"><span data-stu-id="45d08-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="45d08-140">此外，还可以显示或隐藏条目，方法是选择列标题中的 **筛选** 按钮，然后在 **搜索** 框中输入应该用于按项目名称、项目任务、时间条目或资源搜索时间条目的文本。</span><span class="sxs-lookup"><span data-stu-id="45d08-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
