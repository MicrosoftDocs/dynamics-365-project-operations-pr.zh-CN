---
title: Project Operations 设置和配置数据集成
description: 本主题提供有关设置和配置 Project Operations 双重写入映射的信息。
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001055"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a><span data-ttu-id="dac53-103">Project Operations 设置和配置数据集成</span><span class="sxs-lookup"><span data-stu-id="dac53-103">Project Operations setup and configuration data integration</span></span>

<span data-ttu-id="dac53-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="dac53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dac53-105">本主题提供有关用于设置和配置实体的 Project Operations 双重写入集成的信息。</span><span class="sxs-lookup"><span data-stu-id="dac53-105">This topic provides information about Project Operations dual-write integration for setup and configuration entities.</span></span>

## <a name="project-contracts-contract-lines-and-projects"></a><span data-ttu-id="dac53-106">项目合同、合同子项和项目</span><span class="sxs-lookup"><span data-stu-id="dac53-106">Project contracts, contract lines, and projects</span></span>

<span data-ttu-id="dac53-107">在 Dataverse 中创建项目合同、合同子项和项目，并将其同步到 Finance and Operations 应用以进行其他会计工作。</span><span class="sxs-lookup"><span data-stu-id="dac53-107">Project contracts, contract lines, and projects are created in Dataverse and synchronized to Finance and Operations apps for additional accounting.</span></span> <span data-ttu-id="dac53-108">这些实体中的记录只能在 Dataverse 中创建和删除。</span><span class="sxs-lookup"><span data-stu-id="dac53-108">The records in these entities can be created and deleted only in Dataverse.</span></span> <span data-ttu-id="dac53-109">不过，可以在 Finance and Operations 应用中将诸如销售税组默认值和财务维度之类的会计属性添加到这些记录中。</span><span class="sxs-lookup"><span data-stu-id="dac53-109">However, accounting attributes such as sales tax group defaults and financial dimensions can be added to these records in the Finance and Operations apps.</span></span>

  ![项目合同集成概念](./media/1ProjectContract.jpg)

<span data-ttu-id="dac53-111">将在 Dataverse 中跟踪销售活动潜在顾客、商机和报价单，它们不会同步到 Finance and Operations 应用，因为没有与此活动关联的下游会计。</span><span class="sxs-lookup"><span data-stu-id="dac53-111">Sales activity leads, opportunities, and quotes are tracked in Dataverse and don't synchronize to Finance and Operations apps because there is no downstream accounting associated with this activity.</span></span>

<span data-ttu-id="dac53-112">Dataverse 中的项目合同功能使用 **项目合同抬头(salesorders)** 表映射在 Finance and Operations 应用中创建项目合同记录。</span><span class="sxs-lookup"><span data-stu-id="dac53-112">The project contract functionality in Dataverse creates a project contract record in Finance and Operations apps using the **Project contract headers (salesorders)** table map.</span></span> <span data-ttu-id="dac53-113">在 Dataverse 中保存项目合同还将开始创建项目合同客户实体记录。</span><span class="sxs-lookup"><span data-stu-id="dac53-113">Saving a project contract in Dataverse also starts the creation of a project contract customer entity record.</span></span> <span data-ttu-id="dac53-114">此记录使用 **项目资金来源(msdyn\_projectcontractssplitbillingrules)** 表映射同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="dac53-114">This record is synchronized to Finance and Operations apps using the **Project funding source (msdyn\_projectcontractssplitbillingrules)** table map.</span></span> <span data-ttu-id="dac53-115">此映射还同步项目合同客户的添加、更新和删除。</span><span class="sxs-lookup"><span data-stu-id="dac53-115">This map also synchronizes project contract customer additions, updates, and deletions.</span></span> <span data-ttu-id="dac53-116">项目合同客户之间的拆分记帐百分比仅在 Dataverse 中进行控制，而不同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="dac53-116">Split billing percentages between project contract customers are mastered only in Dataverse and not synchronized to Finance and Operations apps.</span></span>

<span data-ttu-id="dac53-117">项目合同在 Dataverse 中创建后，项目会计可以通过转到 **项目管理和会计** > **项目合同** > **设置** > **显示默认会计**，在 Finance and Operations 应用中更新此项目合同的会计属性。</span><span class="sxs-lookup"><span data-stu-id="dac53-117">After a project contract is created in Dataverse, the project accountant can update the accounting attributes for this project contract in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**.</span></span> <span data-ttu-id="dac53-118">会计可以通过在 Finance and Operations 应用中选择项目合同 ID（将在 Dataverse 中打开相关项目合同记录）来查看运营项目合同属性，如请求的交付日期和合同金额。</span><span class="sxs-lookup"><span data-stu-id="dac53-118">The accountant can review operational project contract attributes, such as requested delivery date and contract amount by selecting the project contract ID in Finance and Operations apps which opens the related project contract record in Dataverse.</span></span>

