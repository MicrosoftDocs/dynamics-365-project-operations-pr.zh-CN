---
title: 出差津贴
description: 此主题提供有关在支出管理中使用的出差津贴规则的信息。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072478"
---
# <a name="per-diems"></a>出差津贴

_**适用于：** 面向资源/非库存场景的 Project Operations_


出差津贴是支付给工作中出差的工作人员的津贴。 在“支出管理”中，您可以为各种出差情况创建出差津贴规则。 出差津贴费率可以基于一年的时间、出差地点或这两者。 创建出差津贴规则时，可以指定如果工作人员享受免费餐饮或服务，将扣除的出差津贴费的百分比。 您还可以设置可应用出差津贴费率的工作人员出差的最小和最大时数。

## <a name="configuration"></a>配置 

1. 若要添加出差津贴地点，请转到 **设置** > **计算和代码** > **出差津贴地点** 。
2. 对于上面添加的每个地点，选择在特定开始日期和结束日期之间可用于住宿、餐饮和其他支出的出差津贴费率和货币。 出差津贴费率和货币在 **设置** > **计算和代码** > **出差津贴** 下配置。
3. 在 **出差津贴地点** 页上，配置出差津贴费率层。 出差津贴费率层让您可以定义住宿、餐饮和其他支出的每日津贴的百分比分割。 
4. 若要指定早餐、午餐或晚餐的餐费百分比扣减，请更新 **支出管理参数** 页上 **出差津贴** 选项卡上的字段。 
    
## <a name="submit-expenses-using-per-diem"></a>使用出差津贴提交支出
若要使用出差津贴提交支出，请在创建支出报表时使用 **出差津贴** 支出类别。 输入 **出差津贴起始日期** 、 **出差津贴截止日期** 和 **出差津贴地点** 。 将根据所选地点的出差津贴费率计算金额，根据出差津贴费率层来计算餐费扣减。
