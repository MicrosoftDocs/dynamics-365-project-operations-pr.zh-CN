---
title: 添加新的自定义实体窗体 (Project Service Automation 2.x)
description: 此主题介绍如何在 Dynamics 365 Project Service Automation 2.x 中为商机、报价单、订单或发票添加自定义实体窗体。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284842"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="00594-103">添加新的自定义实体窗体 (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="00594-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="00594-104">“类型”字段</span><span class="sxs-lookup"><span data-stu-id="00594-104">Type field</span></span> 

<span data-ttu-id="00594-105">Dynamics 365 Project Service Automation 依赖商机、报价单、订单和发票实体的 **类型** (**msdyn\_ordertype**) 字段区分这些实体 **基于工作的** 版本与 **基于物料的** 版本和 **基于服务的** 版本。</span><span class="sxs-lookup"><span data-stu-id="00594-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="00594-106">这些实体基于工作的版本由 PSA 处理。</span><span class="sxs-lookup"><span data-stu-id="00594-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="00594-107">解决方案的客户端和服务器端的许多业务逻辑取决于 **类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="00594-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="00594-108">因此，务必在创建实体时使用正确的值初始化该字段。</span><span class="sxs-lookup"><span data-stu-id="00594-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="00594-109">错误值可能导致错误行为，并且某些业务逻辑可能无法正常运行。</span><span class="sxs-lookup"><span data-stu-id="00594-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="00594-110">窗体自动切换</span><span class="sxs-lookup"><span data-stu-id="00594-110">Automatic form switching</span></span>

<span data-ttu-id="00594-111">为了避免销售实体记录错误初始化和编辑导致的数据潜在损坏和意外行为，PSA 现在在自带窗体中增加了窗体自动切换逻辑。</span><span class="sxs-lookup"><span data-stu-id="00594-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="00594-112">此逻辑会将用户带到正确的窗体以处理商机、报价单、订单或发票实体的基于工作的版本或其他任何类型。</span><span class="sxs-lookup"><span data-stu-id="00594-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="00594-113">当用户打开商机、报价单、订单或发票实体基于工作的版本时，窗体将切换到 **项目信息**。</span><span class="sxs-lookup"><span data-stu-id="00594-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="00594-114">窗体自动切换逻辑依赖于 **formId** 值与 **msdyn\_ordertype** 字段之间的映射。</span><span class="sxs-lookup"><span data-stu-id="00594-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="00594-115">已将所有自带窗体添加到了该映射。</span><span class="sxs-lookup"><span data-stu-id="00594-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="00594-116">但是，必须手动添加自定义窗体，以指示应该处理实体的哪个版本。</span><span class="sxs-lookup"><span data-stu-id="00594-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="00594-117">这基于 **msdyn\_ordertype** 字段。</span><span class="sxs-lookup"><span data-stu-id="00594-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="00594-118">如果映射中缺少窗体切换，逻辑将基于实体的 **msdyn\_ordertype** 字段中保存的值切换到自带窗体。</span><span class="sxs-lookup"><span data-stu-id="00594-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="00594-119">添加自定义窗体和开启窗体切换逻辑</span><span class="sxs-lookup"><span data-stu-id="00594-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="00594-120">以下示例显示如何添加自定义窗体 **我的项目信息**，以便处理基于工作的商机。</span><span class="sxs-lookup"><span data-stu-id="00594-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="00594-121">同样的流程用于添加自定义窗体，以便处理报价单、订单和发票。</span><span class="sxs-lookup"><span data-stu-id="00594-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="00594-122">请执行以下步骤创建 **项目信息** 窗体的自定义版本。</span><span class="sxs-lookup"><span data-stu-id="00594-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="00594-123">在商机实体中，打开 **项目信息** 窗体，然后在名称 **我的项目信息** 下保存一个副本。</span><span class="sxs-lookup"><span data-stu-id="00594-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="00594-124">打开新窗体，然后在属性中确保存在来自 **项目信息** 窗体的窗体初始化脚本。</span><span class="sxs-lookup"><span data-stu-id="00594-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="00594-125">切勿删除这些脚本。</span><span class="sxs-lookup"><span data-stu-id="00594-125">Don't remove the scripts.</span></span> <span data-ttu-id="00594-126">否则，可能无法正确初始化某些数据。</span><span class="sxs-lookup"><span data-stu-id="00594-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="00594-127">验证窗体中是否有 **类型** (**msdyn\_ordertype**) 字段。</span><span class="sxs-lookup"><span data-stu-id="00594-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="00594-128">切勿删除此字段。</span><span class="sxs-lookup"><span data-stu-id="00594-128">Don't remove this field.</span></span> <span data-ttu-id="00594-129">否则，初始化脚本将失败。</span><span class="sxs-lookup"><span data-stu-id="00594-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="00594-130">找到新窗体的 **formId** 值。</span><span class="sxs-lookup"><span data-stu-id="00594-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="00594-131">可以通过两种方式完成此步骤：</span><span class="sxs-lookup"><span data-stu-id="00594-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="00594-132">将 **我的项目信息** 窗体作为非托管解决方案的一部分导出，然后在导出的解决方案的 customization.xml 文件中查找 **formId** 值。</span><span class="sxs-lookup"><span data-stu-id="00594-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="00594-133">在窗体编辑器中打开 **我的项目信息** 窗体，然后在 URL 的 **fromId** 参数旁边查找全局唯一标识符 (GUID)，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="00594-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![URL 中新窗体的 formId 值](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="00594-135">通过编辑 msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Web 资源为 **formId** 值创建 **msdyn\_ordertype** 映射。</span><span class="sxs-lookup"><span data-stu-id="00594-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="00594-136">从资源中删除代码，替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="00594-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="00594-137">保存自定义设置，然后发布。</span><span class="sxs-lookup"><span data-stu-id="00594-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]