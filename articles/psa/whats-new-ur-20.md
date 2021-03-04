---
title: Project Service Automation V3 更新版本 20 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 20 中可用的功能和修复
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147102"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="47f18-103">Project Service Automation V3 更新版本 20</span><span class="sxs-lookup"><span data-stu-id="47f18-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="47f18-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="47f18-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="47f18-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="47f18-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="47f18-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="47f18-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="47f18-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="47f18-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="47f18-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="47f18-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="47f18-109">本主题列出了 Project Service Automation V3 更新版本 20 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="47f18-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="47f18-110">该版本的内部版本号为 V 3.10.31.37，并且在 2020 年 6 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="47f18-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="47f18-111">更新发布 20</span><span class="sxs-lookup"><span data-stu-id="47f18-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="47f18-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="47f18-112">Bug fixes</span></span>

<span data-ttu-id="47f18-113">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="47f18-113">**Project Management**</span></span>

<span data-ttu-id="47f18-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="47f18-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="47f18-115">如果使用需要数小时的分配方法导入项目团队成员，而指定的小时数为零，则会产生不明错误消息。</span><span class="sxs-lookup"><span data-stu-id="47f18-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="47f18-116">如果在项目任务的 **说明** 字段中输入的字符达到了最大数量，用户将收到“不正确”错误。</span><span class="sxs-lookup"><span data-stu-id="47f18-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="47f18-117">如果用户的语言设置设置为日语，**Microsoft Dynamics 365 Project Service Automation 加载项下载** 页面将重定向到英文下载页面。</span><span class="sxs-lookup"><span data-stu-id="47f18-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="47f18-118">发生服务器错误时，**项目** 窗体 **日程安排** 选项卡上的同步标签有时不会消失。</span><span class="sxs-lookup"><span data-stu-id="47f18-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="47f18-119">修改任务，正在向服务器发送冗余任务更新。</span><span class="sxs-lookup"><span data-stu-id="47f18-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="47f18-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="47f18-120">**Sales**</span></span>

<span data-ttu-id="47f18-121">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="47f18-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="47f18-122">在 **合同** 窗体中，双击 **创建发票** 会为一条实际值记录创建两张发票。</span><span class="sxs-lookup"><span data-stu-id="47f18-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="47f18-123">在 Internet Explorer 11 中，用户不能创建支出条目。</span><span class="sxs-lookup"><span data-stu-id="47f18-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="47f18-124">成本冲销和未记帐实际销售值冲销不链接。</span><span class="sxs-lookup"><span data-stu-id="47f18-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="47f18-125">**项目** 窗体上的 **刷新实际值** 按钮不刷新 **任务实际工时**。</span><span class="sxs-lookup"><span data-stu-id="47f18-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="47f18-126">当 **msdyn_isgenericresourceprojectscoped** 设置为 **False** 时，**PreValidateProjectTeamMemberCreate** 创建可以创建重复的通用可预订资源。</span><span class="sxs-lookup"><span data-stu-id="47f18-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="47f18-127">**重新计算** 将清除基于产品的报价单明细详细信息和合同子项详细信息的应计成本。</span><span class="sxs-lookup"><span data-stu-id="47f18-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="47f18-128">在特定情况下，**PostEstimateLineUpdate** 插件显示空引用异常错误。</span><span class="sxs-lookup"><span data-stu-id="47f18-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="47f18-129">**利润率分析图表** 中的时间分段持续时间与报价单中固定价格报价单明细详细信息中的成本持续时间不匹配。</span><span class="sxs-lookup"><span data-stu-id="47f18-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="47f18-130">为 **合同子项详细信息** 和 **报价单明细详细信息** 窗体中的费用类别设置的计价单位和计价单位组的值不正确。</span><span class="sxs-lookup"><span data-stu-id="47f18-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="47f18-131">**部门成本费** 列表允许时效重叠。</span><span class="sxs-lookup"><span data-stu-id="47f18-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="47f18-132">当订单类型不基于工作时，不允许用户更改 **部门**，因为这将导致空引用异常错误。</span><span class="sxs-lookup"><span data-stu-id="47f18-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="47f18-133">尝试离开 **报价单明细详细信息** 窗体回到 **报价单** 选项卡时，窗体将刷新并显示 **摘要** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="47f18-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
