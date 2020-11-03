---
title: 提交资源请求
description: 此主题介绍如何提交针对项目资源的请求。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072697"
---
# <a name="submitting-a-resource-request"></a>提交资源请求

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

可将生成的资源要求作为资源请求提交。 然后将请求发给资源经理处理。

1. 在 Project Service Automation (PSA) 的 **项目** 页中，单击 **团队** 选项卡查看可预订资源列表。 
2. 从列表中选择具有资源要求的通用资源，然后单击 **提交请求** 。

![提交资源请求](media/RM-how-to-18.png)

通用团队成员的请求状态将更改为 **已提交** 。

资源经理处理请求之后，如果资源经理使用指定资源的预订处理请求之后，通用资源将替换为指定资源。 否则，如果资源经理已建议指定资源，通用资源将留在团队中，而请求状态则更改为 **需要审阅** 。
