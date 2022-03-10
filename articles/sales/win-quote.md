---
title: 结束报价单
description: 此主题提供有关在 Project Operations 中结束报价单的信息。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993410"
---
# <a name="close-a-quote"></a>结束报价单

_**适用于：** 面向资源/非库存场景的 Project Operations_

项目报价单可作为赢单或丢单结束。 因为 Microsoft Dynamics 365 Project Operations 中不支持对报价单执行激活和修订功能，所以您可以结束草稿报价单。

## <a name="close-a-quote-as-won"></a>作为赢单结束报价单

将项目报价单作为赢单结束会将报价单的状态设置为 **已结束**，将状态描述设置为 **赢单**。 结束报价单会使其变为只读，并创建一个包含所有报价单信息的草稿项目合同。 由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。

从项目报价单创建的项目合同在 Project Operations 的项目管理和会计模块中也会变为可用。 如果项目合同未映射到其任何子项上的项目，此项目合同将作为停用项目合同提供，并在项目至少映射到其合同子项中的一项后即变为可用。

如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。

### <a name="financial-impact-of-closing-a-quote-as-won"></a>将报价单作为赢单结束的财务影响

如果在项目仍附在草稿报价单上时项目中记录了时间的实际值，将仅记录时间或支出成本。 当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。 应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。 如果成本实际值引用时间和材料合同子项，系统将自动为报价单结束和项目合同创建创建相应的未记帐销售实际值。 如果成本实际值引用固定价格合同子项，应用程序将根据项目合同客户的拆分计费规则停止重新处理成本实际值。

所有重新处理的实际值均在项目管理和会计模块中提供，供项目会计查看、更新和过帐到总帐。 

## <a name="close-a-quote-as-lost"></a>作为丢单结束报价单

将项目报价单作为丢单结束会将状态设置为 **已结束**，将状态描述设置为 **丢单**。 结束报价单会使其变为只读。 由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。

如果作为丢单结束的项目报价单在其任意明细上引用了项目，该项目也将标记为“已结束”，那一天之后的所有资源预订都将取消。

> [!NOTE]
> 在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。


[!INCLUDE[footer-include](../includes/footer-banner.md)]