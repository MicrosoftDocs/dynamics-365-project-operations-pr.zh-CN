---
title: 新式审批的升级注意事项
description: 本文介绍管理员在启用新式审批功能时应考虑的要点。
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931733"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>新式审批的升级注意事项 

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

作为 2022 年 4 月第 1 波版本的一部分，新式审批功能将默认启用。 此功能将提高审批逻辑的可靠性，并确保您可以确定审批逻辑失败的原因。

作为此更改的一部分，项目审批的状态更改会更新。 状态现在直接从 **已提交** 变为 **已审批**。 **待处理** 不再是审批状态。 要确定审批是否处于待处理状态，请验证审批是否属于审批集，并查看附加的审批集的状态。

## <a name="before-you-upgrade"></a>升级之前

在升级到新式审批之前，请确保您没有待处理的审批。 新式审批不使用 **待处理** 状态。 因此，不会处理升级后仍标记为 **待处理** 的任何审批。

## <a name="after-you-upgrade"></a>升级之后

升级到新式审批后，管理员必须验证处理审批的云端流是否已启用。

1. 登录 [flow.microsoft.com](https://flow.microsoft.com)
2. 在页面的右上角，将您的环境切换到您已升级的环境。
3. 选择 **解决方案** 列出安装在环境中的解决方案。
4. 在解决方案列表中，选择 **Project Operations** 或 **Project Service**。
5. 将筛选器从 **所有** 更改为 **云端流**。
6. 验证 **Project Service – 定期安排项目审批集** 选项是否设置为 **开**。 如果没有，选择流，然后选择 **打开**。
7. 通过查看 **设置** 区域的 **系统作业** 列表，验证是否每五分钟进行一次处理。

## <a name="short-term-rollback"></a>短期回滚

如果您无法接受更改，或者您使用此功能时遇到严重问题，您可以通过执行以下步骤暂时恢复到原始审批流：
1. 登录您的环境并确认没有待处理的审批。
2. 转到 **设置** > **项目参数**。
3. 选择 **功能控制**，然后选择 **新式审批** 关闭功能。

## <a name="removing-the-feature-flag"></a>移除功能标志

在 2022 年 10 月第 2 波更新中，关闭此功能的功能将被删除。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
