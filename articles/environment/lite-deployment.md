---
title: 部署 Project Operations - 精简
description: 此主题提供有关如何安装“Project Operations 精简部署 - 估价交易开票”的信息。
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14912c612bbf04e232ce712e52330c7bb43eab9f3f8ffa9223a2d2f9ce95eb72
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991565"
---
# <a name="deploy-project-operations---lite"></a>部署 Project Operations - 精简

_**适用于：** 精简部署 - 估价交易开票_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations 支持多个部署模型。 若要确定最佳部署模型，请参阅[部署类型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署（精简部署 – 估价交易开票）引发 **Common Data Service - 仅 Project Operations 部署**。

- [将 Project Operations 安装到新的 CDS 环境中](#new)
- [安装到现有 CD 环境中](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>将 Project Operations 安装到新的 CDS 环境中

1. 作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)创建一个新的 CDS 环境。 确保 **CDS 数据库** 和 **Dynamics 365 应用** 已启用。 已启用，请参阅[在 Power Platform 管理中心创建和管理环境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
2. 从 Dynamics 365 应用的部署列表中选择 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>将 Project Operations 安装到现有 CDS 环境中

1. 作为具有 Project Operations 许可证的[全局或 Power Platform 管理员](/power-platform/admin/global-service-administrators-can-administer-without-license)，在 [PowerPlatform 管理中心](https://admin.powerplatform.com)中找到要安装 Project Operations 的环境。
2. 安装 Dynamics 365 应用的部署列表中的 **Microsoft Dynamics 365 Project Operations**。 有关详细信息，请参阅[管理 Dynamics 365 应用](/power-platform/admin/manage-apps)。




[!INCLUDE[footer-include](../includes/footer-banner.md)]