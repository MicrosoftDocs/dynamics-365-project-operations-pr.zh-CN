---
title: 配置内部项目会计
description: 本文提供有关如何在 Project Operations 中为内部项目设置会计实务的信息。
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919451"
---
# <a name="configure-accounting-for-internal-projects"></a>配置内部项目会计

_**适用于：** 面向资源/非库存场景的 Project Operations_

内部项目允许公司跟踪与未对客户计费的活动相关的成本。 内部项目的示例包括：

- 开发产品（如移动应用），以及跟踪与开发相关的成本。
- 管理预售时间和支出。 如果报价单赢单，此预售内部项目以后可以转换为可计费项目。

未与 Dynamics 365 Project Operations 中的合同关联的任何项目都被视为内部项目。 项目成本和收入模板不用于确定项目的会计规则。 内部项目成本始终使用损益原则过帐。 用于过帐的分类帐科目在 **分类帐过帐设置** 页定义。

- 时间交易通过借记 **成本** 科目并记入 **工资分配** 科目来过帐。
- 支出交易通过借记 **成本** 科目并记入 **支出的抵销科目** 来过帐。
- 项目交易过帐通过借记 **成本** 科目和贷记 **成本 - 项目** 科目来实现。

交易过帐到项目后，如果项目与项目合同相关联，系统将冲销所有累计交易并创建新的可计费交易。 可计费交易遵循在各自的项目成本和收入模板中定义的会计规则。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
