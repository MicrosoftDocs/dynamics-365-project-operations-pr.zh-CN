---
title: 注册获取面向资源/非库存场景的 Project Operations 的预览订阅
description: 此主题提供有关如何订阅和部署面向资源/非库存场景的 Project Operations。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121117"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="0a3dd-103">注册获取面向资源/非库存场景的 Project Operations 的预览订阅</span><span class="sxs-lookup"><span data-stu-id="0a3dd-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="0a3dd-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0a3dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0a3dd-105">此主题说明如何订阅预览/合作伙伴产品/服务以及如何部署面向资源/非库存场景的 Project Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0a3dd-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="0a3dd-106">Prerequisites</span></span>

- <span data-ttu-id="0a3dd-107">您将收到一封电子邮件，邀请您参加预览。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="0a3dd-108">您可以在 [Project Operations 网站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上申请预览。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="0a3dd-109">部署预览的用户必须具有 Azure 租户全局管理员权限。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="0a3dd-110">部署 Finance 环境需要按环境计费有效的 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="0a3dd-111">您可以使用组织现有订阅或使用 [Azure 试用](https://azure.microsoft.com/en-us/free/)开始。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="0a3dd-112">CDS 环境将在 30 天内免费提供。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="0a3dd-113">订阅</span><span class="sxs-lookup"><span data-stu-id="0a3dd-113">Subscribe</span></span>

<span data-ttu-id="0a3dd-114">当您的[预览申请](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)获得批准时，您将通过电子邮件收到 Microsoft 的三项服务。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="0a3dd-115">这些服务让您可以部署 Project Operations 预览：</span><span class="sxs-lookup"><span data-stu-id="0a3dd-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="0a3dd-116">Dynamics 365 Project Operations (CRM) - 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="0a3dd-117">Office 365 Project Operations - 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="0a3dd-118">Dynamics 365 Finance - 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a3dd-119">组织中只有一个人（租户管理员）需要执行此任务。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="0a3dd-120">如果您不是此版本的订阅者，请等待您的组织注册完毕并且您收到用户凭据。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="0a3dd-121">Dynamics 365 Project Operations (CRM) - 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="0a3dd-122">在开始之前，请确保已使用需要 Project Operations 预览的租户中的用户工作帐户登录到浏览器。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="0a3dd-123">通过将服务代码粘贴到浏览器 URL 中来兑换第一个服务代码 **Dynamics 365 Project Operations (CRM) - 预览试用**。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![兑换服务](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="0a3dd-125">确认您的订单。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-125">Confirm your order.</span></span>

![确认订单](./media/17ConfirmOrderNew.png)

<span data-ttu-id="0a3dd-127">您将看到服务已成功兑换的确认。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-127">You will see confirmation offer was successfully redeemed.</span></span>

![确认](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="0a3dd-129">Office 365 Project Operations - 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="0a3dd-130">重复与第一个服务代码相同的步骤。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="0a3dd-131">确保使用与第一个服务代码使用的相同用户帐户添加第二个服务代码。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="0a3dd-132">Dynamics 365 Finance 预览试用</span><span class="sxs-lookup"><span data-stu-id="0a3dd-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="0a3dd-133">对欢迎电子邮件中的最后一个服务重复相同步骤。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="0a3dd-134">分配许可证</span><span class="sxs-lookup"><span data-stu-id="0a3dd-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a3dd-135">您需要组织的 Microsoft 365 门户的管理访问权限才能完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="0a3dd-136">转到 [Microsoft 365 管理中心](https://portal.office.com/)，向您的用户分配许可证。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![管理中心主页](./media/14AdminPortal.png)

2. <span data-ttu-id="0a3dd-138">在 **活动用户** 页上，选择要为其分配许可证的用户。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![分配许可证](./media/15AssignLicenses.png)

3. <span data-ttu-id="0a3dd-140">确认已选择 **Dynamics 365 Project Operations (CRM) 预览** 和 **Office 365 Project Operations - 预览** 许可证，然后选择 **保存更改**。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="0a3dd-141">Finance 试用服务不需要分配给用户。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="0a3dd-142">在 LCS 中启动新项目</span><span class="sxs-lookup"><span data-stu-id="0a3dd-142">Start a new project in LCS</span></span>

<span data-ttu-id="0a3dd-143">按照主题[在 LCS 中启动新项目](create-lcs-project.md)中所述创建新的 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="0a3dd-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="0a3dd-144">将 Azure 订阅添加到 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="0a3dd-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="0a3dd-145">若要完成此任务，请按照主题[将 Azure 订阅添加到 LCS 项目](resource-add-azure-subscription-lcs-project.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="0a3dd-146">使用面向资源/非库存场景的 Project Operations 部署 Finance 演示环境</span><span class="sxs-lookup"><span data-stu-id="0a3dd-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="0a3dd-147">按照主题[设置新环境](resource-provision-new-environment.md)中的指导完成部署。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="0a3dd-148">使用[演示环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署类型进行预览。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="0a3dd-149">安装 CDS 设置和配置数据</span><span class="sxs-lookup"><span data-stu-id="0a3dd-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="0a3dd-150">按照主题[在 Common Data Service 中设置和应用配置数据](resource-apply-pro-setup-config-data.md)中所述安装 CDS 设置和配置数据。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="0a3dd-151">应仅在部署了 Finance 演示环境以及 FO 中的演示数据准备就绪后再完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="0a3dd-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>