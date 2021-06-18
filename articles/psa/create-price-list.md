---
title: 创建价目表
description: 如何在 Project Service 中创建价目表
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32f0cc66d1caa08bd24eb232338444df0388de3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006050"
---
# <a name="create-a-price-list-project-service"></a>创建价目表 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

价目表提供模板，供帐户管理员用于创建报价单和项目及确立项目的成本。 价目表提供角色和费用的明细项目列表以及您对每项收取的价格。 您可创建多个价目表，针对不同的销售地区或销售渠道维护单独的价格结构。 最好为要向客户收取的每种货币至少创建一个价目表。  
  
要为将交付的工作创建财务预算，请确保每个项目都有所依托的成本和销售价目表。 设置应用于组织中创建的所有项目的默认成本和销售价目表。  
  
价目表依赖角色和费用类别，所以创建价目表之前，确保您已配置了要在创建价目表时使用的角色和费用类别。  
  
1.  转到 **Project Service > 价目表**。  
  
2.  单击 **新建**。  
  
3.  在 **上下文** 中，选择此价目表针对 **成本**、**采购** 还是 **销售**。  
  
4.  在 **名称** 中，输入价目表的名称。  
  
5.  在 **货币** 中，选择记帐或成本所用货币。  
  
6.  在 **时间单位** 中，指定价格适用于的时间段（如天还是小时）  
  
7.  根据需要填写 **开始日期**、**结束日期** 和 **说明**。  
  
8.  单击 **保存** 创建记录，以便继续编辑。  
  
9. 要向价目表添加角色价格，单击 **角色价格** 下的 **+**。  
  
10. 在 **角色价格** 窗格中，填写详细信息，然后单击 **保存**。 根据需要继续添加角色价格。 完成后，请单击屏幕右下角的 **保存**。  
  
11. 要向价目表添加费用类别价格，单击 **类别价格** 下的 **+**。  
  
12. 在 **交易类别价格** 窗格中，填写详细信息，然后单击 **保存**。 根据需要继续添加类别价格。 完成后，请单击屏幕右下角的 **保存**。  
  
13. 要向价目表添加价目表项，单击 **价目表项** 下的 **+**。  
  
14. 在 **价目表项** 窗格中，填写详细信息，然后单击 **保存**。 根据需要继续添加价目表项。 完成后，请单击屏幕右下角的 **保存**。  
  
15. 要向价目表添加区域关系，单击 **区域关系** 下的 **+**。  
  
16. 在 **新建连接** 窗口中，填写详细信息，然后单击 **保存**。 根据需要继续添加区域关系。 完成后，请单击屏幕右下角的 **保存**。  
  
### <a name="see-also"></a>另请参阅  
 [配置 Project Service Automation](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]