---
title: Project Service Automation V3 更新版本 17 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 17 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072560"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="833a9-103">Project Service Automation V3 更新版本 17</span><span class="sxs-lookup"><span data-stu-id="833a9-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="833a9-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="833a9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="833a9-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="833a9-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="833a9-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="833a9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="833a9-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="833a9-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="833a9-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="833a9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="833a9-109">本主题列出了 PSA V3 更新版本 17 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="833a9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="833a9-110">该版本的内部版本号为 V3.10.6.34，并且在 2020 年 3 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="833a9-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="833a9-111">更新发布 17</span><span class="sxs-lookup"><span data-stu-id="833a9-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="833a9-112">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="833a9-112">Bug fixes</span></span>

<span data-ttu-id="833a9-113">**常规**</span><span class="sxs-lookup"><span data-stu-id="833a9-113">**General**</span></span>

- <span data-ttu-id="833a9-114">已修复：更新 Project Service Automation 以强制使用 Team Member 许可证（项目资源中心将包括 Team Member Service 计划元数据 3.x）</span><span class="sxs-lookup"><span data-stu-id="833a9-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="833a9-115">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="833a9-115">**Time and Expense**</span></span>

- <span data-ttu-id="833a9-116">已修复：不能将支出估计值从非零价格更改为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="833a9-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="833a9-117">该更改被忽略。</span><span class="sxs-lookup"><span data-stu-id="833a9-117">The change is ignored.</span></span>

<span data-ttu-id="833a9-118">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="833a9-118">**Project Management**</span></span>

- <span data-ttu-id="833a9-119">已修复：已为团队成员的职位名称添加了 null 值检查功能。</span><span class="sxs-lookup"><span data-stu-id="833a9-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="833a9-120">已修复： **msdyn_resourceassignment** 实体的 **msdyn_userresourceid** 字段已被弃用。</span><span class="sxs-lookup"><span data-stu-id="833a9-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="833a9-121">已修复：从 2.x 升级到 3.x，现在可针对任务分配处理空工作量等值线。</span><span class="sxs-lookup"><span data-stu-id="833a9-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="833a9-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="833a9-122">**Sales**</span></span>

- <span data-ttu-id="833a9-123">已修复： **Invoice.PreValidateInvoiceUpdate** 现在可以正确处理重新分派记录负责人的方案。</span><span class="sxs-lookup"><span data-stu-id="833a9-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="833a9-124">已修复：当交易分类是 **时间** 时，对于所有实体（包括 **QuoteLineDetails** 、 **JournalLine** 、 **InvoiceLineDetail** 和 **ContractLineDetails** ）， **UnitGroup** 均不可编辑。</span><span class="sxs-lookup"><span data-stu-id="833a9-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="833a9-125">但是， **单位** 仅对 **JournalLine** 和 **InvoiceLineDetails** 不可编辑。</span><span class="sxs-lookup"><span data-stu-id="833a9-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


