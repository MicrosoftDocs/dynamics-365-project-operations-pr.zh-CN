---
title: 安全模型
description: 本主题提供有关 Dynamics 365 Project Operations 中的安全模型的信息。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072489"
---
# <a name="security-model"></a>安全模型

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Microsoft Dynamics 365 Project Operations 包含一个独特的安全模型，该模型允许使用与 Microsoft Office 组协作的基于角色的业务安全模型。 


## <a name="security-roles"></a>安全角色
Project Operations 前端功能包括下列角色：

| 角色                          | 描述                                                                                                                                                                 | 作用域 |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| 实践经理              | 支持跨项目报告。                                                                                                            | 业务部门              |
| 项目审批者              | 审批项目的时间和支出。                                                                                                                              | 业务部门 |
| 项目计费管理员 | 创建发票方案。                                                                                                                                                 | 业务部门 |
| 项目经理               | 创建项目计划与请求资源。                                                                                                                              | 业务部门 |
| 项目资源              | 可以被预订和报告时间的团队成员。                                                                                                          | 业务部门|
| 资源经理              | 所有资源管理功能（如实施资源请求和预订）分开，以支持混合项目经理 + 资源经理配置以及单个和集中式资源经理角色。 | 业务部门 |


Web 版本的 Microsoft Project 包含以下角色：

| 角色           | 描述                                                                                                        | 作用域  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| 项目用户   | 项目的协作用户，可以创建自己的项目并查看与其共享的任何项目。 | 用户   |
| 项目系统 | 用于应用程序上下文的角色。 客户应该不会使用此系统角色。                                    | 全局 |

## <a name="security-enforcement"></a>安全执行
在项目级别执行的操作将在已登录用户的上下文中执行。 这意味着，为了创建、打开或删除项目，用户需要在 CD 中有访问权限。 可通过平台中包括的任何可能的机制授予 CDS 中的访问权限。 例如，范围较大的用户可以访问项目，或者执行了明确的项目共享操作以授予用户访问权限。

在 Project Operations 中创建项目时，务必考虑这一点。

## <a name="modern-group-collaboration-with-project-operations"></a>使用 Project Operations 进行新式组协作
Web 项目和 Project Operations 项目支持新式组进行协作。 通过组添加到项目中的用户可以编辑项目计划。

Web 项目会在分配后自动将用户添加到组中。

组允许提供项目权限和支持协作项目的协作工作。 下图描述了在组分配流程中发生的事件和状态更改。

Project Operations 不会通过隐式操作创建组，只会通过推进组建立的显式操作来创建组。

**组管理** 对话中的组成员搜索仅限于那些被设置为环境安全组一部分的用户。 有关详细信息，请参阅[控制用户对环境的访问权限：安全组和许可证](https://docs.microsoft.com/power-platform/admin/control-user-access)。

![组模式](./media/groupsmode.png)

1. 项目由创建用户创建和负责。
2. 项目负责人将更新到团队。
3. 负责人团队会映射到指定或创建的 Office 组。
4. 项目的原始负责人将添加到 Office 组中。

## <a name="deployment-recommendation"></a>部署建议
随着 Office 组协作模型的发展，以后会添加功能来提供更详细的控制。 鼓励今天部署 Project Operations 的客户专注于传统的 Microsoft Dynamics 365 安全模型。

有关详细信息，请参阅 [Common Data Service 中的安全性](https://docs.microsoft.com/power-platform/admin/wp-security)。

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations 和 Microsoft Dynamics 365 Finance 的安全性
Project Operations 包括以下角色：：

- 项目经理
- 项目会计

有关 Finance 中的安全性的详细信息，请参阅[基于角色的安全性](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)。


