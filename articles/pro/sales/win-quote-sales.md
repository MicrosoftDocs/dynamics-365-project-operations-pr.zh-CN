---
title: 关闭项目报价单
description: 本文提供有关在 Project Operations 中结束报价单的信息。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826164"
---
# <a name="close-project-quotes"></a>关闭项目报价单

_**适用于：** 精简部署 - 估价交易开票_

项目报价单可作为赢单或丢单结束。 草稿报价单可以结束，因为 Microsoft Dynamics 365 Project Operations 中不支持对报价单执行激活和修订操作。

## <a name="close-a-quote-as-won"></a>作为赢单结束报价单

当您作为赢单结束项目报价单时，状态将设置为“已结束”，状态描述为“赢单”。 结束报价单会使项目报价单成为只读，并创建一个包含报价单信息的草稿项目合同。 由于无法重新开启已结束的报价单，确认对话将确认您的更改。

如果报价单附加到某个商机，该商机中的任何其他项目报价单都将作为丢单自动结束。

### <a name="financial-impact-of-closing-a-quote-as-won"></a>将报价单作为赢单结束的财务影响

如果项目上有任何时间实际值仍附加在草稿报价单上，将仅记录时间或支出成本。 当报价单作为赢单结束后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重构成本。 应用程序将根据关联项目合同子项的计费方法处理这些成本实际值。 如果成本实际值引用时间和物料合同子项，则会针对报价单结束和项目合同创建的情况创建相应的未记帐实际销售额。 如果成本实际值引用固定价格合同子项，应用程序将停止重新处理基于项目合同客户的已拆分记帐规则的成本实际值。

## <a name="closing-a-quote-as-lost"></a>作为丢单结束报价单

当您作为丢单结束项目报价单时，状态将设置为“已结束”，状态描述为“丢单”。 结束报价单会使项目报价单成为只读。 由于无法重新开启已结束的报价单，因此在结束报价单之前，会有一个确认对话框确认您的更改。

如果作为丢单结束的项目报价单引用其任何行中的项目，该项目也将标记为“已结束”。 从当一天之后的任何资源预订都会被取消。

> [!NOTE]
> 在 Project Operations 中，将报价单作为赢单或丢单结束不会影响商机的状态，在手动结束前商机会一直处于开启状态。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
