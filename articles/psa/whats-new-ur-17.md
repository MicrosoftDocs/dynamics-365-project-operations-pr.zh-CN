---
title: Project Service Automation V3 更新版本 17 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 17 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143689"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="4c9b5-103">Project Service Automation V3 更新版本 17</span><span class="sxs-lookup"><span data-stu-id="4c9b5-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4c9b5-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4c9b5-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="4c9b5-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4c9b5-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="4c9b5-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4c9b5-109">本主题列出了 PSA V3 更新版本 17 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="4c9b5-110">该版本的内部版本号为 V3.10.6.34，并且在 2020 年 3 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="4c9b5-111">更新发布 17</span><span class="sxs-lookup"><span data-stu-id="4c9b5-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4c9b5-112">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="4c9b5-112">Bug fixes</span></span>

<span data-ttu-id="4c9b5-113">**常规**</span><span class="sxs-lookup"><span data-stu-id="4c9b5-113">**General**</span></span>

- <span data-ttu-id="4c9b5-114">已修复：更新 Project Service Automation 以强制使用 Team Member 许可证（项目资源中心将包括 Team Member Service 计划元数据 3.x）</span><span class="sxs-lookup"><span data-stu-id="4c9b5-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="4c9b5-115">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="4c9b5-115">**Time and Expense**</span></span>

- <span data-ttu-id="4c9b5-116">已修复：不能将支出估计值从非零价格更改为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="4c9b5-117">该更改被忽略。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-117">The change is ignored.</span></span>

<span data-ttu-id="4c9b5-118">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="4c9b5-118">**Project Management**</span></span>

- <span data-ttu-id="4c9b5-119">已修复：已为团队成员的职位名称添加了 null 值检查功能。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="4c9b5-120">已修复：**msdyn_resourceassignment** 实体的 **msdyn_userresourceid** 字段已被弃用。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="4c9b5-121">已修复：从 2.x 升级到 3.x，现在可针对任务分配处理空工作量等值线。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="4c9b5-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4c9b5-122">**Sales**</span></span>

- <span data-ttu-id="4c9b5-123">已修复：**Invoice.PreValidateInvoiceUpdate** 现在可以正确处理重新分派记录负责人的方案。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="4c9b5-124">已修复：当交易分类是 **时间** 时，对于所有实体（包括 **QuoteLineDetails**、**JournalLine**、**InvoiceLineDetail** 和 **ContractLineDetails**），**UnitGroup** 均不可编辑。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="4c9b5-125">但是，**单位** 仅对 **JournalLine** 和 **InvoiceLineDetails** 不可编辑。</span><span class="sxs-lookup"><span data-stu-id="4c9b5-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


