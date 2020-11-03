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
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072469"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="68683-103">为 Project Operations 精简部署应用演示设置和配置数据 - 估价交易开票</span><span class="sxs-lookup"><span data-stu-id="68683-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="68683-104">_\*\*精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="68683-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="68683-105">下载[主数据包](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。</span><span class="sxs-lookup"><span data-stu-id="68683-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="68683-106">导航到文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ，运行可执行文件 *DataMigrationUtility* 。</span><span class="sxs-lookup"><span data-stu-id="68683-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="68683-107">在 Common Data Service 配置迁移 (CMT) 向导的第 1 页上，选择 **导入数据** ，然后选择 **继续** 。</span><span class="sxs-lookup"><span data-stu-id="68683-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![配置迁移](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="68683-109">在 CMT 向导的第 2 页上，选择 **Microsoft 365** 作为 **部署类型** 。</span><span class="sxs-lookup"><span data-stu-id="68683-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="68683-110">选择 **显示可用组织列表** 和 **显示高级** 复选框。</span><span class="sxs-lookup"><span data-stu-id="68683-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="68683-111">选择您的租户的区域，输入您的凭据，然后选择 **登录** 。</span><span class="sxs-lookup"><span data-stu-id="68683-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![配置登录](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="68683-113">在第 3 页上，在租户的组织列表中，选择要将演示数据导入的组织，然后选择 **登录** 。</span><span class="sxs-lookup"><span data-stu-id="68683-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="68683-114">在第 4 页上，从解压缩的文件夹 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中选择 zip 文件 *MasterAndSetupData* 。</span><span class="sxs-lookup"><span data-stu-id="68683-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip 文件](./media/3ZipFile.png)

![选择 1 个文件](./media/4SelectAFile.png)

9. <span data-ttu-id="68683-117">选择 zip 文件后，选择 **导入数据** 。</span><span class="sxs-lookup"><span data-stu-id="68683-117">After the zip file is selected, select **Import Data**.</span></span>

![导入数据](./media/5ImportData.png)

10. <span data-ttu-id="68683-119">导入将运行大约二到十分钟，具体时间取决于您的网络速度。</span><span class="sxs-lookup"><span data-stu-id="68683-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="68683-120">完成后，退出 CMT 向导。</span><span class="sxs-lookup"><span data-stu-id="68683-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="68683-121">检查您的组织在以下 20 个实体中的数据：</span><span class="sxs-lookup"><span data-stu-id="68683-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="68683-122">货币</span><span class="sxs-lookup"><span data-stu-id="68683-122">Currency</span></span>
- <span data-ttu-id="68683-123">部门</span><span class="sxs-lookup"><span data-stu-id="68683-123">Organizational Unit</span></span>
- <span data-ttu-id="68683-124">联系人​​</span><span class="sxs-lookup"><span data-stu-id="68683-124">Contact</span></span>
- <span data-ttu-id="68683-125">税组</span><span class="sxs-lookup"><span data-stu-id="68683-125">Tax Group</span></span>
- <span data-ttu-id="68683-126">客户组</span><span class="sxs-lookup"><span data-stu-id="68683-126">Customer Group</span></span>
- <span data-ttu-id="68683-127">计价单位</span><span class="sxs-lookup"><span data-stu-id="68683-127">Unit</span></span>
- <span data-ttu-id="68683-128">计价单位组</span><span class="sxs-lookup"><span data-stu-id="68683-128">Unit Group</span></span>
- <span data-ttu-id="68683-129">价目表</span><span class="sxs-lookup"><span data-stu-id="68683-129">Price List</span></span>
- <span data-ttu-id="68683-130">项目参数价目表</span><span class="sxs-lookup"><span data-stu-id="68683-130">Project Parameter Price List</span></span>
- <span data-ttu-id="68683-131">账单频率</span><span class="sxs-lookup"><span data-stu-id="68683-131">Invoice Frequency</span></span>
- <span data-ttu-id="68683-132">发票频率详细信息</span><span class="sxs-lookup"><span data-stu-id="68683-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="68683-133">可预订资源的类别</span><span class="sxs-lookup"><span data-stu-id="68683-133">Bookable Resource Category</span></span>
- <span data-ttu-id="68683-134">交易类别</span><span class="sxs-lookup"><span data-stu-id="68683-134">Transaction Category</span></span>
- <span data-ttu-id="68683-135">费用类别</span><span class="sxs-lookup"><span data-stu-id="68683-135">Expense Category</span></span>
- <span data-ttu-id="68683-136">角色价格</span><span class="sxs-lookup"><span data-stu-id="68683-136">Role Price</span></span>
- <span data-ttu-id="68683-137">交易类别价格</span><span class="sxs-lookup"><span data-stu-id="68683-137">Transaction Category Price</span></span>
- <span data-ttu-id="68683-138">特征</span><span class="sxs-lookup"><span data-stu-id="68683-138">Characteristic</span></span>
- <span data-ttu-id="68683-139">可预订资源</span><span class="sxs-lookup"><span data-stu-id="68683-139">Bookable Resource</span></span>
- <span data-ttu-id="68683-140">可预订资源的类别关联</span><span class="sxs-lookup"><span data-stu-id="68683-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="68683-141">可预订资源的特征</span><span class="sxs-lookup"><span data-stu-id="68683-141">Bookable Resource Characteristic</span></span>

![完成导入](./media/6CompleteImport.png)
