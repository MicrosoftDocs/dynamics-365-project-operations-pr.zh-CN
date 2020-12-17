---
title: 固定价格收入估算项目
description: 本主题提供有关项目中固定价格收入的信息。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531372"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="33d5d-103">固定价格收入估算项目</span><span class="sxs-lookup"><span data-stu-id="33d5d-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="33d5d-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="33d5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="33d5d-105">当您在 Microsoft Dataverse 上的 Dynamics 365 Project Operations 中创建具有以下属性的项目合同子项时，系统会自动创建固定价格收入估算项目。</span><span class="sxs-lookup"><span data-stu-id="33d5d-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="33d5d-106">此项目中的信息基于以下内容：</span><span class="sxs-lookup"><span data-stu-id="33d5d-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="33d5d-107">固定价格记帐方法。</span><span class="sxs-lookup"><span data-stu-id="33d5d-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="33d5d-108">关联的项目。</span><span class="sxs-lookup"><span data-stu-id="33d5d-108">An associated project.</span></span>
  - <span data-ttu-id="33d5d-109">**项目合同子项** 页上 **账单计划** 选项卡上定义的至少一个里程碑。</span><span class="sxs-lookup"><span data-stu-id="33d5d-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="33d5d-110">查看固定价格收入估算项目</span><span class="sxs-lookup"><span data-stu-id="33d5d-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="33d5d-111">要查看固定价格收入估算项目，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="33d5d-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="33d5d-112">在 Dynamics 365 Finance 环境中，转到 **项目管理和会计** > **项目** > **固定价格收入估算项目**。</span><span class="sxs-lookup"><span data-stu-id="33d5d-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="33d5d-113">选择要查看的项目，并双击 **估算项目 ID**，以打开记录并查看项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="33d5d-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="33d5d-114">展开 **项目** 选项卡。您将在 **选定的项目** 网格中看到一个项目。</span><span class="sxs-lookup"><span data-stu-id="33d5d-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="33d5d-115">系统使用此项目作为默认项目，因为它是与项目合同子项关联的项目。</span><span class="sxs-lookup"><span data-stu-id="33d5d-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="33d5d-116">若要更改此关联，请选择其他项目并将其添加到 **选定的项目** 网格中。</span><span class="sxs-lookup"><span data-stu-id="33d5d-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="33d5d-117">如果在此网格中选择了多个项目，则所有选定项目的项目完成百分比和收入估算将一起计算。</span><span class="sxs-lookup"><span data-stu-id="33d5d-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="33d5d-118">可以手动设置项目成本、收入模板、成本模板和期间代码。</span><span class="sxs-lookup"><span data-stu-id="33d5d-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="33d5d-119">如果未手动设置它们，则使用为项目成本和收入配置文件配置的规则在首次计算项目估算期间默认这些值。</span><span class="sxs-lookup"><span data-stu-id="33d5d-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

