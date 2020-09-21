---
title: 部门
description: 此主题介绍 Dynamics 365 Project Service Automation 中的部门。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749799"
---
# <a name="organizational-units"></a><span data-ttu-id="e4e09-103">部门</span><span class="sxs-lookup"><span data-stu-id="e4e09-103">Organizational units</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e4e09-104">在 Dynamics 365 Project Service Automation 中，部门是专业服务公司中聘用具有成本费率的可记帐资源的专门组或部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-104">Dynamics 365 Project Service Automation, an organizational unit is a distinct group or division in a professional services company that employs billable resources that have cost rates.</span></span>

<span data-ttu-id="e4e09-105">对于聘用各种实践环节或业务范围技术资源的专业服务公司，填补一个实践环节或业务范围的角色所需成本与填补另一个实践环节或业务范围的角色所需成本不同。</span><span class="sxs-lookup"><span data-stu-id="e4e09-105">For professional services companies that employ technical resources in various practice areas or business lines, the cost to fill a role in one practice area or business line might differ from the cost to fill a role in another practice area or business line.</span></span> <span data-ttu-id="e4e09-106">部门这一概念在此场景中有所帮助，方法是集中公司中具有一组可记帐角色的专门成本结构的部门内的这些角色。</span><span class="sxs-lookup"><span data-stu-id="e4e09-106">The concept  organizational units helps in this scenario by providing a way to group a set of billable roles in a division of a company that has a distinct cost structure for these roles.</span></span>

## <a name="key-attributes-and-associations-of-organizational-units"></a><span data-ttu-id="e4e09-107">部门的关键属性和关联</span><span class="sxs-lookup"><span data-stu-id="e4e09-107">Key attributes and associations of organizational units</span></span>

<span data-ttu-id="e4e09-108">PSA 中的部门具有专门的货币和专门的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-108">In PSA, an organizational unit in PSA has a specific currency and specific cost price lists.</span></span>

<span data-ttu-id="e4e09-109">部门的货币是用于跟踪成本的主要货币。</span><span class="sxs-lookup"><span data-stu-id="e4e09-109">The currency of an organizational unit is the primary currency that is used to track costs.</span></span>

<span data-ttu-id="e4e09-110">可以将一个或多个成本价目表附加到每个部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-110">One or more cost price lists can be attached to each organizational unit.</span></span> <span data-ttu-id="e4e09-111">PSA 对可附加到部门的价目表实施以下限制：</span><span class="sxs-lookup"><span data-stu-id="e4e09-111">PSA puts the following limitations on the price lists that can be attached to an organizational unit:</span></span>

- <span data-ttu-id="e4e09-112">价目表必须采用部门的货币</span><span class="sxs-lookup"><span data-stu-id="e4e09-112">Price lists must be in the currency of the organizational unit</span></span>
- <span data-ttu-id="e4e09-113">价目表必须是成本价目表</span><span class="sxs-lookup"><span data-stu-id="e4e09-113">Price lists must be of cost price lists</span></span>

<span data-ttu-id="e4e09-114">此外，资源实体中的部门还有一个属性。</span><span class="sxs-lookup"><span data-stu-id="e4e09-114">In addition, there is an attribute for the organizational unit on the Resource entity.</span></span> <span data-ttu-id="e4e09-115">可以将每个资源分派给一个部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-115">Each resource can be assigned to one organizational unit.</span></span>

## <a name="roles-of-organizational-units"></a><span data-ttu-id="e4e09-116">部门的角色</span><span class="sxs-lookup"><span data-stu-id="e4e09-116">Roles of organizational units</span></span>

<span data-ttu-id="e4e09-117">部门在 PSA 中充当两种角色：</span><span class="sxs-lookup"><span data-stu-id="e4e09-117">The organizational unit plays two roles in PSA:</span></span>

