---
title: Project Service Automation V3 更新版本 22 中的新增功能或更改
description: 本文列出了 Project Service Automation 更新版 22 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930629"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation V3 更新版本 22

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation V3 更新版 22 的新增和更改的功能和修补程序。 该版本的内部版本号为 V 3.10.33.48，并且在 2020 年 6 月通过自行更新公开发布。

## <a name="update-release-22"></a>更新发布 22

### <a name="bug-fixes"></a>Bug 修复



**时间和支出**

已修复以下问题：

- 导入后，**时间条目** 不会自动添加到“时间条目”时间表中。
- **时间条目** 网格日期选择器无法识别用户的区域设置。

**资源管理**

已修复以下问题：

- 在手动模式下，生成 **资源要求** 时无法识别对 **资源分配** 等值线所做的更改。
- **资源请求** 不支持自定义请求状态。

**项目管理**

已修复以下问题：

- 在 EstimateGridControl 上使用双击不会正确分析荷兰格式的数字。
- 在使用 Microsoft Project 桌面客户端加载项更改分配后，已分派的小时数未正确更新。
- 当合同货币不同于客户货币并且组织被配置为显示货币代码而非货币符号时，“项目跟踪”和“估计”网格会显示不正确的销售货币代码。
- 如果工作时间日程安排为每天 24 小时，则团队成员的完成日期将增加一天。
- 在“项目日程安排”上，将事务类别添加到任务不会触发自动保存。
- 将团队成员添加到项目模板时显示以下错误：“资源要求不能与项目模板相关联”。 
- 功能区规则脚本“msdyn.Approval.CanApproveOrReject”显示超时错误。

**Sales**

已修复以下问题：

- 在“新建报价单项目价目表”窗体/实体上的“价目表”查找中选择“成本价目表”时，未显示验证错误消息。
- 如果附加到报价单的 BPF 处于最后阶段，则以“赢单”形式结束报价单时，不会导航到创建的合同。
- 在撤回时间条目后，用于冲销的 **未记帐销售额** 会链接到原始成本。
- 选择 **确认** 按钮后，除非刷新发票，否则发票状态不会更改为 **已确认**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
