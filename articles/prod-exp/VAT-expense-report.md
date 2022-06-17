---
title: 增值税返回
description: 本文介绍如何返回增值税 (VAT) 交易的退税。
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5798c11b4f7a9e49318cdab097746f21c2e81e2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934079"
---
# <a name="vat-recovery"></a>增值税返回 

要在符合条件的增值税 (VAT) 交易中接收退款，公司或组织必须识别、收集、验证和提交准确的信息。 此过程包括多个任务，根据公司的规模，可以包括多个员工或角色。

要使用支出管理增值税退税，必须完成以下先决任务：

- 必须为分配到支出类别的国家/地区创建税码。
- 必须为每个税码创建增销售税组。
- 必须为每个销售税组创建项目销售税码。

在完成先决任务后，员工可以完成增值税交易记录退款请求所需要的步骤。

1. 在支出报表中，输入有关信用卡交易的税务信息，以识别符合条件的增值税退款。
2. 确保所有税务信息已完成，然后过帐支出报表。
3. 处理符合国际增值税退回条件的支出。
4. 将增值税退回数据发送给第三方供应商，以提交国际退回申报表。
5. 处理国内增值税退回的支出。

以下各节提供了一些示例，显示了 Contoso 员工如何完成每个步骤。

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>在支出报表中，输入有关信用卡交易记录的税务信息来确定使用的增值税退款

南希是 Contoso 的一位销售代表，她的基地在美国，最近刚从英国出差回来。 在旅行期间，她有一些用于餐费的个人信用卡支出。 南希现在必须创建支出报表来对帐自己的支出。

Nancy 在支出报表中输入信息时，在 **编辑支出报表** 页 **国家/地区** 字段中选择 **英国**。 然后，系统对销售税组列表进行筛选，以仅显示适用于英国的组。 Nancy 选择 **英国 001** 销售税组，然后选择 **餐饮** 项目销售税组。 然后她添加了食宿的新交易记录。 因为在英国只有一个住宿的增值税组和增值税（物料）组，此信息自动填充进南希的支出报表。

根据 Contoso 政策，所有支出必须有匹配的收据。 因此，Nancy 保存支出报表时，将收到一条消息，说明必须附加支出报表中所列每项交易记录的收据。 Nancy 验证她是否已将每张交易收据的数字图像附加到支出报表中，然后提交报表以供审批。 然后，她将纸质收据发送给后端办公系统处理团队。 此团队将把增值税退回数据发送给第三方供应商，后者为 Contoso 提交国际增值税退回申报表。

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>确保所有税务信息已完成，然后过帐支出报表

Contoso 的应付帐款协调员 April 必须在过账报表前输入支出报表中缺少的所有税务信息。 她打开 **支出报表详细信息** 页，看到 Nancy 被批准的支出报表。 然后，April 打开支出报表查看交易详细信息。 她发现 Nancy 没有为其中一项交易输入项目销售税组。 由于未提供此信息，April 无法过帐此支出报表。 因此，April 在支出管理中查看 **税项配置** 页，找到了该国家/地区和交易记录类型的相应增值税（物料）组。 April 现在可以将支出报表过帐到总帐了。

在 April 过帐支出报表时，将创建一个可退回工作项。 此工作项被分配给后端办公系统处理团队的成员。 April 收到一条消息，确认过帐已成功完成。 此消息还列出了已确定要退回的增值税交易的数量。

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>处理符合国际增值税退回条件的支出

Arnie 是 Contoso 的后勤办公室处理团队的成员，负责确认所有增值税退税所需信息已包括在支出报表中。 他打开 **支出退税** 页，选择 Nancy 提交的支出报表。 Arnie 验证已附加所有必需的收据，并已输入正确的增值税组和增值税（物料）代码。

在 Arnie 从南希处接收纸质收货，他验证纸质收货对应数字收据，然后更改支出报表的状态为 **准备退税**。

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>将增值税退税数据发给第三方供应商以提交国际退税收益

当 Arnie 准备好将支出报表数据发送给将提交增值税退回申报表的第三方供应商时，他打开 **支出退税** 页。 他对页面进行筛选，以仅显示标记为 **准备退回** 的支出报表。 Arnie 然后选择 **文件** &gt; **导出到 Excel**。 支出报表中的增值税信息将导出到 Microsoft Excel 工作表。 Arnie 将此工作表提交给第三方供应商，并包含一条消息，说明纸质收据已使用快递发出。

## <a name="process-expenses-for-domestic-vat-recovery"></a>处理国内增值税退回的支出

Arnie 必须验证支出报表交易是否符合增值税退回的条件，以及数字收据是否已附加到报表中。 要开始处理符合国内退税条件的支出，Arnie 打开 **支出退税** 页，然后选择需要验证的支出报表。 他验证收据是以公司的名义而不是员工的名义开具的。 增值税退税的收据必须以公司的名义。 Arnie 然后确认应用了正确的增值税组和增值税（物料）代码。

当 Arnie 收到纸质收据时，他将支出报表的状态更改为 **准备退回**。 然后，他可以向相应的税务机构提交申报表。 在这种情况下，在美国的相应的税务机构是美国国税局 (IRS)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]