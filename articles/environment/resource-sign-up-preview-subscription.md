---
title: 注册获取面向资源/非库存场景的 Project Operations 的预览订阅
description: 本文提供有关如何订阅和部署“基于资源/非库存场景的 Project Operations”的信息。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842004"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>注册获取面向资源/非库存场景的 Project Operations 的预览订阅

_**适用于：** 面向资源/非库存场景的 Project Operations_



本文介绍如何订阅试用产品/服务，以及如何部署“基于资源/非库存场景的 Project Operations 环境”。

## <a name="prerequisites"></a>先决条件
- 部署预览的用户必须具有 Azure 租户全局管理员权限。 您可以在第一个产品/服务兑换期间创建租户。 
- 部署 Finance 环境需要按环境计费有效的 Azure 订阅。 您可以使用组织现有订阅或使用 [Azure 试用](https://azure.microsoft.com/free/)开始。 CDS 环境将在 30 天内免费提供。

> [!IMPORTANT]
> 组织中只有一个人（租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。
> 
> 试用在租户中单次使用。 一次只能运行一个试用。 我们建议您创建一个新租户以进行试用。


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - 预览试用 

在开始之前，请确保已使用需要 Project Operations 预览的租户中的用户工作帐户登录到浏览器。

1. 在此处 [Project Operations 试用](https://aka.ms/try-po)兑换第一个产品/服务代码 **Dynamics 365 Project Operations**。
2. 确认您的订单。

  您将看到服务已成功兑换的确认。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 预览版试用

转到 [Dynamics 365 for Finance 预览试用](https://aka.ms/trypoche)，对产品/服务重复上一部分中的步骤，注册云托管环境。  

## <a name="assign-licenses"></a>分配许可证

> [!IMPORTANT]
> 您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。

1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)，将许可证分配给您的用户。

2. 在 **活动用户** 页上，选择要为其分配许可证的用户。

3. 验证已选择 **Dynamics 365 Project Operations** 许可证，然后选择 **保存更改**。

> [!NOTE]
> Finance 试用服务不需要分配给用户。

## <a name="start-a-new-project-in-lcs"></a>在 LCS 中启动新项目

按照文章[在 LCS 中启动新项目](create-lcs-project.md)中所述创建新 LCS 项目

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>将 Azure 订阅添加到 LCS 项目

要完成此任务，请按照文章[将 Azure 订阅添加到 LCS 项目](resource-add-azure-subscription-lcs-project.md)中的步骤操作。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>使用面向资源/非库存场景的 Project Operations 部署 Finance 演示环境

按照文章[预配新环境](resource-provision-new-environment.md)中的指导完成部署。 使用[演示环境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署类型进行预览。 

## <a name="install-cds-setup-and-configuration-data"></a>安装 CDS 设置和配置数据

按照文章[在 Common Data Service 中设置和应用配置数据](resource-apply-pro-setup-config-data.md)中的说明安装 CDS 设置和配置数据。
仅在部署了 Finance 演示环境并准备好演示数据后完成此步骤。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
