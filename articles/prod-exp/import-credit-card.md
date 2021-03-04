---
title: 导入和维护信用卡交易记录
description: 此主题介绍如何导入和维护与支出相关的信用卡交易记录。 这些交易记录可以设置为对重复执行的计划自动导入或根据需要手动导入。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960416"
---
# <a name="import-and-maintain-credit-card-transactions"></a>导入和维护信用卡交易记录

可以设置与支出相关的信用卡交易记录，以将其自动导入到定期计划中。 或者，可以根据需要手动导入交易记录。 信用卡交易记录通过信用卡交易记录数据实体导入。

有关数据实体的详细信息，请参阅[数据实体](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)。

## <a name="import-credit-card-transactions"></a>导入信用卡交易记录

1. 在 **信用卡交易记录** 页上，选择 **导入交易记录**。 如果您是第一次打开数据管理，系统必须更新数据实体列表，然后才能继续。
2. 在 **名称** 字段中，为导入作业输入唯一说明。
3. 在 **源数据格式** 字段中，选择包含要导入的信用卡交易记录的文件的格式。
4. 选择 **上载**，然后查找并选择要导入的文件。
5. 上载文件后，通过选择磁贴上的 **查看映射** 链接，验证信用卡交易记录文件和信用卡交易记录数据实体的列的映射。 如果存在映射错误，或者您必须更改映射，请从 **映射可视化项** 选项卡或 **映射详细信息** 选项卡更改映射。
6. 若要自动处理信用卡交易记录，请选择 **创建定期数据作业**。 然后，您可以设置定义应如何导入信用卡交易记录的定期计划。 在您完成时，选择 **确定**。
7. 若要立即导入所选的文件，请选择 **导入**。
8. 如果在导入过程中出现错误，您可以查看执行日志或暂存数据，来查看为帮助确保成功导入而必须修复的错误。

> [!NOTE]
> 如果必须导入多个文件格式，必须为每个格式类型创建单独的导入作业。

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>重新分配已离职员工的信用卡交易记录

员工记录终止后，该员工的 Active Directory 域服务 (AD DS) 帐户将被禁用。 不过，可能存在仍需要支出和还款的活动信用卡交易记录。 在 **信用卡交易记录** 页上，您可以为已离职的关联员工的任何信用卡交易记录重新分配员工。

选择一个或多个信用卡交易记录，然后选择 **重新分配交易记录**。 然后，您可以选择要向其分配信用卡交易记录的另一名员工。 在信用卡交易记录重新分配后，可以选择将其用于支出报表，并通过通常的支出报表还款流程进行支付。


[!INCLUDE[footer-include](../includes/footer-banner.md)]