---
title: 使用新的定价维度更新插件属性
description: 此主题介绍如何更新定价维度的插件属性。
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004610"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="3ad24-103">使用新的定价维度更新插件属性</span><span class="sxs-lookup"><span data-stu-id="3ad24-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="3ad24-104">此主题介绍如何更新定价维度的插件属性。</span><span class="sxs-lookup"><span data-stu-id="3ad24-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3ad24-105">此主题仅适用于 Dynamics 365 Project Operations 中的报价单和合同功能。</span><span class="sxs-lookup"><span data-stu-id="3ad24-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ad24-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="3ad24-106">Prerequisites</span></span>
<span data-ttu-id="3ad24-107">在完成本主题中的步骤之前，您必须已完成下列主题中的过程：</span><span class="sxs-lookup"><span data-stu-id="3ad24-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="3ad24-108">创建自定义字段和实体</span><span class="sxs-lookup"><span data-stu-id="3ad24-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="3ad24-109">为价格设置和交易实体添加自定义字段</span><span class="sxs-lookup"><span data-stu-id="3ad24-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="3ad24-110">[将自定义字段设置为定价维度](set-up-custom-fields-pricing-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="3ad24-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="3ad24-111">如果尚未完成这些过程，请完成，然后回到此主题。</span><span class="sxs-lookup"><span data-stu-id="3ad24-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="3ad24-112">注册插件</span><span class="sxs-lookup"><span data-stu-id="3ad24-112">Register a plug-in</span></span>
<span data-ttu-id="3ad24-113">在项目报价单明细的 **报价单明细** 页上创建报价单明细详细信息时，系统会创建两个估算行。</span><span class="sxs-lookup"><span data-stu-id="3ad24-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="3ad24-114">一个行用于估算的成本端，另一个行用于销售端。</span><span class="sxs-lookup"><span data-stu-id="3ad24-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="3ad24-115">项目合同子项也是一样。</span><span class="sxs-lookup"><span data-stu-id="3ad24-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3ad24-116">对成本端的数量或字段进行更改时，也将在销售端上进行该更改。</span><span class="sxs-lookup"><span data-stu-id="3ad24-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="3ad24-117">因为 Quotelinedetail 和 contractline 详细信息实体上的 PreOperation 插件将成本端上的特定属性连接到交易的销售端，所以可能会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="3ad24-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="3ad24-118">如果您也需要在成本端上进行在销售端上对定价维度值所做的更改，则必须在更改定价维度后重新注册以下插件。</span><span class="sxs-lookup"><span data-stu-id="3ad24-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="3ad24-119">以下是要更新和重新注册的插件：</span><span class="sxs-lookup"><span data-stu-id="3ad24-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="3ad24-120">PreOperationContractLineDetailUpdate - **更新 msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3ad24-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="3ad24-121">PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3ad24-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="3ad24-122">完成以下步骤以更新和重新注册插件。</span><span class="sxs-lookup"><span data-stu-id="3ad24-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="3ad24-123">打开 **PluginRegistrationTool**，并连接到您的 Project Operations Dataverse 环境。</span><span class="sxs-lookup"><span data-stu-id="3ad24-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="3ad24-124">选择 **搜索**，然后键入要更新的插件的前几个字母。</span><span class="sxs-lookup"><span data-stu-id="3ad24-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="3ad24-125">找到插件后，将其选中，然后选择 **在主窗体中选择**。</span><span class="sxs-lookup"><span data-stu-id="3ad24-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="3ad24-126">选择 **更新 msdyn_orderlinetransaction** 步骤，右键单击，然后选择 **更新**。</span><span class="sxs-lookup"><span data-stu-id="3ad24-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="3ad24-127">在 **更新** 对话框页中，选择筛选属性中的省略号 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="3ad24-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="3ad24-128">筛选属性窗口将会打开，并提供实体中的所有属性和定价维度的列表。</span><span class="sxs-lookup"><span data-stu-id="3ad24-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="3ad24-129">选中定价维度属性的复选框。</span><span class="sxs-lookup"><span data-stu-id="3ad24-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="3ad24-130">选择 **确定** 关闭页面，然后选择 **更新步骤**。</span><span class="sxs-lookup"><span data-stu-id="3ad24-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="3ad24-131">对第二个插件 **PreOperationQuoteLineDetail** 重复步骤 2 到 7。</span><span class="sxs-lookup"><span data-stu-id="3ad24-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="3ad24-132">对于此插件，您需要更新 **msdyn_quotelinetransaction 更新** 步骤。</span><span class="sxs-lookup"><span data-stu-id="3ad24-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="3ad24-133">关闭 **PluginRegistrationTool**。</span><span class="sxs-lookup"><span data-stu-id="3ad24-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]