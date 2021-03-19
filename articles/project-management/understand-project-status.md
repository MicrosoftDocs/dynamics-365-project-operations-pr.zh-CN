---
title: 了解项目状态
description: 该主题提供了分配给 Dynamics 365 Project Operations 中的项目的状态信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286462"
---
# <a name="understand-project-status"></a><span data-ttu-id="1cd4f-103">了解项目状态</span><span class="sxs-lookup"><span data-stu-id="1cd4f-103">Understand project status</span></span>

<span data-ttu-id="1cd4f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="1cd4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1cd4f-105">**项目实体** 页上的 **状态** 部分提供基于成本和工作量的项目运行状况摘要。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="1cd4f-106">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="1cd4f-106">Status summary fields</span></span>

- <span data-ttu-id="1cd4f-107">**总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="1cd4f-108">此字段使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="1cd4f-109">项目经理可使用 **注释** 字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="1cd4f-110">**状态更新日期** 字段不可编辑。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="1cd4f-111">此字段中的值是指示状态上次更新时间的时间戳。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="1cd4f-112">**计划绩效** 和 **成本绩效** 字段从跟踪网格设置。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="1cd4f-113">如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，这些字段将更新为 **提前**。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="1cd4f-114">如果根节点的计划与成本偏差为负，这些字段将设置为 **落后**。</span><span class="sxs-lookup"><span data-stu-id="1cd4f-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]