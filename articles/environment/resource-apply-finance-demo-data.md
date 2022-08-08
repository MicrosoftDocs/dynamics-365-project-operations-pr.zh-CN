---
title: 在 Finance 云托管环境中应用演示数据
description: 本文说明如何将演示数据从 Project Operations 应用到 Dynamics 365 Finance 云托管环境。
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 793b1a01f3bf692bb9f4c2d9abad9a44b110544a
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029886"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>在 Finance 云托管环境中应用演示数据

_**适用于：** 面向资源/非库存场景的 Project Operations_

> [!IMPORTANT]
> 本文仅适用于 Microsoft Dynamics 365 Finance 版本 10.0.13，并且只能在云托管环境中执行。 请在将质量更新应用到环境 **之前** 完成本文中的步骤。

1. 在您的 LCS 项目中，打开 **环境详细信息** 页。 请注意，此页面包含使用远程桌面协议 (RDP) 连接到环境所需的详细信息。

![环境详细信息。](./media/1EnvironmentDetails.png)

第一组突出显示的凭据是本地帐户凭据，包含指向远程桌面连接的超链接。 这些凭据包含环境管理员用户名和密码。 第二组凭据用于登录到此环境中的 SQL Server。

2. 通过 **本地帐户** 中的超链接远程连接到环境，然后使用 **本地帐户凭据** 进行身份验证。
3. 转到 **Internet Information Services** > **应用程序池** > **AOSService**，停止服务。 此时停止服务是为了可以继续替换 SQL 数据库。

![停止 AOS。](./media/2StopAOS.png)

4. 转到 **服务**，停止以下两项：

- Microsoft Dynamics 365 Unified Operations：批次管理服务
- Microsoft Dynamics 365 Unified Operations：数据导入导出框架

![停止服务。](./media/3StopServices.png)

5. 打开 Microsoft SQL Server Management Studio。 使用 SQL Server 凭据登录，使用 LCS **环境详细信息** 页上的 axdbadmin 用户和密码。

![SQL Server Management Studio。](./media/4SSMS.png)

6. 在对象资源管理器的 **数据库** 中，找到 **AXDB**。 您将数据库替换为位于[下载中心](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)中的新数据库。 
7. 将 zip 文件复制到您要远程访问的 VM 并提取 zip 内容。
8. 在 SQL Server Management Studio 中，右键单击 **AxDB**，然后选择 **任务** > **还原** > **数据库**。

![还原数据库。](./media/5RestoreDatabase.png)

9. 选择 **源设备**，导航到从您复制的 zip 中提取的文件。

![源设备。](./media/6SourceDevice.png)

10. 选择 **选项**，然后选择 **覆盖现有数据库** 和 **关闭与目标数据库的现有连接**。 
11. 选择 **确定**。

![恢复设置。](./media/7RestoreSetting.png)

您将收到 AXDB 恢复已成功的确认消息。 在收到此确认后，可以关闭 SQL Services Management Studio。

12. 返回 **Internet Information Services** > **应用程序池** > **AOSService**，启动 AOSService。
13. 转到 **服务**，启动先前停止的两个服务。

14. 在此 VM 上找到 AdminUserProvisioning 工具。 在 K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 下查找。
15. 使用 **电子邮件地址** 字段中的用户地址运行 .ext 文件。 
16. 选择 **提交**。

![管理员用户设置。](./media/8AdminUserProvisioning.png)

这需要几分钟完成。 您会收到一条确认消息，指示管理员用户已成功更新。

17. 最后，以管理员身份运行命令提示符并执行 iisreset

![IIS 重置。](./media/9IISReset.png)

18. 关闭远程桌面会话，然后使用 LCS **环境详细信息** 页登录到环境，确认它是否按预期工作。

![财务和运营。](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]