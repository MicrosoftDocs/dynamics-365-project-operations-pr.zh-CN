---
title: 移动设备支出应用
description: 此主题提供有关支出管理移动工作区的信息。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88251552a937f0a3a066e08b87dbd5f7b73c46c69776fbc788d37cc21fe73541
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993185"
---
# <a name="mobile-expense-app"></a>移动设备支出应用

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

此主题提供有关 **支出管理** 移动工作区的信息。 此工作区允许用户捕获和上载收据，以便日后可以将其附加到支出报表。 用户还可以通过使用已附加的收据快速创建支出行，并创建和管理其支出报表。 此外，审批者可以使用 **支出管理** 移动工作区查看分配给他们的支出报表，并可以批准或拒绝这些支出报表。

此移动工作区用于与 Dynamics 365 for Unified Ops 移动应用一起使用。

很多组织要求将收据副本附加到员工为处理还款提交的与出差相关或与业务相关的支出报表中。 使用 **支出管理** 移动工作区，用户可以通过使用附加的收据照片在所选的移动设备上快速创建新的支出行。 或者，用户可以捕获收据照片，在以后将其附加到支出报表中。 员工还可以创建和管理其支出报表，然后使用其移动设备提交报表进行审批和还款。

具体来说，**支出管理** 移动工作区允许用户执行以下任务：

- 对收据拍照。 上载收据照片以在以后将其附加到支出报表。
- 作为捕获的收据上载文件。 然后，您可以在以后将该文件附加到支出报表中。
- 使用附加的收据创建新支出行。 然后，您可以在以后将该行项添加到支出报表，并将其提交进行审批和还款。

您还可以使用以下功能：

- 创建新支出报表。
- 将信用卡交易和其他以前创建的支出附加到支出报表中。
- 为支出报表创建新支出。
- 通过拍摄收据照片或作为捕获的收据上载文件来向支出报表的任何支出附加收据。
- 根据公司的支出策略，将来宾列表添加到支出中。
- 根据公司的支出策略，细化支出。
- 提交支出报表进行审批和还款。
- 批准或拒绝您被分配作为审批者的支出报表。

## <a name="prerequisites"></a>先决条件
先决条件根据为您的组织部署的版本有所不同。

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>使用 Dynamics 365 Finance 的先决条件 
如果已经为您的组织部署 Finance，系统管理员必须发布 **支出管理** 移动工作区。 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>使用带平台更新 3 或更高版本的版本 1611 时的先决条件
如果已经为您的组织部署带平台更新 3 或更高版本的版本 1611，系统管理员必须完成以下先决条件。 

<table>
<thead>
<tr class="header">
<th>先决条件</th>
<th>角色</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>实现 KB 4019015。</td>
<td>系统管理员</td>
<td>KB 4019015 是包含<strong>支出管理</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4019015，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Lifecycle Services 下载更新</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ExpenseMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td>发布<strong>支出管理</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>下载并安装 Dynamics 365 Unified Ops 移动应用
下载并安装 Dynamics 365 Unified Ops 移动应用：

