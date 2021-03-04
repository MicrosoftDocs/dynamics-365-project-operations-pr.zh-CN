---
title: 2020 年 11 月新增功能 - Project Operations 精简部署 - 估价交易开票
description: 此主题提供有关 2020 年 11 月版本的 Project Operations 精简部署 - 估价交易开票中推出的质量更新的信息。
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa95406a27e6d32d2be75303904547b59f24c8b2
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367165"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>2020 年 11 月新增功能 - Project Operations 精简部署 - 估价交易开票

_**适用于：** 精简部署 - 估价交易开票_

下表列出了 CDS 环境版本 4.4.0.70 上的 Project Operations 的更新。

| 功能区域                 | 参考编号 | 质量更新                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   商机管理       | 2036993          | 当报价单明细类型为 **所有任务** 时，估算明细和资源分配合同子项将在报价单赢单时更新。                                                 |
|   商机管理       | 2071514          | 无法在启用了基于任务的计费的合同上为固定价格里程碑创建发票。                                                                          |
| 计费和定价          | 2070392          | 发票上的项目合同子项会在每次选择 **刷新发票交易** 时增加。                                                                       |
| 项目规划             | 2043336          | 无法删除项目团队成员记录。                                                                                                                                    |
| 项目规划             | 2046013          | 加载期间和更改时间分段类型时，估算标记列的行为不一致。                                                                                   |
| 项目规划             | 2046647          | 从项目团队成员生成资源要求时，开始时间和结束时间减少一小时。                                                                      |
| 项目规划             | 2053879          | （根据即将到来的 CDS 部署），当出现错误“为 ConditionOperator.In 传递的值为空”时，PublishUnassignedAssignments 会中断保存任务的尝试。 |
| 项目规划             | 2055501          | 将 **项目开始日期** 保留为空会导致计划失败。                                                                                                      |
| 项目规划             | 2066817          | 无法使用 **任务** 选项卡上的人员选取器创建通用资源。                                                                                               |
| 项目规划             | 2067034          | **查看详细信息** 按钮在 **任务详细信息** 页上不可用。                                                                                                         |
| 资源管理          | 2046667          | 通用团队成员不会被删除，即使所有资源都已结束工作。                                                                                                     |
| 时间和快速支出条目 | 2047499          | 时间条目页上的 **新建** 按钮打开的是 **新建电子邮件签名** 页。                                                                                               |
| 时间和快速支出条目 | 2059859          | 创建支出条目时，会打开不是预期的弹出窗口。                                                                                                                         |
| 其他                        | 2044181          | [PO 卸载] - 当您尝试卸载 **msdyn_ProjectServiceCore_Patch** 和 msdyn Project service 核心解决方案时发生错误“记录不可用”。        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]