<span data-ttu-id="dac53-119">项目实体使用 **项目 V2 (msdyn\_projects)** 表映射同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="dac53-119">The project entity is synchronized to Finance and Operations apps using the **Projects V2 (msdyn\_projects)** table map.</span></span> <span data-ttu-id="dac53-120">项目会计可以：</span><span class="sxs-lookup"><span data-stu-id="dac53-120">The project accountant can:</span></span>

  - <span data-ttu-id="dac53-121">转到 **项目管理和会计** > **所有项目** 在 Finance and Operations 应用中查看项目。</span><span class="sxs-lookup"><span data-stu-id="dac53-121">Review projects in Finance and Operations apps by going to **Project management and accounting** > **All projects**.</span></span> 
  - <span data-ttu-id="dac53-122">转到 **项目管理和会计** > **所有项目** > **设置** > **显示默认会计**，更新 Finance and Operations 应用中项目的会计属性。</span><span class="sxs-lookup"><span data-stu-id="dac53-122">Update accounting attributes for the project in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Set up** > **Show default accounting**.</span></span>  
  - <span data-ttu-id="dac53-123">通过在 Finance and Operations 应用中选择项目 ID（将在 Dataverse 中打开相关的项目记录）查看运营项目属性，如估计开始和结束日期。</span><span class="sxs-lookup"><span data-stu-id="dac53-123">Review operational project attributes, such as estimated start and end dates, by selecting the project ID in Finance and Operations apps which opens the related project record in Dataverse.</span></span>

<span data-ttu-id="dac53-124">项目通过 **项目合同子项** 实体与项目合同关联。</span><span class="sxs-lookup"><span data-stu-id="dac53-124">A project is associated with a project contract through the **Project contract line** entity.</span></span>

<span data-ttu-id="dac53-125">Dataverse 中的项目合同子项使用 **项目合同子项(salesorderdetails)** 表映射在 Finance and Operations 应用中创建项目合同记帐规则。</span><span class="sxs-lookup"><span data-stu-id="dac53-125">Project contract lines in Dataverse creates a project contract billing rule in Finance and Operations apps using the **Project contract lines (salesorderdetails)** table map.</span></span> <span data-ttu-id="dac53-126">记帐方法在 Finance and Operations 应用中定义项目合同记帐规则类型：</span><span class="sxs-lookup"><span data-stu-id="dac53-126">The billing method defines the project contract billing rule type in Finance and Operations apps:</span></span>

  - <span data-ttu-id="dac53-127">使用时间和材料记帐方法的项目合同子项创建时间和材料类型的记帐规则。</span><span class="sxs-lookup"><span data-stu-id="dac53-127">Project contract lines with a billing method of time and material create a billing rule of time and material type.</span></span>
  - <span data-ttu-id="dac53-128">固定价格记帐方法合同子项创建里程碑记帐规则。</span><span class="sxs-lookup"><span data-stu-id="dac53-128">Fixed price billing method contract lines create a milestone billing rule.</span></span>

<span data-ttu-id="dac53-129">项目会计可以通过转到 **项目管理和会计** > **项目合同** > **设置** > **显示默认会计**，在 **合同子项** 选项卡上查看详细信息，来在 Finance and Operations 应用中查看项目合同子项。会计还可以在此选项卡上为固定价格记帐方法合同子项设置默认财务维度。</span><span class="sxs-lookup"><span data-stu-id="dac53-129">Project contract lines can be reviewed by the project accountant in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**, and reviewing the details on the **Contract lines** tab. The accountant can also set default financial dimensions for the fixed price billing method contract lines on this tab.</span></span>

## <a name="billing-milestones"></a><span data-ttu-id="dac53-130">记帐里程碑</span><span class="sxs-lookup"><span data-stu-id="dac53-130">Billing milestones</span></span>

<span data-ttu-id="dac53-131">使用固定价格记帐方法的项目合同子项通过记帐里程碑来开票。</span><span class="sxs-lookup"><span data-stu-id="dac53-131">Project contract lines using the fixed price billing method are invoiced through billing milestones.</span></span> <span data-ttu-id="dac53-132">记帐里程碑使用 **Project Operations 集成合同子项里程碑(msdyn\_contractlinescheduleofvalues)** 表映射同步到 Finance and Operations 应用中的项目帐户内交易。</span><span class="sxs-lookup"><span data-stu-id="dac53-132">Billing milestones are synchronized to project on-account transactions in Finance and Operations apps by using the **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** table map.</span></span>

  ![记帐里程碑集成](./media/2Milestones.jpg)

<span data-ttu-id="dac53-134">会计可以转到 **项目管理和会计** > **项目合同** > **维护** > **帐户内交易** 或 **项目管理和会计** > **所有项目** > **维护** > **帐户内交易**，查看帐户内交易并调整这些交易的会计属性。</span><span class="sxs-lookup"><span data-stu-id="dac53-134">The accountant can review on-account transactions and adjust the accounting attributes for those transactions by going to **Project management and accounting** > **Project contracts** > **Maintain** > **On-account transactions** or **Project management and accounting** > **All projects** > **Maintain** > **On-account transactions**.</span></span>