- [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
- [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用
1. 在移动设备上启动应用程序。
2. 输入您的 Dynamics 365 URL。
4. 首次登录时，将提示您输入您的用户名和密码。 输入凭据。
5. 登录后，将显示您的公司的可用工作区。 如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>使用支出管理移动工作区捕获收据

1. 在您的移动设备上，打开 **支出管理** 工作区。
2. 选择 **捕获收据**。
3. 选择 **拍照** 或 **选择图像**。
4. 请执行以下步骤之一：

   - 如果选择了 **拍照**，请执行以下步骤：

      1. 您将进入移动设备上的相机，让您可以对收据进行拍照。 
      2. 拍照完毕后，请选择 **确定** 接受照片。
      3. 可选：为照片输入名称，然后输入注释。

    - 如果选择了 **选择图像**，请执行以下步骤：

        1. 在列表中选择一个图像。
        2. 可选：为图像输入名称，然后输入注释。

5. 选择 **完成**。

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>使用支出管理移动工作区快速输入支出

1. 在您的移动设备上，打开 **支出管理** 工作区。
2. 选择 **快速输入支出**。
3. 选择支出类别。 您将看到加载到应用中以供脱机使用的支出类别列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的类别不在该列表中，请选择 **搜索** 进行在线搜索。 按支出类别搜索，或切换到按支出类型搜索。
4. 输入支出的交易日期。
5. 可选：输入支出的商家。
6. 输入支出金额。
7. 选择支出的货币。 您将看到加载到应用中以供脱机使用的货币代码列表。 默认情况下，加载 400 个货币，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的货币不在该列表中，请选择 **搜索** 进行在线搜索。 按货币搜索，或切换到按名称搜索。
8. 选择 **拍照** 或 **选择图像**。
9. 请执行以下步骤之一：

    - 如果您选择了 **拍照**，您将进入移动设备上的相机，让您可以对收据进行拍照。 拍照完毕后，请选择 **确定** 接受照片。
    - 如果您选择了 **选择图像**，请在列表中选择一个图像。

10. 选择 **完成**。

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用支出管理移动工作区审批支出报表（如果使用 2017 年 7 月版更新）

1. 在您的移动设备上，打开 **支出管理** 工作区。
2. **支出审批** 显示分配给您进行审批的支出报表的数量。 此数字大约每 30 分钟更新一次。 选择 **支出审批**。

    将显示分配给您进行审批的支出报表列表。
    
3. 选择支出报表可查看其支出详细信息。
4. 选择支出可查看其详细信息。 显示的支出信息包括所有收据、来宾和明细详细信息。
5. 返回到 **支出报表** 页，选择批准或拒绝支出报表。
6. 为审批操作输入注释。
7. 选择 **完成**。

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用支出管理移动工作区创建新支出报表并提交进行审批（如果使用 2017 年 7 月版更新）

1. 在您的移动设备上，打开 **支出管理** 工作区。
2. 选择 **输入支出**。
3. 选择 **新建报表**，或选择列表中的现有支出报表。
4. 对于新的支出报表，输入用途和任何其他可用信息。 此信息会有所不同，具体取决于为您的公司配置支出管理的方式。
5. 选择 **完成**。
6. 若要将现有支出（如信用卡交易）添加到支出报表，请选择 **附加**。
7. 在列表中选择一项或多项支出。
8. 选择 **完成**。
9. 若要向支出报表添加新支出，请选择 **新建支出**。
10. 选择支出的类别。 您将看到加载到应用中以供脱机使用的支出类别列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的类别不在该列表中，请选择 **搜索** 进行在线搜索。 按支出类别搜索，或切换到按支出类型搜索。
11. 可选：输入支出的商家。
12. 输入支出的交易日期。
13. 输入支出金额。
14. 选择支出的货币。 您将看到加载到应用中以供脱机使用的货币代码列表。 默认情况下，加载 400 个货币，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的货币不在该列表中，请选择 **搜索** 进行在线搜索。 按货币搜索，或切换到按名称搜索。
15. 选择 **完成**。
16. 若要向支出添加更多详细信息，请选择 **添加更多详细信息**。 可用字段取决于您的公司的支出管理配置。
17. 如果公司政策要求提供支出收据，请选择 **收据**，然后执行以下步骤：

    1. 选择 **捕获收据** 或 **附加收据**。
    2. 请执行以下步骤之一：

        - 如果选择了 **捕获收据**，请执行以下步骤：

            1. 选择 **拍照** 或 **选择图像**。
            2. 请执行以下步骤之一：

                - 如果选择了 **拍照**，请执行以下步骤：

                    1. 您将进入移动设备上的相机，让您可以对收据进行拍照。 拍照完毕后，请选择 **确定** 接受照片。
                    2. 可选：为照片输入名称，然后输入注释。

                - 如果选择了 **选择图像**，请执行以下步骤：

                    1. 在列表中选择一个图像。
                    2. 可选：为图像输入名称，然后输入注释。

            3.  选择 **完成**。

        - 如果选择了 **附加收据**，请执行以下步骤：

            1.  在列表中选择一个或多个图像。
            2.  选择 **完成**。

    3. 选择 **返回** 按钮返回支出详细信息。

18. 如果公司政策要求提供支出的来宾，请选择 **来宾**，然后执行以下步骤：

    1. 选择 **来宾**、**以前来宾** 或 **同事**。
    2. 请执行以下步骤之一：

        - 如果选择了 **来宾**，请执行以下步骤：

            1. 输入来宾的名称。
            2. 可选：输入来宾所在的组织和/或所在国家/地区。
            3. 可选：输入来宾的职务。
            4. 选择 **完成**。

        - 如果选择了 **以前来宾**，请执行以下步骤：

            1. 在列表中选择一个或多个以前的来宾。 您将看到已添加到以前的支出报表并加载到您的应用中以供脱机使用的以前来宾列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果以前来宾不在该列表中，请选择 **搜索** 进行在线搜索。 按名称搜索，或切换到按组织、国家/地区或职务搜索。
            2. 选择 **完成**。

        - 如果选择了 **同事**，请执行以下步骤：

            1. 在列表中选择一个或多个同事。 您将看到加载到应用中以供脱机使用的同事列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的同事不在该列表中，请选择 **搜索** 进行在线搜索。 按名称搜索，或切换到按公司或职务搜索。
            2. 选择 **完成**。

    3. 选择 **返回** 按钮返回支出详细信息。

19. 如果公司政策要求将支出逐条登记，请选择 **细化**，然后按照以下步骤操作：

    1. 选择要细化的第一个日期。
    2. 选择 **添加明细**。
    3. 选择支出明细的子类别。 您将看到加载到应用中以供脱机使用的支出子类别列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应该查看[移动平台](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started)。 如果您的子类别不在该列表中，请选择 **搜索** 进行在线搜索。 按支出子类别名称搜索。
    4. 输入明细的交易金额。
    5. 如果需要，编辑交易日期。
    6. 选择 **完成**。
    7. 重复上述步骤，直到完成添加所选日期的所有明细。
    8. 对于其他日期，您可以选择 **复制到第二天**，将明细复制到第二天。 或者，您可以选择要细化的日期，然后像第一个日期一样添加明细。
    9. 完成支出的细化后，选择 **返回** 按钮返回支出详细信息。

20. 选择 **返回** 按钮返回 **支出报表** 页。
21. 重复上述步骤，直到完成添加所有支出。
22. 选择 **提交**。
23. 为审批者输入注释。
24. 选择 **完成**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]