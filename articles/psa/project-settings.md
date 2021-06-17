---
title: 项目设置
description: 此主题介绍项目管理设置。
author: ruhercul
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
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998310"
---
# <a name="project-settings"></a>项目设置

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

可使用以下设置访问项目规划功能。

## <a name="work-template"></a>工作模板

若要创建项目计划，请创建一个项目日历模板，用于定义每天的工时数和节假日。 若要创建项目日历模板，请将工作模板与项目的 **日历模板** 字段关联。 执行以下步骤创建一个工作模板。

1. 在 PSA 的左侧导航窗格，单击 **资源**。 
2. 在 **资源** 列表页中，打开一条用户记录，然后选择 **显示工时**。

  > [!NOTE]
  > 确保浏览器页中允许弹出窗口。 这样您就可以查看为资源设置的工时。
  
3. 在 **月视图** 选项卡中，单击 **设置**。 将显示三个选项的列表： 

  - 新建周计划
  - 一天的工作计划
  - 休息时间

> ![设置选项](media/project-13.png)

4. 选择 **新建周计划**，然后为此资源计划设置选项。 可设置定期周计划、日工时参数、节假日等。
5. 设置日期范围，选择 **保存**，然后单击 **关闭**。 
6. 回到 **资源** 列表页，然后选择要为其设置工时的资源。 
7. 选择 **日历设置为** 以设置工作模板。 
8. 在 **工作模板** 对话框中，输入工作模板的名称，然后选择 **应用**。 

现在可将此工作模板与项目日历模板关联。

## <a name="resource-roles"></a>资源角色

术语 *资源角色* 指的是要对项目执行一组特定任务的人员必须拥有的一组技能、资格和认证。 可使用 PSA 根据资源关联的角色设置资源时间的成本和记帐。 每个组织必须使用 **Project Service** 菜单左侧导航设置这些角色。

每个组织必须在 **可用的资源类别** 页中设置这些角色。 若要打开此页，请在左侧导航窗格中选择 **资源角色**。

## <a name="price-lists"></a>价目表

可通过价目表设置资源角色、支出类别、产品和组织中的其他元素的成本和销售价。 在为项目设置必须交付的工作的财务估算之前，应创建基础成本和销售价目表。 还应在参数部分中设置应用于组织中创建的每个项目的默认成本和销售价目表。 在 **可用的项目参数** 页中，务必设置默认成本和销售价目表。


[!INCLUDE[footer-include](../includes/footer-banner.md)]