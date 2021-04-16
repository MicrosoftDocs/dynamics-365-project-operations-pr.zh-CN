---
title: 复制基于项目的商机
description: 此主题提供有关如何在 Project Operations 中复制基于项目的商机的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1808469a34e05eb926f13c62ec634e8273b0e33c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278542"
---
# <a name="copy-project-based-opportunities"></a>复制基于项目的商机

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


项目商机可以轻松地复制来创建新的项目商机。 

1. 转到 **项目商机** 列表页，从列表中选择商机。 或者，打开特定商机的详细信息页。 
2. 在任一页面，选择 **复制**。 将打开一个包含以下字段信息的对话页面。 根据在此对话中选择的值，复制过程可能会有变化。

    | **字段** | **说明** | **下游影响** |
    | --- | --- | --- |
    | 主题 | 输入目标商机的相关主题。 当对话打开时，系统会将其设置为源商机的主题，并附加 **copy**。 | 此字段没有下游影响。 |
    | 帐户​​ | 对客户的公司或客户记录的引用。 当对话打开时，系统会将其设置为源商机上的客户。 | 此字段是商机上的主要客户。 |
    | 合同签订部门 | 负责交付与此交易关联的项目的部门。 当对话打开时，系统会将其设置为源商机的合同签订部门。 | 合同签订部门是在交易完成后执行项目的公司的部门。 每个合同签订部门都有一种货币，此货币用于报告项目中产生的预估成本和实际成本。 |
    | 货币 | 进行交易所使用的货币。 当对话页面打开时，系统会将其设置为源商机的货币。 | 货币用于确定默认价目表以及在报价单上生成财务估算值。 最后，当交易赢单时，此货币用于向客户开票。 |
    | 复制定价 | “是/否”值指示是否应从源商机复制商机上的定价。 | 如果选择 **是**，价目表将从源商机复制到目标商机。 如果选择 **否**，会根据设置的最新价目表确定默认价目表。 |

3. 选择 **确定**。 系统将根据选定的参数创建项目商机的副本，新项目商机将打开。


[!INCLUDE[footer-include](../includes/footer-banner.md)]