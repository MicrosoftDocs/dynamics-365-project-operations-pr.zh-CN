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
# <a name="define-project-calendars"></a><span data-ttu-id="0a289-103">定义项目日历</span><span class="sxs-lookup"><span data-stu-id="0a289-103">Define project calendars</span></span>

<span data-ttu-id="0a289-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="0a289-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0a289-105">若要创建项目计划，请创建一个项目日历模板，用于定义每天的工时数和节假日。</span><span class="sxs-lookup"><span data-stu-id="0a289-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="0a289-106">若要创建项目日历模板，请将工作模板与项目的 **日历模板** 字段关联。</span><span class="sxs-lookup"><span data-stu-id="0a289-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="0a289-107">执行以下步骤创建一个工作模板。</span><span class="sxs-lookup"><span data-stu-id="0a289-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="0a289-108">在左侧导航窗格中选择 **资源** 。</span><span class="sxs-lookup"><span data-stu-id="0a289-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="0a289-109">在 **资源** 列表页中，打开一条用户记录，然后选择 **显示工时** 。</span><span class="sxs-lookup"><span data-stu-id="0a289-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="0a289-110">确保浏览器页中允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="0a289-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="0a289-111">这样您就可以查看为资源设置的工时。</span><span class="sxs-lookup"><span data-stu-id="0a289-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="0a289-112">在 **月视图** 选项卡中，选择 **设置** 。</span><span class="sxs-lookup"><span data-stu-id="0a289-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="0a289-113">将显示三个选项的列表：</span><span class="sxs-lookup"><span data-stu-id="0a289-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="0a289-114">新建周计划</span><span class="sxs-lookup"><span data-stu-id="0a289-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="0a289-115">一天的工作计划</span><span class="sxs-lookup"><span data-stu-id="0a289-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="0a289-116">休息时间</span><span class="sxs-lookup"><span data-stu-id="0a289-116">Time Off</span></span>

4. <span data-ttu-id="0a289-117">选择 **新建周计划** ，然后为此资源计划设置选项。</span><span class="sxs-lookup"><span data-stu-id="0a289-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="0a289-118">可设置定期周计划、日工时参数、节假日等。</span><span class="sxs-lookup"><span data-stu-id="0a289-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="0a289-119">设置日期范围，选择 **保存** ，然后选择 **关闭** 。</span><span class="sxs-lookup"><span data-stu-id="0a289-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="0a289-120">回到 **资源** 列表页，然后选择要为其设置工时的资源。</span><span class="sxs-lookup"><span data-stu-id="0a289-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="0a289-121">选择 **日历设置为** 以设置工作模板。</span><span class="sxs-lookup"><span data-stu-id="0a289-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="0a289-122">在 **工作模板** 对话框中，输入工作模板的名称，然后选择 **应用** 。</span><span class="sxs-lookup"><span data-stu-id="0a289-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="0a289-123">现在可将此工作模板与项目日历模板关联。</span><span class="sxs-lookup"><span data-stu-id="0a289-123">You can now associate the work template with a project calendar template.</span></span>