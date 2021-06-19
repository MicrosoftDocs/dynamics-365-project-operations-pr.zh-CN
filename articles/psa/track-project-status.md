---
title: 跟踪项目状态
description: 如何在 Project Service 中跟踪项目状态
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014375"
---
# <a name="track-a-projects-status-project-service"></a>跟踪项目状态 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

使用 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]来跟踪客户端项目的进度。  

作为执行进度，项目阶段更新以反映执行的阶段：  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **新建**    | 创建项目时，该阶段设置为 **新建**。 如果您已从模板创建项目，则在此阶段，项目可能具有计划、估算和团队数据。 否则，它将是项目的概述，您需要手动输入剩余的项目组成部分。 |
|  **报价单**   |      当您将项目关联至报价单或从报价单创建项目时，项目阶段设置为 **报价单**，并且估算的开始和结束日期也会更新。 当项目处于报价单阶段时，有关报价单的详细信息显示在 **项目** 页面上的 **销售** 选项卡上。      |
|   **规划**   |                                     当您获得与项目相关的报价单时，并且当执行进度为合同阶段时，项目阶段更新为 **规划**。 合同详细信息显示在 **项目** 页面上的 **销售** 选项卡上。                                      |
| **完成** |                    项目工作完成后，可将阶段切换为 **完工**。 当项目阶段设置为完工时，可理解工作 100% 完成，但项目保持打开，便于记录任何待定时间或费用条目。                     |
|  **关闭**   |           当所有事务已记录在项目上且不希望再记录任何事务时，可手动将阶段设置为 **关闭**。 当将项目设置为 **结束** 时，将无法在项目上记录任何事务，并且项目是只读的。           |

## <a name="to-track-a-projects-status"></a>跟踪项目状态  

1.  转到 **Project Service > 项目**。  

2.  单击要处理的项目。  

3.  在屏幕顶部横栏中，选择项目名称旁边的向下箭头，然后单击 **项目跟踪**。  

4.  在任务列表上方的下拉列表中选择 **工作量跟踪** 或 **成本跟踪**。  

5.  双击任何任务以进行编辑。 您还可移动甘特图中的条形或调整其大小，以更改任务的时间和进度。  

### <a name="see-also"></a>另请参阅  
 [项目经理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]