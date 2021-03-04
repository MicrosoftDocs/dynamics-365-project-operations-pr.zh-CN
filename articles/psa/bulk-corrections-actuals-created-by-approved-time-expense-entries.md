---
title: 批量更正通过批准的时间和支出条目创建的实际值
description: 此主题解释在账单未完成时，管理员如何对以前批准的时间或支出条目进行单项或批量更正。
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144942"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>批量更正通过批准的时间和支出条目创建的实际值

[!include [banner](../includes/psa-now-project-operations.md)]

有时，可能未正确输入时间或支出条目。 例如，顾问在创建时间条目时可能会选择错误的日期，也可能会在输入支出时转置这些数字。 如果顾问无法更新提交的条目，则管理员可以直接更正项目的条目。

若要完成本主题中的过程，您将需要管理员权限。

## <a name="correct-approved-time-entries"></a>更正已批准的时间条目     

完成以下步骤以更正项目的一个或多个时间条目。

1. 在 **销售** 区域中，选择 **交易**，然后选择 **已批准的时间**。 

2. 在 **已批准的时间** 列表中，找到并选择一个或多个要更正的已批准时间条目。 您可以使用筛选器来查找相关条目。 例如，您可以对项目 ID 进行筛选，然后选择具有该项目 ID 的所有已批准时间条目。

3. 选择 **更正条目**。 系统会自动创建已分配类型为 **时间更正** 的新更正日记帐。 您选择的条目会添加到日记帐中。 

4. 在 **新建日记帐** 页上，输入您的更正日记帐的 **说明**，然后选择 **时间条目更正** 选项卡。  
5. 在 **时间条目的新值** 部分中，根据需要使用正确的信息更新字段。 例如，您可以更改指派的项目或可预订资源。

6. 选择 **预览**。 在对话框中，选择 **确定**。 在 **日记帐行** 选项卡上，您可以查看与已冲销的所选时间条目相关的原始实际值列表，以及已创建的所更正相应行。 如果需要进行其他更正，请重复步骤 5 和步骤 6。 

> [!NOTE]
> 所有已更正的实际值将与您在 **时间条目的新值** 部分中选择的值相同。

7. 如果更正按预期方式显示，请选择 **确认**。 在对话框中，选择 **确定**。

8. 返回到 **销售** 区域，选择 **项目**，然后打开刚刚更新时间条目所针对的项目。 

9. 在 **项目** 页上的 **实际值** 选项卡中，查看所做的更改。 

> [!NOTE]
> 如果 **实际值** 选项卡不可见，请选择 **相关** > **实际值**。  

10. 在 **实际关联视图** 列表中，您可以看到仍然列出了已冲销的原始时间条目，以及相应的已更正时间条目。 

例如，在下图中，有两个数量为 8.00 的行项，“金额”列中列出了其相应的借项。 此外，还有两个数量为 -8.00 的行项，这些行项在“金额”列中显示了贷项金额。 这些更正会将数量调为零。

![实际关联视图列表](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>更正已批准的支出条目

完成以下步骤以更正一个或多个支出条目。 

1. 在 **销售** 区域左侧导航窗格中的 **交易** 下面，选择 **已批准的支出**。

2. 在 **已批准的支出** 列表中，选择要更正的项目，然后选择 **更正条目**。 系统将自动创建已分配类型为 **支出更正** 的新更正日记帐。 

3. 在 **新建日记帐** 页上，输入有关更正的 **说明**，然后在 **支出更正** 选项卡上的 **支出的新值** 部分中，选择要为所选支出行更正的数据字段。 例如，您可以将支出分配给其他 **项目**，或者更正 **支出类别**、**支出日期** 或 **可预订的资源**。

4. 选择 **预览**。 在对话框中，选择 **确定**。 

5. 在 **日记帐行** 选项卡上验证更正。您可以查看与已冲销的所选支出条目相关的原始实际值列表，以及已创建的所更正相应行。

6. 如果更正的值符合预期，请选择 **确认**。 在对话框中，选择 **确定**。 如果这些值未按预期方式显示，请选择 **取消** 以返回到 **已批准的支出** 列表。 重复步骤 2 到步骤 5。 

> [!NOTE]
> 已更正的实际值将与您在 **支出的新值** 部分中选择的值相同。

7. 在确认了更正日记帐之后，请导航回您更新的一个或一些项目，以查看所做的更改。  

8. 在项目页中的 **实际值** 选项卡上，查看 **实际关联视图**。 系统会列出原始条目和已更正的条目。 下图显示了原始支出条目金额和相应的已更正支出条目金额。 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]