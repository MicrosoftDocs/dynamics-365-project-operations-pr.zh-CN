---
title: 注册获取面向资源/非库存场景的 Project Operations 的预览订阅
description: 此主题提供有关如何订阅和部署面向资源/非库存场景的 Project Operations。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948772"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>注册获取面向资源/非库存场景的 Project Operations 的预览订阅

_**适用于：** 面向资源/非库存场景的 Project Operations_

此主题说明如何订阅预览/合作伙伴产品/服务以及如何部署面向资源/非库存场景的 Project Operations 环境。

## <a name="prerequisites"></a>先决条件

- 您将收到一封电子邮件，邀请您参加预览。 您可以在 [Project Operations 网站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上申请预览。
- 部署预览的用户必须具有 Azure 租户全局管理员权限。
- 部署 Finance 环境需要按环境计费有效的 Azure 订阅。 您可以使用组织现有订阅或使用 [Azure 试用](https://azure.microsoft.com/en-us/free/)开始。 CDS 环境将在 30 天内免费提供。

## <a name="subscribe"></a>订阅

当您的[预览申请](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)获得批准时，您将通过电子邮件收到 Microsoft 的两项服务。 这些服务让您可以部署 Project Operations 预览：

- Dynamics 365 Project Operations – 预览试用
- Dynamics 365 for Finance and Operations 预览试用。

> [!IMPORTANT]
> 组织中只有一个人（租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – 预览试用

1. 使用欢迎电子邮件中提供的 URL 兑换第一个服务 **Dynamics 365 Project Operations 试用**。

![第一个服务](./media/1FirstOffer.png)

2. 验证您是否以属于要订阅服务的组织的用户身份登录。
3. 继续兑换服务。 
4. 选择**是，添加到我的帐户**。

![兑换服务](./media/2RedeemFirstOffer.png)

![确认服务](./media/3ConfirmFirstOffer.png)

![服务已兑换](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 预览试用

对欢迎电子邮件中的第二个服务重复相同步骤。

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Office 365 门户的管理访问权限才能完成以下步骤。

1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。

![Office 管理门户](./media/5OfficeAdminPortal.png)

2. 在**活动用户**页上，选择要为其分配许可证的用户。

![分配许可证](./media/6AssignLicenses.png)

3. 确认已选择 Project Operations 许可证，然后选择**保存更改**。 

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

