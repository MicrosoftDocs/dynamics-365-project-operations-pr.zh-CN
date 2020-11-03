---
title: 配置项目类别
description: 此主题提供有关设置项目类别的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072500"
---
# <a name="configure-project-categories"></a>配置项目类别

_**适用于：** 面向资源/非库存场景的 Project Operations_

Project Operations 提供强大的功能，可以对项目的收入和支出进行分类。 类别提供报告和分析项目交易以及推进向总帐过帐的能力。

下图说明了交易类别、共享类别和项目类别之间的相关性。 

交易类别是项目交易的基本分组。 在该分组中，存在一组可以在应用程序和模块之间共享的共享类别。 更深入地讲，项目类别是粒度级别最细的类别。 项目类别特定于法人、模块和应用程序。

![交易类别、共享类别和项目类别之间的相关性](media/project-categories.png)

## <a name="transaction-categories"></a>交易记录类别

交易类别代表项目交易的基本分组，不特定于公司或交易类型。 例如，Contoso Robotics 使用“设计”、“旅行”、“安装”和“服务交易”类别对项目交易进行分组。

交易类别在 Project Operations 模块中定义。 
1. 转到 **设置**\>**交易类别** 打开窗体。 
2. 通过选择 **新建** 或选择 **从 Excel 导入** ，创建一个新交易类别。

## <a name="shared-categories"></a>共享类别

Dynamics 365 使用共享类别概念对不同应用程序中的支出进行分类，如 Dynamics 365 Finance、Dynamics 365 Supply Chain 和 Dynamics 365 Project Operations。 对于创建的每个交易类别，Project Operations 会自动创建四个相关的共享类别：工时、支出、费用和项目。 您可以转到 **项目管理和会计** \> **设置** \> **类别** \> **共享类别** 查看和调整共享类别。

## <a name="project-categories"></a>项目类别

项目类别代表类别配置的最细粒度级别，必须由项目会计单独为每个公司进行配置。

1. 转到 **项目管理和会计** \> **设置** \> **类别** \> **项目类别** 。
2. 选择 **新建** 。
3. 选择在上一节中创建的共享类别的 **类别 ID** 。 Project Operations 仅允许使用与交易类别关联的那些共享类别。
4. 选择类别组。

## <a name="category-groups"></a>类别组

类别组用于在相关项目类别之间共享属性，主要是过帐模板。 每个交易类型必须至少有一个类别组，并且为每个项目类别分配一个组。

Project Operations 中的过帐规范由项目成本和收入模板规则、项目类别以及类别组定义。 您可以转到 **项目管理和会计** \> **设置** \> **类别** \> **类别组** 设置类别组。
