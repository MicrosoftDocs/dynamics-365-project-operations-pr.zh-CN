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
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>使用新的定价维度更新插件属性

此主题介绍如何更新定价维度的插件属性。

> [!NOTE]
> 此主题仅适用于 Dynamics 365 Project Operations 中的报价单和合同功能。

## <a name="prerequisites"></a>先决条件
在完成本主题中的步骤之前，您必须已完成下列主题中的过程：

  - [创建自定义字段和实体](create-custom-fields-entities-pricing-dimensions.md) 
  - [为价格设置和交易实体添加自定义字段](add-custom-fields-price-setup-transactional-entities.md)
  - [将自定义字段设置为定价维度](set-up-custom-fields-pricing-dimensions.md)。 
  
如果尚未完成这些过程，请完成，然后回到此主题。

## <a name="register-a-plug-in"></a>注册插件
在项目报价单明细的 **报价单明细** 页上创建报价单明细详细信息时，系统会创建两个估算行。 一个行用于估算的成本端，另一个行用于销售端。 项目合同子项也是一样。

对成本端的数量或字段进行更改时，也将在销售端上进行该更改。 因为 Quotelinedetail 和 contractline 详细信息实体上的 PreOperation 插件将成本端上的特定属性连接到交易的销售端，所以可能会出现这种情况。 如果您也需要在成本端上进行在销售端上对定价维度值所做的更改，则必须在更改定价维度后重新注册以下插件。

以下是要更新和重新注册的插件：

- PreOperationContractLineDetailUpdate - **更新 msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**

完成以下步骤以更新和重新注册插件。

1. 打开 **PluginRegistrationTool**，并连接到您的 Project Operations Dataverse 环境。
2. 选择 **搜索**，然后键入要更新的插件的前几个字母。
3. 找到插件后，将其选中，然后选择 **在主窗体中选择**。
4. 选择 **更新 msdyn_orderlinetransaction** 步骤，右键单击，然后选择 **更新**。
5. 在 **更新** 对话框页中，选择筛选属性中的省略号 (**...**)。
6. 筛选属性窗口将会打开，并提供实体中的所有属性和定价维度的列表。 选中定价维度属性的复选框。
7. 选择 **确定** 关闭页面，然后选择 **更新步骤**。
8. 对第二个插件 **PreOperationQuoteLineDetail** 重复步骤 2 到 7。 对于此插件，您需要更新 **msdyn_quotelinetransaction 更新** 步骤。
9. 关闭 **PluginRegistrationTool**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]