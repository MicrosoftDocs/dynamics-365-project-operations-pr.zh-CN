---
title: 安全和审批
description: 本文提供有关在 Microsoft Dynamics 365 Project Operations 中使用审批的安全设置的信息。
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841912"
---
# <a name="security-and-approvals"></a>安全和审批

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Microsoft Dynamics 365 Project Operations 使用两个安全角色来允许时间、支出和材料条目的审批：

- 项目审批者
- 项目审批者管理员

## <a name="project-approver"></a>项目审批者

您必须具有 **项目审批者** 安全角色才能审批项目时间、支出和材料条目。 您还必须有权访问相关实体，如 **项目**。 该访问权限可由具有 **项目经理** 角色的人员分配。 此外，您必须是项目的团队成员并被标记为审批者。

要审批非项目条目，您必须是提交者的经理。

## <a name="project-approver-admin"></a>项目审批者管理员

> [!NOTE]
> 必须先启用[审批集](approval-sets.md)功能，然后才能使用项目审批者管理员功能。

**项目审批者管理员** 安全角色允许用户绕过策略并允许跨所有项目审批条目。 分配此角色将绕过需要团队成员身份的验证逻辑，并被标记为审批者。 您必须有通过分配给您的安全角色访问相关的相关表（如 **项目**）的权限。

系统用户上下文以与项目审批者管理员安全角色相同的方式绕过验证。
