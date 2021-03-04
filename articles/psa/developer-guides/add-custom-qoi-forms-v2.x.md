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
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144582"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>添加新的自定义实体窗体 (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>“类型”字段 

Dynamics 365 Project Service Automation 依赖商机、报价单、订单和发票实体的 **类型** (**msdyn\_ordertype**) 字段区分这些实体 **基于工作的** 版本与 **基于物料的** 版本和 **基于服务的** 版本。 这些实体基于工作的版本由 PSA 处理。 解决方案的客户端和服务器端的许多业务逻辑取决于 **类型** 字段。 因此，务必在创建实体时使用正确的值初始化该字段。 错误值可能导致错误行为，并且某些业务逻辑可能无法正常运行。

## <a name="automatic-form-switching"></a>窗体自动切换

为了避免销售实体记录错误初始化和编辑导致的数据潜在损坏和意外行为，PSA 现在在自带窗体中增加了窗体自动切换逻辑。 此逻辑会将用户带到正确的窗体以处理商机、报价单、订单或发票实体的基于工作的版本或其他任何类型。 当用户打开商机、报价单、订单或发票实体基于工作的版本时，窗体将切换到 **项目信息**。

窗体自动切换逻辑依赖于 **formId** 值与 **msdyn\_ordertype** 字段之间的映射。 已将所有自带窗体添加到了该映射。 但是，必须手动添加自定义窗体，以指示应该处理实体的哪个版本。 这基于 **msdyn\_ordertype** 字段。 如果映射中缺少窗体切换，逻辑将基于实体的 **msdyn\_ordertype** 字段中保存的值切换到自带窗体。

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>添加自定义窗体和开启窗体切换逻辑

以下示例显示如何添加自定义窗体 **我的项目信息**，以便处理基于工作的商机。 同样的流程用于添加自定义窗体，以便处理报价单、订单和发票。

请执行以下步骤创建 **项目信息** 窗体的自定义版本。

1. 在商机实体中，打开 **项目信息** 窗体，然后在名称 **我的项目信息** 下保存一个副本。
2. 打开新窗体，然后在属性中确保存在来自 **项目信息** 窗体的窗体初始化脚本。 

    > [!IMPORTANT]
    > 切勿删除这些脚本。 否则，可能无法正确初始化某些数据。

3. 验证窗体中是否有 **类型** (**msdyn\_ordertype**) 字段。 

    > [!IMPORTANT]
    > 切勿删除此字段。 否则，初始化脚本将失败。

4. 找到新窗体的 **formId** 值。 可以通过两种方式完成此步骤：

    - 将 **我的项目信息** 窗体作为非托管解决方案的一部分导出，然后在导出的解决方案的 customization.xml 文件中查找 **formId** 值。
    - 在窗体编辑器中打开 **我的项目信息** 窗体，然后在 URL 的 **fromId** 参数旁边查找全局唯一标识符 (GUID)，如下图中所示。

    ![URL 中新窗体的 formId 值](media/how-to-add-custom-forms-in-v2.0.png)

5. 通过编辑 msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Web 资源为 **formId** 值创建 **msdyn\_ordertype** 映射。 从资源中删除代码，替换为以下代码。

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

6. 保存自定义设置，然后发布。