<span data-ttu-id="dac53-135">当您首次为给定项目合同子项创建记帐里程碑时，系统会自动为与此合同子项关联的项目创建固定价格收入估算项目。</span><span class="sxs-lookup"><span data-stu-id="dac53-135">When you first create a billing milestone for a given project contract line, the system automatically creates a fixed price revenue estimate project for the project associated with this contract line.</span></span> <span data-ttu-id="dac53-136">固定价格收入估算项目可以转到 **项目管理和会计** > **固定价格收入估算项目** 查看。</span><span class="sxs-lookup"><span data-stu-id="dac53-136">Fixed-price revenue estimate projects can be reviewed by going to **Project management and accounting** > **Fixed-price revenue estimate projects**.</span></span>

### <a name="project-tasks"></a><span data-ttu-id="dac53-137">项目任务</span><span class="sxs-lookup"><span data-stu-id="dac53-137">Project tasks</span></span>

<span data-ttu-id="dac53-138">项目任务通过 **项目任务(msdyn\_projecttasks)** 表映射同步到 Finance and Operations 应用，同步后仅用于引用目的。</span><span class="sxs-lookup"><span data-stu-id="dac53-138">Project tasks are synchronized to Finance and Operations apps through the **Project tasks (msdyn\_projecttasks)** table map for reference purposes only.</span></span> <span data-ttu-id="dac53-139">不支持通过 Finance and Operations 应用创建、更新和删除操作。</span><span class="sxs-lookup"><span data-stu-id="dac53-139">Creating, updating, and deleting operations isn't supported through Finance and Operations apps.</span></span>

  ![项目任务集成](./media/3Tasks.jpg)

## <a name="project-resources"></a><span data-ttu-id="dac53-141">项目资源</span><span class="sxs-lookup"><span data-stu-id="dac53-141">Project resources</span></span>

<span data-ttu-id="dac53-142">**项目资源角色** 实体使用 **所有公司的项目资源角色(bookableresourcecategories)** 表映射同步到 Finance and Operations 应用，同步后仅用于引用目的。</span><span class="sxs-lookup"><span data-stu-id="dac53-142">The **Project resource roles** entity is synchronized to Finance and Operations apps using the **Project resource roles for all companies (bookableresourcecategories)** table map for reference purposes only.</span></span> <span data-ttu-id="dac53-143">由于 Dataverse 中的资源角色不是特定于公司的，因此系统会自动为双重写入集成范围内包含的所有法人在 Finance and Operations 应用中创建各自的公司特定的资源角色记录。</span><span class="sxs-lookup"><span data-stu-id="dac53-143">Because resource roles in Dataverse are not company-specific, the system automatically creates respective company-specific resource roles records in Finance and Operations apps automatically for all legal entities included into dual-write integration scope.</span></span>

![资源角色集成](./media/5Resources.jpg)

<span data-ttu-id="dac53-145">Project Operations 中的项目资源在 Dataverse 中维护，不同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="dac53-145">Project resources in Project Operations are maintained in Dataverse and aren't synchronized to Finance and Operations apps.</span></span>

### <a name="transaction-categories"></a><span data-ttu-id="dac53-146">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="dac53-146">Transaction categories</span></span>

<span data-ttu-id="dac53-147">交易类别在 Dataverse 中维护，并使用 **项目交易类别(msdyn\_transactioncategories)** 表映射同步到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="dac53-147">Transaction categories are maintained in Dataverse and synchronized to Finance and Operations apps using the **Project transaction categories (msdyn\_transactioncategories)** table map.</span></span> <span data-ttu-id="dac53-148">交易类别记录同步后，系统将自动创建四个共享类别记录。</span><span class="sxs-lookup"><span data-stu-id="dac53-148">After the transaction category record is synchronized, the system automatically creates four shared category records.</span></span> <span data-ttu-id="dac53-149">每个记录对应于 Finance and Operations 应用中的交易类型，并将它们链接到交易类别记录。</span><span class="sxs-lookup"><span data-stu-id="dac53-149">Each record corresponds to a transaction type in Finance and Operations apps and links them to the transaction category record.</span></span>

![交易类别集成](./media/4TransactionCategories.jpg)

<span data-ttu-id="dac53-151">为估计值和实际值使用交易类别需要项目会计或系统管理员在每个法人中创建相应的项目类别。</span><span class="sxs-lookup"><span data-stu-id="dac53-151">Using transaction categories for estimates and actuals requires the project accountant or system administrator to create corresponding project categories in every legal entity.</span></span> <span data-ttu-id="dac53-152">有关详细信息，请参阅[配置项目类别](../project-accounting/configure-project-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="dac53-152">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md).</span></span>
