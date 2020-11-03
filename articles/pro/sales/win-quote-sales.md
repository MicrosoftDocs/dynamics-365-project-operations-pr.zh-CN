---
title: 结束报价单
description: 此主题提供有关在 Project Operations 中结束报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072525"
---
# <a name="close-quotes"></a>结束报价单 

_**适用于：** 精简部署 - 估价交易开票_

项目报价单可作为赢单或丢单结束。 Microsoft Dynamics 365 Project Operations 中不支持对报价单执行“激活”和“修订”操作，因此可以结束报价单草稿。

## <a name="close-a-quote-as-won"></a>作为赢单结束报价单

将项目报价单作为赢单结束将结束报价单，并将状态设置为“已结束”，将状态描述设置为“赢单”。 结束报价单会使项目报价单成为只读，并创建一个包含报价单信息的草稿项目合同。 由于无法重新开启已结束的报价单，因此有一个确认对话框。由于无法重新开启已结束的报价单，并且更改不可逆，因此，在进行更改之前，会出现一个确认对话框。

如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。

### <a name="financial-impact-of-closing-a-quote-as-won"></a>将报价单作为赢单结束的财务影响

如果在项目仍附在草稿报价单上时项目中记录了时间的实际值，将仅记录时间或支出成本。 当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。 应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。 如果成本实际值引用时间和材料合同子项，系统将自动为报价单结束和项目合同创建创建相应的未记帐销售实际值。 如果成本实际值引用固定价格合同子项，应用程序将根据项目合同客户的拆分计费规则停止重新处理成本实际值。

## <a name="closing-a-quote-as-lost"></a>作为丢单结束报价单：

将项目报价单作为丢单结束会将状态设置为“已结束”，将状态描述设置为“丢单”。 结束报价单会使项目报价单成为只读。 由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。

如果作为丢单结束的项目报价单在其任意明细上引用了项目，该项目也将标记为“已结束”，那一天之后的所有资源预订都将取消。

> [!NOTE]
> 在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。
