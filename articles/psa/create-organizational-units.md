---
title: 创建部门
description: 如何在 Project Service 中创建部门
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
ms.openlocfilehash: f8d44254adc9fc1e35d39080e284ea6195bfa821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144717"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="4e3f4-103">创建部门 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4e3f4-103">Create organizational units (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4e3f4-104">您的公司可能按地域、职能或者其他区域组织其咨询业务。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="4e3f4-105">您可以创建一个反映您的咨询业务的部门。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="4e3f4-106">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]部门是专业服务公司内的一个组或部门，其使用具有与公司中的其他此类组或部门不同的成本费率的计费资源。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4e3f4-107">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]部门独立于 [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] 中的业务部门。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="4e3f4-108">业务部门不只是影响 [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] 信息访问级别的安全结构，其通常围绕公司部门组织，例如母公司和子公司或部门。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="4e3f4-109">部门表示您的咨询公司如何分类其不同业务，按地理位置（如 EMEA 或 LATAM）、按职能（如产品开发或 IT 外包），还是按其他参数。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="4e3f4-110">转到 **Project Service > 部门**。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="4e3f4-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4e3f4-112">在 **常规** 区域中的 **名称** 内输入部门的名称，然后根据需要填写其他字段。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-112">In the **General** area, enter a name for the organization unit in **Name**, and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="4e3f4-113">单击 **保存** 创建记录，以便继续编辑。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="4e3f4-114">在 **成本价目表** 下，单击 **+** 添加价目表。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-114">Under **Cost Price Lists**, click **+** to add a price list.</span></span> <span data-ttu-id="4e3f4-115">此处只能添加具有 **成本** 上下文的价目表。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="4e3f4-116">在 **名称** 字段中，单击 **搜索** 按钮并选择您要将其用于此部门的价目表。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="4e3f4-117">根据需要继续添加价目表。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="4e3f4-118">完成后，请单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4e3f4-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4e3f4-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e3f4-119">See Also</span></span>  
 [<span data-ttu-id="4e3f4-120">配置 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4e3f4-120">Configure Project Service Automation</span></span>](../psa/configure.md)
