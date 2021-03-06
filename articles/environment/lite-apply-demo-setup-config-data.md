---
title: 应用演示设置和配置数据
description: 此主题提供有关如何为 Project Operations 应用演示设置和配置数据的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948767"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>为 Project Operations 精简部署应用演示设置和配置数据 - 估价交易开票

_**精简部署 - 估价交易开票_

1. 下载[主数据包](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。 
2. 导航到文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*，运行可执行文件 *DataMigrationUtility*。
3. 在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择**导入数据**，然后选择**继续**。

![配置迁移](./media/1ConfigurationMigration.png)

4. 在 CMT 向导的第 2 页上，选择 **Office 365** 作为**部署类型**。
5. 选择**显示可用组织列表**和**显示高级**复选框。
6. 选择您的租户的区域，输入您的凭据，然后选择**登录**。

![配置登录](./media/2ConfigurationSignin.png)

7. 在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择**登录**。
8. 在第 4 页上，从解压缩的文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中选择 zip 文件 *MasterAndSetupData*。

![Zip 文件](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. 选择 zip 文件后，选择**导入数据**。

![导入数据](./media/5ImportData.png)

10. 导入将运行大约二到十分钟，具体时间取决于您的网络速度。 完成后，退出 CMT 向导。 
11. 检查您的组织在以下 20 个实体中的数据：

- 货币
- 部门
- 联系人​​
- 税组
- 客户组
- 计价单位
- 计价单位组
- 价目表
- 项目参数价目表
- 账单频率
- 发票频率详细信息
- 可预订资源的类别
- 交易类别
- 费用类别
- 角色价格
- 交易类别价格
- 特征
- 可预订资源
- 可预订资源的类别关联
- 可预订资源的特征

![完成导入](./media/6CompleteImport.png)
