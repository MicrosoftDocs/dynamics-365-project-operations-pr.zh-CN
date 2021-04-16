---
title: 将项目合同和项目直接从 Project Service Automation 同步到 Finance
description: 此主题介绍用于直接同步 Microsoft Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 的项目合同和项目的模板和基础任务。
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 319000e6a826580049e8575def5790ab595a3165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289583"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>将项目合同和项目直接从 Project Service Automation 同步到 Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍用于直接同步 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 的项目合同和项目的模板和基础任务。

> [!NOTE] 
> 如果在使用 Enterprise edition 7.3.0，则必须安装 KB 4074835。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 到 Finance 的数据传输

> [!NOTE]
> 应先熟悉 Dynamics 365 Data integration 功能，才能使用 Project Service Automation 到 Finance 集成解决方案。

Project Service Automation 到 Finance 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance 的实例之间同步数据。 可通过数据集成功能提供的集成模板将有关项目合同、项目、项目合同行和项目合同行里程碑的数据从 Project Service Automation 传输到 Finance。

下图显示 Project Service Automation 与 Finance 之间中如何同步数据。

[![Project Service Automation 与 Finance 集成的数据传输](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，请在 Microsoft Power Apps 管理员中心中选择 **项目**，然后在右上角中选择 **新建项目** 以选择公共模板。

以下模板和基础任务用于将项目合同和项目从 Project Service Automation 同步到 Finance：

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>与 Dynamics 365 Project Service Automation v2.x 集成
- **数据集成中模板的名称：** 项目和合同（Project Service Automation 到 Finance）
- **项目中的任务名称：**

    - 项目合同 Project Service Automation 到 Finance
    - 项目 Project Service Automation 到 Finance
    - 项目合同子项 Project Service Automation 到 Finance
    - 项目合同子项里程碑 Project Service Automation 到 Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>与 Dynamics 365 Project Service Automation v3.x 集成
Project Service Automation 中有一项会影响项目合同行里程碑模板的架构更改，需要使用此模板的 v2 版才能将 Project Service Automation v3.x 与 Dynamics 365 集成。

- **数据集成中模板的名称：** 项目和合同（Project Service Automation 3.x 到 Finance）- v2
- **项目中的任务名称：**

    - 项目合同 Project Service Automation 到 Finance
    - 项目 Project Service Automation 到 Finance
    - 项目合同子项 Project Service Automation 到 Finance
    - 项目合同子项里程碑 Project Service Automation 到 Finance

必须先同步科目，才能同步项目合同和项目。

## <a name="entity-set"></a>实体集

| Project Service Automation       | 财经                                                |
|----------------------------------|--------------------------------------------------------|
| 订单                           | 项目合同集成实体                |
| 项目                         | 项目的集成实体                         |
| 订单明细                      | 项目合同行集成实体           |
| 项目合同行里程碑 | 项目合同行里程碑集成实体 |

## <a name="entity-flow"></a>实体流

项目合同在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同。 在集成模板中，可在 Finance 中为项目合同设置集成源。

时间和材料以及固定价格项目在 Project Service Automation 中进行管理，并作为项目同步到 Finance。 作为模板集成的一部分，您可以在 Finance 中设置项目的集成源。 当前，仅支持时间和材料以及固定价格项目。


项目合同行在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同计费规则。 如果交付方法与默认项目类型不同，同步将更新合同行项目和项目组的项目类型。

项目合同行里程碑在 Project Service Automation 中管理，并同步到 Finance 中充当项目合同计费规则里程碑。

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation 到 Finance 集成解决方案

**项目合同** 页上有 **项目合同 ID** 字段。 该字段由一个自然唯一密钥组成以支持集成。

新建项目合同时，如果 **项目合同 ID** 值不存在，则使用编号规则自动生成。 该值由 **ORD** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。 下面是一个示例：**ORD-01022-Z4M9Q0**。

**项目编号** 字段在 **项目** 页提供。 该字段由一个自然唯一密钥组成以支持集成。

新建项目时，如果 **项目编号** 值不存在，则使用编号规则自动生成。 该值由 **PRJ** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。 下面是一个示例：**PRJ-01049-CCNID0**。

应用 Project Service Automation 到 Finance 集成解决方案时，升级脚本将在 Project Service Automation 为现有项目合同设置 **项目合同 ID** 字段，为现有项目设置 **项目编号** 字段。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

- 必须先同步科目，才能同步项目合同和项目。
- 在连接集中，向 **msdyn\_name \[Name\]** 添加 **msdyn\_organizationalunits** 的集成密钥字段映射。 可能首先需要向连接集添加一个项目。 有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。
- 在连接集中，向 **msdynce\_projectnumber \[Project Number\]** 添加 **msdyn\_projects** 的集成密钥字段映射。 可能首先需要向连接集添加一个项目。 有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator)。
- 可将项目合同和项目的 **SourceDataID** 更新为其他值，也可以将其从映射中移除。 默认模板值为 **Project Service Automation**。
- 必须更新 **PaymentTerms** 映射，才能在 Finance 中体现有效的付款期限。 也可以从项目任务中移除映射。 默认值映射具有演示数据的默认值。 下表显示 Project Service Automation 中的值。

    | Value | 描述   |
    |-------|---------------|
    | 7     | N30        |
    | 2     | 2/10 N30 |
    | 3     | N45        |
    | 4     | N60        |

## <a name="power-query"></a>Power Query

如果满足以下条件，请使用 Microsoft Power Query for Excel 筛选数据。

- 您在 Dynamics 365 Sales 中有销售订单。
- 您在 Project Service Automation 中有多个组织单位，并且这些组织单位将映射到 Finance 中的多个法人。

如果必须使用 Power Query，请遵守以下准则：

- 项目和合同（PSA 到 Fin and Ops）模板有一个默认筛选器，其中仅包含类型为 **工作项 (msdyn\_ordertype = 192350001)** 的销售订单。 此筛选器有助于确保不在 Finance 中为销售订单创建项目合同。 如果创建自己的模板，则必须添加这个筛选器。
- 创建一个 Power Query 筛选器，让它仅包含应同步到集成连接集的法人的合同组织。 例如，应将您的包含合同组织单位 Contoso US 的项目合同同步到 USSI 法人，但您的包含合同组织单位 Contoso Global 的项目合同则应同步到 USMF 法人。 如果不向任务映射添加此筛选器，则将把所有项目合同同步到为连接集定义的法人，而不考虑合同组织单位。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE] 
> 项目合同的默认映射中不包含 **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState** 和 **AddressZipCode** 字段。 如果需要为项目合同同步此数据，可添加这些映射。
>
> 项目的默认映射中不包含 **Description**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber** 和 **ProjectType** 字段。 如果需要为项目同步此数据，可添加这些映射。

下图显示了数据集成中的模板任务映射的示例。 此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。

[![项目合同模板映射](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![项目模板映射](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![项目合同子项模板映射](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![项目合同子项里程碑模板映射](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>项目和合同中的项目合同行里程碑映射（PSA 3.x 到 Dynamics）- v2 模板：

[![使用第二版模板的项目合同子项里程碑映射](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]