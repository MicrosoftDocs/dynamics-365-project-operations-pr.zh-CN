---
title: 配置内部公司开票
description: 本主题提供了有关配置内部公司项目开票的信息和示例。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9894a405403d4faeb2f02387b03c77a40a6cea3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001145"
---
# <a name="configure-intercompany-invoicing"></a>配置内部公司开票

_**适用于：** 面向资源/非库存场景的 Project Operations_

完成以下步骤以在 Dynamics 365 Project Operations 中设置内部公司项目开票。 内部公司交易是项目合同中属于一个公司或部门的时间和支出交易，而项目合同上的资源属于其他公司或部门。

## <a name="example-configure-intercompany-invoicing"></a>示例：配置内部公司开票

在下列示例中，Contoso Robotics USA (USPM) 是借款法人，Contoso Robotics UK (GBPM) 是贷款法人。 

1. **配置法律实体之间的内部公司会计**。 必须在总帐[内部公司会计](/dynamics365/finance/general-ledger/intercompany-accounting-setup)页上配置每对借款和贷款法律实体。
    
    1. 在 Dynamics 365 Finance 中，转到 **总帐** > **过帐设置** > **内部公司会计**。 使用以下信息创建记录：

        - **起源公司** = **GBPM**
        - **目标公司** = **USPM**

2. **配置法律实体之间的贸易关系**。 必须在贷款法律实体中创建代表借款法律实体的客户记录。 必须在贷款法律实体中创建代表贷款法律实体的供应商记录。

     1. 在 Finance 中，选择法律实体 **GBPM**。
     2. 转到 **应收帐款** > **客户** > **所有客户**。 为法律实体 **USPM** 创建新记录。
     3. 展开 **名称**，按 **类型** 筛选记录并选择 **法律实体**。 
     4. 查找并选择 **Contoso Robotics USA (USPM)** 的客户记录。
     5. 选择 **使用匹配项**。 
     6. 选择客户组 **50 - 内部公司客户**，然后保存记录。
     7. 选择法律实体 **USPM**。
     8. 转至 **应付帐款** > **供应商** > **所有供应商**。 为法律实体 **GBPM** 创建新记录。
     9. 展开 **名称**，按 **类型** 筛选记录并选择 **法律实体**。 
     10. 查找并选择 **Contoso Robotics UK (GBPM)** 的客户记录。
     11. 选择 **使用匹配项**，选择供应商组，然后保存记录。
     12. 在供应商记录中，选择 **常规** > **设置** > **内部公司**。
     13. 在 **贸易关系** 选项卡上，将 **可用** 设置为 **是**。
     14. 将 **客户公司** 字段设置为 **GBPM**，在 **我的客户记录** 中，选择您在过程的前面创建的客户记录。

3. **在项目管理和会计参数中配置内部公司设置**。 

    1. 选择法律实体 **USPM**，然后转到 **项目管理和会计** > **设置** > **项目管理和会计参数**。
    2. 在 **内部公司** 选项卡上，选择采购类别以与自动生成的供应商发票匹配。
    3. 在 **默认类别** 中，选择 **内部公司资源**。
    4. 选择法律实体 **GBPM**，然后转到 **项目管理和会计** > **设置** > **项目管理和会计参数**。
    5. 在 **内部公司** 选项卡上，为每种交易类型选择默认项目类别。 当仅在借入法人存在内部公司交易记录的开票类别时，项目类别用于税务配置。 您可以选择应计内部公司交易的收入。 在通过贷款法律实体中的 Project Operations 集成日记帐过帐交易时，会发生应计。 在过帐内部公司账单时，将冲销该日记帐。
    6. 在 **当借出资源时** 组中，选择 **...** > **新建**。 
    7. 在此网格中，选择以下信息：

          - **借款法律实体** = **USPM**
          - **应计收入** = **是**
          - **默认工时单类别** = **默认值 – 小时**
          - **默认支出类别** = **默认值 – 支出**

4. **在分类帐过帐设置中设置内部公司成本和收入帐户**。 在贷款法律实体中过帐内部公司客户账单后，会贷记内部公司收入帐户。 在借款法律实体中过帐匹配的待定供应商账单后，会借记内部公司成本帐户。 这些帐户在相应的法律实体中设置。 
      
     1. 在 Finance 中，选择借款法律实体 **USPM**。 
     2. 转到 **项目管理和会计** > **设置** > **过帐** > **分类帐过帐设置**。 
     3. 在 **成本帐户** 选项卡上的 **分类帐帐户类型** 中，选择 **内部公司成本**。 使用以下信息创建新记录：
      
        - **贷款法律实体** = **GBPM**
        - **主客户** = 选择内部公司成本的主客户。 此设置是必需的。 此设置用于 Finance 中的内部公司流，但不用于与项目相关的内部公司流。 此选择没有下游影响。 
        
     4. 选择贷款法律实体 **GBPM**。 
     5. 转到 **项目管理和会计** > **设置** > **过帐** > **分类帐过帐设置**。 
     6. 在 **收入帐户** 选项卡上的 **分类帐帐户类型** 中，选择 **内部公司收入**。 使用以下信息创建新记录：

        - **借款法律实体** = **USPM**
        - **主客户** = 选择内部公司收入的主客户。 此设置是必需的。 此设置用于 Finance 中的内部公司流，但不用于与项目相关的内部公司流。 此选择没有下游影响。 

5. **设置人工转帐定价**。 在 Dataverse 上的 Project Operations 中配置了内部公司转帐定价。 为内部公司开票配置[人工成本费率](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity)和[人工帐单费率](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions)。 对于内部公司支出交易，不支持转帐定价。 组织间单位销售价格始终会设置为与资源单位成本费相同的值。

      Contoso Robotics UK 的开发人员资源成本为每小时 88 英镑。 对于此资源在美国项目中的工作，Contoso Robotics UK 每小时向 Contoso Robotics USA 收取 120 美元。 对于 Contoso Robotics UK 开发人员资源所做的工作，Contoso Robotics USA 向客户 Adventure Works 收取 200 美元。

      1. 在 Dataverse 上的 Project Operations 中，转到 **销售** > **价目表**。 创建一个新的成本价目表，称为 **Contoso Robotics UK 成本费率**。 
      2. 在此成本价目表中，使用以下信息创建记录：
         - **角色** = **开发人员**
         - **成本** = **88 GBP**
      3. 转到 **设置** > **组织单位**，将此成本价目表附加到 **Contoso Robotics UK** 组织单位。
      4. 转到 **销售** > **价目表**。 创建一个成本价目表，称为 **Contoso Robotics USA 成本费率**。 
      5. 在此成本价目表中，使用以下信息创建记录：
          - **角色** = **开发人员**
          - **资源供给公司** = **Contoso Robotics UK**
          - **成本** = **120 美元**
      6. 转到 **设置** > **组织单位**，将 **Contoso Robotics USA 成本费率** 成本价目表附加到 **Contoso Robotics USA** 组织单位。
      7. 转到 **销售** > **价目表**。 创建一个名为 **Adventure Works 帐单费率** 的销售价目表。 
      8. 在此销售价目表中，使用以下信息创建记录：
          - **角色** = **开发人员**
          - **资源供给公司** = **Contoso Robotics UK**
          - **帐单费率** = **200 美元**
      9. 转到 **销售** > **项目合同**，并将 **Adventure Works 帐单费率** 价目表附加到项目合同的 Adventure Works 项目价目表。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
