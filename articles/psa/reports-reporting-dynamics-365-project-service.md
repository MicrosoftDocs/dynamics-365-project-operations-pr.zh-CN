---
title: 报表主页
description: 此主题介绍 Dynamics 365 Project Service Automation 中的报表功能。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147687"
---
# <a name="reporting-home-page"></a><span data-ttu-id="e23c6-103">报表主页</span><span class="sxs-lookup"><span data-stu-id="e23c6-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e23c6-104">基于项目的组织可使用 Microsoft Dynamics 365 Project Service Automation 高效管理业务运营。</span><span class="sxs-lookup"><span data-stu-id="e23c6-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="e23c6-105">在任何项目中，团队成员必须管理商机，为工作报价，规划工作，为项目安排资源，根据规划管理工作，为工作记帐，然后执行工作以完成项目。</span><span class="sxs-lookup"><span data-stu-id="e23c6-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="e23c6-106">运营报告能力的关键是确定组织的运行状况和采取必需的纠正措施。</span><span class="sxs-lookup"><span data-stu-id="e23c6-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="e23c6-107">PSA 对所有报告使用 Microsoft Dynamics 365 报表方法和技术。</span><span class="sxs-lookup"><span data-stu-id="e23c6-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="e23c6-108">有关报告选项的详细信息，请参阅 [Dynamics 365 Customer Engagement (on-premises) 版本 9 报表编写指南](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365)。</span><span class="sxs-lookup"><span data-stu-id="e23c6-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="e23c6-109">报表向导</span><span class="sxs-lookup"><span data-stu-id="e23c6-109">Report Wizard</span></span>

<span data-ttu-id="e23c6-110">非开发人员可使用报表向导创建简单报表。</span><span class="sxs-lookup"><span data-stu-id="e23c6-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="e23c6-111">由于此应用程序基于现有平台，所以其体验与[使用报表向导创建或编辑报表](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard)中介绍的体验相同。</span><span class="sxs-lookup"><span data-stu-id="e23c6-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="e23c6-112">但是，您将使用 Project Service Automation 的专有实体。</span><span class="sxs-lookup"><span data-stu-id="e23c6-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="e23c6-113">自定义的 SQL Server Reporting Services 报表</span><span class="sxs-lookup"><span data-stu-id="e23c6-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="e23c6-114">如果您的业务需要不能通过使用报表向导创建的特定报表，可创建自定义报表。</span><span class="sxs-lookup"><span data-stu-id="e23c6-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="e23c6-115">必须安装 Microsoft Visual Studio，以及相应的 Microsoft SQL Server Data Tools 和 Report Authoring Extensions。</span><span class="sxs-lookup"><span data-stu-id="e23c6-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="e23c6-116">有关工具和版本的详细信息，请参阅[使用 SQL Server Data Tools 的报表编写环境](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools)。</span><span class="sxs-lookup"><span data-stu-id="e23c6-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="e23c6-117">有关如何创建自定义报表的信息，请参阅[使用 SQL Server Data Tools 创建新报表](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)。</span><span class="sxs-lookup"><span data-stu-id="e23c6-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="e23c6-118">Power BI 见解应用程序</span><span class="sxs-lookup"><span data-stu-id="e23c6-118">Power BI insights apps</span></span>

<span data-ttu-id="e23c6-119">Microsoft Power BI 和 Dynamics 365 一起以见解应用程序的形式让您可以妥善处理数据。</span><span class="sxs-lookup"><span data-stu-id="e23c6-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="e23c6-120">有关见解应用程序可用性的信息，请参阅 [Power BI见解应用程序页](https://powerbi.microsoft.com/power-bi-insights-apps/)。</span><span class="sxs-lookup"><span data-stu-id="e23c6-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="e23c6-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="e23c6-121">Additional resources</span></span>
<span data-ttu-id="e23c6-122">有关 PSA 中的报表功能的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="e23c6-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="e23c6-123">使用 Project Service 数据模型</span><span class="sxs-lookup"><span data-stu-id="e23c6-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="e23c6-124">仪表板</span><span class="sxs-lookup"><span data-stu-id="e23c6-124">Dashboards</span></span>](reports-dashboards.md)

