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
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="eca1b-103">在 Project Operations 的 Common Data Service 中设置和应用配置数据</span><span class="sxs-lookup"><span data-stu-id="eca1b-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="eca1b-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="eca1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="eca1b-105">安装设置和配置数据</span><span class="sxs-lookup"><span data-stu-id="eca1b-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="eca1b-106">下载、取消阻止和解压缩[设置和配置数据包](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。</span><span class="sxs-lookup"><span data-stu-id="eca1b-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="eca1b-107">导航到解压缩的文件夹，运行可执行文件 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="eca1b-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="eca1b-108">在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择**导入数据**，然后选择**继续**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![配置迁移](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="eca1b-110">在 CMT 向导的第 2 页上，选择 **Office 365** 作为**部署类型**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="eca1b-111">选择**显示可用组织列表**和**显示高级**复选框。</span><span class="sxs-lookup"><span data-stu-id="eca1b-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="eca1b-112">选择您的租户的区域，输入您的凭据，选择**登录**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![配置登录](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="eca1b-114">在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择**登录**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="eca1b-115">在第 4 页上，从解压缩的文件夹中选择 zip 文件 *SampleSetupAndConfigData*。</span><span class="sxs-lookup"><span data-stu-id="eca1b-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip 文件选择](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. <span data-ttu-id="eca1b-118">选择 zip 文件后，选择**导入数据**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-118">After the zip file is selected, select **Import Data**.</span></span>

![导入数据](./media/5ImportData.png)

10. <span data-ttu-id="eca1b-120">导入将运行大约二到十分钟，具体时间取决于您的网络速度。</span><span class="sxs-lookup"><span data-stu-id="eca1b-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="eca1b-121">完成导入后，退出 CMT 向导。</span><span class="sxs-lookup"><span data-stu-id="eca1b-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="eca1b-122">检查您的组织在以下 19 个实体中的数据：</span><span class="sxs-lookup"><span data-stu-id="eca1b-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="eca1b-123">货币</span><span class="sxs-lookup"><span data-stu-id="eca1b-123">Currency</span></span>
  - <span data-ttu-id="eca1b-124">部门</span><span class="sxs-lookup"><span data-stu-id="eca1b-124">Organizational Unit</span></span>
  - <span data-ttu-id="eca1b-125">联系人​​</span><span class="sxs-lookup"><span data-stu-id="eca1b-125">Contact</span></span>
  - <span data-ttu-id="eca1b-126">税组</span><span class="sxs-lookup"><span data-stu-id="eca1b-126">Tax Group</span></span>
  - <span data-ttu-id="eca1b-127">客户组</span><span class="sxs-lookup"><span data-stu-id="eca1b-127">Customer Group</span></span>
  - <span data-ttu-id="eca1b-128">计价单位</span><span class="sxs-lookup"><span data-stu-id="eca1b-128">Unit</span></span>
  - <span data-ttu-id="eca1b-129">计价单位组</span><span class="sxs-lookup"><span data-stu-id="eca1b-129">Unit Group</span></span>
  - <span data-ttu-id="eca1b-130">价目表</span><span class="sxs-lookup"><span data-stu-id="eca1b-130">Price List</span></span>
  - <span data-ttu-id="eca1b-131">项目参数价目表</span><span class="sxs-lookup"><span data-stu-id="eca1b-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="eca1b-132">账单频率</span><span class="sxs-lookup"><span data-stu-id="eca1b-132">Invoice Frequency</span></span>
  - <span data-ttu-id="eca1b-133">可预订资源的类别</span><span class="sxs-lookup"><span data-stu-id="eca1b-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="eca1b-134">交易类别</span><span class="sxs-lookup"><span data-stu-id="eca1b-134">Transaction Category</span></span>
  - <span data-ttu-id="eca1b-135">费用类别</span><span class="sxs-lookup"><span data-stu-id="eca1b-135">Expense Category</span></span>
  - <span data-ttu-id="eca1b-136">角色价格</span><span class="sxs-lookup"><span data-stu-id="eca1b-136">Role Price</span></span>
  - <span data-ttu-id="eca1b-137">交易类别价格</span><span class="sxs-lookup"><span data-stu-id="eca1b-137">Transaction Category Price</span></span>
  - <span data-ttu-id="eca1b-138">特征</span><span class="sxs-lookup"><span data-stu-id="eca1b-138">Characteristic</span></span>
  - <span data-ttu-id="eca1b-139">可预订资源</span><span class="sxs-lookup"><span data-stu-id="eca1b-139">Bookable Resource</span></span>
  - <span data-ttu-id="eca1b-140">可预订资源的类别关联</span><span class="sxs-lookup"><span data-stu-id="eca1b-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="eca1b-141">可预订资源的特征</span><span class="sxs-lookup"><span data-stu-id="eca1b-141">Bookable Resource Characteristic</span></span>

![完成导入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="eca1b-143">更新 Project Operations 配置</span><span class="sxs-lookup"><span data-stu-id="eca1b-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="eca1b-144">导航到 CE 环境。</span><span class="sxs-lookup"><span data-stu-id="eca1b-144">Navigate to the CE environment.</span></span> <span data-ttu-id="eca1b-145">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，选择环境，然后选择**打开环境**可以找到它。</span><span class="sxs-lookup"><span data-stu-id="eca1b-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![打开环境](./media/7OpenEnvironment.png)

2. <span data-ttu-id="eca1b-147">转到**项目** > **资源**，然后选择**新建**为您的用户创建可预订资源。</span><span class="sxs-lookup"><span data-stu-id="eca1b-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![可预订资源](./media/8BookableResources.png)

3. <span data-ttu-id="eca1b-149">在**常规**选项卡上，选择您的管理员用户。</span><span class="sxs-lookup"><span data-stu-id="eca1b-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="eca1b-150">验证时区是否与您所在的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="eca1b-150">Verify that the time zone matches the one you are in.</span></span> 

![新增可预订资源](./media/9NewBookableResource.png)

4. <span data-ttu-id="eca1b-152">在**计划**选项卡上的**公司**字段中，选择 **USPM** 公司，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![“计划”选项卡](./media/10SchedulingTab.png)

5. <span data-ttu-id="eca1b-154">选择**工作时间**选项卡。</span><span class="sxs-lookup"><span data-stu-id="eca1b-154">Select the **Work hours** tab.</span></span>  

![工作时间](./media/11WorkHours.png)

6. <span data-ttu-id="eca1b-156">双击日历中的任意值，然后选择**编辑** > **系列中的所有事件**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![工作日历](./media/12WorkCalendar.png)

7. <span data-ttu-id="eca1b-158">将工作时间更改为八 (8) 小时工作日，将周末标记为非工作日，确保时区与您的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="eca1b-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="eca1b-159">选择**保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-159">Select **Save and close**.</span></span>

![更新日历](./media/13UpdateCalendar.png)

9. <span data-ttu-id="eca1b-161">转到**设置** > **日历模板**，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![日历模板](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="eca1b-163">输入名称，选择所创建的模板资源，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![保存日历模板](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="eca1b-165">转到**参数**，双击记录。</span><span class="sxs-lookup"><span data-stu-id="eca1b-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![项目参数](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="eca1b-167">更新以下字段：</span><span class="sxs-lookup"><span data-stu-id="eca1b-167">Update the following fields:</span></span>

 - <span data-ttu-id="eca1b-168">**默认公司**：USPM</span><span class="sxs-lookup"><span data-stu-id="eca1b-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="eca1b-169">**默认部门**：Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="eca1b-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="eca1b-170">**发票频率**：第七天和最后一天</span><span class="sxs-lookup"><span data-stu-id="eca1b-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="eca1b-171">**工作时间模板**：更改为您创建的模板。</span><span class="sxs-lookup"><span data-stu-id="eca1b-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="eca1b-172">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="eca1b-172">Select **Save**.</span></span> 

![更新后的项目参数](./media/17UpdatedProjectParameters.png)
