---
title: 通过双重写入支持手动部署 Project Operations Dataverse 应用
description: 本主题说明了如何手动部署 Project Operations Dataverse 应用，以便它支持双重写入。
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986435"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>通过双重写入支持手动部署 Project Operations Dataverse 应用

_**适用于：** 面向资源/非库存场景的 Project Operations_

本主题说明了如何在 Microsoft Dataverse 中手动部署 Microsoft Dynamics 365 Project Operations，以便它支持双重写入。 Project Operations 可检测环境的配置，并在满足先决条件时添加对双重写入的额外支持。

在通过 Microsoft Dynamics Lifecycle Services (LCS) 进行部署期间，如果您已按照本主题中的说明操作，可以跳过 Microsoft Power Platform 集成（以前称为 Common Data Service 环境）的部署。

在 Dataverse 中部署 Project Operations 以使其支持双重写入的流程具有四个主要步骤：

1. [在 Dataverse 中创建支持双重写入的新环境](#create)。
2. [将双重写入先决条件添加到环境](#prerequisites)。
3. [添加 Project Operations Dataverse 应用](#dataverse)。
4. [链接您的环境](#link)。

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>在 Dataverse 中创建支持双重写入的新环境

若要完成此过程，您必须以管理员身份登录。

1. 打开 [Power Platform 管理中心](https://admin.powerplatform.com)，然后以管理员身份登录。
2. 创建新环境并对其进行命名。
3. 选择环境类型。 如果您已注册试用产品/服务，请选择 **试用（基于订阅）**。
4. 确认部署区域。
5. 启用 **为此环境创建数据库** 选项。 
6. 确认语言，然后确认货币与您的 Finance and Operations 应用的货币匹配。
7. 启用 **Dynamics 365 应用** 选项，并确认 **自动部署这些应用** 字段设置为 **无**。
8. 如果需要安全组，请添加安全组。
9. 选择 **保存** 创建环境。
10. 等待，直到部署完成，并且环境到达 **准备就绪** 状态。

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>将双重写入先决条件添加到环境

双重写入支持包括添加到关键实体（例如 **公司** 实体）的其他字段。 如果您要向现有环境添加双重写入支持，可能必须更新数据才能启用该支持。 有关如何启动数据的信息，请参阅[启动公司数据](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)。 有关双重写入的详细信息，请参阅[双重写入系统要求](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)。

完成此过程以将双重写入先决条件添加到您的环境。

1. 打开您刚才创建的环境，然后转到 **资源** \> **Dynamics 365 应用**。
2. 在应用列表中选择 **双重写入核心解决方案**，然后安装它。
3. 等待，直到安装完成。 然后，在应用列表中选择 **双重写入应用程序业务流程解决方案**，然后安装它。

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>添加 Project Operations Dataverse 应用

仅在安装 Project Operations 之前完成了前面的过程，才能完成此过程。 在安装期间，系统会分析环境配置，并添加对双重写入的支持（如果需要）。

1. 打开您之前创建的环境，然后转到 **资源** \> **Dynamics 365 应用**。
2. 在应用列表中选择 **Microsoft Dynamics 365 Project Operations**，然后安装它。

## <a name="link-your-environments"></a><a name="link"></a>链接您的环境

在部署 Dataverse 环境后，您可以在 Finance and Operations 应用中设置链接。 按照[使用双重写入向导链接您的环境](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)中的步骤操作。
