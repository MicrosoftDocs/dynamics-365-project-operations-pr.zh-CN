---
title: 项目进度和成本消耗
description: 此主题介绍如何跟踪项目进度和成本消耗。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 56b78aa70f23a9a723f008973678bb29c4bbce1d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575247"
---
# <a name="project-progress-and-cost-consumption"></a>项目进度和成本消耗

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

对跟踪进度与计划的需要视行业而定。 某些行业以粒度级别跟踪，而其他行业则以较高级别跟踪。 此主题介绍如何进行计划以满足组织的要求。

## <a name="effort-tracking-view"></a>工作量跟踪视图

**工作量跟踪** 视图跟踪计划中的任务的进度。 该视图比较任务实际所用工时与任务的计划工时。 Project Service Automation 使用以下公式计算跟踪度量：

最初在任务创建时：计划成本将设置为完工估算成本。 在任务中记录了“实际值”之后，将在“工作量”的“跟踪”视图上进行以下计算

- 进度百分比 = 迄今实际已用工作量 ÷ 完工估算 (EAC) 
- 待完成估算 (ETC) = 完工估算 (EAC) – 迄今实际已用工作量 
- EAC = 剩余工作量 + 迄今实际已用工作量 
- 预估工作量偏差 = 计划工作量 – EAC

Project Service Automation 显示任务的工作量偏差预估。 如果 EAC 比计划工作量大，则预估任务需要的时间比最初计划的多。 因此，进度比计划落后。 如果 EAC 比计划工作量小，则预估任务需要的时间比最初计划的少。 因此，进度比计划提前。

## <a name="reprojecting-effort"></a>重新预估工作量

项目经理经常修订任务的原始估算。 项目重新预估是项目经理基于项目当前状态对估算的感知。 但是，建议项目经理不要更改基准数字，因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。

项目经理可通过两种方法重新预估任务的工作量：

- 将默认 ETC 替换为任务的实际剩余工作量新估算。 
- 将默认进度百分比替换为项目真实进度新估算。

这些方法都会导致重新计算任务的 ETC、EAC、进度百分比，以及任务的预估工作量偏差。 还会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。

## <a name="reprojection-of-effort-on-summary-tasks"></a>重新预估汇总任务的工作量

可以重新预估汇总任务或容器任务的工作量。 无论用户是使用汇总任务的剩余工作量还是进度百分比来重新预估，都会开始进行下面的这组计算：

- 计算任务的 EAC、ETC 和进度百分比。
- 按任务原始 EAC 的相同比例将新 EAC 分配给子任务。
- 计算向下到叶节点任务的每一个任务的新 EAC。 
- 基于 EAC 值重新计算向下到叶节点的受影响子任务的 ETC 和进度百分比。 这会导致重新估算任务工作量偏差。 
- 重新计算绘制任务直到根节点的 EAC。

### <a name="cost-tracking-view"></a>成本跟踪视图 

**成本跟踪** 视图比较任务的已用实际成本与计划成本。 

> [!NOTE]
> 此视图仅显示人员成本，不包括支出估算的成本。 

Project Service Automation 使用以下公式计算跟踪度量：

在创建任务时，计划成本等于完工估算成本。 在任务中记录了“实际值”之后，将在成本的 **跟踪** 视图上计算以下值：

 - 消耗成本百分比 = 迄今实际已用成本 ÷ 任务的完工估算成本
 - 待完成成本 (CTC) = 完工估算成本 – 迄今实际已用成本
 - 完工估算成本 = CTC + 迄今实际已用成本
 - 预估成本偏差 = 计划成本 – 完工估算成本

显示任务的成本偏差预估。 如果完工估算成本比计划成本大，则预估成本需要的时间比最初计划的多。 因此，趋向超出预算。 如果完工估算成本比计划成本小，则预估成本需要的时间比最初计划的少，并且趋向低于预算。

## <a name="project-managers-reprojection-of-cost"></a>项目经理对成本的重新预估

重新预估工作量时，**成本跟踪** 视图中将全部重新计算 CTC、完工估算成本、消耗成本百分比和预估成本偏差。

## <a name="project-status-summary"></a>项目状态汇总

**工作量跟踪** 和 **成本跟踪** 视图中的跟踪数据显示项目根节点、汇总任务和叶节点任务级的进度和成本消耗。 **项目实体** 页中的 **状态** 部分显示项目级状态的汇总。

## <a name="status-summary-fields"></a>“状态摘要”字段

**总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。 其使用颜色编码（如绿色、黄色和红色）来指示上升的风险。 项目经理可使用 **注释** 字段输入有关状态的特定注释。 **状态更新时间** 字段不可编辑，其值是时间戳，用于指示状态的上次更新时间。

**计划绩效** 和 **成本绩效** 字段从跟踪日期设置。 如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，可将这些字段设置为 **提前**。 如果根节点的计划与成本偏差为负，可将其设置为 **落后**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
