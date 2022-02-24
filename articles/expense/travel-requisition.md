---
title: 出差申请
description: 此主题提供有关出差申请的信息。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123727"
---
# <a name="travel-requisitions"></a>出差申请

_**适用于：** 面向资源/非库存场景的 Project Operations_

出差申请列出了由于出差目的所发生的支出。 出差申请将提交以供审核，可用于对支出授权。

在您产生向组织收取的任何支出之前，您可能需要提交出差申请。 无论您是使用公司信用卡产生的支出，使用预付现金发放的现金，还是产生组织会报销的自付支出，此要求均适用。

出差申请和政策可用于帮助管理组织支出。 例如，如果您的组织正在处理需要出差的固定价格项目，项目的团队成员的出差支出必须在项目预算之内。 通过要求在支出发生之前审批出差支出，组织可以帮助确保项目保持在预算范围内。

## <a name="configuration"></a>配置 

通过在“支出管理参数”中启用“出差必须预授权”参数，可以将出差申请配置为“强制”。 

## <a name="create-and-submit-a-travel-requisition"></a>创建和提交出差申请

1. 转到 **我的支出: 出差申请**，选择 **新建出差申请**。
2. 为申请输入目的和目的地。
3. 在 **出差说明** 字段中，输入任何其他信息。 
4. 对于每个预期支出（如航班、餐费或租车），创建一个支出明细项目。 包括每项支出的预估日期、预估金额和货币。 
5. 完成预期支出的添加后，选择 **保存**。
6. 当您准备好提交出差申请时，选择 **工作流** > **提交**。

您可以在 **我的支出: 出差申请** 下查看已批准的出差申请 。 

## <a name="view-available-travel-requisitions"></a>查看可用出差申请

您可以在 **我的支出: 出差申请** 下查看您的所有出差申请 。

## <a name="approve-travel-requisitions"></a>审批出差申请

选择要审批的出差申请，然后选择 **工作流** > **审批**。  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>使用已批准的出差申请提交支出报表

1. 创建一个新的支出报表，然后在支出报表标题中，从已批准出差申请列表中选择 **映射到出差申请**。
2. 支出报表标题中的 **出差申请金额** 字段会自动更新。
3. 添加出差期间发生的每项支出。 如果启用了 **预授权** 字段，将更新特定支出类别的对帐金额和授权金额。

> [!NOTE]
> 当您将某一支出报表映射到批准的出差申请时，交易金额不能大于授权金额。 
