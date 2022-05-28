---
title: 资源管理常见问题
description: 此主题提供资源管理常见问题的解答。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8ce1edf7d7c535271fa8076befd26f092fbd495
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587483"
---
# <a name="resource-management-faq"></a>资源管理常见问题

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>团队成员与资源要求之间有何区别？

项目团队成员可以分派给任务，预订或超额预订，以及设置为审批者。 资源要求不能作为需求的草稿说明独立于项目团队成员存在。 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>建议工时与软预订工时之间有何区别？

建议工时和软预订工时在可视化方面不同。 建议工时仅对资源经理和使用资源请求发起需求的项目经理显示。 软预订工时对可访问日程安排板的任何人显示。

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>如何查看为项目软预订的资源工时？

当您预订资源要求时，可进行软预订。 为项目团队软预订的资源显示为具有软预订工时的团队成员。 也在日程安排板中显示。

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>如何更改我预订的资源（通用资源或指定资源）的所需工时和开始日期与结束日期？

预订资源之后，选择 **维护预订** 以进行所需任何更改。

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation 支持哪些资源类型？

Dynamics 365 Project Service Automation 中仅支持 **用户** 和 **联系人** 资源类型。 虽然可以创建其他类型的资源（例如，**设备** 和 **组**），但是它们不支持端到端用例。

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>分派与预订之间有何区别？

分派是将资源分派给项目计划中的项目任务。 资源可以是实际资源，也可以是通用资源。 预订是将资源硬性或软性分配给项目。 硬预订占用资源的产能。 理想情况下，实际资源、预订和分派应一致，因为它们没有区别。 但是，PSA 不强制执行此共识。 “协调”视图为项目经理显示资源的预订和分派不一致的位置。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
