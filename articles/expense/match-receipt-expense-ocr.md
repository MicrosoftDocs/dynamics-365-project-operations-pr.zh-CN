---
title: 使用 OCR 使收据与支出匹配
description: 此主题提供有关收据的光学字符识别 (OCR) 处理的信息。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124312"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>使用 OCR 使收据与支出匹配

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

通过引入对收据的光学字符识别 (OCR) 处理，支出输入得到了增强。 此功能的目的是改进用户创建支出报表的体验。

## <a name="key-features"></a>主要功能

- 系统从收据中提取商家名称、日期和总金额。
- 系统会尝试将未附加的收据与未附加的支出交易记录匹配。
- 您可以创建从收据手动输入的支出交易记录。

## <a name="attach-receipts-to-an-expense-report"></a>将收据附加到支出报表

若要在创建支出报表时自动附加包含信用卡交易记录的收据，请完成以下步骤。

  1. 打开 **支出管理** 工作区。
  2. 在 **收据** 选项卡上，验证是否存在未附加的收据。 您还可以在 **收据** 选项卡上上载收据。
  3. 在 **支出** 选项卡上，验证是否存在未附加的支出。 通常情况下，支出管理员从信用卡提供商处导入这些支出。
  4. 选择 **新建支出报表**。 请注意，在您创建支出报表时，现在还可以包括支出和收据。 如果同时添加支出和收据，则会触发根据支出自动匹配收据。

## <a name="create-or-match-receipts-to-an-expense-report"></a>创建收据或将其与支出报表匹配
若要创建支出，或从收据匹配支出，请完成以下步骤。

  1. 在支出报表的 **收据** 选项卡上，选择 **添加收据** 来附加收据。
  2. 在上载的收据图像下，注意 **创建** 和 **匹配** 选项。

      - 选择 **创建** 来创建手动输入的支出交易记录，并填写从收据中提取的值。
      - 如果选择 **匹配**，系统将尝试匹配现有支出与收据。

## <a name="installation"></a>安装

若要使用这些高级支出功能，请安装适用于 Microsoft Dynamics 365 Finance 的支出管理服务加载项，并启用您的实例中的功能。 您可以从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目访问该加载项。

1. 登录到 LCS，打开所需的环境。
2. 转到 **完整详细信息**。
3. 选择 **维护**，或向下滚动到 **环境加载项** 快速选项卡。
4. 选择 **安装新加载项**。
5. 选择 **支出管理服务**。
6. 按照安装指南操作，并同意条款和条件。
7. 选择 **安装**。

在 **功能管理** 工作区中，打开以下功能：

- 重新打造支出报表
- 自动匹配并从收据创建支出

当您启用这些功能时，会发生以下操作：

- 现有的 **支出管理** 工作区将替换为新工作区。
- 将添加用于显示支出字段的新菜单项。
- 您仍然可以转到 **支出管理 > 我的支出 > 支出报表** 来打开以前的 **支出报表** 页面。
- 工作流和所有审批仍会将您带到现有的支出报表页。
- 收据将通过 Microsoft Azure Cognitive Services 处理，并将提取和添加元数据。
- 添加了一个选项，使您可以创建包含匹配的未附加收据的支出报表。
- 添加到支出报表的一个选项，使您可以从收据创建支出行，或尝试将现有收据与现有支出行匹配。

## <a name="frequently-asked-questions"></a>常见问题

**Microsoft 是否在其模型中使用我的数据？**

否，Microsoft 已经为其收据处理服务构建了常规的机器学习模型。 此模型不基于您上载的收据。

**哪里提供和处理此功能？**

目前，支持在美国使用。

**我的收据会去向哪里？**

Finance 将与 Cognitive Services 连接来提取字段数据。 在进行处理时，Cognitive Services 最长会将您的收据副本保留 24 小时。 处理完成后，Cognitive Services 将删除收据。 收据仍存储在 Finance 中。

有关详细信息，请参阅[使用表单识别器的新功能支持收据了解功能](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。
