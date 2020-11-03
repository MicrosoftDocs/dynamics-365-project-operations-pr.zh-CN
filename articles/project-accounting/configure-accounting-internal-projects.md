---
title: 配置内部项目会计
description: 此主题提供有关如何在 Project Operations 中为内部项目设置会计实践的信息。
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072538"
---
# <a name="configure-accounting-for-internal-projects"></a>配置内部项目会计

_**适用于：** 面向资源/非库存场景的 Project Operations_

内部项目允许公司跟踪与未对客户计费的活动相关的成本。 内部项目的示例包括：

- 开发产品（如移动应用），以及跟踪与开发相关的成本。
- 管理预售时间和支出。 如果报价单赢单，此预售内部项目以后可以转换为可计费项目。

与 Dynamics 365 Project Operations 中的合同不关联的任何项目都将被视为内部项目。 项目成本和收入模板不用于确定项目的会计规则。 内部项目成本始终使用损益原则过帐。 用于过帐的分类帐科目在 **分类帐过帐设置** 页定义。

- 时间交易通过借记 **成本** 科目并记入 **工资分配** 科目来过帐。
- 支出交易通过借记 **成本** 科目并记入 **支出的抵销科目** 来过帐。

交易过帐到项目后，如果项目与项目合同相关联，系统将冲销所有累计交易并创建新的可计费交易。 可计费交易遵循在各自的项目成本和收入模板中定义的会计规则。


