---
title: 审批开发人员注释
description: 此主题提供有关处理审批的其他开发人员信息。
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290258"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="903ba-103">审批开发人员注释</span><span class="sxs-lookup"><span data-stu-id="903ba-103">Developer notes for Approvals</span></span>

<span data-ttu-id="903ba-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="903ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="903ba-105">Dynamics 365 Project Operations 包含确保通过审批阶段正确进行记录转换的验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="903ba-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="903ba-106">正确的记录转换确保：</span><span class="sxs-lookup"><span data-stu-id="903ba-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="903ba-107">所有支持行全部在相关表中创建，如日记帐和实际值。</span><span class="sxs-lookup"><span data-stu-id="903ba-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="903ba-108">在继续之前，审批者在项目中将标记为 **项目审批者**。</span><span class="sxs-lookup"><span data-stu-id="903ba-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]