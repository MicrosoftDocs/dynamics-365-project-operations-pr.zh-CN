---
title: 配置其他参数设置
description: 如何在 Project Service 中配置其他参数设置
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072604"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="0f97f-103">配置其他参数设置 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0f97f-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0f97f-104">一旦您在之前主题中配置了项目，您需要设置其他项目参数以使用项目。</span><span class="sxs-lookup"><span data-stu-id="0f97f-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="0f97f-105">首次安装 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时，您创建了参数设置以首先创建运行 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 所需的所有记录。</span><span class="sxs-lookup"><span data-stu-id="0f97f-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="0f97f-106">现在是时间返回并为这些设置配置其他字段。</span><span class="sxs-lookup"><span data-stu-id="0f97f-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="0f97f-107">您需要已经配置了以下设置：</span><span class="sxs-lookup"><span data-stu-id="0f97f-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="0f97f-108">部门</span><span class="sxs-lookup"><span data-stu-id="0f97f-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="0f97f-109">发票频率</span><span class="sxs-lookup"><span data-stu-id="0f97f-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="0f97f-110">工作时间模板</span><span class="sxs-lookup"><span data-stu-id="0f97f-110">Work hours template</span></span>  
  
-   <span data-ttu-id="0f97f-111">价目表</span><span class="sxs-lookup"><span data-stu-id="0f97f-111">Price list</span></span>  
 
<span data-ttu-id="0f97f-112">在此步骤中，您还可以指出所需的资源分配类型：</span><span class="sxs-lookup"><span data-stu-id="0f97f-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="0f97f-113">**中心** 。</span><span class="sxs-lookup"><span data-stu-id="0f97f-113">**Central**.</span></span> <span data-ttu-id="0f97f-114">只有资源经理可以将资源分配到项目中。</span><span class="sxs-lookup"><span data-stu-id="0f97f-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="0f97f-115">**混合** 。</span><span class="sxs-lookup"><span data-stu-id="0f97f-115">**Hybrid**.</span></span> <span data-ttu-id="0f97f-116">资源经理、项目经理和客户经理可以将资源分配到项目中。</span><span class="sxs-lookup"><span data-stu-id="0f97f-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="0f97f-117">设置项目参数：</span><span class="sxs-lookup"><span data-stu-id="0f97f-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="0f97f-118">转到 **Project Service > 参数** 。</span><span class="sxs-lookup"><span data-stu-id="0f97f-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="0f97f-119">单击要配置的参数设置（首次安装 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时创建的参数设置），或单击 **新建** 新建一个。</span><span class="sxs-lookup"><span data-stu-id="0f97f-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="0f97f-120">在 **常规** 区域，为您的项目参数设置所有选项。</span><span class="sxs-lookup"><span data-stu-id="0f97f-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="0f97f-121">在 **价目表** 区域中，单击 **+** 添加价目表，在 **项目参数价目表** 下拉列表中选择价目表，然后单击 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="0f97f-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="0f97f-122">在屏幕右下角，单击 **保存** 按钮。</span><span class="sxs-lookup"><span data-stu-id="0f97f-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="0f97f-123">若要使 Project Service 能够正常运行，必须维护项目参数记录。</span><span class="sxs-lookup"><span data-stu-id="0f97f-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="0f97f-124">不应删除该记录。</span><span class="sxs-lookup"><span data-stu-id="0f97f-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="0f97f-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f97f-125">See Also</span></span>  
 [<span data-ttu-id="0f97f-126">设置资源</span><span class="sxs-lookup"><span data-stu-id="0f97f-126">Set up resources</span></span>](../psa/set-up-resources.md)