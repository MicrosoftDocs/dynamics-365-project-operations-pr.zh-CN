---
title: 定义资源日历
description: 此主题提供有关如何为 Project Operations 中的资源定义工作时间日历的信息。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123907"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="4e6e6-103">定义资源日历</span><span class="sxs-lookup"><span data-stu-id="4e6e6-103">Define resource calendars</span></span>

<span data-ttu-id="4e6e6-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="4e6e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4e6e6-105">项目上的每个可预订资源都必须有工作时间日历来定义他们的可用性。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="4e6e6-106">可通过以下两种方式定义资源的工作时间：</span><span class="sxs-lookup"><span data-stu-id="4e6e6-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="4e6e6-107">定义资源的各个日历规则</span><span class="sxs-lookup"><span data-stu-id="4e6e6-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="4e6e6-108">为资源应用现有日历模板</span><span class="sxs-lookup"><span data-stu-id="4e6e6-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="4e6e6-109">定义资源的工作时间</span><span class="sxs-lookup"><span data-stu-id="4e6e6-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="4e6e6-110">在 **资源** 菜单上，选择 **资源**。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="4e6e6-111">从网格视图中，选择适用的 **可预订资源**。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="4e6e6-112">在 **资源详细信息** 页上，选择 **工作时间** 选项卡。默认情况下，可预订资源日历默认为为组织定义的默认工作时间模板的工作时间。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="4e6e6-113">要更新工作时间，右键单击要定义的建议日历规则的开始日期。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="4e6e6-114">使用日历规则菜单可以为特定日期、系列的其余部分或整个日历定义日历规则。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="4e6e6-115">选择此选项后，您可以定义：</span><span class="sxs-lookup"><span data-stu-id="4e6e6-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="4e6e6-116">将应用工作时间的周几。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="4e6e6-117">每天的工作时间。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-117">The working times within each day.</span></span>
    - <span data-ttu-id="4e6e6-118">日历规则的时区。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="4e6e6-119">如果适用，还可以为规则指定非工作时间。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="4e6e6-120">将日历模板应用于资源</span><span class="sxs-lookup"><span data-stu-id="4e6e6-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="4e6e6-121">在 **资源** 菜单上，选择 **资源**。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="4e6e6-122">在网格视图中，最多选择 25 个要更新的 **可预订资源**。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="4e6e6-123">选择 **设置日历**，一个对话框将显示可用工作小时模板的列表，向您发出提示。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="4e6e6-124">选择您要使用的模板，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="4e6e6-124">Select the template you want to use, and then select **Apply**.</span></span>
