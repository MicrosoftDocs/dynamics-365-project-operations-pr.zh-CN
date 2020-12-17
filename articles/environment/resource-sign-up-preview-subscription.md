---
title: 注册获取面向资源/非库存场景的 Project Operations 的预览订阅
description: 此主题提供有关如何订阅和部署面向资源/非库存场景的 Project Operations。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642938"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>注册获取面向资源/非库存场景的 Project Operations 的预览订阅

_**适用于：** 面向资源/非库存场景的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题说明如何订阅预览/合作伙伴产品/服务以及如何部署面向资源/非库存场景的 Project Operations 环境。

## <a name="prerequisites"></a>先决条件

- 您将收到一封电子邮件，邀请您参加预览。 您可以在 [Project Operations 网站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上申请预览。
- 部署预览的用户必须具有 Azure 租户全局管理员权限。
- 部署 Finance 环境需要按环境计费有效的 Azure 订阅。 您可以使用组织现有订阅或使用 [Azure 试用](https://azure.microsoft.com/en-us/free/)开始。 CDS 环境将在 30 天内免费提供。

## <a name="subscribe"></a>订阅

当您的[预览申请](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)获得批准时，您将通过电子邮件收到 Microsoft 的三项服务。 这些服务让您可以部署 Project Operations 预览：

- Dynamics 365 Project Operations (CRM) - 预览试用
- Office 365 Project Operations - 预览试用
- Dynamics 365 Finance - 预览试用

> [!IMPORTANT]
> 组织中只有一个人（租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - 预览试用 

在开始之前，请确保已使用需要 Project Operations 预览的租户中的用户工作帐户登录到浏览器。

1. 通过将第一个服务代码 **Dynamics 365 Project Operations (CRM) - 预览试用** 粘贴到浏览器 URL 来兑换它。

![兑换服务](./media/16RedeemFirstOfferNew.png)

2. 确认您的订单。

![确认订单](./media/17ConfirmOrderNew.png)

您将看到服务已成功兑换的确认。

![确认](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - 预览试用

重复与第一个服务代码相同的步骤。 确保使用与第一个服务代码使用的相同用户帐户添加第二个服务代码。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 预览试用

对欢迎电子邮件中的最后一个服务重复相同步骤。

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。

1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。

![管理中心主页](./media/14AdminPortal.png)

2. 在 **活动用户** 页上，选择要为其分配许可证的用户。

![分配许可证](./media/15AssignLicenses.png)

3. 验证是否已选择 **Dynamics 365 Project Operations (CRM) 预览** 和 **Office 365 Project Operations - 预览** 许可证，并选择 **保存更改**。

> [!NOTE]
> Finance 试用服务不需要分配给用户。

## <a name="start-a-new-project-in-lcs"></a>在 LCS 中启动新项目

按照主题[在 LCS 中启动新项目](create-lcs-project.md)中所述创建新的 LCS 项目

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>将 Azure 订阅添加到 LCS 项目

若要完成此任务，请按照主题[将 Azure 订阅添加到 LCS 项目](resource-add-azure-subscription-lcs-project.md)中的步骤操作。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>使用面向资源/非库存场景的 Project Operations 部署 Finance 演示环境

按照主题[设置新环境](resource-provision-new-environment.md)中的指导完成部署。 使用[演示环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署类型进行预览。 

## <a name="install-cds-setup-and-configuration-data"></a>安装 CDS 设置和配置数据

按照主题[在 Common Data Service 中设置和应用配置数据](resource-apply-pro-setup-config-data.md)中所述安装 CDS 设置和配置数据。
应仅在部署了 Finance 演示环境以及 FO 中的演示数据准备就绪后再完成此步骤。
