---
title: 应用演示设置和配置数据 - 精简
description: 此主题提供有关如何为 Project Operations 应用演示设置和配置数据的信息。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401252"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="e40ff-103">为 Project Operations 应用演示设置和配置数据 - 精简</span><span class="sxs-lookup"><span data-stu-id="e40ff-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="e40ff-104">_\*\*精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="e40ff-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e40ff-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="e40ff-105">Prerequisites</span></span>

<span data-ttu-id="e40ff-106">在开始配置之前，必须为 Dynamics 365 Project Operations 预配 Common Data Service (CDS) 环境。</span><span class="sxs-lookup"><span data-stu-id="e40ff-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="e40ff-107">指令</span><span class="sxs-lookup"><span data-stu-id="e40ff-107">Instructions</span></span>

1. <span data-ttu-id="e40ff-108">下载[主数据包](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。</span><span class="sxs-lookup"><span data-stu-id="e40ff-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="e40ff-109">导航到文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*，运行可执行文件 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="e40ff-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e40ff-110">在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择 **导入数据**，然后选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="e40ff-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![配置迁移](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e40ff-112">在 CMT 向导的第 2 页上，选择 **Microsoft 365** 作为 **部署类型**。</span><span class="sxs-lookup"><span data-stu-id="e40ff-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e40ff-113">选择 **显示可用组织列表** 和 **显示高级** 复选框。</span><span class="sxs-lookup"><span data-stu-id="e40ff-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e40ff-114">选择您的租户的区域，输入您的凭据，然后选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="e40ff-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![配置登录](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e40ff-116">在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择 **登录**。</span><span class="sxs-lookup"><span data-stu-id="e40ff-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="e40ff-117">在第 4 页上，从解压缩的文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中选择 zip 文件 *MasterAndSetupData*。</span><span class="sxs-lookup"><span data-stu-id="e40ff-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip 文件](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. <span data-ttu-id="e40ff-120">选择 zip 文件后，选择 **导入数据**。</span><span class="sxs-lookup"><span data-stu-id="e40ff-120">After the zip file is selected, select **Import Data**.</span></span>

![导入数据](./media/5ImportData.png)

10. <span data-ttu-id="e40ff-122">导入将运行大约二到十分钟，具体时间取决于您的网络速度。</span><span class="sxs-lookup"><span data-stu-id="e40ff-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e40ff-123">完成后，退出 CMT 向导。</span><span class="sxs-lookup"><span data-stu-id="e40ff-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e40ff-124">检查您的组织在以下 20 个实体中的数据：</span><span class="sxs-lookup"><span data-stu-id="e40ff-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="e40ff-125">货币</span><span class="sxs-lookup"><span data-stu-id="e40ff-125">Currency</span></span>
-   <span data-ttu-id="e40ff-126">帐户​​</span><span class="sxs-lookup"><span data-stu-id="e40ff-126">Account</span></span>
-   <span data-ttu-id="e40ff-127">部门</span><span class="sxs-lookup"><span data-stu-id="e40ff-127">Organizational Unit</span></span>
-   <span data-ttu-id="e40ff-128">联系人​​</span><span class="sxs-lookup"><span data-stu-id="e40ff-128">Contact</span></span>
-   <span data-ttu-id="e40ff-129">税组</span><span class="sxs-lookup"><span data-stu-id="e40ff-129">Tax Group</span></span>
-   <span data-ttu-id="e40ff-130">客户组</span><span class="sxs-lookup"><span data-stu-id="e40ff-130">Customer Group</span></span>
-   <span data-ttu-id="e40ff-131">计价单位</span><span class="sxs-lookup"><span data-stu-id="e40ff-131">Unit</span></span>
-   <span data-ttu-id="e40ff-132">计价单位组</span><span class="sxs-lookup"><span data-stu-id="e40ff-132">Unit Group</span></span>
-   <span data-ttu-id="e40ff-133">价目表</span><span class="sxs-lookup"><span data-stu-id="e40ff-133">Price List</span></span>
-   <span data-ttu-id="e40ff-134">项目参数价目表</span><span class="sxs-lookup"><span data-stu-id="e40ff-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="e40ff-135">账单频率</span><span class="sxs-lookup"><span data-stu-id="e40ff-135">Invoice Frequency</span></span>
-   <span data-ttu-id="e40ff-136">可预订资源的类别</span><span class="sxs-lookup"><span data-stu-id="e40ff-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="e40ff-137">交易类别</span><span class="sxs-lookup"><span data-stu-id="e40ff-137">Transaction Category</span></span>
-   <span data-ttu-id="e40ff-138">费用类别</span><span class="sxs-lookup"><span data-stu-id="e40ff-138">Expense Category</span></span>
-   <span data-ttu-id="e40ff-139">角色价格</span><span class="sxs-lookup"><span data-stu-id="e40ff-139">Role Price</span></span>
-   <span data-ttu-id="e40ff-140">交易类别价格</span><span class="sxs-lookup"><span data-stu-id="e40ff-140">Transaction Category Price</span></span>
-   <span data-ttu-id="e40ff-141">特征</span><span class="sxs-lookup"><span data-stu-id="e40ff-141">Characteristic</span></span>
-   <span data-ttu-id="e40ff-142">可预订资源</span><span class="sxs-lookup"><span data-stu-id="e40ff-142">Bookable Resource</span></span>
-   <span data-ttu-id="e40ff-143">可预订资源的类别关联</span><span class="sxs-lookup"><span data-stu-id="e40ff-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="e40ff-144">可预订资源的特征</span><span class="sxs-lookup"><span data-stu-id="e40ff-144">Bookable Resource Characteristic</span></span>

![完成导入](./media/6CompleteImport.png)
