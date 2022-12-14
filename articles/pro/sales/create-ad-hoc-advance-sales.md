---
title: 在项目合同中创建临时预付款
description: 本文提供有关根据需要在合同中创建预付款的信息。
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824833"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>在项目合同中创建临时预付款

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Microsoft Dynamics 365 Project Operations 支持涉及预付款的开票场景。 在 **Project Operations** 中使用 **预付款** 的流程与 **保留款** 合同类似。 

完成以下步骤为客户的预付款开票。

1. 转到 **项目合同** 页，然后选择 **预付款和保留款** 选项卡。
2. 在列出所有以前记录的预付款的子网格中，选择 **+ 新建项目合同保留款**。 

    **快速创建** 窗体将打开以记录预付款。
    
3. 下表列出了记录预付款的字段，以及在创建新预付款时需要记住的注意事项：

    | 字段 | 描述 | 下游影响 |
    | --- | --- | --- |
    | **项目合同客户** | 此字段指示将就此预付款为合同中的哪个客户开票。 | 如果您在合同中有多个客户，想要为每个客户的特定保留款或预付款金额开票，请为每个客户单独创建预付款。 |
    | **说明** | 预付款的用途或时间的说明，帮助识别此预付款。 | 此说明显示在此预付款的发票明细上。 |
    | **金额** | 预付款的金额。 | 此金额显示在此预付款的发票明细上。 |
    | **账单日期** | 就此预付款向客户开票的日期。 | 此日期是为此预付款创建发票明细的自动发票创建流程的日期。 |
    | **账单状态** | 这是一个选项设置，指示此预付款是否已添加到此客户的草稿发票中。 值可以为：</br>- **未准备好开具账单**</br>- **已准备好开具账单** | 在将预付款标记为 **可开票** 时，它将在草稿发票上添加为明细时间。 只有完全开票的预付款才能用于与下一个发票期间的项目成本对帐。 |

4. 在快速创建对话中选择 **保存并关闭** 记录预付款。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
