---
title: 资源管理模式概述
description: 此主题介绍 Dynamics 365 Project Operations 中的资源管理功能。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000875"
---
# <a name="resource-management-modes-overview"></a>资源管理模式概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


Dynamics 365 Project Operations 支持两种模式，以便您执行整个预订流。 管理模式定义为项目参数，如果您的业务需求发生变化，可以进行修改。    

## <a name="central-mode"></a>集中模式
对于将资源集中分配到项目的组织，集中模式提供了一种确保项目经理可以在项目级别定义资源要求的方法。 资源要求的完成将委派给资源经理。 项目经理可以接受或拒绝资源经理建议的资源。

![集中模式](./media/resource-management-central.png)

若要使用集中模式管理资源，请参阅：

- [为任务分配通用可预订资源，并生成资源要求](/dynamics365/project-service/assign-generic-bookable-resource)
- [根据资源要求预订指定资源](/dynamics365/project-service/book-named-resource)
- [提交资源请求](/dynamics365/project-service/submit-resource-request)
- [实施资源请求](/dynamics365/project-service/resource-management-fulfill-requests)
- [接受或拒绝资源请求的建议项目资源](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>混合模式
对于需要灵活分配资源的组织，混合模式让项目经理和资源经理都可以预订资源。

![混合模式](./media/resource-management-hybrid.png)

除了受支持的集中模式流程之外，另请参阅以下主题来在混合模式下管理所有其他支持的预订流：

将资源直接预订到项目：
- [为项目团队预订指定的可预订资源和分派任务](/dynamics365/project-service/assign-named-bookable-resource)

从资源要求预订资源：
- [为任务分配通用可预订资源，并生成资源要求](/dynamics365/project-service/assign-generic-bookable-resource)
- [根据资源要求预订指定资源](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]