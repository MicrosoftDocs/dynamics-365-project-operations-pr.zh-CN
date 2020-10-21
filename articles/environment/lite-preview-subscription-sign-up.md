---
title: 注册获取预览订阅
description: 此主题提供有关如何订阅和部署“Project Operations 精简部署 - 估价交易开票”的信息。
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948769"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>注册获取“精简部署 – 估价交易开票”的预览订阅

此主题说明如何订阅预览合作伙伴产品/服务以及部署“Dynamics 365 Project Operations 精简部署 - 估价交易开票”。

> [!NOTE]
> 此流程将在即将发布的 Project Operations 中更改。

## <a name="prerequisites"></a>先决条件

- 您将收到一封电子邮件，邀请您参加预览。 您可以在 [Project Operations 网站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上申请预览。
- 部署预览的用户必须具有 Azure 租户全局管理员权限。
- 部署预览的用户将需要一个电话号码和一个有效的信用卡。 注册过程中，卡在六个月内不会扣费。 六个月后，您需要取消订阅。 
- 查看所有条款和条件。

## <a name="subscribe"></a>订阅

当您收到[预览申请](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)批准时，您将通过电子邮件收到 Microsoft 的两项服务。 这些服务让您可以部署 Project Operations 预览：

- Dynamics 365 Customer Service 预览试用 – 一次性使用代码
- Dynamics 365 Project Operations – 预览试用

### <a name="dynamics-365-customer-service-paid-offer"></a>Dynamics 365 Customer Service 付费服务

1. 使用 InPrivate/Incognito 浏览器窗口，兑换 Dynamics 365 Customer Service 的第一个服务代码。 若要注册 Customer Service，您需要：

- 电话号码
- 信用卡。 注册时，卡在六个月内不会扣费。 六个月后，您需要取消订阅。
- 查看所有条款和条件。

2. 提供联系信息。

![联系信息](./media/1ContactInformation.png)

3. 提供新租户的详细信息。

![创建用户 ID](./media/2CreateUserID.png)

4. 验证您的身份，保存您的新用户 ID，然后选择**设置**。

![保存信息](./media/3SaveInfo.png)

5. 完成信用卡注册并查看所有条款和条件。 

![完成信用卡注册](./media/4CompleteCreditCard.png)

![信用卡结账](./media/5CreditCardCheckout.png)

![保存订单](./media/6SaveOrder.png)

![信用卡确认](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>取消 Dynamics 365 Customer Service 企业服务

Dynamics 365 Customer Service 企业服务免费提供六个月。 此服务将在六个月结束时以全价续订。 若要在续订日期之前取消，请完成以下操作。 

> [!NOTE]
> 完成这些步骤后，您不能再使用 Project Operations 公开预览环境。

1. 转到[管理门户](https://admin.microsoft.com/)，在**记帐**下选择**您的产品**。

![管理门户中“您的产品”页面](./media/8AdminPortal.png)

2. 选择 **Dynamics 365 Customer Service 企业服务**。

![取消订阅](./media/9CancelSubscription.png)

3. 选择**设置** > **操作** > **取消订阅**。
4. 在**订阅取消**窗体上，在必填字段中输入信息。
5. 选择**取消** > **订阅**。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – 预览试用

1. 使用欢迎电子邮件中提供的 URL 兑换第二个服务 Dynamics 365 Project Operations 试用。

![兑换服务 2](./media/10RedeemOffer2.png)

2. 验证您是否以使用第一个服务代码订阅的同一组织的用户身份登录，然后继续兑换服务。 
3. 选择**是，添加到我的帐户**。

![添加到帐户](./media/11AddToAccount.png)

![立即试用屏幕](./media/12TryNow.png)

![订单详细信息](./media/13Confirmation.png)

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Office 365 门户的管理访问权限才能完成以下步骤。

1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。

![管理中心主页](./media/14AdminPortal.png)

2. 在**活动用户**页上，选择要为其分配许可证的用户。

![分配许可证](./media/15AssignLicenses.png)

3. 确认已选择 **Customer Service Enterprise** 和 **Project Operations** 许可证，然后选择**保存更改**。

## <a name="create-a-new-cds-environment"></a>创建新 CDS 环境

按照主题 [CDS 部署模型](lite-deployment.md)中的说明设置新的 Project Operations CDS 部署环境。

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安装 CDS 配置和设置演示数据

按照主题[应用演示设置和配置数据](lite-apply-demo-setup-config-data.md)中的说明安装 CDS 配置和设置演示数据。
