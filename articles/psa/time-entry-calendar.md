---
title: 时间条目日历
description: 此主题介绍如何使用时间条目日历。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: afc31609c51f48db61ce359c18707b5a92211082
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072694"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="02209-103">时间条目日历</span><span class="sxs-lookup"><span data-stu-id="02209-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="02209-104">在 **时间条目** 页中，可使用 **显示为** \> **日历控件** 查看日历中的时间条目。</span><span class="sxs-lookup"><span data-stu-id="02209-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="02209-105">更新的日历控件</span><span class="sxs-lookup"><span data-stu-id="02209-105">Updated calendar control</span></span>

<span data-ttu-id="02209-106">Dynamics 365 Project Service Automation 提供新的可扩展时间条目体验。</span><span class="sxs-lookup"><span data-stu-id="02209-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="02209-107">这种新体验取代了早期版本中使用的自定义日历控件。</span><span class="sxs-lookup"><span data-stu-id="02209-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="02209-108">但是，仍然可以通过统一接口框架为日、周或月视图提供的只读日历控件查看时间条目。</span><span class="sxs-lookup"><span data-stu-id="02209-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="02209-109">此日历不支持对单个日历项执行操作，您不能选择提交或删除一个或多个日历项。</span><span class="sxs-lookup"><span data-stu-id="02209-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="02209-110">但是可以选择日历项打开 **时间条目** 实体页，可在其中完成所需操作。</span><span class="sxs-lookup"><span data-stu-id="02209-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="02209-111">扩展性</span><span class="sxs-lookup"><span data-stu-id="02209-111">Extensibility</span></span>

<span data-ttu-id="02209-112">在具有时间条目网格的 **时间条目** 页中，可以添加自定义字段，设置查找字段和创建自定义视图。</span><span class="sxs-lookup"><span data-stu-id="02209-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="02209-113">也可以设置基于在自定义字段中选择或输入的值设置自定义业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="02209-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
