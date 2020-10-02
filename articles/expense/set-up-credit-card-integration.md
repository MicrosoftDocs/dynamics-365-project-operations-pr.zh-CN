---
title: 设置信用卡集成
description: 此主题介绍如何导入和维护与支出相关的信用卡交易记录。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896810"
---
# <a name="set-up-credit-card-integration"></a>设置信用卡集成

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

可以设置与支出相关的信用卡交易记录，以将其自动导入到定期计划中。 或者，可以根据需要手动导入交易记录。 信用卡交易记录通过信用卡交易记录数据实体导入。

## <a name="import-credit-card-transactions"></a>导入信用卡交易记录

1. 在**信用卡交易记录**页上，选择**导入交易记录**。 如果您是第一次打开数据管理，系统必须更新数据实体列表，然后才能继续。
2. 在**名称**字段中，为导入作业输入唯一说明。
3. 在**源数据格式**字段中，选择包含要导入的信用卡交易记录的文件的格式。
4. 选择**上载**，然后查找并选择要导入的文件。
5. 上载文件后，通过选择磁贴上的**查看映射**链接，验证信用卡交易记录文件和信用卡交易记录数据实体的列的映射。 如果存在映射错误，或者您必须更改映射，请从**映射可视化项**选项卡或**映射详细信息**选项卡更改映射。
6. 若要自动处理信用卡交易记录，请选择**创建定期数据作业**。 然后，您可以设置定义应如何导入信用卡交易记录的定期计划。 在您完成时，选择**确定**。
7. 若要立即导入所选的文件，请选择**导入**。
8. 如果在导入过程中出现错误，您可以查看执行日志或暂存数据，来查看为帮助确保成功导入而必须修复的错误。

> [!NOTE]
> 如果必须导入多个文件格式，必须为每个格式类型创建单独的导入作业。

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>重新分配已离职员工的信用卡交易记录

员工记录终止后，该员工的 Active Directory 域服务 (AD DS) 帐户将被禁用。 不过，可能存在仍需要支出和还款的活动信用卡交易记录。 在**信用卡交易记录**页上，您可以为已离职的关联员工的任何信用卡交易记录重新分配员工。

选择一个或多个信用卡交易记录，然后选择**重新分配交易记录**。 然后，您可以选择要向其分配信用卡交易记录的另一名员工。 在信用卡交易记录重新分配后，可以选择将其用于支出报表，并通过通常的支出报表还款流程进行支付。
