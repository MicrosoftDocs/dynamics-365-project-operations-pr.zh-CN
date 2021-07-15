---
title: 注册获取预览订阅 - 精简
description: 此主题提供有关如何订阅和部署“Project Operations 精简部署 - 估价交易开票”的信息。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334771"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>注册获取预览订阅 - 精简 

本主题说明了如何订阅试用产品/服务和部署 Dynamics 365 Project Operations 精简部署 - 估价开票交易。

> [!NOTE]
> 此流程将在即将发布的 Project Operations 中更改。

## <a name="prerequisites"></a>先决条件
- 部署预览的用户必须具有 Azure 租户全局管理员权限。 您可以在第一个产品/服务兑换期间创建租户。

> [!IMPORTANT]
> 组织中只有一个人（租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。
> 
> 试用在租户中单次使用。 一次只能运行一个试用。 我们建议您创建一个新租户以进行试用。

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations 试用 

在开始之前，请确保已使用需要 Project Operations 预览的租户中的用户工作帐户登录到浏览器。

1. 转到 [Project Operations 试用](https://aka.ms/try-po)以兑换第一个产品/服务代码 **Dynamics 365 Project Operations**。
2. 确认您的订单。

  您将看到产品/服务已成功兑换的确认。

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。


1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。
2. 在 **活动用户** 页上，选择要为其分配许可证的用户。
3. 验证是否选择 **Dynamics 365 Project Operations** 许可证。 
4. 选择 **保存更改**。

## <a name="create-a-new-dataverse-environment"></a>创建新的 Dataverse 环境

1. 按照主题 [Dataverse 部署模型](lite-deployment.md)中的说明预配新的 Project Operations Dataverse 部署环境。 选择环境类型时，请确保使用 **试用(基于订阅)**。

  ![新环境](./media/19CreateEnvironment.png)

2. 选择 **启用 Dynamics 365 应用** 设置，将 **自动部署这些应用** 留空。  
3. 选择 **保存** 创建环境。

  ![添加数据库](./media/20CreateEnvironment1.png)

4. 创建该环境后，安装 **Microsoft Dynamics 365 Project Operations** 解决方案。 

![安装解决方案](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安装 CDS 配置和设置演示数据

按照主题[应用演示设置和配置数据](lite-apply-demo-setup-config-data.md)中的说明安装 CDS 配置和设置演示数据。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
