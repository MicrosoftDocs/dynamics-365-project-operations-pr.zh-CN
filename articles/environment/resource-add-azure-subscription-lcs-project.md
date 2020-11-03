---
title: 将 Azure 订阅添加到 LCS 项目
description: 此主题提供有关如何将您的 Azure 订阅连接到 LCS 项目的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072475"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>将 Azure 订阅添加到 LCS 项目

_**适用于：** 面向资源/非库存场景的 Project Operations_

必须使用现有 Azure 订阅部署云托管环境。 此主题说明如何将现有的 Azure 订阅连接到 LCS 项目。 

## <a name="grant-admin-consent"></a>授权管理员同意

1. 在 LCS 项目的 **环境** 部分，选择 **Microsoft Azure 设置** 。

![Microsoft Azure 设置](./media/1MicrosoftAzureSettings.png)

2. 在 **项目设置** 页上的 **Azure 连接器** 选项卡上，选择 **授权** 。 这样即可以将环境部署到此项目。

![Azure 连接器](./media/2AzureConnectors.png)

3. 再次选择 **授权** 提供管理员同意。

![授权管理员同意](./media/3GrantAdminConsent.png)

4. 接受权限请求。

![接受权限请求](./media/4AcceptPermissionRequest.png)

授权现已完成。 

![授权成功](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>提供对您的 Azure 订阅的 Dynamics 部署服务访问权限

1. 转到 [Microsoft Azure 记帐](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)，选择您的订阅。 Dynamics 部署服务需要访问此订阅才能够部署环境。

![Azure 订阅详细信息](./media/6AzureSubscription.png)

2. 在导航窗格中选择 **访问控制 (IAM)** ，然后选择 **添加角色分配** 。
3. 在右侧的滑块中，选择 **参与者角色** ，在提供的列表中找到并选择 **Dynamics 部署服务** 。 
4. 选择 **保存** 。

![订阅访问](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>将订阅连接器添加到 LCS 项目

1. 在 LCS 项目的 **Microsoft Azure 设置** 页上，选择 **添加** 添加新连接器。
2. 输入 Azure 订阅 ID。 您可以在 [Azure 门户](https://ms.portal.azure.com/)中，在屏幕左下方的 **设置** 下找到您的 Azure 订阅 ID。
3. 在 **配置以使用 Azure 资源管理器** 字段中，选择 **是** 。
4. 确保 Azure 的订阅 AAD 租户域与您所使用的域属 Azure 订阅匹配，然后选择 **下一步** 。
5. 在 **Microsoft Azure 设置** 屏幕上，选择 **下一步** 进行确认。 如果在此屏幕上收到错误，请返回本主题中的[提供对 Azure 订阅的 Dynamics 部署服务访问权限](#provide)一节，确保您已完成所有步骤。
6. 将 Azure 管理证书下载到计算机上的本地文件夹，然后转到 **设置** > **管理证书** ，将其上载到 Azure 管理门户。 此证书可以让 LCS 代表您与 Azure 通信。 如果您的用户具有对订阅的访问权限，可以跳过此步骤。
7. 选择 **下一步** 。
8. 选择要进行部署的 Azure 区域，然后选择一个靠近计划要使用此系统的位置的数据中心。
9.  选择 **连接** 。

您已成功连接 Azure 订阅。 现在，您可以部署 Dynamics 365 Finance 云托管环境了。


