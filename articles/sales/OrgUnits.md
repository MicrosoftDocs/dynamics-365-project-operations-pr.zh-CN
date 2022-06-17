---
title: 部门
description: 本文介绍部门概念，并解释了如何在 Microsoft Dynamics 365 Project Operations 中创建和维护部门。
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921613"
---
# <a name="organizational-units-overview"></a>部门概述

在 Microsoft Dynamics 365 Project Operations 中，*部门* 是专业服务公司中聘用具有成本费率的可记帐资源的专门组或部门。

对于在不同实践环节或业务线中使用技术资源的专业服务公司，填补职位的成本可能会有所不同，具体取决于填补该职位的实践环节或业务线。 在此场景中，部门这一概念会有所帮助，方法是集中公司中具有一组可记帐角色的专门成本结构的部门内的那些角色。

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Project Operations 中的部门概念

在 Project Operations 中，部门具有专门的货币和专门的成本价目表。

部门的货币是用于跟踪成本的主要货币。

可以将一个或多个成本价目表附加到每个部门。 Project Operations 对可附加到部门的价目表实施以下限制：

- 价目表必须采用部门的货币。
- 价目表必须是成本价目表。

此外，资源实体中包括部门的属性。 可以将每个资源分派给一个部门。

### <a name="roles-of-organizational-units"></a>部门的角色

部门在 Project Operations 中充当两种角色：

- **合同签订部门** – 代表主要负责赢得销售和管理对客户的工作和服务交付的公司组或部门的部门。 合同签订部门通过 **商机**、**报价单**、**项目合同** 和 **项目** 页标题部门中的 **合同签订部门** 字段识别。
- **资源单位** – 资源所属部门或将资源分派给的部门。 这种部门可以将自己的资源提供给工作说明书 (SOW) 中和合同签订部门负责的项目中的某些角色。

