---
title: 在 Microsoft Project 中使用 Project Service 加载项规划工作 | MicrosoftDocs
description: 此主题介绍如何在 Microsoft Project Service 中添加、配置和使用 Microsoft Project 加载项。
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749668"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>在 Microsoft Project 中使用 Project Service Automation 加载项规划工作

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 让您可以更轻松地执行项目规划，包括预计。 您可以自定义工作，以便成本、工作和销售值可以非常清晰，因为提交的是最终建议。  

 现在可以在熟悉的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 环境中安装 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 和开展规划工作。 可使用 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 强大的规划和管理功能，然后在 Project Service Automation 中更新您的计划。  

> [!IMPORTANT]
> - 若要使用 SharePoint 文档管理为 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目存储 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件，[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 管理员需要开启文档管理。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [为特定实体启用 SharePoint 文档管理](../admin/enable-sharepoint-document-management-specific-entities.md)  
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 仅兼容 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition。  

## <a name="download-and-install-the-add-in"></a>下载并安装此加载项  
 准备好 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 登录信息。 从 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 连接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时需要此信息。  

1.  从下载中心下载适用于您的 Project Service 支持版本（[V2.X](https://go.microsoft.com/fwlink/?linkid=828268) 或 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)）的加载项。  

2.  单击下载链接。  

3.  下载完成后，单击**是**安装此加载项。  

## <a name="configure-the-add-in"></a>配置加载项  

1. 打开 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并单击 **Project Service** 选项卡。  

2. 单击**连接**。  

3. 输入您的登录信息，然后单击**登录**。  

   现在可以开始使用此加载项。  

## <a name="read-from-a-template"></a>从模板读取  
 从在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中创建并复制到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 的模板读取，以便开始执行项目规划。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [创建项目模板 (Project Service Automation)](../project-service/create-project-template.md)  

1.  在 **Project Service** 选项卡中，单击**读取** > **Project Service Automation Project 模板**。  

2.  从列表中选择一个项目模板，然后单击**打开**。  

    > [!NOTE]
    >  默认情况下，从模板复制到 Project 的任务设置为手动计划的。  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>将 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 角色分派给项目资源  

1.  打开项目，然后单击**任务**功能区。  

2.  单击**甘特图** 菜单，然后选择**资源工作表**。  

3.  在“资源工作表”中，单击**Project Service资源角色**下拉菜单，然后选择一个 Project Service Automation 角色。  

## <a name="staff-your-project-with-resources"></a>为项目安排员工资源  

1.  从“Project Service”选项卡中选择一行，然后单击**查找资源**。  

2.  在**预订资源**屏幕中，选择要用于该项目的资源。  

3.  单击**预订**，然后单击**确定**。  

## <a name="publish-your-project"></a>发布项目  
项目规划完成后，下一步是导入项目并发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

项目将导入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。 将应用定价和团队生成流程。 在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中打开项目可以看到已生成了团队项目预计和工作分解结构。 下表介绍结果的位置：


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **甘特图**   | 导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **工作分解结构**屏幕中。 |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **资源表** |   导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **项目团队成员**屏幕中。   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **使用情况**    |    导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]**项目估算**屏幕中。     |

**导入和发布项目**  
1. 在 **Project Service** 选项卡中，单击**发布** > **新 Project Service Automation Project 项目**。  

2. 在**发布到 Project Service 中的新项目**对话框中，输入**项目名称**，然后选择**客户**。  

3. 或者，选中**将项目计划链接到 Project Service Automation**，将计划的 Project 文件链接到 Project Service Automation。  

4. 单击**发布**。  

   将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 将让 Project 文件成为主文件，并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中将工作分解结构设置为只读。  若要更改项目计划，需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中更改，再作为更新发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

## <a name="edit-a-project-thats-been-imported"></a>编辑已导入的项目  
 可通过两种方法更改已导入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的项目计划：  

- 在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开主文件并编辑。  

- 取消链接文件并直接在 Project Service 中编辑。 默认情况下，从 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 上传的项目已锁定，只能在 Project 中编辑。 若要在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中编辑文件，必须将其取消链接。  

### <a name="edit-in-pn_microsoft_project"></a>在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中编辑  

1. 单击主菜单中的 **Project Service** > **项目**。  

2. 从项目列表打开在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中创建的项目。  

3. 单击功能区中的**在 MS Project 中打开**。 这将在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开链接的主文件。  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>取消链接文件并在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service 中编辑  

1. 单击主菜单中的 **Project Service** > **项目**。  

2. 从项目列表打开在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中创建的项目。  

3. 单击功能区中的**从 MS Project 取消链接**。  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>将 Project 文件上传到 SharePoint 或 Office Groups  
 可以将 Project 文件上传到 SharePoint 并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的“关联的文档”下找到。  需要请管理员为“项目”实体配置并开启 SharePoint 文档管理。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [设置 SharePoint 集成](../admin/set-up-sharepoint-integration.md)  

 如果您安装了 Office Groups，还可以将 Project 文件上传到 [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [使用 Office 365 组与您的同事协作](../basics/collaborate-with-colleagues-using-office-365-groups.md)  

### <a name="upload-a-file-for-sharepoint"></a>为 SharePoint 上载文件  

1. 单击主菜单中的 **Project Service** > **上传**。  

2. 选择**到 Project Service Automation Project 文档**。  

3. 在**启用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**对话框中，选择**是**或**否**。  

   - 如果单击**是**，则可以在 Project Service Automation 中选择**在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**按钮，启动 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并从 SharePoint 文档库加载 Project 文件。  

   - 如果单击**否**，则**在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**按钮的链接无效。  

4. 可以在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中具体 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的**文档**下找到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件。  

### <a name="upload-a-file-for-office-groups"></a>为 Office Groups 上传文件  

1. 单击主菜单中的 **Project Service** > **上传**。  

2. 选择**到 Project Service Automation Project 文档**。  

3. 在**启用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**对话框中，选择**是**或**否**。  

   - 如果单击**是**，则可以在 Project Service Automation 中选择**在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**按钮，启动 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并从 SharePoint 文档库加载 Project 文件。  

   - 如果单击**否**，则**在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开**按钮的链接无效。  

4. 可以在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中具体 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的**文档**下找到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件。  

## <a name="publish--your-project-as-a-template"></a>将项目发布为模板  
 可以通过在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中将项目保存为项目模板来保存项目并重复使用。  在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中，项目模板是可重复使用的项目计划。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [创建项目模板 (Project Service Automation)](../project-service/create-project-template.md)  

1. 在 **Project Service** 选项卡中，单击**发布** > **新 Project Service Automation Project 模板**。  

2. 在**发布到 Project Service 模板中的新项目**对话框中，输入**项目模板名称**。  

3. 也可以选中**将项目计划链接到 Project Service Automation**，将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

4. 单击**发布**。  

将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 将让 Project 文件成为主文件，并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 模板中将工作分解结构设置为只读。  若要更改项目计划，需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中更改，再作为更新发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。

### <a name="see-also"></a>另请参阅  
 [项目经理指南](../project-service/project-manager-guide.md)
