---
title: 在 Finance 云托管环境中应用演示数据
description: 此主题说明如何将 Project Operations 中的演示数据应用于 Dynamics 365 Finance 云托管环境。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289853"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="d8d8c-103">在 Finance 云托管环境中应用演示数据</span><span class="sxs-lookup"><span data-stu-id="d8d8c-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="d8d8c-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d8d8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8d8c-105">此主题仅适用于 Microsoft Dynamics 365 Finance 版本 10.0.13，并且只能在云托管环境中执行。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="d8d8c-106">在向环境应用高质量更新 **之前**，请先完成本主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="d8d8c-107">在您的 LCS 项目中，打开 **环境详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="d8d8c-108">请注意，此页面包含使用远程桌面协议 (RDP) 连接到环境所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ 环境详细信息](./media/1EnvironmentDetails.png)

<span data-ttu-id="d8d8c-110">第一组突出显示的凭据是本地帐户凭据，包含指向远程桌面连接的超链接。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="d8d8c-111">这些凭据包含环境管理员用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="d8d8c-112">第二组凭据用于登录到此环境中的 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="d8d8c-113">通过 **本地帐户** 中的超链接远程连接到环境，然后使用 **本地帐户凭据** 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="d8d8c-114">转到 **Internet Information Services** > **应用程序池** > **AOSService**，停止服务。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="d8d8c-115">此时停止服务是为了可以继续替换 SQL 数据库。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![停止 AOS](./media/2StopAOS.png)

4. <span data-ttu-id="d8d8c-117">转到 **服务**，停止以下两项：</span><span class="sxs-lookup"><span data-stu-id="d8d8c-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="d8d8c-118">Microsoft Dynamics 365 Unified Operations：批次管理服务</span><span class="sxs-lookup"><span data-stu-id="d8d8c-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="d8d8c-119">Microsoft Dynamics 365 Unified Operations：数据导入导出框架</span><span class="sxs-lookup"><span data-stu-id="d8d8c-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![停止服务](./media/3StopServices.png)

5. <span data-ttu-id="d8d8c-121">打开 Microsoft SQL Server Management Studio。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="d8d8c-122">使用 SQL Server 凭据登录，使用 LCS **环境详细信息** 页上的 axdbadmin 用户和密码。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="d8d8c-124">在对象资源管理器的 **数据库** 中，找到 **AXDB**。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="d8d8c-125">您将数据库替换为位于[下载中心](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)中的新数据库。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="d8d8c-126">将 zip 文件复制到您要远程访问的 VM 并提取 zip 内容。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="d8d8c-127">在 SQL Server Management Studio 中，右键单击 **AxDB**，然后选择 **任务** > **还原** > **数据库**。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![还原数据库](./media/5RestoreDatabase.png)

9. <span data-ttu-id="d8d8c-129">选择 **源设备**，导航到从您复制的 zip 中提取的文件。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![源设备](./media/6SourceDevice.png)

10. <span data-ttu-id="d8d8c-131">选择 **选项**，然后选择 **覆盖现有数据库** 和 **关闭与目标数据库的现有连接**。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="d8d8c-132">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-132">Select **OK**.</span></span>

![恢复设置](./media/7RestoreSetting.png)

<span data-ttu-id="d8d8c-134">您将收到 AXDB 恢复已成功的确认消息。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="d8d8c-135">在收到此确认后，可以关闭 SQL Services Management Studio。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="d8d8c-136">返回 **Internet Information Services** > **应用程序池** > **AOSService**，启动 AOSService。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="d8d8c-137">转到 **服务**，启动先前停止的两个服务。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="d8d8c-138">在此 VM 上找到 AdminUserProvisioning 工具。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="d8d8c-139">在 K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 下查找。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="d8d8c-140">使用 **电子邮件地址** 字段中的用户地址运行 .ext 文件。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="d8d8c-141">选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-141">Select **Submit**.</span></span>

![管理员用户设置](./media/8AdminUserProvisioning.png)

<span data-ttu-id="d8d8c-143">这需要几分钟完成。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="d8d8c-144">您会收到一条确认消息，指示管理员用户已成功更新。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="d8d8c-145">最后，以管理员身份运行命令提示符并执行 iisreset</span><span class="sxs-lookup"><span data-stu-id="d8d8c-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS 重置](./media/9IISReset.png)

18. <span data-ttu-id="d8d8c-147">关闭远程桌面会话，然后使用 LCS **环境详细信息** 页登录到环境，确认它是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="d8d8c-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]