---
title: 项目发票集成
description: 本文提供有关客户开票的 Project Operations 双写入集成的信息。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912091"
---
# <a name="project-invoice-integration"></a>项目发票集成

本文提供有关客户开票的 Project Operations 双写入集成的信息。

在 Project Operations 中，项目经理管理项目记帐积压，并在 Microsoft Dataverse 中为客户创建估价发票。 根据此估价发票，应收帐款职员或项目会计创建面向客户的发票。 双写入集成确保估价发票详细信息与财务和运营应用同步。 过帐面向客户的发票后，系统会使用会计详细信息更新 Dataverse 中的相关项目实际值。 下图提供了此集成的高级概念概述图。

   ![项目发票集成。](./media/DW5Invoicing.png)

当项目经理在 Dataverse 中确认估价发票后，估价发票抬头信息将使用双写入表映射 **项目发票方案 V2（发票）** 同步到财务和运营应用。 这是从 Dataverse 到财务和运营应用的单向集成。 不支持直接在财务和运营应用中创建或删除项目发票方案。

Dataverse 中的发票确认还会触发业务逻辑，来在 **实际值** 实体中创建与记帐相关的记录。 这些记录将使用双写入表映射 **Project Operations 集成实际值 (msdyn\_actuals)** 同步到 Finance and Operations。 有关详细信息，请参阅[项目估计值和实际值](resource-dual-write-estimates-actuals.md)。 

项目发票方案明细通过定期流程 **从暂存导入** 创建。 此流程基于 **实际值暂存** 表中的已记帐实际销售额详细信息。 有关详细信息，请参阅[管理项目发票方案](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)。 
