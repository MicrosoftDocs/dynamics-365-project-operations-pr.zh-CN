---
title: 卸载 Dynamics 365 Project Operations
description: 本文提供有关如何卸载 Dynamics 365 Project Operations 的信息。
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911953"
---
# <a name="uninstall-dynamics-365-project-operations"></a>卸载 Dynamics 365 Project Operations 

_**适用于：** 面向资源/非库存场景的 Project Operations_

若要卸载 Dynamics 365 Project Operations，您必须分配有管理员角色。

1. 转到 **设置** > **解决方案**。

    ![设置页面。](./media/uninstall-proj-ops-solutions.png)
  
2. 按照下表中列出解决方案的确切顺序删除解决方案。 

    | 步长 | 解决方案   名称                                    | 备注                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | 如果未找到，请跳过此解决方案。                                                            |
    | 2 | ProjectOperations_Anchor                           | 如果未找到，请跳过此解决方案。                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | 如果未找到，请跳过此解决方案。                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | 如果未找到，请跳过此解决方案。                                                            |
    | 5 | ProjectService                                     | 无其他注释。                                                                         |
    | 6 | ProjectServiceCore_Patch                           | 无其他注释。                                                                         |
    | 7 | ProjectServiceCore                                 | 无其他注释。                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | 如果未找到，请跳过此解决方案。                                                            |
    | 9 | FieldServiceCommon                                 | Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的双写入的必需项。   |
    | 10 | msdyn_AssetCommon                                  | Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的双写入的必需项。   |
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
