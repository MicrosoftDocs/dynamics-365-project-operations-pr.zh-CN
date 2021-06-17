---
title: 了解项目状态
description: 该主题提供了分配给 Dynamics 365 Project Operations 中的项目的状态信息。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993405"
---
# <a name="understand-project-status"></a><span data-ttu-id="7aa6a-103">了解项目状态</span><span class="sxs-lookup"><span data-stu-id="7aa6a-103">Understand project status</span></span>

<span data-ttu-id="7aa6a-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="7aa6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7aa6a-105">**项目实体** 页上的 **状态** 部分提供基于成本和工作量的项目运行状况摘要。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="7aa6a-106">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="7aa6a-106">Status summary fields</span></span>

- <span data-ttu-id="7aa6a-107">**总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="7aa6a-108">此字段使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="7aa6a-109">项目经理可使用 **注释** 字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="7aa6a-110">**状态更新日期** 字段不可编辑。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="7aa6a-111">此字段中的值是指示状态上次更新时间的时间戳。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="7aa6a-112">**计划绩效** 和 **成本绩效** 字段从跟踪网格设置。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="7aa6a-113">如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，这些字段将更新为 **提前**。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="7aa6a-114">如果根节点的计划与成本偏差为负，这些字段将设置为 **落后**。</span><span class="sxs-lookup"><span data-stu-id="7aa6a-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]