---
title: 复制基于项目的报价单
description: 此主题提供有关如何在 Project Operations 中复制基于项目的报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928547"
---
# <a name="copy-project-based-quotes"></a>复制基于项目的报价单

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

您可以通过复制现有项目报价单轻松地创建新的项目报价单。 

- 要复制项目报价单，在**项目报价单**列表页或**项目报价单**详细信息页上，选择要复制的项目报价单，然后选择**复制**。

这将打开一个对话页面，您可以在其中输入副本的参数。 下表列出了对话页面中包含的字段。 根据您选择的值，复制过程可能会有变化。

| **字段** | **关联性、用途和指导** | **下游影响** |
| --- | --- | --- |
| 主题 | 输入目标报价单的相关主题或名称。 当对话打开时，系统会将其设置为源报价单的主题，并附加 **-copy**。 | |
| 潜在客户 | 对客户的公司或客户记录的引用。 当对话打开时，系统会将其设置为源报价单上的客户。 | 此字段是报价单上的主要客户。 |
| 合同签订部门 | 负责交付与此交易关联的项目的部门。
当对话打开时，系统会将其设置为源报价单的合同签订部门。 | 合同签订部门是在交易完成后将执行项目的公司的部门。 每个合同签订部门有一种货币。 此货币用于报告项目执行过程中产生的预估成本和实际成本。 |
| 货币 | 这是进行交易所使用的货币。 当对话打开时，系统会将其设置为源报价单的货币。 此字段可以修改，如果更改，**复制定价**字段始终设置为**否**。 这是因为与源报价单上的价目表不再相关。 | 货币用于为价目表确定默认值、在报价单上生成财务估算值，最终用于在交易赢单时为客户开票。 |
| 要求交货日期 | 这是客户要求的交货日期。 | 在按照特定频率创建开票日期时，此字段用作结束日期。 |
| 复制定价 | “是/否”值指示是否应从源报价单复制报价单上的定价。 | 如果选择**是**，会将项目价目表和产品价目表引用从源报价单复制到目标报价单。 如果选择**否**，会根据客户或项目参数上设置的最新价目表重新设置价目表的默认值。 |

当您在对话页面上选择**确定**时，系统将根据在对话中选择的参数创建项目报价单的副本。 新项目报价单此时将打开。 

> [!NOTE]
> 以下信息不会从源报价单复制到目标报价单：
>
> - 发票计划
> - 报价单和报价单明细客户
> - 基于项目的报价单明细上的项目引用 – 客户预算信息
>
>由于此信息对于每个报价单都非常特定，因此不会复制这些字段和记录。 项目和产品的报价单明细、报价单明细详细信息中的估算值以及报价单级别的上限值将被复制。 价格和成本率默认值取决于在**复制参数**对话页面上选择的**复制定价**选项。