![合同签订部门和资源部门。](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>部门常见问题

以下是有关部门的一些最常见的问题。

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Project Operations 中的部门实体与 Dynamics 365 中的现有组织实体之间有何关系？

Dynamics 365 中的组织实体代表全球性 Dynamics 365 实例的名称。 此名称通常是全球性企业的名称。

部门实体代表全球性企业的一个组或部门。 这个组或部门有一组角色和这些角色的成本价目表，而这些角色和价目表则与企业中其他组或部门的角色和价目表不同。

安装 Project Operations 时，将根据组织创建一个默认部门。 将把所有现有资源分派给这个默认部门。 如果将任何新 Active Directory 用户或资源导入 Dynamics 365 中，用户导入流程将把这些用户或资源分派给 Project Operations 中的默认部门。

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>部门实体与业务部门实体有何区别？

在 Dynamics 365 中，业务部门实体是一种安全构造。 将用户与业务部门关联可以确定用户可访问的实体和实体记录。 还可以确定该用户对这些实体记录的权限（创建、读取、写入、删除、附加、附加到、分派或共享）。

部门实体代表具有为其分派的员工的独占成本费率的公司组或部门。 资源与部门的关联决定资源在项目协定中的成本。

实施 Dynamics 365 时，请优化业务部门层次结构的安全授权和业务部门的用户分派。 将通常访问同一组记录的所有用户分派给同一个业务部门。 部门不影响安全授权或访问权限。

**显示部门和业务部门建模的一个潜在区别的示例**

Contoso, Ltd. 的 Microsoft 技术业务非常兴旺。 建和方银都是 C\# 开发人员，但是方银在美国，而建在印度。 大多数项目协定同时需要 Contoso 印度和 Contoso 美国的资源，而建和方银需要这些业务区域中的项目的相同级别安全访问权限。 但是，Contoso 印度开发人员的成本与 Contoso 美国开发人员的成本相差很大。

下面是使用 Dynamics 365 和 Project Operations 针对这种场景进行设计的最佳方式。

1. 创建Microsoft 技术业务作为业务部门，并将建和方银与其关联。 这样就可以帮助确保两位员工对该业务区域中的所有项目具有相同级别的安全访问权限。 她们都可以检查进度和报告时间、支出、材料使用情况和任务更新。
2. 创建两个部门以帮助确保正确体现项目的成本。
3. 将方银与 Contoso 美国关联，将建与 Contoso 印度关联。
4. 为这两个部门分派适当的成本价目表。 这样，就可以帮助确保项目中为建和方银记录的成本准确体现 Contoso 美国与 Contoso 印度之间的成本差额。

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>部门是否与 Dynamics 365 中的销售区域有关？

销售区域与部门之间没有任何关联或关系。 销售区域通常是开展销售的地理区域。 可以为每个销售区域关联销售价目表。

部门是公司中的内部组或部门，用于跟踪销售给其他部门或外部客户的一组角色的成本。

**显示部门和销售区域建模的一个潜在区别的示例**

Contoso, Ltd. 有两个开发中心：Contoso 美国和 Contoso 印度。 这两个开发中心的资源成本相差很大。 Contoso 在大量国际市场（如拉丁美洲、北美、亚太、西欧和中东）销售其信息技术 (IT) 服务。 相同项目角色的帐单费率在这些市场中相差很大。 应该将 Contoso 美国和 Contoso 印度设置为部门，而每个部门应该有自己的成本价目表。 应该将亚太、拉丁美洲、北美、西欧和中东设置为销售区域，而每个销售区域应该有自己的销售价目表。

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>为什么要限制价目表与部门的关联？

出售服务的地理区域或市场中的销售定价通常各不相同。 公司的内部部门自己通常没有同一种类型的服务的销售定价。 但是，内部部门有不同的售出商品成本 (COGS)，具体取决于聘用的人员的技能和运营区域的劳工条件。 因为部门建模为公司的内部部门，所以只能有成本价目表。

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>为什么不能将销售价目表与部门关联？

在 Project Operations 中，可以将销售价目表与客户和销售区域关联。 商机、报价单、项目合同和项目等交易实体使用附加到客户帐户或销售区域的销售价目表，以便确定项目参与的帐单费率和潜在收入。

成本价目表与部门关联。 商机、报价单、项目合同和项目等交易实体使用附加到合同签订部门的成本价目表，以便确定项目参与的成本。

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Project Operations 中的部门是否分层？

不需要。 在 Project Operations 当前版本中，部门不分层。 因此，您无法执行以下任务：

- 配置用于输入遍历层次结构的默认成本价的模式。
- 报告在不同部门层次结构级别汇总的收入或成本。

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>我们是一家大型跨国公司，具有复杂、多级的成本中心、部门、记帐办公室层次结构。 如何在 Project Operations 当前版本中充分利用部门概念？

如果采用复杂的成本中心、部门、记帐办公室等层次结构，请将该层次结构的叶节点设置为不同的部门。

以下示例显示典型的层次结构。

**Contoso 印度**

- SAP 业务

    - 技术顾问
    - 职能顾问

- Microsoft 技术业务

    - 技术顾问
    - 职能顾问

**Contoso US**

- SAP 业务

    - 技术顾问
    - 职能顾问

- Microsoft 技术业务

    - 技术顾问
    - 职能顾问

如果您的层次结构与此示例类似，则必须将其设置为简单列表，如下所示：

- Contoso 印度 - SAP 业务 - 技术顾问
- Contoso 印度 - SAP 业务 - 职能顾问
- Contoso 印度 - Microsoft 技术业务职能顾问
- Contoso 印度 - Microsoft 技术业务职能顾问
- Contoso 美国 - SAP 业务 - 技术顾问
- Contoso 美国 - SAP 业务 - 职能顾问
- Contoso 美国 - Microsoft 技术业务 - 技术顾问
- Contoso 美国 - Microsoft 技术业务 - 职能顾问

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>我们是仅以一个部门的形式运营的小型专业服务公司。 如何在 Project Operations 当前版本中充分利用部门概念？

如果您的公司以拥有一个成本价目表的部门的形式运营，则不必设置任何部门。 安装 Project Operations 时会创建一个与组织同名的默认部门。 默认情况下，将把所有用户分派给这个部门。 只要系统需要选择部门，都会默认选择此部门。

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>基于报价单或项目合同子项创建项目时，默认合同签订部门来自报价单或项目合同。 如果项目是在报价单或项目合同之类销售实体之前创建的，则什么是默认合同签订部门？

当磁盘时，项目的项目需要创建收缩根据默认的计价创建该活动的用户。 该用户也是默认项目经理。 如果项目映射到报价单或项目合同之类销售实体，则项目的合同签订部门改为基于销售实体。 在此情况下，可能会重新计算项目估算，因为如果更改合同签订部门，则使用成本价目表计算成本估算变化。 销售价目表用于计算将更改的销售估算，因此将与报价单的项目价目表同步。

项目的 **合同签订部门** 和 **货币** 字段已锁定，不能编辑，因为这些字段必须与项目映射到的销售实体（报价单或项目合同）的值同步。

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>在 Project Operations 中创建和维护部门

要在 Project Operations 中创建部门，请执行以下步骤。

1. 转到 **设置 \> 部门**。
2. 选择 **新建**。
3. 在 **常规** 区域的 **名称** 字段中，为部门输入名称。 然后根据需要设置其他字段。
4. 选择 **保存** 创建记录，以可以继续编辑。
5. 在 **成本价目表** 下，选择加号 (**+**) 添加价目表。 此处只能添加具有 **成本** 上下文的价目表。
6. 在 **名称** 字段中，选择 **搜索** 按钮，选择您要将其用于此部门的价目表。 根据需要继续添加价目表。
7. 当完成添加价目表时，选择页面右下角的 **保存**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
