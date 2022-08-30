---
title: 同步项目状态以阻止进入已关闭的项目
description: 本文介绍如何同步项目状态以阻止进入停用或已关闭的项目。
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2022
ms.locfileid: "9347997"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>同步项目状态以阻止进入已关闭的项目

_**适用于：** 面向资源/非库存场景的 Project Operations_

## <a name="scenario"></a>场景

Contoso 与 Microsoft Dynamics 365 Project Operations 一起上线，用于资源/非库存场景。 作为常规业务活动的一部分，项目可能会完成或暂停。 您可以停用项目以确保不会产生费用或生成发票。

## <a name="solution"></a>解决方案

### <a name="prerequisites"></a>先决条件

-   必须安装 Microsoft Dynamics 365 Finance 10.0.29 或更高版本。
-   必须安装或手动配置 Projects V2 (msdyn\_projects) 的双重写入映射 1.0.0.3，如下所述。

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>创建 Project Operations 集成项目 V2 双重写入映射的更新版本

要更新 Project Operations 项目 V2 双重写入映射：

1. 转到 **数据管理** 工作区，选择 **双重写入**。
2. 选择 **双重写入** 磁贴。
3. 从 **表映射** 列，找到并选择 **项目 V2 (msdyn\_projects)**，然后选择“停止”。
4. 选择映射名称打开映射，然后选择 **[无]**。
5. 在“选择列”对话框中，选择 **statecode \[项目状态\]**，然后选择“确定”。 您可以在筛选器值中键入 **state** 来缩小列表范围。
6.  在 **映射类型** 列中选择 **添加或编辑转换** 对转换进行编辑。
7.  从 **转换类型**，选择 **ValueMap**。
8.  选择 **添加值映射**，然后添加以下 **键** 和 **值**：

   键       | 值 
   ----------|-------
   InProcess | 12     
   已完成 | 1     

![显示双重写入映射的屏幕截图](media/projectstage-dw-mapping.png)

9. 选择 **保存**。
10. 从 **双重写入 > 项目 V2 (msdyn_projects)** 页面的顶部，选择 **另存为**。
11. 在 **发布者** 字段的 **添加表** 中，选择 **CDS 默认发布者**。
12. 将 **版本** 字段设置为 1.0.0.3。
13. 键入 **说明**，然后选择 **保存**。
14. 从 **双重写入 > 项目 V2 (msdyn_projects)** 页面的顶部，选择 **运行** 开始映射，然后在要求在运行前确认时选择 **是**。 

### <a name="close-a-newly-completed-project"></a>关闭新完成的项目

Dynamics 365 Finance 使用 **项目阶段** 字段来区分项目 **正在进行** 还是 **已完成**。 **已完成** 项目无法产生费用或向客户开具发票。

1. 打开要停用的项目。
2. 在功能区中选择 **停用**。

> [!NOTE]
> 您可以停用或关闭项目，因为它们在 Finance 上下文中的行为相同。

3. 在 Finance 中，打开 **所有项目列表** 页。
4. 确认已停用项目没有显示在列表中。
5. 在列表上方的 **显示项目** 筛选器中，将值从 **可用** 更改为 **所有**。
6. 您现在将看到已停用的项目。

如果您尝试在 Finance 中记录此项目的时间或费用，应该不会看到可供选择的项目。 如果您在费用中手动输入项目编号，您会看到类似“已完成的项目阶段不允许在项目中有记录”的消息。 应禁用开票和其他账单功能，因为它们将在已关闭项目的上下文中。

