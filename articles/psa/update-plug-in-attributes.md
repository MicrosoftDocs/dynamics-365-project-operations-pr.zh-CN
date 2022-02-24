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
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147057"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>更新插件属性以包括新定价维度

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> 如果未在使用 Project Service Automation (PSA) 报价和合同签订功能，可跳过此主题。

此主题假设您已完成了主题[创建自定义字段和实体](create-custom-fields-entities.md)、[向价格设置和交易实体添加自定义字段](field-references.md)和[将自定义字段设置为定价维度](set-up-pricing-dimensions.md)中的过程。 如果尚未完成这些过程，请回去完成，然后回到此主题。

如果在 **报价单明细** 页中为项目报价单明细创建报价单明细详细信息，系统将在后台创建两项估算明细 -- 一项明细针对估算的成本端，一项针对销售端。 项目合同子项也是一样。

对成本端的数量或字段进行更改时，将把该更改传播到销售端。 这是对定价维度进行更改后必须重新注册的以下插件促成的。

- PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction**。
- PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**。

以下步骤引导您完成插件的注册流程。

1. 打开 **PluginRegistrationTool**，然后连接到您的在线实例。
2. 单击 **搜索**，然后搜索要更新的插件。

 ![搜索树的屏幕截图](media/PRT-1.png)

3. 找到插件后，将其选中，然后单击 **在主窗体中选择**。

4. 选择要更新的插件的步骤，然后选择 **更新**。

 ![要更新的插件的屏幕截图](media/PRT-2.png)
 
5. 在更新窗口中，单击筛选属性中的省略号 (**...**)。

 ![更新现有步骤配置信息的屏幕截图](media/PRT-3.png)
 
6. 选中定价属性复选框。

 ![显示定价属性的复选框选择情况的屏幕截图](media/PRT-4.png)

7. 单击 **确定** 关闭页面，然后选择 **更新步骤**。

 ![显示“更新步骤”按钮的屏幕截图](media/PRT-5.png)
 
8. 对第二个插件 (**PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**) 重复此流程。

9. 关闭插件注册工具。

