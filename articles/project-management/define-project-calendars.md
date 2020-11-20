---
title: 定义项目日历
description: 此主题提供有关使用项目日历跟踪项目计划的信息。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131647"
---
# <a name="define-project-calendars"></a><span data-ttu-id="ec683-103">定义项目日历</span><span class="sxs-lookup"><span data-stu-id="ec683-103">Define project calendars</span></span>

<span data-ttu-id="ec683-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="ec683-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec683-105">若要创建项目计划，请创建一个项目日历模板，用于定义每天的工时数和节假日。</span><span class="sxs-lookup"><span data-stu-id="ec683-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="ec683-106">若要创建项目日历模板，请将工作模板与项目的 **日历模板** 字段关联。</span><span class="sxs-lookup"><span data-stu-id="ec683-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="ec683-107">执行以下步骤创建一个工作模板。</span><span class="sxs-lookup"><span data-stu-id="ec683-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="ec683-108">在左侧导航窗格中选择 **资源**。</span><span class="sxs-lookup"><span data-stu-id="ec683-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="ec683-109">在 **资源** 列表页中，打开一条用户记录，然后选择 **显示工时**。</span><span class="sxs-lookup"><span data-stu-id="ec683-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ec683-110">确保浏览器页中允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="ec683-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="ec683-111">这样您就可以查看为资源设置的工时。</span><span class="sxs-lookup"><span data-stu-id="ec683-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="ec683-112">在 **月视图** 选项卡中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="ec683-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="ec683-113">将显示三个选项的列表：</span><span class="sxs-lookup"><span data-stu-id="ec683-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="ec683-114">新建周计划</span><span class="sxs-lookup"><span data-stu-id="ec683-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="ec683-115">一天的工作计划</span><span class="sxs-lookup"><span data-stu-id="ec683-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="ec683-116">休息时间</span><span class="sxs-lookup"><span data-stu-id="ec683-116">Time Off</span></span>

4. <span data-ttu-id="ec683-117">选择 **新建周计划**，然后为此资源计划设置选项。</span><span class="sxs-lookup"><span data-stu-id="ec683-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="ec683-118">可设置定期周计划、日工时参数、节假日等。</span><span class="sxs-lookup"><span data-stu-id="ec683-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="ec683-119">设置日期范围，选择 **保存**，然后选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="ec683-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="ec683-120">回到 **资源** 列表页，然后选择要为其设置工时的资源。</span><span class="sxs-lookup"><span data-stu-id="ec683-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="ec683-121">选择 **日历设置为** 以设置工作模板。</span><span class="sxs-lookup"><span data-stu-id="ec683-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="ec683-122">在 **工作模板** 对话框中，输入工作模板的名称，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="ec683-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="ec683-123">现在可将此工作模板与项目日历模板关联。</span><span class="sxs-lookup"><span data-stu-id="ec683-123">You can now associate the work template with a project calendar template.</span></span>
