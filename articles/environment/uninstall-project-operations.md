---
title: 卸载 Dynamics 365 Project Operations
description: 此主题介绍如何卸载 Dynamics 365 Project Operations。
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783632"
---
# <a name="uninstall-dynamics-365-project-operations"></a>卸载 Dynamics 365 Project Operations 

_**适用于：** 面向资源/非库存场景的 Project Operations_

若要卸载 Dynamics 365 Project Operations，您必须分配有管理员角色。

1. 转到 **设置** > **解决方案**。

    ![设置页面。](./media/uninstall-proj-ops-solutions.png)
  
2. 按照下表中列出解决方案的确切顺序删除解决方案。 

    | 步长 | 解决方案   名称                                    | 备注                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 7 | msdyn_ProjectServiceUpgrade_managed.cab            | 如果未找到，请跳过此解决方案。                                                            |
    | 2 | ProjectOperations_Anchor                           | 如果未找到，请跳过此解决方案。                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | 如果未找到，请跳过此解决方案。                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | 如果未找到，请跳过此解决方案。                                                            |
    | 5 | ProjectService                                     | 无其他注释。                                                                         |
    | 6 | ProjectServiceCore_Patch                           | 无其他注释。                                                                         |
    | 7 | ProjectServiceCore                                 | 无其他注释。                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | 如果未找到，请跳过此解决方案。                                                            |
    | 9 | FieldServiceCommon                                 | Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的双写模块的必需项。   |
    | 10 | msdyn_AssetCommon                                  | Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的双写模块的必需项。   |
    | 11 | msdyn_TESA_Anchor                                  | Dynamics 365 Field Service 的必需项。                                                     |
    | 12 | msdyn_TESA_Patch                                   | Dynamics 365 Field Service 的必需项。                                                     |
    | 13 | msdyn_TESA                                         | Dynamics 365 Field Service 的必需项。                                                     |
    | 14 | ResourceSchedulingControls                         | Dynamics 365 Field Service 的必需项。                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Dynamics 365 Field Service 的必需项。                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Dynamics 365 Field Service 的必需项。                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Dynamics 365 Field Service 的必需项。                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | 如果未找到，请跳过此解决方案。                                                            |
    | 19 | Dynamics365Notes                                   | 如果未找到，请跳过此解决方案。                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | 如果未找到，请跳过此解决方案。                                                            |
    | 21 | DualWriteCore                                      | 如果未找到，请跳过此解决方案。                                                            |
    | 22 | Dynamics365AssetManagementApp                      | 如果未找到，请跳过此解决方案。                                                            |
    | 23 | Dynamics365AssetManagement                         | 如果未找到，请跳过此解决方案。                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | 如果未找到，请跳过此解决方案。                                                            |
    | 25 | Dynamics365FinanceExtended                         | 如果未找到，请跳过此解决方案。                                                            |
    | 26 | HCMCommon                                          | 如果未找到，请跳过此解决方案。                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | 如果未找到，请跳过此解决方案。                                                            |
    | 28 | 当事方                                              | 如果未找到，请跳过此解决方案。                                                            |
    | 29 | Dynamics365Company                                 | 如果未找到，请跳过此解决方案。                                                            |
    | 30 | CurrencyExchangeRates                              | 如果未找到，请跳过此解决方案。                                                            |
    | 31 | AssetCommon                                        | 如果未找到，请跳过此解决方案。                                                            |
