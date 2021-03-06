---
title: 部署类型
description: 此主题提供的信息可帮助您确定您公司的 Project operations 的正确部署类型。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948768"
---
# <a name="deployment-types"></a>部署类型

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

> [!IMPORTANT]
> 购买许可证后，请从此处开始，使用[引导式安装流](https://aka.ms/provisionprojectoperations)确定 Dynamics 365 Project Operations 的最佳部署模型。
> 完成引导式安装流后，您将被定向到正确的管理门户来完成安装。 请参阅下面的部署详细信息完成安装。


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>使用 Dynamics 365 Project Service Automation 的现有 Dynamics 客户
Project Operations 包含 Project Service Automation 随附的功能。 将来将为这些客户发布升级路径。

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>使用“项目管理和会计”的现有 Dynamics 365 Finance 客户 

使用“项目管理和会计”功能的现有 Finance 客户可以继续像以前一样使用此功能。 请参阅[面向库存/生产订单场景的 Project Operations](#pma)。

Project Operations 支持多个部署选项以满足您的要求。 无论您是 Dynamics 365 的新客户还是现有客户，Project Operations 都可以满足您的需求。

我们的[部署调查表](https://aka.ms/provisionprojectoperations)将帮助您确定正确的部署。 结果将指导您执行以下一种部署类型：

- [精简部署 - 估价交易开票](#lite)
- [面向资源/非库存场景的 Project Operations](#integrated)
- [面向库存/生产订单场景的 Project Operations](#pma)

Project Operations 通过法人级别的配置在同一环境中支持库存/生产订单场景和非库存/资源场景。 例如，Contoso 可以在其美国制造工厂（法人 = Contoso Manufacturing United States）中利用库存/生产订单功能，在其英国的 Contoso Robotics Arms 维修厂利用非库存/资源功能（法人 = Contoso Robotics United Kingdom）。

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>精简部署 - 估价交易开票
精简部署包括以下功能：

- 使用 Web 版本的 Microsoft Project 进行项目规划
- 多维定价
- 统一资源管理
- 时间跟踪
- 基本支出
- 发票方案

### <a name="deployment-steps"></a>部署步骤：
使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。

对于此部署，请参阅[注册获取预览订阅](lite-preview-subscription-sign-up.md)和[设置新环境](lite-deployment.md)。 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>面向资源/非库存场景的 Project Operations
面向资源/非库存场景的 Project Operations 包括以下功能：
  
- 使用 Web 版本的 Microsoft Project 进行项目规划
- 多维定价
- 统一资源管理
- 时间跟踪
- 基本支出
- 全部支出
- 收据 OCR
- 完整开票
- 收入确认

### <a name="deployment-steps"></a>部署步骤：
使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。

对于此部署，请参阅[注册获取预览订阅](resource-sign-up-preview-subscription.md)和[设置新环境](resource-provision-new-environment.md)。 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>面向库存/生产订单场景的 Project Operations

- 使用 WBS 进行项目计划
- 资源管理
- 时间跟踪
- 全部支出
- 收据 OCR
- 完整开票
- 收入确认
- 生产订单
- 材料支持

### <a name="deployment-steps"></a>部署步骤：
使用[部署调查表](https://aka.ms/provisionprojectoperations)确定 Project Operations 的最佳部署模型。

对于此部署，请参阅[注册获取预览订阅](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[设置新环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。 



