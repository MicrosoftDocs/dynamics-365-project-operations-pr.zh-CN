---
title: 在 Common Data Service 中设置和应用配置数据
description: 此主题提供有关在 Project Operations 中设置和应用配置数据的信息。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642217"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="03280-103">在 Common Data Service 中设置和应用配置数据</span><span class="sxs-lookup"><span data-stu-id="03280-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="03280-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="03280-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="03280-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="03280-105">Prerequisites</span></span>

<span data-ttu-id="03280-106">在开始在 Common Data Service (CDS) 中配置数据之前，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="03280-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="03280-107">为Project Operations 预配 CDS 环境和 Dynamics 365 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="03280-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="03280-108">将 Dynamics 365 Finance 中的法人信息共享到 CDS 环境。</span><span class="sxs-lookup"><span data-stu-id="03280-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="03280-109">这意味着 CDS 中的 **公司** 实体具有以下公司记录：</span><span class="sxs-lookup"><span data-stu-id="03280-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="03280-110">THPM</span><span class="sxs-lookup"><span data-stu-id="03280-110">THPM</span></span>
  - <span data-ttu-id="03280-111">USPM</span><span class="sxs-lookup"><span data-stu-id="03280-111">USPM</span></span>
  - <span data-ttu-id="03280-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="03280-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="03280-113">安装设置和配置数据</span><span class="sxs-lookup"><span data-stu-id="03280-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="03280-114">下载、取消阻止和解压缩[设置和配置数据包](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。</span><span class="sxs-lookup"><span data-stu-id="03280-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="03280-115">导航到解压缩的文件夹，运行可执行文件 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="03280-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="03280-116">在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择 **导入数据**，然后选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="03280-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![配置迁移](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="03280-118">在 CMT 向导的第 2 页上，选择 **Microsoft 365** 作为 **部署类型**。</span><span class="sxs-lookup"><span data-stu-id="03280-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="03280-119">选择 **显示可用组织列表** 和 **显示高级** 复选框。</span><span class="sxs-lookup"><span data-stu-id="03280-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="03280-120">选择您的租户的区域，输入您的凭据，选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="03280-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![配置登录](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="03280-122">在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="03280-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="03280-123">在第 4 页上，从解压缩的文件夹中选择 zip 文件 *SampleSetupAndConfigData*。</span><span class="sxs-lookup"><span data-stu-id="03280-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip 文件选择](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. <span data-ttu-id="03280-126">选择 zip 文件后，选择 **导入数据**。</span><span class="sxs-lookup"><span data-stu-id="03280-126">After the zip file is selected, select **Import Data**.</span></span>

![导入数据](./media/5ImportData.png)

10. <span data-ttu-id="03280-128">导入将运行大约二到十分钟，具体时间取决于您的网络速度。</span><span class="sxs-lookup"><span data-stu-id="03280-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="03280-129">完成导入后，退出 CMT 向导。</span><span class="sxs-lookup"><span data-stu-id="03280-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="03280-130">检查您的组织在以下 19 个实体中的数据：</span><span class="sxs-lookup"><span data-stu-id="03280-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="03280-131">货币</span><span class="sxs-lookup"><span data-stu-id="03280-131">Currency</span></span>
  - <span data-ttu-id="03280-132">部门</span><span class="sxs-lookup"><span data-stu-id="03280-132">Organizational Unit</span></span>
  - <span data-ttu-id="03280-133">联系人​​</span><span class="sxs-lookup"><span data-stu-id="03280-133">Contact</span></span>
  - <span data-ttu-id="03280-134">税组</span><span class="sxs-lookup"><span data-stu-id="03280-134">Tax Group</span></span>
  - <span data-ttu-id="03280-135">客户组</span><span class="sxs-lookup"><span data-stu-id="03280-135">Customer Group</span></span>
  - <span data-ttu-id="03280-136">计价单位</span><span class="sxs-lookup"><span data-stu-id="03280-136">Unit</span></span>
  - <span data-ttu-id="03280-137">计价单位组</span><span class="sxs-lookup"><span data-stu-id="03280-137">Unit Group</span></span>
  - <span data-ttu-id="03280-138">价目表</span><span class="sxs-lookup"><span data-stu-id="03280-138">Price List</span></span>
  - <span data-ttu-id="03280-139">项目参数价目表</span><span class="sxs-lookup"><span data-stu-id="03280-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="03280-140">账单频率</span><span class="sxs-lookup"><span data-stu-id="03280-140">Invoice Frequency</span></span>
  - <span data-ttu-id="03280-141">可预订资源的类别</span><span class="sxs-lookup"><span data-stu-id="03280-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="03280-142">交易类别</span><span class="sxs-lookup"><span data-stu-id="03280-142">Transaction Category</span></span>
  - <span data-ttu-id="03280-143">费用类别</span><span class="sxs-lookup"><span data-stu-id="03280-143">Expense Category</span></span>
  - <span data-ttu-id="03280-144">角色价格</span><span class="sxs-lookup"><span data-stu-id="03280-144">Role Price</span></span>
  - <span data-ttu-id="03280-145">交易类别价格</span><span class="sxs-lookup"><span data-stu-id="03280-145">Transaction Category Price</span></span>
  - <span data-ttu-id="03280-146">特征</span><span class="sxs-lookup"><span data-stu-id="03280-146">Characteristic</span></span>
  - <span data-ttu-id="03280-147">可预订资源</span><span class="sxs-lookup"><span data-stu-id="03280-147">Bookable Resource</span></span>
  - <span data-ttu-id="03280-148">可预订资源的类别关联</span><span class="sxs-lookup"><span data-stu-id="03280-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="03280-149">可预订资源的特征</span><span class="sxs-lookup"><span data-stu-id="03280-149">Bookable Resource Characteristic</span></span>

![完成导入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="03280-151">更新 Project Operations 配置</span><span class="sxs-lookup"><span data-stu-id="03280-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="03280-152">导航到 CE 环境。</span><span class="sxs-lookup"><span data-stu-id="03280-152">Navigate to the CE environment.</span></span> <span data-ttu-id="03280-153">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，选择环境，然后选择 **打开环境** 可以找到它。</span><span class="sxs-lookup"><span data-stu-id="03280-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![打开环境](./media/7OpenEnvironment.png)

2. <span data-ttu-id="03280-155">转到 **项目** > **资源**，然后选择 **新建** 为您的用户创建可预订资源。</span><span class="sxs-lookup"><span data-stu-id="03280-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![可预订资源](./media/8BookableResources.png)

3. <span data-ttu-id="03280-157">在 **常规** 选项卡上，选择您的管理员用户。</span><span class="sxs-lookup"><span data-stu-id="03280-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="03280-158">验证时区是否与您所在的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="03280-158">Verify that the time zone matches the one you are in.</span></span> 

![新增可预订资源](./media/9NewBookableResource.png)

4. <span data-ttu-id="03280-160">在 **计划** 选项卡上的 **公司** 字段中，选择 **USPM** 公司，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="03280-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![“计划”选项卡](./media/10SchedulingTab.png)

5. <span data-ttu-id="03280-162">选择 **工作时间** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="03280-162">Select the **Work hours** tab.</span></span>  

![工作时间](./media/11WorkHours.png)

6. <span data-ttu-id="03280-164">双击日历中的任意值，然后选择 **编辑** > **系列中的所有事件**。</span><span class="sxs-lookup"><span data-stu-id="03280-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![工作日历](./media/12WorkCalendar.png)

7. <span data-ttu-id="03280-166">将工作时间更改为八 (8) 小时工作日，将周末标记为非工作日，确保时区与您的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="03280-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="03280-167">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="03280-167">Select **Save and close**.</span></span>

![更新日历](./media/13UpdateCalendar.png)

9. <span data-ttu-id="03280-169">转到 **设置** > **日历模板**，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="03280-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![日历模板](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="03280-171">输入名称，选择所创建的模板资源，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="03280-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![保存日历模板](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="03280-173">转到 **参数**，双击记录。</span><span class="sxs-lookup"><span data-stu-id="03280-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![项目参数](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="03280-175">更新以下字段：</span><span class="sxs-lookup"><span data-stu-id="03280-175">Update the following fields:</span></span>

 - <span data-ttu-id="03280-176">**默认公司**：USPM</span><span class="sxs-lookup"><span data-stu-id="03280-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="03280-177">**默认部门**：Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="03280-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="03280-178">**发票频率**：第七天和最后一天</span><span class="sxs-lookup"><span data-stu-id="03280-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="03280-179">**工作时间模板**：更改为您创建的模板。</span><span class="sxs-lookup"><span data-stu-id="03280-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="03280-180">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="03280-180">Select **Save**.</span></span> 

![更新后的项目参数](./media/17UpdatedProjectParameters.png)
