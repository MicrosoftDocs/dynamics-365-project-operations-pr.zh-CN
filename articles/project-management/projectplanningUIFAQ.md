---
title: 在“任务”网格中工作故障排除
description: 本主题提供在“任务”网格中工作时所需的故障排除信息。
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547188"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>在“任务”网格中工作故障排除 


_**适用于**：基于资源/非库存场景的 Project Operations、精简部署 - 估价交易开单、Project for the Web_

Dynamics 365 Project Operations 利用的“任务”网格是 Microsoft Dataverse 内的托管 iframe。 由于使用了这一项，因此必须满足特定要求，才能确保身份验证和授权能够正常运行。 本主题概述的常见问题可能会影响用于呈现网格或在工作分解结构 (WBS) 中管理任务的功能。

常见问题包括：

- “任务”网格上的 **任务** 选项卡为空。
- 打开项目时，项目不会加载，且用户界面 (UI) 停滞在旋转图标上。
- **Project for the Web** 的特权管理。
- 创建、更新或删除任务时不会保存更改。

## <a name="issue-the-task-tab-is-empty"></a>问题：“任务”选项卡为空

### <a name="mitigation-1-enable-cookies"></a>缓解 1：启用 Cookie

Project Operations 需要启用第三方 Cookie 来呈现工作分解结构。 如果未启用第三方 Cookie，在选择 **项目** 页上的 **任务** 选项卡时，您会看到空白页面，而不是看到任务。

对于 Microsoft Edge 或 Google Chrome 浏览器，以下过程概述了如何更新浏览器设置以启用第三方 Cookie。

#### <a name="microsoft-edge"></a>Microsoft Edge

1. 打开 Edge 浏览器。
2. 在右上角选择 **省略号** (...)，然后选择 **设置**。
3. 在 **Cookie 和站点权限** 下，选择 **Cookie 和站点数据**。
4. 关闭 **阻止第三方 Cookie**。
5. 刷新浏览器。 

#### <a name="google-chrome"></a>Google Chrome

1. 打开 Chrome 浏览器。
2. 在右上角，选择三个垂直排列的点，然后选择 **设置**。
3. 在 **隐私和安全性** 下，选择 **Cookie 和其他站点数据**。
4. 选择 **允许所有 Cookie**。
5. 刷新浏览器。 

> [!NOTE]
> 如果您阻止第三方 Cookie，将阻止其他站点的所有 Cookie 和站点数据，即使您的例外列表中允许该站点。

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>缓解 2：验证是否正确配置了 PEX 终结点

Project Operations 需要项目参数引用 PEX 终结点。 需要使用此终结点才能与用于呈现工作分解结构的服务通信。 如果未启用此参数，您将收到错误“项目参数无效”。 若要更新 PEX 终结点，请完成以下步骤。

1. 将 **PEX 终结点** 字段添加到 **项目参数** 页中。
2. 识别您正在使用的产品类型。 设置 PEX 终结点时使用此值。 检索后，已在 PEX 终结点中定义了产品类型。 保留该值。
3. 使用以下值更新此字段：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`。 下表提供了应该根据产品类型使用的类型参数。

      | **产品类型**                     | **类型参数** |
      |--------------------------------------|--------------------|
      | 默认组织中的 Project for the Web   | 类型=0             |
      | 名为 CDS 的组织中的 Project for the Web | 类型=1             |
      | Project Operations                   | 类型=2             |

4. 从 **项目参数** 页删除此字段。

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>问题：项目未加载且 UI 停滞在旋转图标上

为了执行身份验证，必须启用弹出窗口以便加载“任务”网格。 如果未启用弹出窗口，则加载旋转图标时屏幕将会停滞。 下图显示了地址栏中具有阻止的弹出窗口标签的 URL，这会导致在尝试加载页面时旋转图标停滞。 

   ![旋转图标停滞并且阻止了弹出窗口。](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>缓解 1：启用弹出窗口

当项目停滞在旋转图标上时，可能未启用弹出窗口。

#### <a name="microsoft-edge"></a>Microsoft Edge

在 Edge 浏览器中启用弹出窗口的方法有两种。

1. 在 Edge 浏览器中，选择浏览器右上角的通知。
2. 选择 **始终允许出现弹出窗口并从特定 Dataverse 环境重定向**。
 
     ![弹出窗口阻止了窗口。](media/enablepopups.png)

或者，您可以完成以下步骤。

1. 打开 Edge 浏览器。
2. 在右上角，选择 **省略号** (...)，然后选择 **设置** > **站点权限** > **弹出窗口和重定向**。
3. 关闭 **弹出窗口和重定向** 可以阻止弹出窗口，打开可以允许设备上出现弹出窗口。
4. 启用弹出窗口后，刷新您的浏览器。 

#### <a name="google-chrome"></a>Google Chrome
1. 打开 Chrome 浏览器。
2. 导航到阻止弹出窗口的页面。
3. 在地址栏中，选择 **已阻止弹出窗口**。
4. 选择您所看到的弹出窗口的链接。
5. 启用弹出窗口后，刷新您的浏览器。 

> [!NOTE]
> 若要始终查看站点的弹出窗口，请选择 **始终允许出现弹出窗口并从 [站点] 进行重定向**，然后选择 **完成**。

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>问题 3：Project for the Web 的特权管理

Project Operations 依赖于外部计划服务。 该服务要求为用户分配多个角色，以允许用户读取和写入与 WBS 相关的实体。 这些实体包括项目任务、资源分配和任务依赖关系。 如果用户在导航到 **任务** 选项卡时无法呈现 WBS，这可能是因为尚未对 **Project Operations** 启用 **项目**。 用户可能会收到安全角色错误或与拒绝访问相关的错误。

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>缓解 1：验证应用程序用户和最终用户安全角色

1. 转到 **设置** > **安全** > **用户** > **应用程序用户**。  

   ![应用程序读取器。](media/applicationuser.jpg)
   
2. 双击应用程序用户记录以验证：

     - 用户有权访问项目。 可以通过验证用户是否具有 **项目经理** 安全角色来执行此操作。
     - Microsoft Project 应用程序用户已存在并且配置正确。
 
3. 如果该用户不存在，请创建新用户记录。 
4. 选择 **新建用户**，将条目窗体更改为 **应用程序用户**，然后添加 **应用程序 ID**。

   ![应用程序用户详细信息。](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>问题 4：创建、更新或删除任务时不会保存更改

在对 WBS 进行一项或多项更新时，更改将失败并且不会保存。 在计划网格中发生了一个错误，消息指出“您最近所做的更改无法保存”。

### <a name="mitigation-1-validate-the-license-assignment"></a>缓解 1：验证许可证分配

1. 在许可证的服务计划详细信息中验证是否已为用户分配了正确的许可证，并且已启用了服务。  
2. 验证用户是否可以打开 **project.microsoft.com**。
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>缓解 2：验证项目应用程序用户的配置
1. 验证是否已创建项目应用程序用户。
2. 向用户应用以下安全角色：
  
  - Dataverse 用户或基本用户
  - Project Operations 系统
  - 项目系统
  - Project Operations 双重写入系统。 基于资源/非库存场景的 Project Operations 部署方案需要此角色。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
