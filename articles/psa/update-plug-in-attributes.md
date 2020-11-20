---
title: 更新插件属性以包括新定价维度
description: 此主题介绍如何更新定价维度的插件属性。
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121837"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="3ca1c-103">更新插件属性以包括新定价维度</span><span class="sxs-lookup"><span data-stu-id="3ca1c-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="3ca1c-104">如果未在使用 Project Service Automation (PSA) 报价和合同签订功能，可跳过此主题。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="3ca1c-105">此主题假设您已完成了主题[创建自定义字段和实体](create-custom-fields-entities.md)、[向价格设置和交易实体添加自定义字段](field-references.md)和[将自定义字段设置为定价维度](set-up-pricing-dimensions.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="3ca1c-106">如果尚未完成这些过程，请回去完成，然后回到此主题。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="3ca1c-107">如果在 **报价单明细** 页中为项目报价单明细创建报价单明细详细信息，系统将在后台创建两项估算明细 -- 一项明细针对估算的成本端，一项针对销售端。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="3ca1c-108">项目合同子项也是一样。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3ca1c-109">对成本端的数量或字段进行更改时，将把该更改传播到销售端。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="3ca1c-110">这是对定价维度进行更改后必须重新注册的以下插件促成的。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="3ca1c-111">PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction**。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="3ca1c-112">PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="3ca1c-113">以下步骤引导您完成插件的注册流程。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="3ca1c-114">打开 **PluginRegistrationTool**，然后连接到您的在线实例。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="3ca1c-115">单击 **搜索**，然后搜索要更新的插件。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![搜索树的屏幕截图](media/PRT-1.png)

3. <span data-ttu-id="3ca1c-117">找到插件后，将其选中，然后单击 **在主窗体中选择**。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="3ca1c-118">选择要更新的插件的步骤，然后选择 **更新**。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![要更新的插件的屏幕截图](media/PRT-2.png)
 
5. <span data-ttu-id="3ca1c-120">在更新窗口中，单击筛选属性中的省略号 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![更新现有步骤配置信息的屏幕截图](media/PRT-3.png)
 
6. <span data-ttu-id="3ca1c-122">选中定价属性复选框。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-122">Select the pricing attribute check boxes.</span></span>

 ![显示定价属性的复选框选择情况的屏幕截图](media/PRT-4.png)

7. <span data-ttu-id="3ca1c-124">单击 **确定** 关闭页面，然后选择 **更新步骤**。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![显示“更新步骤”按钮的屏幕截图](media/PRT-5.png)
 
8. <span data-ttu-id="3ca1c-126">对第二个插件 (**PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**) 重复此流程。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="3ca1c-127">关闭插件注册工具。</span><span class="sxs-lookup"><span data-stu-id="3ca1c-127">Close the plug-in registration tool.</span></span>

