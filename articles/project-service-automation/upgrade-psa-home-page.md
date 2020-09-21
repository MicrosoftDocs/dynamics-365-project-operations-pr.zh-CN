---
title: “升级”主页
description: 此主题介绍何处可以找到有关 Dynamics 365 Project Service Automation 中的新功能和更新功能和用于升级到最新版本的流程的重要信息。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749740"
---
# <a name="upgrade-home-page"></a>“升级”主页

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>从 PSA 版本 2.x 或 1.x 升级到版本 3.x

### <a name="new-instances"></a>新实例

从 2019 年 5 月 17 日开始，如果在配置新实例期间选择 Project Service Automation，将默认安装版本 3.x。

### <a name="existing-instances"></a>现有实例

以前，已有 PSA 版本 2.x 实例，但需要更新到版本 3.x（此版本是基于统一客户端接口 (UCI) 的 PSA 版本）的客户必须联系 Microsoft 支持人员，并提供自己实例的详细信息，以便支持人员能够让该实例升级到版本 3.x。 从 2020 年 3 月 1 日开始，已有 PSA 版本 2.x 实例但需要升级到版本 3.x 的客户，将能够直接从管理门户升级其实例，而无需与 Microsoft 支持人员联系。  

> [!NOTE]
> PSA 版本 3.x 中有一些重大更改。 其基于统一接口框架，可帮助提供改进的用户体验。 这款经过重新设计的应用程序提供一致、统一的用户界面 (UI)，该界面采用了响应式设计理念，非常适合在任何屏幕尺寸或设备上查看。 整个应用程序还有其他一些更改。 已更改的一些领域包括定价、预订和分派资源、时间、支出与审批。

建议在开始升级流程之前完成以下任务：

- 验证确定的实例中是否已同时安装了 Dynamics 365 Field Service 和 Project Service Automation。 如果已安装了这两个解决方案，应计划在恢复正常使用此解决方案之前升级这两个解决方案。
- 请仔细阅读以下主题。 注意和了解版本之间的变化有助于完成升级流程。 这些主题介绍 PSA 中的主要更改，以及计划升级到版本 3.x 之前的注意事项和建议。

    - [Project Service Automation 版本 3 中的新增功能或更改](whats-new-changed-v3.md)
    - [升级注意事项 - Project Service Automation 版本 2.x 或 1.x 到版本 3](upgrade-v3.md)

- 升级生产实例之前，升级沙盒实例，以便评估实施中的更改。

阅读前面介绍的主题并准备好升级到 PSA 版本 3.x 或基于 UCI 的版本之后，向 Microsoft 支持提交请求，以便从管理中心获取升级。 在请求中提供实例的详细信息。

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>新建实例中的旧 PSA 版本（PSA 版本 2.x）

从 2019 年 5 月 17 日开始，所有新实例都采用 UCI 作为默认客户端。 为了与此项更改保持一致，将默认设置 PSA 版本 3.x 和 Field Service 版本 8.x，因为这些版本设计为支持 UCI 客户端。

从 2020 年 3 月 1 日开始，Dynamics PSA 的客户将无法再创建具有旧版 PSA（例如 PSA 版本 2.x 或更低版本）的新环境。 任何新环境都将仅获取 PSA 版本 3.x。

> [!NOTE]
> 若要在使用 Field Service 和 PSA 应用程序的旧版本时获得最佳体验，请转到**系统设置**页，为**仅使用新的统一接口(推荐)** 字段选择**否**，因为这些版本未设计为可在 UCI 中正确加载。 关闭 UCI 之后，可使用旧 Web 客户端打开和运行这些 Field Service 和 PSA 版本。 有关如何关闭 UCI 客户端的说明，请参阅[仅启用统一接口](../admin/enable-unified-interface-only.md)。
