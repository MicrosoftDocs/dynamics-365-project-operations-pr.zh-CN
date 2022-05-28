---
title: 2021 年 10 月的新增内容 - 基于资源/非库存场景的 Project Operations
description: 本主题提供有关 2021 年 10 月版 Project Operations 中可用于基于资源/非库存方案的质量更新的信息。
author: sigitac
ms.date: 10/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64ef1e2ba9e33b2ca7575a40cc51e0ae987a9f8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598477"
---
# <a name="whats-new-october-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 10 月的新增内容 - 基于资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

   - Microsoft Dataverse 环境中的 Project Operations 版本 4.25.0.91
   - Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.21

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- [项目采购订单](../procurement/non-stocked-materials-project-purchase-orders.md)现在可用于项目采购部门管理/集中的采购。
- [供应商保留](../procurement/vendor-retention-overview.md)允许您保留一部分应付给供应商的款项。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在版本列中的双重写入页面上查看映射的活动版本。 要激活映射的新版本，请选择表映射版本，选择最新版本，然后保存所选版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2209402 | 更正了在确认项目合同后阻止对保留金额开发票的验证。 |
|   商机管理 | 2227414 | **产品**、**目录外** 和 **IsProductOverriden** 字段会复制到报价单子项明细和合同子项明细中。 |
| 计费和定价 | 2338357 | 选择项目时，材料使用日志上的货币必须默认自项目货币。 |
| 时间和支出 | 2414777 | 当支出或时间条目具有多个相关项目审批时，必须可以取消审批。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [412077](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D412077&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020681298%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JT2OvagELTPqep4rOiFTwGYF80KkgSHgBJmd%2BHBBgA8%3D&amp;reserved=0) | 如果允许采购经理角色访问一个法人，则也会筛选对所有法人中所有项目的访问权限。 |
| 项目管理和会计 | [555604](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D555604&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=NGAT/5r0sezqdisYP%2BDzyFDDi5f9gyrr5ZhJZaDLV0k%3D&amp;reserved=0) | 启用了 **启用项目合同货币以进行估算计算** 功能后，估算消除失败。 |
| 项目管理和会计 | [564701](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564701&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IyhrFb59YBXjNpJdtPhlEDxoYiFCTrqzQtKZsBZk2DM%3D&amp;reserved=0) | [FRA] 将供应商保留和预付款应用于采购订单发票后，未正确计算最后一次付款的条件税。 |
| 项目管理和会计 | [569250](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569250&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020741035%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YcB6z9MvvtiyT9d8g2GkHXDUcNfnPdxlYsHblbk%2BCXs%3D&amp;reserved=0) | WIP 过帐到总帐的过帐金额不正确。 |
| 项目管理和会计 | [581167](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D581167&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020989941%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=9UjX3lX/DOJOPiz%2BlYVge5F3Tpbb%2BUBaN7PVXkpwYJE%3D&amp;reserved=0) | 项目发票报表将跳过某些行。 |
| 项目管理和会计 | [598810](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598810&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021408104%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=f2oJYnmjpfUiIKvF6qfLsBcfTjoSOq955%2B87%2BSIh0Io%3D&amp;reserved=0) | 项目发票过帐批次存在问题，即使尚未生成发票行，它也会处理和过帐发票方案。 |
| 项目管理和会计 | [578970](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D578970&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021876048%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JMg%2BIRbLiSKeIXN/JArWC3hSGFhNhabERbuKzGBKCC8%3D&amp;reserved=0) | 更新创建项目估算批处理作业以支持执行多个子任务。 |
| 项目管理和会计 | [586034](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586034&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021895962%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MRGsdBRM5spFKDJZ/IjrAoWy%2BGTyFVyUU7SCfFJSj6g%3D&amp;reserved=0) | 凭证交易记录不平衡，结果为“XX/XX/XXXX”（会计货币：0.00 - 报告货币：0.01）。 |
| 项目管理和会计 | [596669](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D596669&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021955698%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IpJrV7LW0CegdNrRXfDqBhLEsy8tlSvlaipvZBQFZVg%3D&amp;reserved=0) | 法人的免税编号未显示在打印的项目发票上。 |
| 项目管理和会计 | [598109](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598109&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021975611%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=erjkqXSdKwjU62xNiVEJomzc5JoiiC9U7f6ofrv4KGE%3D&amp;reserved=0) | 应用 KB 4619395 后，不支持在发布估算时设置连续数字序列。 |
| 项目管理和会计 | [602677](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602677&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4TBJC6dKbgZxWQTlyDkTm%2BzHpL%2BJx5ZcueNWkMJfUK4%3D&amp;reserved=0) | 发票过帐中的 WIP 冲销值与时间条目中原始过帐 WIP 值不同。 |
| 项目管理和会计 | [602728](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Ux5tLxoBzA%2BJtbf5MhLB63/GNJqYcBg8PH4tncXLTsM%3D&amp;reserved=0) | 由于已应用保留款案例中项目开票收入过帐有问题，因此未正确平衡凭证交易记录。 |
| 项目管理和会计 | [607324](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D607324&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022065219%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=I/SwbTsPpFvMkxLIK7JpligW%2B4nlObh3nCCSppVGvhE%3D&amp;reserved=0) | 仅针对一个周期创建了项目估算。 |
| 出差和支出 | [551911](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D551911&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=fDFL3GM5jXJAzIzxwRlOIaq3/ytSHXnpIzGsC4Jjphg%3D&amp;reserved=0) | 忽略了旅行申请政策以正确审批工作流。 |
| 出差和支出 | [563752](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D563752&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SVrkNdniaVfhOjc3Brf1gtrFv3SJpPNQ4JYOGnCOxlQ%3D&amp;reserved=0) | 可计费的支出行项目 ID 和活动编号未保存在移动支出应用中。 |
| 出差和支出 | [569458](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569458&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020750990%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=cC33gCOlM8aa3jR5Hy1Hubf5bszsu2YWwraLLrIYCYk%3D&amp;reserved=0) | 即使没有对支出行附加收据，**已附加收据** 字段也被设置为 **是**。 |
| 出差和支出 | [571334](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D571334&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020760950%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Y6dd19CzWyWPa%2BItpWXBEgUuSx8evJxth6VslSRMYsg%3D&amp;reserved=0) | 尝试将支出类别更改为 **个人** 时出现错误消息。 |
| 出差和支出 | [572783](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D572783&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020770904%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=nugD/4Rj3d8CNanZf%2BY3vNm9aRqHoh5vF/bHFZD9UxE%3D&amp;reserved=0) | 在支出报告上拆分信用卡交易后，您无法编辑父项支出或附加收据。 |
| 出差和支出 | [574252](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574252&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020790818%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=uKYIlgBpKju4jBH%2BK8GXVKCgi6kxSG1AxXVvF75WsbA%3D&amp;reserved=0) | 具有项目 ID 的公司间交易的支出政策无法正常工作。 |
| 出差和支出 | [574489](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574489&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=ErBwfDvDtWWzEJP3STHd5kzPjTe7%2B4nCeG02kH64dWU%3D&amp;reserved=0) | 发布的支出报表缺少发布日期。 |
| 出差和支出 | [574504](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574504&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SeW6L68CNpJ86TJ2aNqLZoTMq5PHRfu3542mNkKqf%2Bg%3D&amp;reserved=0) | 支出移动应用中存在付款方式问题。 |
| 出差和支出 | [584799](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D584799&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021129331%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4Q%2B/R9wPra2P/%2BEk63qgSenyNoJMa5OJsBv2Nn9s%2B%2Bo%3D&amp;reserved=0) | 为一名员工创建的出差申请可用于另一名员工的支出报表，并且可在委托日期之前使用出差申请。 |
| 出差和支出 | [586023](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586023&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021169156%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=d9Kmf1ng415Uw0U4aQ5N%2B0RboRmjDW1S2lt91rG9ofc%3D&amp;reserved=0) | 创建支出时，更改财务维度值不会在 **支出管理** 工作区中的会计分配级别正常更新。 |
| 出差和支出 | [586081](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586081&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021179116%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=LlWjcIANIl1gudmiD4WIsluKkF21w9EgVC5uDvBOzg4%3D&amp;reserved=0) | 主要支出行审批状态与明细化行工作流审批状态不同步。 |
| 出差和支出 | [590544](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D590544&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021318495%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MolkGywocB%2BG404npaOv7fcfunnlDUGgAYFOcw8OlKg%3D&amp;reserved=0) | 在“支出管理参数”中启用 **退税** 后，在发布支出报表时出现错误。 |
| 出差和支出 | [564851](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564851&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021856138%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YBsBJdzH%2BqbGzq07u7WILEs%2Bi5Ap6WYzqWnpGWcI4Ac%3D&amp;reserved=0) | 代理无法删除离职员工的支出单据。 |
| 出差和支出 | [587306](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D587306&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021905919%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=TbWDuK1sHY//jTw%2BmehJG3M3N3feEl2oRkTMTkqWOVE%3D&amp;reserved=0) | 删除支出行需要很长时间，会影响性能。 |
| 出差和支出 | [600455](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D600455&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021995524%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MH0sIRbAKhNNyAgYZzO9NovWHM7ZWKsoZYqXCIVHJ5A%3D&amp;reserved=0) | **TrvExpTrans** 因仅删除 **SourceDocumentLine** 而产生了孤立的 **TaxUncommitted** 记录。 |
