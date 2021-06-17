---
title: 如何自定义项目阶段业务流程？
description: 有关如何自定义项目阶段业务流程的概述。
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993135"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="87643-103">如何自定义项目阶段业务流程？</span><span class="sxs-lookup"><span data-stu-id="87643-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="87643-104">在早期的 Project Service 应用程序版本中存在一个已知限制：项目阶段业务流程中阶段的名称必须完全匹配预期的英文名称（**Quote**、**Plan**、**Close**）。</span><span class="sxs-lookup"><span data-stu-id="87643-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="87643-105">否则，依赖英文阶段名称的业务逻辑将不能按预期工作。</span><span class="sxs-lookup"><span data-stu-id="87643-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="87643-106">因此您在项目窗体上看不到熟悉的操作，如 **切换流程** 或 **编辑流程**，因而不建议自定义业务流程。</span><span class="sxs-lookup"><span data-stu-id="87643-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="87643-107">版本 2.4.5.48 及更高版本中已解决了此限制。</span><span class="sxs-lookup"><span data-stu-id="87643-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="87643-108">如果您需要为早期版本自定义默认业务流程，本文提供了建议方法。</span><span class="sxs-lookup"><span data-stu-id="87643-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="87643-109">业务逻辑需要与英文的阶段名称完全匹配</span><span class="sxs-lookup"><span data-stu-id="87643-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="87643-110">项目阶段业务流程包括在应用程序中推动以下行为的业务逻辑：</span><span class="sxs-lookup"><span data-stu-id="87643-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="87643-111">在与报价单关联的项目中，代码设置 **Quote** 阶段的业务流程。</span><span class="sxs-lookup"><span data-stu-id="87643-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="87643-112">在与合同关联的项目中，代码设置 **Plan** 阶段的业务流程。</span><span class="sxs-lookup"><span data-stu-id="87643-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="87643-113">在业务流程进入到 **Close** 阶段时，项目记录将停用。</span><span class="sxs-lookup"><span data-stu-id="87643-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="87643-114">当项目停用时，项目窗体和工作分解结构 (WBS) 设置为只读，指定资源预订被释放，任何关联的价目表将停用。</span><span class="sxs-lookup"><span data-stu-id="87643-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="87643-115">此业务逻辑依赖项目阶段的英文名称。</span><span class="sxs-lookup"><span data-stu-id="87643-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="87643-116">对英文阶段名称的这种依赖是不建议自定义项目阶段业务流程的主要原因，也是您在项目实体中看不到 **切换流程** 或 **编辑流程** 等通用业务流程操作的原因。</span><span class="sxs-lookup"><span data-stu-id="87643-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="87643-117">如果阶段名称与英文名称不匹配会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="87643-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="87643-118">在 8.2 平台上的 Project Service 应用程序版本 1.x 中，当业务流程中的阶段名称不与英文阶段名称完全匹配时，则设置正确的报价单或合同阶段或关闭项目的业务逻辑将跳过。</span><span class="sxs-lookup"><span data-stu-id="87643-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="87643-119">不显示任何错误消息。</span><span class="sxs-lookup"><span data-stu-id="87643-119">No error messages are displayed.</span></span> <span data-ttu-id="87643-120">因此，看来您可以自定义项目阶段业务流程。</span><span class="sxs-lookup"><span data-stu-id="87643-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="87643-121">但是，您不会看到用于报价单、合同和项目关闭的任何自动流程。</span><span class="sxs-lookup"><span data-stu-id="87643-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="87643-122">在 9.0 平台上的 Project Service 应用程序版本 2.4.4.30 或更早版本中，对业务流程有重大的结构更改，这需要重写业务流程业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="87643-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="87643-123">因此，如果流程阶段名称与预期的英文名称不匹配，您一定会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="87643-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="87643-124">因此，如果您希望自定义项目实体的项目阶段业务流程，您可以仅向项目实体的默认业务流程添加全新阶段，同时保留 **报价单**、**计划** 和 **关闭** 阶段不变。</span><span class="sxs-lookup"><span data-stu-id="87643-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="87643-125">此限制将确保您不会收到在业务流程预期英文阶段名称的业务逻辑发出的错误。</span><span class="sxs-lookup"><span data-stu-id="87643-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="87643-126">在版本 2.4.5.48 或更高版本中，本文所介绍的业务逻辑已从项目实体的默认业务流程中删除。</span><span class="sxs-lookup"><span data-stu-id="87643-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="87643-127">升级到该版本或更高版本后，您将可以自定义默认业务流程或将其替换为您自己的业务流程。</span><span class="sxs-lookup"><span data-stu-id="87643-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="87643-128">针对早期版本的方法</span><span class="sxs-lookup"><span data-stu-id="87643-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="87643-129">如果不能升级，您可以通过以下两种方法之一自定义项目实体的项目阶段业务流程：</span><span class="sxs-lookup"><span data-stu-id="87643-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="87643-130">向默认配置添加更多阶段，同时保留 **报价单**、**计划** 和 **关闭** 的英文阶段名称。</span><span class="sxs-lookup"><span data-stu-id="87643-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![向默认配置添加阶段的屏幕截图](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="87643-132">创建您自己的业务流程并将其作为项目实体的主要业务流程，这样您可以有所希望的任何阶段名称。</span><span class="sxs-lookup"><span data-stu-id="87643-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="87643-133">但是，如果要使用相同的标准项目阶段 **报价单**、**计划** 和 **关闭**，您需要进行一些自定义来取消您的自定义阶段名称。</span><span class="sxs-lookup"><span data-stu-id="87643-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="87643-134">更复杂的逻辑位于项目的关闭阶段，您仍然可以通过停用项目记录触发它。</span><span class="sxs-lookup"><span data-stu-id="87643-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF 自定义](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="87643-136">平台 9.0 上的 Project Service 应用程序版本 2.4.4.30 或更早版本的其他注意事项</span><span class="sxs-lookup"><span data-stu-id="87643-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="87643-137">在平台 9.0 上的 Project Service 2.4.4.30 或更早版本（具有自定义业务流程）中，在 **按阶段列出的项目** 图表和项目列表视图中使用的项目实体上的 **阶段名称** 字段不会更新，因为它与默认的项目阶段业务流程关联。</span><span class="sxs-lookup"><span data-stu-id="87643-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="87643-138">您可以通过执行以下步骤解决此问题：</span><span class="sxs-lookup"><span data-stu-id="87643-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="87643-139">通过自定义业务流程添加自定义字段以获取更新为用户高级设置的当前业务流程阶段。</span><span class="sxs-lookup"><span data-stu-id="87643-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="87643-140">修改 **按阶段列出的项目** 图表来处理您的自定义字段，而不是使用默认配置。</span><span class="sxs-lookup"><span data-stu-id="87643-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="87643-141">创建您自己的项目实体的业务流程的步骤</span><span class="sxs-lookup"><span data-stu-id="87643-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="87643-142">若要创建您自己的项目实体的业务流程，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="87643-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="87643-143">转到 **设置** > **流程中心**。</span><span class="sxs-lookup"><span data-stu-id="87643-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="87643-144">不要复制项目阶段业务流程，因为这同时会复制项目服务业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="87643-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![创建流程](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="87643-146">使用流程设计器创建所需的阶段名称。</span><span class="sxs-lookup"><span data-stu-id="87643-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="87643-147">如果您需要与默认的 **报价单**、**计划** 和 **关闭** 阶段相同的功能，则必须根据自定义业务流程的阶段名称进行创建。</span><span class="sxs-lookup"><span data-stu-id="87643-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![用于自定义 BPF 的流程设计器的屏幕截图](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="87643-149">在流程设计器中，单击 **流程排序** 将自定义业务流程设置为项目实体的主要业务流程，方法是将其移到列表顶部的项目阶段业务流程的上方。</span><span class="sxs-lookup"><span data-stu-id="87643-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="87643-150">使用“流程排序”的屏幕截图</span><span class="sxs-lookup"><span data-stu-id="87643-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="87643-151">以下步骤适用于 9.0 平台上的 Project Service 应用程序 2.4.4.30 或更高版本</span><span class="sxs-lookup"><span data-stu-id="87643-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="87643-152">向项目实体添加新的自定义字段来获取自定义业务流程中的自定义阶段。</span><span class="sxs-lookup"><span data-stu-id="87643-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="87643-153">您将需要添加业务逻辑（插件/工作流）来在更新自定义业务流程中的阶段时更新此字段。</span><span class="sxs-lookup"><span data-stu-id="87643-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![自定义项目实体的屏幕截图](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="87643-155">修改 **按阶段列出的项目** 图表以为阶段使用新的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="87643-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![使用“按阶段列出的项目”图表的屏幕截图](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="87643-157">修改项目实体的所有视图以为阶段包含新的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="87643-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![修改项目实体上的视图的屏幕截图](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]