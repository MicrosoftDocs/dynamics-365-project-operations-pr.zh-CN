---
title: Project Service Automation V3 更新版本 24 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 24 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 63bf96bfeed30ceefab072640172a6a0dafd20f5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581549"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation V3 更新版本 24

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 24 中新增或更改的功能和修复。 该版本的内部版本号为 V 3.10.42.43，并且在 2020 年 10 月通过自行更新公开发布。

## <a name="update-release-24"></a>更新发布 24

### <a name="bug-fixes"></a>Bug 修复

**Sales**

已修复以下问题：

- 设置默认产品价目表时出现问题。
- 由于嵌入的价目表和角色价格记录副本，报价单赢单的性能很慢。
- **项目合同/销售中心** > **产品明细项目/订单行数量** 将自动舍入到最接近的整数。
- 在读取价目表时提升为系统特权。
- 将客户地址字段 **address1_freighttermscode** 和 **address1_shippingmethodcode** 复制到报价单/订单。 


**时间和支出**

已修复以下问题：

- **时间条目网格** 不支持 **仅限日期** 时间行为。
- **时间条目** 不能自动刷新。 需要手动刷新。
- 资源的工作中有工间休息时间（0 小时）时，无法从工作导入时间条目。
- 创建时间条目时，将开始日期设置为与 **msdyn_date** 相同的值。
- 为时间条目重新启用批量编辑。

**资源管理**

已修复以下问题：

- 尝试在无要求的情况下更新日间预订状态会引发 null 引用异常。
- 加载 **协调视图** 时出错。


**项目管理**

已修复以下问题：

- 在 **项目计划** 中，从 **手动** 更改为 **自动** 时，无法完成自动保存。
- 不应针对 **项目跟踪网格** 上的差异计算支出成本。
- 加载期间 **估算标记** 列的行为与更改 **时间分段** 类型的行为不一致。
- 项目中的实际成本无法反映 **实际值** 中的总计。
- **摘要** 选项卡上的 **估计完成日期** 与 **WBS 计划** 不匹配。
- 升级中的 **更新实际时数** 不能正常工作。
- 根 **BU** 之外的项目经理无法创建项目。
- 对 **支出估算** 中的任务或类别的更改不会保留。
- **合同副本** 复制发票计划和运行状态。
- **刷新实际值** 按钮无法正确计算摘要任务。
- Microsoft Project 加载项：如果有任何团队成员具有空资源单位，则修复 null 引用错误。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
