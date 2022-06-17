---
title: 应用演示设置和配置数据 - 精简
description: 本文提供有关如何为 Project Operations 应用演示设置和配置数据的信息。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 68e504dd031596b295b1383a8e81621744cae8d2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922303"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>为 Project Operations 应用演示设置和配置数据 - 精简 

_**精简部署 - 估价交易开票_



## <a name="prerequisites"></a>先决条件

在开始配置之前，必须为 Dynamics 365 Project Operations 预配 Common Data Service (CDS) 环境。


## <a name="instructions"></a>指令

1. 下载[主数据包](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip)。 
2. 导航到文件夹 *ProjOpsSampleSetupData - CE only CMT* 并运行可执行文件 *DataMigrationUtility*。
3. 在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择 **导入数据**，然后选择 **继续**。

    ![配置迁移。](./media/1ConfigurationMigration.png)

4. 在 CMT 向导的第 2 页上，选择 **Microsoft 365** 作为 **部署类型**。
5. 选择 **显示可用组织列表** 和 **显示高级** 复选框。
6. 选择您的租户的区域，输入您的凭据，然后选择 **登录**。

   ![配置登录。](./media/2ConfigurationSignin.png)

7. 在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择 **登录**。
8. 在第 4 页上，从解压缩文件夹 *ProjOpsSampleSetupData - CE only CMT* 中选择 zip 文件 *SampleSetupAndConfigData*。

   ![Zip 文件。](./media/3ZipFile.png)

   ![选择文件。](./media/4SelectAFile.png)

9. 选择 zip 文件后，选择 **导入数据**。

   ![导入数据。](./media/5ImportData.png)

10. 导入将运行大约二到十分钟，具体时间取决于您的网络速度。 完成后，退出 CMT 向导。 
11. 检查您的组织在以下 18 个实体中的数据：

    -   货币
    -   帐户​​
    -   部门
    -   联系人​​
    -   计价单位
    -   计价单位组
    -   价目表
    -   项目参数价目表 
    -   账单频率
    -   可预订资源的类别
    -   交易类别
    -   费用类别
    -   角色价格
    -   交易类别价格
    -   特征
    -   可预订资源
    -   可预订资源的类别关联
    -   可预订资源的特征

    ![完成导入。](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
