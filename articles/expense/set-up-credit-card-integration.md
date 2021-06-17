---
title: 设置信用卡集成
description: 本主题介绍如何处理与支出相关的信用卡交易。
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001794"
---
# <a name="set-up-credit-card-integration"></a>设置信用卡集成

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

可以设置与支出相关的信用卡交易记录，以将其自动导入到定期计划中。 或者，可以根据需要手动导入交易记录。 信用卡交易记录通过信用卡交易记录数据实体导入。

## <a name="import-credit-card-transactions"></a>导入信用卡交易记录

若要导入信用卡交易，请执行以下步骤：

1. 在 **信用卡交易记录** 页上，选择 **导入交易记录**。 如果您是第一次打开数据管理，系统必须更新数据实体列表，然后才能继续。
2. 在 **名称** 字段中，输入导入作业的特有说明。
3. 在 **源数据格式** 字段中，选择包含要导入的信用卡交易记录的文件的格式。
4. 选择 **上载**，然后查找并选择要导入的文件。
5. 上载文件后，通过选择磁贴上的 **查看映射** 链接，验证信用卡交易记录文件和信用卡交易记录数据实体的列的映射。 如果存在映射错误，或者您必须更改映射，请从 **映射可视化项** 选项卡或 **映射详细信息** 选项卡更改映射。
6. 若要自动处理信用卡交易记录，请选择 **创建定期数据作业**。 然后，您可以设置定义应如何导入信用卡交易记录的定期计划。 在您完成时，选择 **确定**。
7. 若要立即导入所选的文件，请选择 **导入**。
8. 如果在导入期间发生错误，则可以查看执行日志或暂存数据，以查看必须修复的错误，帮助确保导入成功。

> [!NOTE]
> 如果您需要导入多种文件格式，则必须为每种格式类型创建单独的导入作业。

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>重新分配已离职员工的信用卡交易记录

员工记录终止后，该员工的 Active Directory 域服务 (AD DS) 帐户将被禁用。 不过，可能存在仍需要支出和还款的活动信用卡交易记录。 在 **信用卡交易** 页上，可以为关联员工已被解聘的任何信用卡交易重新分派员工。

选择一个或多个信用卡交易记录，然后选择 **重新分配交易记录**。 然后，您可以选择要向其分配信用卡交易记录的另一名员工。 在信用卡交易记录重新分配后，可以选择将其用于支出报表，并通过通常的支出报表还款流程进行支付。

## <a name="delete-credit-card-transactions"></a>删除信用卡交易 

有时，在导入信用卡交易后，可能需要删除某些交易。 这可能是因为交易是重复交易，或者因为数据可能不够准确。 管理员可以使用 **删除信用卡交易** 功能来选择和删除 **未附加** 到支出报表的信用卡交易。 

1. 转到 **定期任务** > **删除信用卡交易**。
2. 选择 **筛选** 并提供用于标识要包含的记录的信息。
3. 选择 **确定** 以删除记录。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
