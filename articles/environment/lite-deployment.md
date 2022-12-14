---
title: 部署 Project Operations 精简版
description: 本文提供有关如何安装“Project Operations 精简部署 - 估价交易开票”的信息。
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810967"
---
# <a name="deploy-project-operations-lite"></a>部署 Project Operations 精简版

_**适用于：** 精简部署 - 估价交易开票_



Project Operations 支持多个部署模型。 若要确定最佳部署模型，请参阅[部署类型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署（精简部署 – 估价交易开票）引发 **Dataverse - 仅 Project Operations 部署**。

- [将 Project Operations 安装到新的 Dataverse 环境中](#new)
- [安装到现有 Dataverse 环境中](#existing)
- [安装到具有双重写入组件的现有 Dataverse 环境中](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>将 Project Operations 精简版安装到新的 Dataverse 环境中

1. 作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)创建一个新的 Dataverse 环境。 确保 **为此环境创建数据库** 和 **Dynamics 365 应用** 已启用。 已启用，请参阅[在 Power Platform 管理中心创建和管理环境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
1. 从 Dynamics 365 应用的部署列表中选择 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>将 Project Operations 精简版安装到现有 Dataverse 环境中 
1. 作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)中找到要安装 Project Operations 的环境。
1. 安装 Dynamics 365 应用的部署列表中的 **Microsoft Dynamics 365 Project Operations**。 有关详细信息，请参阅[管理 Dynamics 365 应用](/power-platform/admin/manage-apps)。

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>将 Project Operations 精简版安装到已存在双重写入解决方案的现有 Dataverse 环境中

如果您想继续在精简部署模式下运行 Project Operations，您应该遵循以下步骤：

1. 作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)中找到要安装 Project Operations 的环境。
1. 安装 Dynamics 365 应用的部署列表中的 **Microsoft Dynamics 365 Project Operations**。 有关详细信息，请参阅[管理 Dynamics 365 应用](/power-platform/admin/manage-apps)。
1. 由于您的环境具有双重写入组件，这些组件有助于集成到已安装的财务和运营应用，因此 Project Operations 安装还将安装将项目相关数据集成到财务和运营应用所需的功能和扩展。 由于您希望在精简部署中运行 Project Operations，因此应删除这些集成组件，因为它们会为精简部署方案带来限制和开销。 手动卸载解决方案 **Dynamics 365 Project Operations 双重写入** 和 **Dynamics 365 Project Operations 双重写入实体映射**，以删除这些组件。
1. 转到 **Project Operations -> 设置 -> 参数**。 打开 **项目参数** 详细信息页，将 **解决方案升级行为** 字段设置为 **仅限精简版**。 这可确保 Project Operations 的任何后续升级都不会将集成组件带回到 Project Operations 中。  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
