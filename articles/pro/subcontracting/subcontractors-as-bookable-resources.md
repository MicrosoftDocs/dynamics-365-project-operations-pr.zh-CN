---
title: 将分包商设置为可预订资源
description: 本主题解释了如何设置和维护根据系统中的用户和联系人创建的分包商资源，以便他们可以与 Microsoft Dynamics 365 Project Operations 中的分包合同关联。
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994175"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>将分包商设置为可预订资源

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

按照以下步骤在 Microsoft Dynamics 365 Project Operations 中将分包商设置为可预订资源。

1. 转到 **项目** \> **资源**，并选择 **新建**。
2. 在 **新可预订资源** 页面内的 **资源类型** 字段中，选择以下选项之一：

    - **用户** – 如果分包商必须访问 Project Operations 才能输入时间或支出，请选择此资源类型。 如果您选择 **用户**，分包商需要使用有效的许可证才能访问系统。
    - **联系人** 或 **客户** - 如果分包商不需要访问 Project Operations，但必须可用于项目任务分配或预订，请选择其中一种资源类型。 这两种资源类型都不提供系统访问权限。 选择 **客户** 以将供应商的公司表示为可预订资源。 选择 **联系人** 以代表供应商的个别员工。

3. 系统会根据您选择的资源类型提示您选择相应的用户、客户或联系人记录。
4. 在 **工作人员的类型** 字段中，选择“合同工”以将分包商设置为可预订资源。

    > [!NOTE]
    > 如果将 **工作人员的类型** 字段留空，则可预订资源将被视为员工。

5. 如果您选择了 **合同工** 作为工作人员的类型，请选择资源为其工作的供应商。
6. 选择资源的时区，然后选择 **保存**。 要将工作时间模板分配给可预订资源，您可以在 **可预订资源** 列表页面上选择 **设置日历**。

要与分包合同子项相关联，可预订资源必须满足以下条件：

- 可预订资源必须是合同工。
- **联系人** 资源类型的可预订资源必须与作为联系人的供应商客户关联。 **用户** 资源类型的可预订资源不必与作为联系人的供应商客户关联。
- 可预订资源的 **供应商** 字段的值必须与分包商的 **供应商** 字段的值相匹配。

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>更新可预订资源的工作人员和供应商映射的类型

可预订资源的 **工作人员的类型** 字段决定了可预订资源是合同工还是员工。 **供应商** 字段定义与可预订资源关联的供应商客户。 通过将可预订资源与作为联系人的供应商关联，您表明该联系人是供应商公司的员工。

如果可预订资源的 **工作人员的类型** 和 **供应商** 字段发生了变化，则更改将影响可预订资源创建的新记录（如时间条目）的任何未来验证。 但是，这些更改不会使现有记录失效。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
