---
title: 配置资源角色
description: 如何在 Project Service 中配置资源角色
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: deaff0977ebb50382a28494fba2a1c34ed5cc9b4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144897"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="82878-103">配置资源角色 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="82878-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="82878-104">在确定资源要求或项目成本时，角色是项目规划的重要组成部分。</span><span class="sxs-lookup"><span data-stu-id="82878-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="82878-105">需要为项目所需的每个角色创建一个资源角色，并为该角色关联技能和熟练程度。</span><span class="sxs-lookup"><span data-stu-id="82878-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="82878-106">例如，可能需要为开发人员、项目经理或游戏测试人员创建角色。</span><span class="sxs-lookup"><span data-stu-id="82878-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="82878-107">也可以设置角色所需的技能和熟练级别。</span><span class="sxs-lookup"><span data-stu-id="82878-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="82878-108">请配置资源角色以确保贵组织的项目预计效率。</span><span class="sxs-lookup"><span data-stu-id="82878-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="82878-109">另请确保准确地设置记帐类型。</span><span class="sxs-lookup"><span data-stu-id="82878-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="82878-110">合同或报价单明细中不显示设置有非应计费记帐类型的项目。</span><span class="sxs-lookup"><span data-stu-id="82878-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="82878-111">设置资源角色之后，可以为价目表设置成本和销售价格。</span><span class="sxs-lookup"><span data-stu-id="82878-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="82878-112">请对要添加的每个角色执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="82878-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="82878-113">转到 **Project Service > 资源角色**。</span><span class="sxs-lookup"><span data-stu-id="82878-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="82878-114">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="82878-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="82878-115">在 **常规** 区域中的 **名称** 内输入角色的名称，然后根据需要填写其他字段。</span><span class="sxs-lookup"><span data-stu-id="82878-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="82878-116">单击 **保存** 创建记录，以便继续编辑。</span><span class="sxs-lookup"><span data-stu-id="82878-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="82878-117">在 **技能** 区域中单击 **+** 添加技能。</span><span class="sxs-lookup"><span data-stu-id="82878-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="82878-118">在 **角色资格要求** 窗格中的 **技能** 字段内单击，单击 **搜索** 按钮，然后选择技能。</span><span class="sxs-lookup"><span data-stu-id="82878-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="82878-119">选择该技能的熟练程度，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82878-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="82878-120">根据需要继续添加技能。</span><span class="sxs-lookup"><span data-stu-id="82878-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="82878-121">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82878-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="82878-122">要使该资源角色可供项目使用，单击 **激活**。</span><span class="sxs-lookup"><span data-stu-id="82878-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="82878-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82878-123">See Also</span></span>  
 [<span data-ttu-id="82878-124">设置资源</span><span class="sxs-lookup"><span data-stu-id="82878-124">Set up resources</span></span>](../psa/set-up-resources.md)
