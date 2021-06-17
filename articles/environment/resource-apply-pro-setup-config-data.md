---
title: 在 Common Data Service 中设置和应用配置数据
description: 此主题提供有关在 Project Operations 中设置和应用配置数据的信息。
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001280"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="b2d9a-103">在 Common Data Service 中设置和应用配置数据</span><span class="sxs-lookup"><span data-stu-id="b2d9a-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="b2d9a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b2d9a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="b2d9a-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="b2d9a-105">Prerequisites</span></span>

<span data-ttu-id="b2d9a-106">在开始在 Common Data Service (CDS) 中配置数据之前，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="b2d9a-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="b2d9a-107">为Project Operations 预配 CDS 环境和 Dynamics 365 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="b2d9a-108">将 Dynamics 365 Finance 中的法人信息共享到 CDS 环境。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="b2d9a-109">这意味着 CDS 中的 **公司** 实体具有以下公司记录：</span><span class="sxs-lookup"><span data-stu-id="b2d9a-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="b2d9a-110">THPM</span><span class="sxs-lookup"><span data-stu-id="b2d9a-110">THPM</span></span>
  - <span data-ttu-id="b2d9a-111">USPM</span><span class="sxs-lookup"><span data-stu-id="b2d9a-111">USPM</span></span>
  - <span data-ttu-id="b2d9a-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="b2d9a-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="b2d9a-113">安装设置和配置数据</span><span class="sxs-lookup"><span data-stu-id="b2d9a-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="b2d9a-114">下载、取消阻止和解压缩[设置和配置数据包](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="b2d9a-115">导航到解压缩的文件夹，运行可执行文件 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b2d9a-116">在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择 **导入数据**，然后选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![配置迁移](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b2d9a-118">在 CMT 向导的第 2 页上，选择 **Microsoft 365** 作为 **部署类型**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b2d9a-119">选择 **显示可用组织列表** 和 **显示高级** 复选框。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b2d9a-120">选择您的租户的区域，输入您的凭据，选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![配置登录](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b2d9a-122">在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="b2d9a-123">在第 4 页上，从解压缩的文件夹中选择 zip 文件 *SampleSetupAndConfigData*。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip 文件选择](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. <span data-ttu-id="b2d9a-126">选择 zip 文件后，选择 **导入数据**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-126">After the zip file is selected, select **Import Data**.</span></span>

![导入数据](./media/5ImportData.png)

10. <span data-ttu-id="b2d9a-128">导入将运行大约二到十分钟，具体时间取决于您的网络速度。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b2d9a-129">完成导入后，退出 CMT 向导。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b2d9a-130">检查您的组织在以下 26 个实体中的数据：</span><span class="sxs-lookup"><span data-stu-id="b2d9a-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="b2d9a-131">货币</span><span class="sxs-lookup"><span data-stu-id="b2d9a-131">Currency</span></span>
  - <span data-ttu-id="b2d9a-132">会计科目表</span><span class="sxs-lookup"><span data-stu-id="b2d9a-132">Chart of Accounts</span></span>
  - <span data-ttu-id="b2d9a-133">会计日历</span><span class="sxs-lookup"><span data-stu-id="b2d9a-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="b2d9a-134">货币汇率类型</span><span class="sxs-lookup"><span data-stu-id="b2d9a-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="b2d9a-135">付款日</span><span class="sxs-lookup"><span data-stu-id="b2d9a-135">Payment Day</span></span>
  - <span data-ttu-id="b2d9a-136">付款计划</span><span class="sxs-lookup"><span data-stu-id="b2d9a-136">Payment Schedule</span></span>
  - <span data-ttu-id="b2d9a-137">付款条款</span><span class="sxs-lookup"><span data-stu-id="b2d9a-137">Payment Term</span></span>
  - <span data-ttu-id="b2d9a-138">部门</span><span class="sxs-lookup"><span data-stu-id="b2d9a-138">Organizational Unit</span></span>
  - <span data-ttu-id="b2d9a-139">联系人​​</span><span class="sxs-lookup"><span data-stu-id="b2d9a-139">Contact</span></span>
  - <span data-ttu-id="b2d9a-140">税组</span><span class="sxs-lookup"><span data-stu-id="b2d9a-140">Tax Group</span></span>
  - <span data-ttu-id="b2d9a-141">客户组</span><span class="sxs-lookup"><span data-stu-id="b2d9a-141">Customer Group</span></span>
  - <span data-ttu-id="b2d9a-142">供应商组</span><span class="sxs-lookup"><span data-stu-id="b2d9a-142">Vendor Group</span></span>
  - <span data-ttu-id="b2d9a-143">计价单位</span><span class="sxs-lookup"><span data-stu-id="b2d9a-143">Unit</span></span>
  - <span data-ttu-id="b2d9a-144">单位组</span><span class="sxs-lookup"><span data-stu-id="b2d9a-144">Unit Group</span></span>
  - <span data-ttu-id="b2d9a-145">价目表</span><span class="sxs-lookup"><span data-stu-id="b2d9a-145">Price List</span></span>
  - <span data-ttu-id="b2d9a-146">项目参数价目表</span><span class="sxs-lookup"><span data-stu-id="b2d9a-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="b2d9a-147">账单频率</span><span class="sxs-lookup"><span data-stu-id="b2d9a-147">Invoice Frequency</span></span>
  - <span data-ttu-id="b2d9a-148">可预订资源的类别</span><span class="sxs-lookup"><span data-stu-id="b2d9a-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="b2d9a-149">交易类别</span><span class="sxs-lookup"><span data-stu-id="b2d9a-149">Transaction Category</span></span>
  - <span data-ttu-id="b2d9a-150">费用类别</span><span class="sxs-lookup"><span data-stu-id="b2d9a-150">Expense Category</span></span>
  - <span data-ttu-id="b2d9a-151">角色价格</span><span class="sxs-lookup"><span data-stu-id="b2d9a-151">Role Price</span></span>
  - <span data-ttu-id="b2d9a-152">交易类别价格</span><span class="sxs-lookup"><span data-stu-id="b2d9a-152">Transaction Category Price</span></span>
  - <span data-ttu-id="b2d9a-153">特征</span><span class="sxs-lookup"><span data-stu-id="b2d9a-153">Characteristic</span></span>
  - <span data-ttu-id="b2d9a-154">可预订资源</span><span class="sxs-lookup"><span data-stu-id="b2d9a-154">Bookable Resource</span></span>
  - <span data-ttu-id="b2d9a-155">可预订资源的类别关联</span><span class="sxs-lookup"><span data-stu-id="b2d9a-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="b2d9a-156">可预订资源的特征</span><span class="sxs-lookup"><span data-stu-id="b2d9a-156">Bookable Resource Characteristic</span></span>

![完成导入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="b2d9a-158">更新 Project Operations 配置</span><span class="sxs-lookup"><span data-stu-id="b2d9a-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="b2d9a-159">导航到 CE 环境。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-159">Navigate to the CE environment.</span></span> <span data-ttu-id="b2d9a-160">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，选择环境，然后选择 **打开环境** 可以找到它。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![打开环境](./media/7OpenEnvironment.png)

2. <span data-ttu-id="b2d9a-162">转到 **项目** > **资源**，然后选择 **新建** 为您的用户创建可预订资源。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![可预订资源](./media/8BookableResources.png)

3. <span data-ttu-id="b2d9a-164">在 **常规** 选项卡上，选择您的管理员用户。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="b2d9a-165">验证时区是否与您所在的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-165">Verify that the time zone matches the one you are in.</span></span> 

![新增可预订资源](./media/9NewBookableResource.png)

4. <span data-ttu-id="b2d9a-167">在 **计划** 选项卡上的 **公司** 字段中，选择 **USPM** 公司，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![“计划”选项卡](./media/10SchedulingTab.png)

5. <span data-ttu-id="b2d9a-169">选择 **工作时间** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-169">Select the **Work hours** tab.</span></span>  

![工作时间](./media/11WorkHours.png)

6. <span data-ttu-id="b2d9a-171">双击日历中的任意值，然后选择 **编辑** > **系列中的所有事件**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![工作日历](./media/12WorkCalendar.png)

7. <span data-ttu-id="b2d9a-173">将工作时间更改为八 (8) 小时工作日，将周末标记为非工作日，确保时区与您的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="b2d9a-174">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-174">Select **Save and close**.</span></span>

![更新日历](./media/13UpdateCalendar.png)

9. <span data-ttu-id="b2d9a-176">转到 **设置** > **日历模板**，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![日历模板](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="b2d9a-178">输入名称，选择所创建的模板资源，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![保存日历模板](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="b2d9a-180">转到 **参数**，双击记录。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![项目参数](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="b2d9a-182">更新以下字段：</span><span class="sxs-lookup"><span data-stu-id="b2d9a-182">Update the following fields:</span></span>

 - <span data-ttu-id="b2d9a-183">**默认公司**：USPM</span><span class="sxs-lookup"><span data-stu-id="b2d9a-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="b2d9a-184">**默认部门**：Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="b2d9a-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="b2d9a-185">**发票频率**：第七天和最后一天</span><span class="sxs-lookup"><span data-stu-id="b2d9a-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="b2d9a-186">**工作时间模板**：更改为您创建的模板。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="b2d9a-187">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b2d9a-187">Select **Save**.</span></span> 

![更新后的项目参数](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
