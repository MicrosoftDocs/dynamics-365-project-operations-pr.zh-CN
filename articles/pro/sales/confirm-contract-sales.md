---
title: 确认项目合同
description: 本文提供如何在 Project Operations 中确认合同的信息。
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929985"
---
# <a name="confirm-a-project-contract"></a>确认项目合同

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 中的项目合同可以由于 **已确认** 的原因而处于活动状态，或者由于 **丢失** 的原因而处于关闭状态。 在确认项目合同时，状态将从 **草稿** 更新为 **有效**，状态描述为 **已确认**。 有效或关闭的合同无法编辑或重新打开。 

### <a name="financial-impact-of-confirming-a-project-contract"></a>确认项目合同的财务影响

确认项目合同后，应用程序将通过冲销较旧成本实际值并重新创建新成本实际值来重新计算成本。 然后根据关联项目合同子项的计费方法处理新的成本实际值。 如果成本实际值引用时间和材料合同子项，应用程序会自动重新创建相应的未记帐实际销售额。 如果成本实际值引用固定价格合同子项，应用程序将停止重新处理成本实际值。

实际值中的上限、应计费设置以及定价和成本核算将在确认过程中评估，然后更新。

## <a name="close-a-project-contract-as-lost"></a>作为丢单关闭项目合同

当作为丢单关闭项目合同时，合同状态将更新为 **已关闭**，状态描述为 **丢单**。 项目合同将变为只读。 在完成更改之前，会提供确认对话框，因为您无法重新打开已关闭的项目合同。

如果作为丢单关闭的项目合同在其子项上引用了项目，该项目也会标记为关闭。 从当一天之后的任何资源预订都会被取消。 发票上尚未包含的项目合同上的任何未记帐实际销售额都将被冲销。

> [!NOTE]
> 在 Dynamics 365 Project Operations中，以丢单形式结束项目合同不会影响相关商机的状态。 商机仍保持开启状态，必须手动结束。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]