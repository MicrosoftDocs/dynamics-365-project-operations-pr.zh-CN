---
title: 注册 Project Operations 试用版
description: 此主题介绍如何部署 Dynamics 365 Project Operations 试用版。
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418446"
---
# <a name="sign-up-for-project-operations-trials"></a>注册 Project Operations 试用版 

_**适用范围：** 面向资源/非库存场景的 Project Operations，精简部署 - 估价交易开票，面向库存/生产订单场景的 Project Operations_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题介绍如何订阅预览版合作伙伴套餐和部署 Dynamics 365 Project Operations 环境。

借助新 Project Operations 试用版，可通过完成用于推荐最佳部署方法的问卷，自动部署支持的三种部署方案中的任何一种。 本主题提供有关以下方法的信息：

- 部署试用版套餐。
- 开始预配。
- 配置双重写入。
- 详细了解 Project Operations。 

下表概述新试用版套餐的详细信息。

| **套餐项**               | **详细信息**                                  |
|------------------------------|----------------------------------------------|
| 套餐类型                   | 套餐类型为管理员引导，因此需要租户管理员才能兑换。 |
| 套餐用法                    | 每个租户一次                          |
| 套餐持续时间               | 30 个日历日                             |
| 每个租户的兑换数量       | 7                                            |
| 用户数              | 25                                           |
| 分机                    | 1 次延期，30 个日历日               |
| 试用版环境数量 | 3                                            |


## <a name="admin-trial-details"></a>管理员试用版详细信息
下表列出了试用版详细信息及其如何应用于各种部署类型。

| **项**                      | **精简版**                                     | **非库存材料** | **库存材料** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| 提供的安装程序数据           | 是                                          | 是                       | 是 (USSI)            |
| 事务性数据            | No                                           | No                        | No                    |
| 以分钟为单位的预配时间  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>先决条件
需要满足下列先决条件，才能部署 Dynamics 365 Project Operations 试用版。

- 注册 [Dynamics 365 Project Operations - 预览试用](https://www.aka.ms/try-po).
- 部署预览的用户必须具有 Azure 租户全局管理员权限。

> [!IMPORTANT]
> 组织中只有一人（即租户管理员）需要执行此任务。 如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - 预览试用 

首先，在浏览器中使用用户工作帐户登录需要 Project Operations 预览版的租户。

1. 通过将第一个服务代码 **Dynamics 365 Project Operations - 预览试用** 粘贴到浏览器 URL 来兑换它。

    ![兑换服务](./media/16RedeemFirstOfferNew.png)

2. 确认您的订单。

    ![确认订单](./media/17ConfirmOrderNew.png)

  您将看到套餐已成功兑换的确认。

   ![确认](./media/18OrderConfirmationNew.png)

  将把您重定向到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/projectoperationstrial)。

## <a name="questionnaire-and-provisioning"></a>问卷和预配

1.  转到 [Power Platform 管理中心](https://admin.powerplatform.com/projectoperationstrial)，然后完成问卷。  
2.  查看推荐的部署类型，然后选择 **开始设置** 以启动预配。
3.  查看条款和条件，然后选择 **开始**。

   预配开始后，将把您重定向到 Power Platform 管理中心中的环境列表。 进行预配时，您的环境的状态为 **正在准备实例**。
 
  预配完成后，您的环境的状态为 **就绪**。
 
4.  预配完成后，选择相应的 Microsoft Dataverse URL，以及用于验证部署的 Finance and Operations 应用 URL。

## <a name="demo-data-installation"></a>安装演示数据

请使用以下链接访问非库存材料和精简部署场景的演示数据包。 
- [非库存材料演示数据](resource-apply-pro-setup-config-data.md)
- [精简版演示数据](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>配置双重写入
仅限非库存材料部署：配置双重写入映射。 有关详细信息，请参阅 [Project Operations 双重写入映射版本](resource-dual-write-maps.md)。

## <a name="assign-licenses"></a>分配许可证

您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。

1. 转到 [Microsoft 365 管理中心](https://portal.office.com/)将许可证分配给用户。

   ![管理中心主页](./media/14AdminPortal.png)

2. 在 **活动用户** 页上，选择要为其分配许可证的用户。

   ![分配许可证](./media/15AssignLicenses.png)

3. 验证已选择 **Dynamics 365 Project Operations 预览版** 许可证，然后选择 **保存更改**。

## <a name="additional-resources"></a>其他资源

以下资源提供在您开始使用 Project Operations 时的有用指导。

- [视频系列 -Project Operations 概述、功能深入研究和路线图](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [确定部署类型](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>如果 Finance and Operations 应用环境需要 ALM 或 ELM，该如何操作？

- 对于需要完整环境生命周期管理功能的合作伙伴，请参阅[合作伙伴沙盒许可证请求](https://experience.dynamics.com/requestlicense)以查看新的合作伙伴套餐。 
- 对于需要有关内部使用权详细信息的合作伙伴，请参阅[内部使用权云和软件福利 (microsoft.com](https://partner.microsoft.com/membership/internal-use-software)。

### <a name="can-i-extend-my-trial-beyond-30-days"></a>是否可将试用期延长到超过 30 天？
若要延长试用期，请完成以下步骤。

1. 在 **Microsoft 365 管理中心** 中，转到 **记帐** > **您的产品**。
2. 选择 **Dynamics 365 Project Operations (CE) - 预览试用**。
3. 在 **到期日期** 下，选择 **延长日期**。

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>是否可以从精简部署升级到基于资源/非库存的场景部署？
现在不支持将环境从精简版升级到基于非库存的部署。

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>是否可以访问我的 Finance 环境的 Lifecycle Services (LCS)？  
号码 对于这些试用版，部署通过 Power Platform 管理中心处理。 对 Finance 环境的访问受限。

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>是否可以在现有环境中安装我的试用版？
如果您已有环境，将允许您从 Power Platform 管理中心在现有 sales Dataverse 环境中安装精简部署。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
