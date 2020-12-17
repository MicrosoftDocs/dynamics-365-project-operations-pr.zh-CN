---
title: 使用“复制项目”开发项目模板
description: 此主题提供有关如何使用“复制项目”自定义操作创建项目模板的信息。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642397"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="0fe63-103">使用“复制项目”开发项目模板</span><span class="sxs-lookup"><span data-stu-id="0fe63-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="0fe63-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="0fe63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0fe63-105">Dynamics 365 Project Operations 支持复制项目并将所有工作重新分配给代表该角色的一般资源的功能。</span><span class="sxs-lookup"><span data-stu-id="0fe63-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="0fe63-106">客户可以使用此功能来构建基本项目模板。</span><span class="sxs-lookup"><span data-stu-id="0fe63-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="0fe63-107">选择 **复制项目** 时，目标项目的状态将更新。</span><span class="sxs-lookup"><span data-stu-id="0fe63-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="0fe63-108">使用 **状态描述** 可以确定复制操作完成的时间。</span><span class="sxs-lookup"><span data-stu-id="0fe63-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="0fe63-109">如果未在目标项目实体中检测到目标日期，选择 **复制项目** 还会将项目的开始日期更新为当前的开始日期。</span><span class="sxs-lookup"><span data-stu-id="0fe63-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="0fe63-110">“复制项目”自定义操作</span><span class="sxs-lookup"><span data-stu-id="0fe63-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="0fe63-111">客户</span><span class="sxs-lookup"><span data-stu-id="0fe63-111">Name</span></span> 

<span data-ttu-id="0fe63-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="0fe63-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="0fe63-113">输入参数</span><span class="sxs-lookup"><span data-stu-id="0fe63-113">Input parameters</span></span>
<span data-ttu-id="0fe63-114">有三个输入参数：</span><span class="sxs-lookup"><span data-stu-id="0fe63-114">There are three input parameters:</span></span>

| <span data-ttu-id="0fe63-115">参数</span><span class="sxs-lookup"><span data-stu-id="0fe63-115">Parameter</span></span>          | <span data-ttu-id="0fe63-116">Type</span><span class="sxs-lookup"><span data-stu-id="0fe63-116">Type</span></span>   | <span data-ttu-id="0fe63-117">值</span><span class="sxs-lookup"><span data-stu-id="0fe63-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="0fe63-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="0fe63-118">ProjectCopyOption</span></span>  | <span data-ttu-id="0fe63-119">String</span><span class="sxs-lookup"><span data-stu-id="0fe63-119">String</span></span> | <span data-ttu-id="0fe63-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="0fe63-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="0fe63-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="0fe63-121">SourceProject</span></span>      | <span data-ttu-id="0fe63-122">实体引用</span><span class="sxs-lookup"><span data-stu-id="0fe63-122">Entity Reference</span></span> | <span data-ttu-id="0fe63-123">源项目</span><span class="sxs-lookup"><span data-stu-id="0fe63-123">Source Project</span></span> |
| <span data-ttu-id="0fe63-124">目标</span><span class="sxs-lookup"><span data-stu-id="0fe63-124">Target</span></span>             | <span data-ttu-id="0fe63-125">实体引用</span><span class="sxs-lookup"><span data-stu-id="0fe63-125">Entity Reference</span></span> | <span data-ttu-id="0fe63-126">目标项目</span><span class="sxs-lookup"><span data-stu-id="0fe63-126">Target Project</span></span> |


- <span data-ttu-id="0fe63-127">**{"clearTeamsAndAssignments":true}**：Web 版本的 Project 的默认行为，将删除所有工作和团队成员。</span><span class="sxs-lookup"><span data-stu-id="0fe63-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="0fe63-128">**{"removeNamedResources":true}** Project Operations 的默认行为，将工作还原为通用资源。</span><span class="sxs-lookup"><span data-stu-id="0fe63-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="0fe63-129">有关操作的更多默认行为，请参阅[使用 Web API 操作](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="0fe63-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="0fe63-130">指定要复制的字段</span><span class="sxs-lookup"><span data-stu-id="0fe63-130">Specify fields to copy</span></span> 
<span data-ttu-id="0fe63-131">当调用操作时，**复制项目** 将查看项目视图 **复制项目列**，以确定在复制项目时要复制哪些字段。</span><span class="sxs-lookup"><span data-stu-id="0fe63-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
