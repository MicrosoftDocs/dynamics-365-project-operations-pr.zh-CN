---
title: 出差津贴
description: 此主题提供有关在支出管理中使用的出差津贴规则的信息。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128497"
---
# <a name="per-diems"></a><span data-ttu-id="bf57d-103">出差津贴</span><span class="sxs-lookup"><span data-stu-id="bf57d-103">Per diems</span></span>

<span data-ttu-id="bf57d-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bf57d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="bf57d-105">出差津贴是支付给工作中出差的工作人员的津贴。</span><span class="sxs-lookup"><span data-stu-id="bf57d-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="bf57d-106">在“支出管理”中，您可以为各种出差情况创建出差津贴规则。</span><span class="sxs-lookup"><span data-stu-id="bf57d-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="bf57d-107">出差津贴费率可以基于一年的时间、出差地点或这两者。</span><span class="sxs-lookup"><span data-stu-id="bf57d-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="bf57d-108">创建出差津贴规则时，可以指定如果工作人员享受免费餐饮或服务，将扣除的出差津贴费的百分比。</span><span class="sxs-lookup"><span data-stu-id="bf57d-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="bf57d-109">您还可以设置可应用出差津贴费率的工作人员出差的最小和最大时数。</span><span class="sxs-lookup"><span data-stu-id="bf57d-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="bf57d-110">配置</span><span class="sxs-lookup"><span data-stu-id="bf57d-110">Configuration</span></span> 

1. <span data-ttu-id="bf57d-111">若要添加出差津贴地点，请转到 **设置** > **计算和代码** > **出差津贴地点**。</span><span class="sxs-lookup"><span data-stu-id="bf57d-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="bf57d-112">对于上面添加的每个地点，选择在特定开始日期和结束日期之间可用于住宿、餐饮和其他支出的出差津贴费率和货币。</span><span class="sxs-lookup"><span data-stu-id="bf57d-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="bf57d-113">出差津贴费率和货币在 **设置** > **计算和代码** > **出差津贴** 下配置。</span><span class="sxs-lookup"><span data-stu-id="bf57d-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="bf57d-114">在 **出差津贴地点** 页上，配置出差津贴费率层。</span><span class="sxs-lookup"><span data-stu-id="bf57d-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="bf57d-115">出差津贴费率层让您可以定义住宿、餐饮和其他支出的每日津贴的百分比分割。</span><span class="sxs-lookup"><span data-stu-id="bf57d-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="bf57d-116">若要指定早餐、午餐或晚餐的餐费百分比扣减，请更新 **支出管理参数** 页上 **出差津贴** 选项卡上的字段。</span><span class="sxs-lookup"><span data-stu-id="bf57d-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="bf57d-117">使用出差津贴提交支出</span><span class="sxs-lookup"><span data-stu-id="bf57d-117">Submit expenses using per diem</span></span>
<span data-ttu-id="bf57d-118">若要使用出差津贴提交支出，请在创建支出报表时使用 **出差津贴** 支出类别。</span><span class="sxs-lookup"><span data-stu-id="bf57d-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="bf57d-119">输入 **出差津贴起始日期**、**出差津贴截止日期** 和 **出差津贴地点**。</span><span class="sxs-lookup"><span data-stu-id="bf57d-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="bf57d-120">将根据所选地点的出差津贴费率计算金额，根据出差津贴费率层来计算餐费扣减。</span><span class="sxs-lookup"><span data-stu-id="bf57d-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
