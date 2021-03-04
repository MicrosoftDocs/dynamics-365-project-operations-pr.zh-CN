---
title: 如何自定义项目阶段业务流程？
description: 有关如何自定义项目阶段业务流程的概述。
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148992"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>如何自定义项目阶段业务流程？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

在早期的 Project Service 应用程序版本中存在一个已知限制：项目阶段业务流程中阶段的名称必须完全匹配预期的英文名称（**Quote**、**Plan**、**Close**）。 否则，依赖英文阶段名称的业务逻辑将不能按预期工作。 因此您在项目窗体上看不到熟悉的操作，如 **切换流程** 或 **编辑流程**，因而不建议自定义业务流程。 

版本 2.4.5.48 及更高版本中已解决了此限制。 如果您需要为早期版本自定义默认业务流程，本文提供了建议方法。  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>业务逻辑需要与英文的阶段名称完全匹配

项目阶段业务流程包括在应用程序中推动以下行为的业务逻辑：
- 在与报价单关联的项目中，代码设置 **Quote** 阶段的业务流程。
- 在与合同关联的项目中，代码设置 **Plan** 阶段的业务流程。
- 在业务流程进入到 **Close** 阶段时，项目记录将停用。 当项目停用时，项目窗体和工作分解结构 (WBS) 设置为只读，指定资源预订被释放，任何关联的价目表将停用。

此业务逻辑依赖项目阶段的英文名称。 对英文阶段名称的这种依赖是不建议自定义项目阶段业务流程的主要原因，也是您在项目实体中看不到 **切换流程** 或 **编辑流程** 等通用业务流程操作的原因。

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>如果阶段名称与英文名称不匹配会发生什么情况？

在 8.2 平台上的 Project Service 应用程序版本 1.x 中，当业务流程中的阶段名称不与英文阶段名称完全匹配时，则设置正确的报价单或合同阶段或关闭项目的业务逻辑将跳过。 不显示任何错误消息。 因此，看来您可以自定义项目阶段业务流程。 但是，您不会看到用于报价单、合同和项目关闭的任何自动流程。

在 9.0 平台上的 Project Service 应用程序版本 2.4.4.30 或更早版本中，对业务流程有重大的结构更改，这需要重写业务流程业务逻辑。 因此，如果流程阶段名称与预期的英文名称不匹配，您一定会收到错误消息。 

因此，如果您希望自定义项目实体的项目阶段业务流程，您可以仅向项目实体的默认业务流程添加全新阶段，同时保留 **报价单**、**计划** 和 **关闭** 阶段不变。 此限制将确保您不会收到在业务流程预期英文阶段名称的业务逻辑发出的错误。

在版本 2.4.5.48 或更高版本中，本文所介绍的业务逻辑已从项目实体的默认业务流程中删除。 升级到该版本或更高版本后，您将可以自定义默认业务流程或将其替换为您自己的业务流程。 

## <a name="workarounds-for-earlier-versions"></a>针对早期版本的方法

如果不能升级，您可以通过以下两种方法之一自定义项目实体的项目阶段业务流程：

1. 向默认配置添加更多阶段，同时保留 **报价单**、**计划** 和 **关闭** 的英文阶段名称。


![向默认配置添加阶段的屏幕截图](media/FAQ-Customize-BPF-1.png)
 
2. 创建您自己的业务流程并将其作为项目实体的主要业务流程，这样您可以有所希望的任何阶段名称。 但是，如果要使用相同的标准项目阶段 **报价单**、**计划** 和 **关闭**，您需要进行一些自定义来取消您的自定义阶段名称。 更复杂的逻辑位于项目的关闭阶段，您仍然可以通过停用项目记录触发它。

![BPF 自定义](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>平台 9.0 上的 Project Service 应用程序版本 2.4.4.30 或更早版本的其他注意事项

在平台 9.0 上的 Project Service 2.4.4.30 或更早版本（具有自定义业务流程）中，在 **按阶段列出的项目** 图表和项目列表视图中使用的项目实体上的 **阶段名称** 字段不会更新，因为它与默认的项目阶段业务流程关联。 您可以通过执行以下步骤解决此问题：

- 通过自定义业务流程添加自定义字段以获取更新为用户高级设置的当前业务流程阶段。

- 修改 **按阶段列出的项目** 图表来处理您的自定义字段，而不是使用默认配置。

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>创建您自己的项目实体的业务流程的步骤

若要创建您自己的项目实体的业务流程，请执行以下步骤：

1. 转到 **设置** > **流程中心**。 不要复制项目阶段业务流程，因为这同时会复制项目服务业务逻辑。

  ![创建流程](media/FAQ-Customize-BPF-3.png)

2. 使用流程设计器创建所需的阶段名称。 如果您需要与默认的 **报价单**、**计划** 和 **关闭** 阶段相同的功能，则必须根据自定义业务流程的阶段名称进行创建。

   ![用于自定义 BPF 的流程设计器的屏幕截图](media/FAQ-Customize-BPF-4.png) 

3. 在流程设计器中，单击 **流程排序** 将自定义业务流程设置为项目实体的主要业务流程，方法是将其移到列表顶部的项目阶段业务流程的上方。


   [使用“流程排序”的屏幕截图](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>以下步骤适用于 9.0 平台上的 Project Service 应用程序 2.4.4.30 或更高版本

4. 向项目实体添加新的自定义字段来获取自定义业务流程中的自定义阶段。 您将需要添加业务逻辑（插件/工作流）来在更新自定义业务流程中的阶段时更新此字段。

   ![自定义项目实体的屏幕截图](media/FAQ-Customize-BPF-6-720.png)

5. 修改 **按阶段列出的项目** 图表以为阶段使用新的自定义字段。

   ![使用“按阶段列出的项目”图表的屏幕截图](media/FAQ-Customize-BPF-7-720.png)

6. 修改项目实体的所有视图以为阶段包含新的自定义字段。

   ![修改项目实体上的视图的屏幕截图](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]