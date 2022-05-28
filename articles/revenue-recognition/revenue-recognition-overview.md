---
title: 收入确认概述
description: 本主题提供有关 Project Operations 中的收入确认的信息。
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 51c553ecf45452615cbcadce6386f32be427acaa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601421"
---
# <a name="revenue-recognition-overview"></a>收入确认概述

_**适用于：** 面向资源/非库存场景的 Project Operations_

在 Dynamics 365 Project Operations 中，收入确认原则因项目或部分项目的选定记帐方法而异。 本主题提供有关 Project Operations 中的收入确认的信息。

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>使用时间和材料记帐方法记帐的交易

- 成本和收入确认相互关联。 交易成本和未记帐销售额使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。
- 项目成本和收入配置文件确定是否将未记帐销售交易过帐到总帐。 如果选择了 **应计收入**，则系统在过帐期间会使用 **WIP 销售值** 和 **应计收入销售值** 帐户。 下面是此方法的示例。  

  | 交易记录类型 | 借方/贷方 | 应收总额 |
  | --- | --- | --- |
  | WIP 销售值 | 借方 | 100 |
  | 应计收入销售值 | 贷方 | 100 |

- 开票期间确认了收入。 系统在过帐期间使用 **开票收入** 帐户。 下面是此方法的示例。  

  | 交易记录类型 | 借方/贷方 | 应收总额 |
  | --- | --- | --- |
  | 客户余额 | 借方 | 120 |
  | 销售税应付款 | 贷方 | 20 |
  | 已开票收入 | 贷方 | 100 |

- 如果在过帐未记帐销售额时增加了收入，则系统将在开票时冲销应计收入。

  | 交易记录类型 | 借方/贷方 | 应收总额 |
  | --- | --- | --- |
  | WIP 销售值 | 贷方 | 100 |
  | 应计收入销售值 | 借方 | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>使用固定价格记帐方法记帐的交易

- 成本和收入确认相互独立。 交易成本使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。 系统未创建未记帐销售交易。
- 如果针对项目成本和收入配置文件将 **用于项目完成计算的原则** 设置为 **无 WIP**，则可以在开票期间确认收入。 仅对短期、简单的项目使用此方法。
- 可以将固定价格收入估算与 **已完成合同** 或 **完成百分比收入确认** 方法配合使用来确认收入。

## <a name="additional-resources"></a>其他资源
[“配置收费项目会计”文章](../project-accounting/configure-accounting-billable-projects.md)

[固定价格收入估算项目](rev-rec-percentage-completion-method.md)

[管理收入估算](rev-rec-completed-contract-method.md)

[完成成本计算方法](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]