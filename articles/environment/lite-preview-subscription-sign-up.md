---
title: 注册获取预览订阅
description: 此主题提供有关如何订阅和部署“Project Operations 精简部署 - 估价交易开票”的信息。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072467"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>注册获取“精简部署 – 估价交易开票”的预览订阅

此主题说明如何订阅预览合作伙伴产品/服务以及部署“Dynamics 365 Project Operations 精简部署 - 估价交易开票”。

> [!NOTE]
> 此流程将在即将发布的 Project Operations 中更改。

## <a name="prerequisites"></a>先决条件

- 您将收到一封电子邮件，邀请您参加预览。 您可以在 [Project Operations 网站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上申请预览。
- 部署预览的用户必须具有 Azure 租户全局管理员权限。
- 查看所有条款和条件。

## <a name="subscribe"></a>订阅

当您收到[预览申请](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)批准时，您将通过电子邮件收到 Microsoft 的两项服务。 这些服务让您可以部署 Project Operations 预览：

- Dynamics 365 Project Operations (CRM) - 预览试用
- Office 365 Project Operations - 预览试用

> [!IMPORTANT]
> 组织中只有一个人（租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - 预览试用 

在开始之前，请确保已使用需要 Project Operations 预览的租户中的用户工作帐户登录到浏览器。

1. 通过将服务代码粘贴到浏览器 URL 中来兑换第一个服务代码 **Dynamics 365 Project Operations (CRM) - 预览试用** 。

![兑换服务](./media/16RedeemFirstOfferNew.png)

2. 确认您的订单。
![确认订单](./media/17ConfirmOrderNew.png)

您将看到服务已成功兑换的确认。

![确认](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - 预览试用

重复与第一个服务代码相同的步骤。 确保使用与第一个服务代码使用的相同用户帐户添加第二个服务代码。

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。


1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。

![管理中心主页](./media/14AdminPortal.png)

2. 在 **活动用户** 页上，选择要为其分配许可证的用户。

![分配许可证](./media/15AssignLicenses.png)

3. 确认已选择 **Dynamics 365 Project Operations (CRM) 预览** 和 **Office 365 Project Operations - 预览** 许可证。 
4. 选择 **保存更改** 。

## <a name="create-a-new-cds-environment"></a>创建新 CDS 环境

1. 按照主题 [CDS 部署模型](lite-deployment.md)中的说明设置新的 Project Operations CDS 部署环境。 选择环境类型时，请确保使用 **试用(基于订阅)** 。
![新建环境](./media/19CreateEnvironment.png)

2. 选择 **启用 Dynamics 365 应用** 设置，将 **自动部署这些应用** 留空。  
3. 选择 **保存** 创建环境。

![添加数据库](./media/20CreateEnvironment1.png)

4. 创建环境后，安装 **Microsoft Dynamics 365 Project Operations** 解决方案。 

![安装解决方案](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安装 CDS 配置和设置演示数据

按照主题[应用演示设置和配置数据](lite-apply-demo-setup-config-data.md)中的说明安装 CDS 配置和设置演示数据。
