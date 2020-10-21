---
title: 在 Project Operations 的 Common Data Service 中设置和应用配置数据
description: 此主题提供有关在 Project Operations 中设置和应用配置数据的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948770"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>在 Project Operations 的 Common Data Service 中设置和应用配置数据

_**适用于：** 面向资源/非库存场景的 Project Operations_

## <a name="install-setup-and-configuration-data"></a>安装设置和配置数据

1. 下载、取消阻止和解压缩[设置和配置数据包](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。
2. 导航到解压缩的文件夹，运行可执行文件 *DataMigrationUtility*。
3. 在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择**导入数据**，然后选择**继续**。

![配置迁移](./media/1ConfigurationMigration.png)

4. 在 CMT 向导的第 2 页上，选择 **Office 365** 作为**部署类型**。
5. 选择**显示可用组织列表**和**显示高级**复选框。
6. 选择您的租户的区域，输入您的凭据，选择**登录**。

![配置登录](./media/2ConfigurationSignin.png)

7. 在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择**登录**。
8. 在第 4 页上，从解压缩的文件夹中选择 zip 文件 *SampleSetupAndConfigData*。

![Zip 文件选择](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. 选择 zip 文件后，选择**导入数据**。

![导入数据](./media/5ImportData.png)

10. 导入将运行大约二到十分钟，具体时间取决于您的网络速度。 完成导入后，退出 CMT 向导。 
11. 检查您的组织在以下 19 个实体中的数据：

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

## <a name="update-project-operations-configurations"></a>更新 Project Operations 配置

1. 导航到 CE 环境。 打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，选择环境，然后选择**打开环境**可以找到它。 

![打开环境](./media/7OpenEnvironment.png)

2. 转到**项目** > **资源**，然后选择**新建**为您的用户创建可预订资源。

![可预订资源](./media/8BookableResources.png)

3. 在**常规**选项卡上，选择您的管理员用户。 验证时区是否与您所在的时区匹配。 

![新增可预订资源](./media/9NewBookableResource.png)

4. 在**计划**选项卡上的**公司**字段中，选择 **USPM** 公司，然后选择**保存**。 

![“计划”选项卡](./media/10SchedulingTab.png)

5. 选择**工作时间**选项卡。  

![工作时间](./media/11WorkHours.png)

6. 双击日历中的任意值，然后选择**编辑** > **系列中的所有事件**。 

![工作日历](./media/12WorkCalendar.png)

7. 将工作时间更改为八 (8) 小时工作日，将周末标记为非工作日，确保时区与您的时区匹配。 
8. 选择**保存并关闭**。

![更新日历](./media/13UpdateCalendar.png)

9. 转到**设置** > **日历模板**，选择**新建**。
 
 ![日历模板](./media/14CalendarTemplates.png)
 
 10. 输入名称，选择所创建的模板资源，然后选择**保存**。 
 
 ![保存日历模板](./media/15SaveCalendarTemplate.png)
 
 11. 转到**参数**，双击记录。 
 
 ![项目参数](./media/16ProjectParameters.png)
 
12. 更新以下字段：

 - **默认公司**：USPM
 - **默认部门**：Contoso Robotics Global
 - **发票频率**：第七天和最后一天
 - **工作时间模板**：更改为您创建的模板。

13. 选择**保存**。 

![更新后的项目参数](./media/17UpdatedProjectParameters.png)
