---
title: Project Service Automation V3 更新版本 13 中的新增功能或更改
description: 本主题介绍 Project Service Automation V3 更新版本 13 中的新增功能。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121612"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="8067d-103">Project Service Automation V3 更新版本 13</span><span class="sxs-lookup"><span data-stu-id="8067d-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="8067d-104">我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。</span><span class="sxs-lookup"><span data-stu-id="8067d-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="8067d-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="8067d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8067d-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="8067d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8067d-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="8067d-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="8067d-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="8067d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8067d-109">本主题列出了 Project Service Automation V3 更新版本 13 中新增或更改的功能和修补。</span><span class="sxs-lookup"><span data-stu-id="8067d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="8067d-110">此版本的内部版本号为 V3.10.3.18，并且按以下计划提供：</span><span class="sxs-lookup"><span data-stu-id="8067d-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="8067d-111">**公开发布（自行更新）：** 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8067d-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="8067d-112">**自动更新：** 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="8067d-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="8067d-113">更新发布 13</span><span class="sxs-lookup"><span data-stu-id="8067d-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="8067d-114">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="8067d-114">Bug fixes</span></span>

- <span data-ttu-id="8067d-115">时间和支出</span><span class="sxs-lookup"><span data-stu-id="8067d-115">Time and Expense</span></span>

     - <span data-ttu-id="8067d-116">已修复：按支出用途搜索时，**支出审批** 页面上的搜索功能不起作用。</span><span class="sxs-lookup"><span data-stu-id="8067d-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="8067d-117">资源管理</span><span class="sxs-lookup"><span data-stu-id="8067d-117">Resource Management</span></span>

     - <span data-ttu-id="8067d-118">已修复：已将协调中的数字更新为右对齐。</span><span class="sxs-lookup"><span data-stu-id="8067d-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="8067d-119">已修复：无法通过 **计划** 选项卡将指定的资源分派给任务。</span><span class="sxs-lookup"><span data-stu-id="8067d-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="8067d-120">项目管理</span><span class="sxs-lookup"><span data-stu-id="8067d-120">Project Management</span></span>

     - <span data-ttu-id="8067d-121">已修复：当 **TransactionType** 缺少 **Unit** 和 **DefaultGroup** 的设置信息时，分配团队成员期间会出现空引用异常。</span><span class="sxs-lookup"><span data-stu-id="8067d-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="8067d-122">Sales</span><span class="sxs-lookup"><span data-stu-id="8067d-122">Sales</span></span>

     - <span data-ttu-id="8067d-123">已修复：创建角色价格记录时，重复的交易类型记录会返回错误。</span><span class="sxs-lookup"><span data-stu-id="8067d-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="8067d-124">已修复：商机、报价单、订单产品和基于项目的明细子网格中可以看到额外的 **新建商机**、**报价单**、**订单明细** 和 **添加产品** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8067d-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