- <span data-ttu-id="e4e09-118">**合同签订部门** – 代表主要负责赢得销售和管理对客户的工作和服务交付的公司组或部门的部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-118">**Contracting unit** – The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> <span data-ttu-id="e4e09-119">合同签订部门通过**商机**、**报价单**、**项目合同**和**项目**页标题部门中的**合同签订部门**字段识别。</span><span class="sxs-lookup"><span data-stu-id="e4e09-119">The contracting unit is identified by the **Contracting Unit** field in the header section of the **Opportunity**, **Quote**, **Project Contract**, and **Project** pages.</span></span>
- <span data-ttu-id="e4e09-120">**资源单位** – 资源所属部门或将资源分派给的部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-120">**Resourcing unit** – The organizational unit that a resource belongs to or is assigned to.</span></span> <span data-ttu-id="e4e09-121">这种部门可以将自己的资源提供给工作说明书 (SOW) 中和合同签订部门负责的项目中的某些角色。</span><span class="sxs-lookup"><span data-stu-id="e4e09-121">This organizational unit can provide its resources for some roles on statements of work (SOWs) and projects that are owned by the contracting unit.</span></span>

> ![合同签订部门和资源部门](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a><span data-ttu-id="e4e09-123">部门常见问题</span><span class="sxs-lookup"><span data-stu-id="e4e09-123">Organizational unit FAQs</span></span>

<span data-ttu-id="e4e09-124">以下是有关部门的一些最常见的问题。</span><span class="sxs-lookup"><span data-stu-id="e4e09-124">Here are some of the most frequently asked questions about organizational units.</span></span>

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a><span data-ttu-id="e4e09-125">PSA 中的部门实体与 Dynamics 365 中的现有组织实体之间有何关系？</span><span class="sxs-lookup"><span data-stu-id="e4e09-125">How is the Organizational Unit entity in PSA related to the Organization entity that already exists in Dynamics 365?</span></span>

<span data-ttu-id="e4e09-126">Microsoft Dynamics 365 中的组织实体代表全球性 Dynamics 365 实例的名称。</span><span class="sxs-lookup"><span data-stu-id="e4e09-126">The Organization entity in Microsoft Dynamics 365 represents the name of a global Dynamics 365 instance.</span></span> <span data-ttu-id="e4e09-127">此名称通常是全球性企业的名称。</span><span class="sxs-lookup"><span data-stu-id="e4e09-127">This name is usually the name of the global enterprise.</span></span>

<span data-ttu-id="e4e09-128">部门实体代表全球性企业的一个组或部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-128">The Organizational Unit entity represents a group or division in the global enterprise.</span></span> <span data-ttu-id="e4e09-129">这个组或部门有一组角色和这些角色的成本价目表，而这些角色和价目表则与企业中其他组或部门的角色和价目表不同。</span><span class="sxs-lookup"><span data-stu-id="e4e09-129">This group or division has a set of roles and a cost price list for those roles, and those roles and price list differ from the roles and price list of other groups or divisions in the enterprise.</span></span>

<span data-ttu-id="e4e09-130">安装 PSA 时，将根据组织创建一个默认部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-130">When PSA is installed, a default organizational unit is created based on the organization.</span></span> <span data-ttu-id="e4e09-131">将把所有现有资源分派给这个默认部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-131">All existing resources are assigned to the default organizational unit.</span></span> <span data-ttu-id="e4e09-132">如果将任何新 Active Directory 用户或资源导入 Dynamics 365 中，用户导入流程将把这些用户或资源分派给 PSA 中的默认部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-132">If any new Active Directory users or resources are imported into Dynamics 365, the user import process assigns them to the default organizational unit in PSA.</span></span>
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a><span data-ttu-id="e4e09-133">部门实体与业务部门实体有何区别？</span><span class="sxs-lookup"><span data-stu-id="e4e09-133">How does the organizational unit entity differ from the business unit entity?</span></span>

<span data-ttu-id="e4e09-134">在 Dynamics 365 中，业务部门实体是一种安全构造。</span><span class="sxs-lookup"><span data-stu-id="e4e09-134">In Dynamics 365, the Business Unit entity is a security construct.</span></span> <span data-ttu-id="e4e09-135">将用户与业务部门关联可以确定用户可访问的实体和实体记录。</span><span class="sxs-lookup"><span data-stu-id="e4e09-135">The association of a user with a business unit determines the entities and entity records that the user has access to.</span></span> <span data-ttu-id="e4e09-136">还可以确定该用户对这些实体记录的权限（创建、读取、写入、删除、附加、附加到、分派或共享）。</span><span class="sxs-lookup"><span data-stu-id="e4e09-136">It also determines the permissions (Create, Read, Write, Delete, Append, Append To, Assign, or Share) that the user has for those entity records.</span></span>

<span data-ttu-id="e4e09-137">部门实体代表具有为其分派的员工的独占成本费率的公司组或部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-137">The Organizational Unit entity represents a company group or division that has distinct cost rates for employees that are assigned to it.</span></span> <span data-ttu-id="e4e09-138">资源与部门的关联决定资源在项目协定中的成本。</span><span class="sxs-lookup"><span data-stu-id="e4e09-138">The association of a resource with an organizational unit determines the resource's cost to a project engagement.</span></span>

<span data-ttu-id="e4e09-139">实施 Dynamics 365 时，请优化业务部门层次结构的安全授权和业务部门的用户分派。</span><span class="sxs-lookup"><span data-stu-id="e4e09-139">When you implement Dynamics 365, optimize security authorization for the hierarchy of business units and the assignment of users to business units.</span></span> <span data-ttu-id="e4e09-140">将通常访问同一组记录的所有用户分派给同一个业务部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-140">Assign all users who must typically access the same set of records to the same business unit.</span></span> <span data-ttu-id="e4e09-141">部门不影响安全授权或访问权限。</span><span class="sxs-lookup"><span data-stu-id="e4e09-141">The organizational unit has no effect on security authorization or access.</span></span>

#### <a name="example-of-organizational-units-and-business-units"></a><span data-ttu-id="e4e09-142">部门和业务部门的示例</span><span class="sxs-lookup"><span data-stu-id="e4e09-142">Example of organizational units and business units</span></span>

<span data-ttu-id="e4e09-143">Contoso, Ltd. 的 Microsoft 技术业务非常兴旺。</span><span class="sxs-lookup"><span data-stu-id="e4e09-143">Contoso, Ltd. has a thriving Microsoft technology practice.</span></span> <span data-ttu-id="e4e09-144">建和方银都是 C\# 开发人员，但是方银在美国，而建在印度。</span><span class="sxs-lookup"><span data-stu-id="e4e09-144">Prakash and Tricia are both C\# developers, but Tricia is in the United States, whereas Prakash is in India.</span></span> <span data-ttu-id="e4e09-145">大多数项目协定需要 Contoso 印度和 Contoso 美国的资源，而建和方银需要这些业务区域中的项目的相同级别安全访问权限。</span><span class="sxs-lookup"><span data-stu-id="e4e09-145">Most of the project engagements require resources from Contoso India and Contoso US, and Prakash and Tricia require the same level of security access to projects in this practice area.</span></span> <span data-ttu-id="e4e09-146">但是，Contoso 印度开发人员的成本与 Contoso 美国开发人员的成本相差很大。</span><span class="sxs-lookup"><span data-stu-id="e4e09-146">However, the cost of developers from Contoso India differs significantly from the cost of developers from Contoso US.</span></span>

<span data-ttu-id="e4e09-147">下面是使用 Dynamics 365 和 PSA 针对这种场景进行设计的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="e4e09-147">Here is an optimal way to design for this scenario by using Dynamics 365 and PSA.</span></span>

1. <span data-ttu-id="e4e09-148">创建Microsoft 技术业务作为业务部门，并将建和方银与其关联。</span><span class="sxs-lookup"><span data-stu-id="e4e09-148">Create the Microsoft technology practice as a business unit, and associate Prakash and Tricia with it.</span></span> <span data-ttu-id="e4e09-149">这样就可以帮助确保两位员工对该业务区域中的所有项目具有相同级别的安全访问权限。</span><span class="sxs-lookup"><span data-stu-id="e4e09-149">In this way, you help guarantee that both employees have the same level of security access to any projects in that practice area.</span></span> <span data-ttu-id="e4e09-150">她们都可以检查进度和报告时间、支出和任务更新。</span><span class="sxs-lookup"><span data-stu-id="e4e09-150">They both will be able to check progress and report time, expenses, and task updates.</span></span> 
2. <span data-ttu-id="e4e09-151">创建两个部门以帮助确保正确体现项目的成本。</span><span class="sxs-lookup"><span data-stu-id="e4e09-151">Create two organizational units to hel guarantee that the cost to the project is correctly reflected.</span></span> 
3. <span data-ttu-id="e4e09-152">将方银与 Contoso 美国关联，将建与 Contoso 印度关联。</span><span class="sxs-lookup"><span data-stu-id="e4e09-152">Associate Tricia wtih Contoso US and associate Prakash with Contoso India.</span></span>
4. <span data-ttu-id="e4e09-153">为这两个部门分派适当的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-153">Assign appropriate cost price lists to both organizational units.</span></span> <span data-ttu-id="e4e09-154">这样，就可以帮助确保项目中为建和方银记录的成本准确体现 Contoso 美国与 Contoso 印度之间的成本差额。</span><span class="sxs-lookup"><span data-stu-id="e4e09-154">TIn this way, you help guarantee that the costs that are recorded on the project for Prakash and Tricia accurately reflect the difference in costs between Contoso US and Contoso India.</span></span>

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a><span data-ttu-id="e4e09-155">部门是否与 Dynamics 365 中的销售区域有关？</span><span class="sxs-lookup"><span data-stu-id="e4e09-155">Are organizational units related to sales territories in Dynamics 365?</span></span>

<span data-ttu-id="e4e09-156">销售区域与部门之间没有任何关联或关系。</span><span class="sxs-lookup"><span data-stu-id="e4e09-156">There is no association or relationship between sales territories and organizational units.</span></span> <span data-ttu-id="e4e09-157">销售区域通常是开展销售的地理区域。</span><span class="sxs-lookup"><span data-stu-id="e4e09-157">A sales territory is typically a geographical area where sales occur.</span></span> <span data-ttu-id="e4e09-158">可以为每个销售区域关联销售价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-158">A sales price list can be associated with each sales territory.</span></span>

<span data-ttu-id="e4e09-159">部门是公司中的内部组或部门，用于跟踪销售给其他部门或外部客户的一组角色的成本。</span><span class="sxs-lookup"><span data-stu-id="e4e09-159">An organizational unit is an internal group or division in the company that tracks costs for a set of roles that it sells to other divisions or to external customers.</span></span>

#### <a name="example-of-organizational-units-and-sales-territories"></a><span data-ttu-id="e4e09-160">部门和销售区域的示例</span><span class="sxs-lookup"><span data-stu-id="e4e09-160">Example of organizational units and sales territories</span></span>

<span data-ttu-id="e4e09-161">Contoso, Ltd. 有两个开发中心：Contoso 美国和 Contoso 印度。</span><span class="sxs-lookup"><span data-stu-id="e4e09-161">Contoso, Ltd. has two development centers: Contoso US and Contoso India.</span></span> <span data-ttu-id="e4e09-162">这两个开发中心的资源成本相差很大。</span><span class="sxs-lookup"><span data-stu-id="e4e09-162">Costs of resources differ greatly between these two development centers.</span></span>

<span data-ttu-id="e4e09-163">Contoso 在大量国际市场（如拉丁美洲、北美、亚太、西欧和中东）销售其 IT 服务。</span><span class="sxs-lookup"><span data-stu-id="e4e09-163">Contoso sells its IT services in many international markets, such as Latin America, North America, Asia-Pacific, Western Europe, and the Middle East.</span></span> <span data-ttu-id="e4e09-164">相同项目角色的帐单费率在这些市场中相差很大。</span><span class="sxs-lookup"><span data-stu-id="e4e09-164">Bill rates for the same project roles can vary widely across these markets.</span></span>

<span data-ttu-id="e4e09-165">应该将 Contoso 美国和 Contoso 印度设置为部门，而每个部门应该有自己的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-165">Contoso US and Contoso India should be set up as organizational units, and each organizational unit should have its own cost price list.</span></span> <span data-ttu-id="e4e09-166">应该将亚太、拉丁美洲、北美、西欧和中东设置为销售区域，而每个销售区域应该有自己的销售价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-166">Asia-Pacific, Latin America, North America, Western Europe, and the Middle East should be set up as sales territories, and each sales territory should have its own sales price list.</span></span>

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a><span data-ttu-id="e4e09-167">为什么要限制价目表与部门的关联？</span><span class="sxs-lookup"><span data-stu-id="e4e09-167">Why is there a restriction on the association of price lists with organizational units?</span></span> 

<span data-ttu-id="e4e09-168">出售服务的地理区域或市场中的销售定价通常各不相同。</span><span class="sxs-lookup"><span data-stu-id="e4e09-168">Sales pricing is usually unique to the geographical areas or markets where services are sold.</span></span> <span data-ttu-id="e4e09-169">公司的内部部门自己通常没有同一种类型的服务的销售定价。</span><span class="sxs-lookup"><span data-stu-id="e4e09-169">Internal divisions of a company don't usually have their own sales pricing for the same type of services.</span></span> <span data-ttu-id="e4e09-170">但是，内部部门有不同的售出商品成本 (COGS)，具体取决于聘用的人员的技能和运营区域的劳工条件。</span><span class="sxs-lookup"><span data-stu-id="e4e09-170">However, internal divisions have a different cost of goods sold (COGS), depending on the skills of the people that they employ and the labor conditions of the region where they operate.</span></span> <span data-ttu-id="e4e09-171">因为部门建模为公司的内部部门，所以只能有成本价目表。</span><span class="sxs-lookup"><span data-stu-id="e4e09-171">Because organizational units are modeled as internal divisions of a company, they can have only cost price lists.</span></span>

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a><span data-ttu-id="e4e09-172">为什么不能将销售价目表与部门关联？</span><span class="sxs-lookup"><span data-stu-id="e4e09-172">Why can’t we associate sales price lists to organizational units?</span></span>

<span data-ttu-id="e4e09-173">在 PSA 中，可以将销售价目表与客户和销售区域关联。</span><span class="sxs-lookup"><span data-stu-id="e4e09-173">In PSA, sales price lists can be associated with customers and sales territories.</span></span> <span data-ttu-id="e4e09-174">商机、报价单、项目合同和项目等交易实体使用附加到客户帐户或销售区域的销售价目表，以便确定项目协定中的帐单费率和潜在收入。</span><span class="sxs-lookup"><span data-stu-id="e4e09-174">Transactional entities like Opportunity, Quote, Project Contract, and Project use sales price lists that are attached to the customer account or the sales territory to determine bill rates and potential revenue on the project engagement.</span></span>

<span data-ttu-id="e4e09-175">成本价目表与部门关联。</span><span class="sxs-lookup"><span data-stu-id="e4e09-175">Cost price lists are associated with organizational units.</span></span> <span data-ttu-id="e4e09-176">商机、报价单、项目合同和项目等交易实体使用附加到合同签订部门的成本价目表，以便确定项目协定中的成本。</span><span class="sxs-lookup"><span data-stu-id="e4e09-176">Transactional entities like Opportunity, Quote, Project Contract, and Project use cost price lists that are attached to the contracting unit to determine costs to a project engagement.</span></span>

### <a name="are-organizational-units-hierarchical-in-psa"></a><span data-ttu-id="e4e09-177">PSA 中的部门是否分层？</span><span class="sxs-lookup"><span data-stu-id="e4e09-177">Are organizational units hierarchical in PSA?</span></span>

<span data-ttu-id="e4e09-178">编号</span><span class="sxs-lookup"><span data-stu-id="e4e09-178">No.</span></span> <span data-ttu-id="e4e09-179">在 PSA 当前版本中，部门不分层。</span><span class="sxs-lookup"><span data-stu-id="e4e09-179">In the current release of PSA, organizational units are not hierarchical.</span></span> <span data-ttu-id="e4e09-180">这意味着您不能：</span><span class="sxs-lookup"><span data-stu-id="e4e09-180">This means that you can’t:</span></span>

- <span data-ttu-id="e4e09-181">为遍历层次结构的默认成本价配置模式。</span><span class="sxs-lookup"><span data-stu-id="e4e09-181">Configure a pattern for defaulting cost prices that traverses up a hierarchy.</span></span> 
- <span data-ttu-id="e4e09-182">报告不同部门层次结构级别的汇总收入或成本。</span><span class="sxs-lookup"><span data-stu-id="e4e09-182">Report revenue or cost rolled up at different levels of the organizational unit hierarchy.</span></span>

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a><span data-ttu-id="e4e09-183">我们是一家大型跨国公司，采用了复杂、多级的成本中心、部门、记帐办公室层次结构。</span><span class="sxs-lookup"><span data-stu-id="e4e09-183">We're a big multinational firm with a complex, multilevel hierarchy of cost centers, divisions, and billing offices.</span></span> <span data-ttu-id="e4e09-184">如何充分利用此 Project Service 应用程序版本中的部门概念？</span><span class="sxs-lookup"><span data-stu-id="e4e09-184">How can we make the best use of the organizational unit concept in this version of the Project Service app?</span></span>

<span data-ttu-id="e4e09-185">如果采用复杂的成本中心、部门、记帐办公室层次结构，请将该层次结构的叶节点设置为不同的部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-185">When you have a complex hierarchy of cost centers, divisions, billing offices, etc., set up the leaf nodes of that hierarchy as distinct organizational units.</span></span>
<span data-ttu-id="e4e09-186">以下示例显示典型的层次结构：</span><span class="sxs-lookup"><span data-stu-id="e4e09-186">The following example shows a typical hierarchy:</span></span>

<span data-ttu-id="e4e09-187">**Contoso 印度**</span><span class="sxs-lookup"><span data-stu-id="e4e09-187">**Contoso India**</span></span>

  - <span data-ttu-id="e4e09-188">SAP 业务</span><span class="sxs-lookup"><span data-stu-id="e4e09-188">SAP Practice</span></span> 

    - <span data-ttu-id="e4e09-189">技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-189">Technical Consultants</span></span> 
    - <span data-ttu-id="e4e09-190">职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-190">Functional Consultants</span></span> 
    
  - <span data-ttu-id="e4e09-191">Microsoft 技术业务</span><span class="sxs-lookup"><span data-stu-id="e4e09-191">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="e4e09-192">技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-192">Technical Consultants</span></span>
    - <span data-ttu-id="e4e09-193">职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-193">Functional Consultants</span></span> 
    
<span data-ttu-id="e4e09-194">**Contoso US**</span><span class="sxs-lookup"><span data-stu-id="e4e09-194">**Contoso US**</span></span>

 - <span data-ttu-id="e4e09-195">SAP 业务</span><span class="sxs-lookup"><span data-stu-id="e4e09-195">SAP Practice</span></span> 

    - <span data-ttu-id="e4e09-196">技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-196">Technical Consultants</span></span> 
    - <span data-ttu-id="e4e09-197">职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-197">Functional Consultants</span></span> 
    
 - <span data-ttu-id="e4e09-198">Microsoft 技术业务</span><span class="sxs-lookup"><span data-stu-id="e4e09-198">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="e4e09-199">技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-199">Technical Consultants</span></span> 
    - <span data-ttu-id="e4e09-200">职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-200">Functional Consultants</span></span> 
 
<span data-ttu-id="e4e09-201">如果您的层次结构类似，则必须将其设置为简单列表，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e4e09-201">If your hierarchy is similar, you must set it up as a flat list, as shown here:</span></span>
- <span data-ttu-id="e4e09-202">Contoso 印度 - SAP 业务 - 技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-202">Contoso India - SAP Practice - Technical Consultants</span></span> 
- <span data-ttu-id="e4e09-203">Contoso 印度 - SAP 业务 - 职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-203">Contoso India - SAP Practice - Functional Consultants</span></span>       
- <span data-ttu-id="e4e09-204">Contoso 印度 - Microsoft 技术业务职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-204">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="e4e09-205">Contoso 印度 - Microsoft 技术业务职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-205">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="e4e09-206">Contoso 美国 - SAP 业务 - 技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-206">Contoso US - SAP Practice - Technical Consultants</span></span>  
- <span data-ttu-id="e4e09-207">Contoso 美国 - SAP 业务 - 职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-207">Contoso US - SAP Practice - Functional Consultants</span></span>  
- <span data-ttu-id="e4e09-208">Contoso 美国 - Microsoft 技术业务 - 技术顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-208">Contoso US - Microsoft Technology Practice - Technical Consultants</span></span> 
- <span data-ttu-id="e4e09-209">Contoso 美国 - Microsoft 技术业务 - 职能顾问</span><span class="sxs-lookup"><span data-stu-id="e4e09-209">Contoso US - Microsoft Technology Practice - Functional Consultants</span></span>

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a><span data-ttu-id="e4e09-210">我们是仅以一个部门的形式运营的小型专业服务公司。</span><span class="sxs-lookup"><span data-stu-id="e4e09-210">We're a small professional services company that operates as only one division.</span></span> <span data-ttu-id="e4e09-211">如何在 PSA 当前版本中充分利用部门概念？</span><span class="sxs-lookup"><span data-stu-id="e4e09-211">How can we best use the organizational unit concept in the current version of PSA?</span></span>

<span data-ttu-id="e4e09-212">如果您的公司以拥有一个成本价目表的部门的形式运营，则不必设置任何部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-212">If your company operates as one unit that has one cost price list, you don't have to set up any organizational units.</span></span> <span data-ttu-id="e4e09-213">PSA 安装期间，Dynamics 365 创建一个与组织同名的默认部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-213">During PSA installation, Dynamics 365 creates one default organizational unit that has the same name as the organization.</span></span> <span data-ttu-id="e4e09-214">默认情况下，将把所有用户分派给这个部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-214">By default, all users are assigned to this organizational unit.</span></span> <span data-ttu-id="e4e09-215">只要系统需要选择部门，都会默认选择此部门。</span><span class="sxs-lookup"><span data-stu-id="e4e09-215">Whenever the system requires that an organizational unit be selected, this organizational unit is selected by default.</span></span>

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a><span data-ttu-id="e4e09-216">基于报价单或项目合同子项创建项目时，默认合同签订部门来自报价单或项目合同。</span><span class="sxs-lookup"><span data-stu-id="e4e09-216">When a project is created from a quote or project contract line, the default contracting unit comes from the quote or project contract.</span></span> <span data-ttu-id="e4e09-217">如果项目是在报价单或项目合同之类销售实体之前创建的，则什么是默认合同签订部门？</span><span class="sxs-lookup"><span data-stu-id="e4e09-217">If a project is created before sales entities such as quote or project contract, what is the default contracting unit?</span></span>

<span data-ttu-id="e4e09-218">当磁盘时，项目的项目需要创建收缩根据默认的计价创建该活动的用户。</span><span class="sxs-lookup"><span data-stu-id="e4e09-218">When a project is created on its own, the default contracting unit of the project is based on the user who creates it.</span></span> <span data-ttu-id="e4e09-219">该用户也是默认项目经理。</span><span class="sxs-lookup"><span data-stu-id="e4e09-219">That user is also the default project manager.</span></span> <span data-ttu-id="e4e09-220">如果项目映射到报价单或项目合同之类销售实体，则项目的合同签订部门改为基于销售实体。</span><span class="sxs-lookup"><span data-stu-id="e4e09-220">If the project is mapped to a sales entity such as a quote or project contract, the contracting unit on the project is based on the sales entity instead.</span></span> <span data-ttu-id="e4e09-221">在此情况下，可能会重新计算项目估算，因为如果更改合同签订部门，则使用成本价目表计算成本估算变化。</span><span class="sxs-lookup"><span data-stu-id="e4e09-221">In this case, project estimates might be recalculated, because the cost price list is used to calculate the cost estimate changes if the contracting unit is changed.</span></span> <span data-ttu-id="e4e09-222">销售价目表用于计算将更改的销售估算，因此将与报价单中的项目价目表同步。</span><span class="sxs-lookup"><span data-stu-id="e4e09-222">The sales price list is used to calculate the sales estimates that will be changed so that they are in sync with the project price list on the quote.</span></span>

<span data-ttu-id="e4e09-223">项目的**合同签订部门**和**货币**字段已锁定，不能编辑，因为这些字段必须与项目映射到的销售实体（报价单或项目合同）中的值同步。</span><span class="sxs-lookup"><span data-stu-id="e4e09-223">The **Contracting Unit** and **Currency** fields on the project are locked for editing, because they must be in sync with the values on the sales entity (quote or project contract) that the project is mapped to.</span></span>
