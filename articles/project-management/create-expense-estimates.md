---
title: 费用估算
description: 此主题提供有关定义或预估基于项目的支出的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072526"
---
# <a name="expense-estimates"></a><span data-ttu-id="5828c-103">费用估算</span><span class="sxs-lookup"><span data-stu-id="5828c-103">Expense estimates</span></span>
<span data-ttu-id="5828c-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="5828c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5828c-105">除了定义基于资源的预估之外，Dynamics 365 Project Operations 还允许项目经理为每个项目定义基于项目的支出。</span><span class="sxs-lookup"><span data-stu-id="5828c-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="5828c-106">每个支出项都可与特定项目任务或支出类别关联。</span><span class="sxs-lookup"><span data-stu-id="5828c-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="5828c-107">支出类别通常在组织级别定义。</span><span class="sxs-lookup"><span data-stu-id="5828c-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="5828c-108">每个支出类别的定价通常在以下层次结构中定义：</span><span class="sxs-lookup"><span data-stu-id="5828c-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="5828c-109">组织</span><span class="sxs-lookup"><span data-stu-id="5828c-109">Organization</span></span>
- <span data-ttu-id="5828c-110">客户</span><span class="sxs-lookup"><span data-stu-id="5828c-110">Customer</span></span>
- <span data-ttu-id="5828c-111">报价单/合同</span><span class="sxs-lookup"><span data-stu-id="5828c-111">Quote/contract</span></span>

<span data-ttu-id="5828c-112">完成以下步骤来查看、添加或删除项目支出。</span><span class="sxs-lookup"><span data-stu-id="5828c-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="5828c-113">转到 **项目** ，然后选择要处理的项目。</span><span class="sxs-lookup"><span data-stu-id="5828c-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="5828c-114">选择 **项目预估** 选项卡，查看项目支出列表。</span><span class="sxs-lookup"><span data-stu-id="5828c-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="5828c-115">选择 **新建支出** 添加支出。</span><span class="sxs-lookup"><span data-stu-id="5828c-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="5828c-116">或者，选择要删除的支出，然后选择 **删除支出** 。</span><span class="sxs-lookup"><span data-stu-id="5828c-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="5828c-117">将为每个支出明细项目定义以下属性：</span><span class="sxs-lookup"><span data-stu-id="5828c-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="5828c-118">**类别** ：用于描述项目中产生的所有支出的常用分组。</span><span class="sxs-lookup"><span data-stu-id="5828c-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="5828c-119">**开始日期** ：预测将产生支出的日期。</span><span class="sxs-lookup"><span data-stu-id="5828c-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="5828c-120">**数量** ：预估的特定类别的支出项目的数量。</span><span class="sxs-lookup"><span data-stu-id="5828c-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="5828c-121">**成本单价** ：用于计算支出成本的单价。</span><span class="sxs-lookup"><span data-stu-id="5828c-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="5828c-122">**销售单价** ：用于计算支出的销售价格的单价。</span><span class="sxs-lookup"><span data-stu-id="5828c-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>
