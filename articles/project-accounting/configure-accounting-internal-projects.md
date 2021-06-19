---
title: 配置内部项目会计
description: 此主题提供有关如何在 Project Operations 中为内部项目设置会计实践的信息。
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012845"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="9cd7c-103">配置内部项目会计</span><span class="sxs-lookup"><span data-stu-id="9cd7c-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="9cd7c-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="9cd7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9cd7c-105">内部项目允许公司跟踪与未对客户计费的活动相关的成本。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="9cd7c-106">内部项目的示例包括：</span><span class="sxs-lookup"><span data-stu-id="9cd7c-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="9cd7c-107">开发产品（如移动应用），以及跟踪与开发相关的成本。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="9cd7c-108">管理预售时间和支出。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="9cd7c-109">如果报价单赢单，此预售内部项目以后可以转换为可计费项目。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="9cd7c-110">未与 Dynamics 365 Project Operations 中的合同关联的任何项目都被视为内部项目。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="9cd7c-111">项目成本和收入模板不用于确定项目的会计规则。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="9cd7c-112">内部项目成本始终使用损益原则过帐。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="9cd7c-113">用于过帐的分类帐科目在 **分类帐过帐设置** 页定义。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="9cd7c-114">时间交易通过借记 **成本** 科目并记入 **工资分配** 科目来过帐。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="9cd7c-115">支出交易通过借记 **成本** 科目并记入 **支出的抵销科目** 来过帐。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="9cd7c-116">项目交易过帐通过借记 **成本** 科目和贷记 **成本 - 项目** 科目来实现。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="9cd7c-117">交易过帐到项目后，如果项目与项目合同相关联，系统将冲销所有累计交易并创建新的可计费交易。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="9cd7c-118">可计费交易遵循在各自的项目成本和收入模板中定义的会计规则。</span><span class="sxs-lookup"><span data-stu-id="9cd7c-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
