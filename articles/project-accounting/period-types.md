---
title: 期间类型
description: 本主题提供有关如何为收入估算设置期间类型的信息。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531371"
---
# <a name="period-types"></a><span data-ttu-id="bf6a1-103">期间类型</span><span class="sxs-lookup"><span data-stu-id="bf6a1-103">Period types</span></span>

<span data-ttu-id="bf6a1-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bf6a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bf6a1-105">期间类型定义项目收入的估计频率。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="bf6a1-106">本主题提供有关如何为收入估算设置期间类型的信息。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="bf6a1-107">创建和使用期间类型</span><span class="sxs-lookup"><span data-stu-id="bf6a1-107">Create and work with period types</span></span>
<span data-ttu-id="bf6a1-108">若要创建和使用期间类型，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bf6a1-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="bf6a1-109">在您的 Dynamics 365 Finance 环境中，转到 **项目管理和会计** > **设置** > **估计** > **期间类型**。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="bf6a1-110">选择 **新建** 以创建新期间类型。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-110">Select **New** to create new period type.</span></span> <span data-ttu-id="bf6a1-111">输入名称和说明。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-111">Enter a name and description.</span></span>
3. <span data-ttu-id="bf6a1-112">在 **频率** 字段中选择值：</span><span class="sxs-lookup"><span data-stu-id="bf6a1-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="bf6a1-113">如果选择 **周**、**双周**、**半月**、**月**、**日**、**季度** 或 **年**，则日历将用于生成期间。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="bf6a1-114">如果选择 **分类帐期间**，则总帐配置中的分类帐期间将用于生成期间。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="bf6a1-115">如果选择 **无限**，则可以指定自定义期间。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="bf6a1-116">选择期间类型记录，然后选择 **生成期间** 以为期间类型创建期间。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="bf6a1-117">根据所选的期间频率，您可以选择指定开始日期或要生成期间数。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="bf6a1-118">选择 **期间** 以查看生成的期间。</span><span class="sxs-lookup"><span data-stu-id="bf6a1-118">Select **Periods** to review generated periods.</span></span>

