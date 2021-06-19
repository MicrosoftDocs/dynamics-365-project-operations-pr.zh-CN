---
title: Project Operations 更新
description: 本主题提供有关 Dynamics 365 Project Operations 的发行版本的信息。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d19148c868aa5be77db59e70fcf1fb8b7de6868c
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213434"
---
# <a name="project-operations-updates"></a>Project Operations 更新

_**适用范围：** 面向资源/非库存场景的 Project Operations，精简部署 - 估价交易开票，以及面向库存/生产订单场景的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations 组件

Dynamics 365 Project Operations 包括两个组件：

- Dataverse 环境中的 Project Operations 包含从商机到估价开票的各项功能。 Dataverse 用于 Project Operations 的精简部署和资源/非库存场景部署。
- Dynamics 365 Finance 环境中的项目管理和会计包含支出管理功能、项目会计和收入确认。 Finance and Operations 应用环境用于面向资源/非库存场景的 Project Operations 和面向库存/生产订单场景的 Project Operations。

## <a name="project-operations-release-notes"></a>Project Operations 发行说明
- [资源/非库存](whats-new-may-2021-resource-based.md)场景的 Project Operations 最新发行说明。
- [精简部署](../pro/whats-new/whats-new-may-2021-lite.md)场景的 Project Operations 最新发行说明。
- [库存/生产订单](../prod-pma/whats-new/whats-new-apr-2021-stocked.md)场景的 Project Operations 最新发行说明。

## <a name="project-operations-latest-version"></a>Project Operations 最新版本

| Dataverse 环境中的 Project Operations | Finance and Operations 应用环境中的项目管理和会计 | 
| --- | --- |
| 4.10.0.186 | 10.0.18 |

对于 Project Operations 资源/非库存方案，建议使用双重写入业务流程版本 2.2.2.60 或更高版本。

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Dataverse 环境中的 Project Operations 的发行计划

Dataverse 环境中的 Project Operations 更新每月推出。 

| 站 | 区域 | 当前版本号 | 精简部署的自动更新 | 资源/非库存部署的自动更新 | 下一个版本号 | 下一个版本公开发布 |
|-----------|-----------------------|-----------------|--------------|---------------------|---------------------|---------------------|
| 第 1 站 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 第一版         |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
| 第 2 站 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 南美         |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
|    &nbsp; | 加拿大                |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 印度                 |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 法国                |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 阿拉伯联合酋长国  |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 南非          |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 5 月 28 日           |
| 第 3 站 |      &nbsp;           |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 日本                 |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 亚太          |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 英国         |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 大洋洲               |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 6 月 4 日          |
| 第 4 站 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 欧洲                |  4.10.0.186     | 完成     | 完成            | TBD                 | 2021 年 6 月 11 日          |
| 第 5 站 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 北美         |  4.10.0.186     | 完成     | 2021 年 6 月 11 日          | TBD                 | 2021 年 6 月 18 日          |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Finance and Operations 应用环境中的项目管理和会计的发行计划

项目管理和会计的更新每年发布八次。

|          支持版本          | 预览版可用性 (PEAP) | 公开发布（自动更新） | 自动更新计划（通过 LCS 更新设置）生产开始日期 |   服务结束   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.18          |        2021 年 3 月 5 日        |           2021 年 4 月 16 日          |                            2021 年 4 月 30 日                            |    2021 年 7 月 16 日   |
|          10.0.17          |       2021 年 2 月 1 日      |           2021 年 3 月 19 日          |                             2021 年 4 月 2 日                            |    2021 年 6 月 11 日   |

目标发布日期可能会发生更改。 有关详细信息，请参阅[服务更新可用性](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json)。

|          目标版本          | 预览版可用性 (PEAP) | 公开发布（自动更新） | 自动更新计划（通过 LCS 更新设置）生产开始日期 |   服务结束   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.19          |        2021 年 4 月 23 日       |            2021 年 6 月 18 日           |                             2021 年 7 月 2 日                             | 2021 年 9 月 17 日 |
|          10.0.20          |         2021 年 5 月 28 日        |           2021 年 7 月 16 日           |                             2021 年 7 月 30 日                             |  2021 年 10 月 22 日  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
