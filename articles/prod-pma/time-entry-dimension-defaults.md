---
title: 项目时间条目的默认财务维度
description: 本主题提供有关如何将默认财务维度应用于时间条目的信息。
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597925"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>项目时间条目的默认财务维度

[!include [banner](../includes/banner.md)]

将财务维度用于项目时间条目时，默认维度值按以下顺序评估：

1. 资源
2. 集成
3. 融资来源

例如，如果在资源上指定了默认维度，默认值将应用于为项目指定的默认值。 同样，如果在项目上指定了默认维度，默认值将应用于为资金来源指定的默认值。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
