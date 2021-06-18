---
title: 示例数据安装
description: 此主题提供有关在 Project Service Automation 中安装示例数据的信息。
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 19fae15bf309936cab415c2a71a414ab37837fce
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007265"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Project Service 应用程序的示例数据安装

[!include [banner](../includes/psa-now-project-operations.md)]

为帮助您构建自己的演示环境，Microsoft 提供演示您的应用程序功能的可下载示例数据包。 有两种类型的示例数据包：
- 引用/设置数据
- 演示数据（引用/设置和事务数据，如工作订单和项目）

示例 **引用** 数据包可安装在三个不同包中，以便可以仅安装 Project Service 的数据或仅安装 Field Service 的数据，或者可以一次安装两个应用程序的示例数据。

示例引用/设置数据包有：

- [**V902PSMasterData** - 仅用于 Project Service 版本 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - 仅用于 Field Service 版本 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x 和 Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

最新的 **演示** 数据包有：

 - [**FPSDemoData** - Field Service 8.x 和 Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   用户创建和配置部分的安装说明稍有不同，但其他方面与之前的 [**博客文章**](https://aka.ms/fpsdemodatablog)相同。 此包使用减少的演示数据集，大约需要 3 小时安装。

这些示例数据包仅提供英语版。

> [!IMPORTANT]
> **不能卸载示例数据。** 只应在演示、评估、培训或测试系统上安装这些包。 另请注意，不支持先安装单个包，然后再安装其他单个包。 （也就是说，您不能在安装 **PSMasterData** 后安装 **FSMasterData**，反之亦然。）如果您以后在任何时间发现自己需要两个应用程序的示例数据，您应该安装 **v902FPSMasterData** 包。

在安装任何示例数据包时，安装过程会执行以下操作：

- 为使用 Project Service、Field Service 或者两个应用程序（如果适用）创建或设置默认参数。

- 导入应用程序的示例数据，例如可预订资源、应用程序特定角色、销售和成本价目表、部门、销售流程记录及其他要演示重要功能的实体。  

通过 **演示数据** 包，您将获得上述及其他事务数据，如工作订单和项目。

想知道哪些功能可以通过示例数据演示？ 请参见[技术说明](#technical-notes)中的 Fabrikam Robotics 虚构场景。

如果您有安装这些示例数据包方面的问题，请[通过 fpsdemodata@microsoft.com 向我们发送电子邮件](mailto:fpsdemodata@microsoft.com)。

## <a name="requirements"></a>要求

安装协议假设您的目标实例（组织）满足以下条件：

- 基本语言为英语，基础货币为美元（USD、$）。

- 组织还没有 Project Service 或 Field Service 数据，或只有很少的新组织附带的默认数据。

- 业务应用程序的正确版本已经安装：
       
    - **对于 FPSDemoData 或 v902FPSMasterData：** 组织已经安装 Field Service 版本 8.x 和 Project Service 版本 3.x。

    - **对于 v902PSMasterData：** 组织已经安装 Project Service 版本 3.x。

    - **对于 v902FSMasterData：** 组织已经安装 Field Service 版本 8.x。

> [!NOTE]
> 如果需要在已有数据的现有 Project Service 和 Field Service 试用或演示环境最上层安装示例数据（不推荐），您需要暂停安装程序执行的安全预检验。 有关详细信息，请参阅下面的技术说明。

## <a name="prepare-for-installation"></a>准备安装

需要在安装最新版本 Windows（首选 Windows 10）的计算机上运行安装程序。

您应将计算机计划为保持连接到网络，并将 **设置/引用数据** 的安装计划为最长运行 **1 小时**。 （通常安装 **FPSMasterData** 大约需要 30 分钟，包括两个应用程序的示例数据。）对于 **FPSDemoData**，安装需要约 **3 小时**。

计算机应关闭屏幕保护程序功能。 否则，安装的会话凭据可能在屏幕保护程序加入时丢失（除非您全程保持会话处于活动状态）。

> [!div class="mx-imgBorder"]
> ![关闭屏幕保护程序的屏幕保护程序设置的屏幕截图](media/sample-data-1.png)

## <a name="download-and-unpack"></a>下载和解压缩

Project Service 和 Field Service 示例数据安装程序作为自解压的可执行文件分发。 文件名可能因示例数据包而不同，但是步骤是相同的，不论您安装的是哪个包。

在下载包后，运行 .exe 文件，然后接受条款和条件以解压缩 zip 压缩文件。 然后需要将该文件的内容提取到计算机上的文件夹。

根据操作系统及安全设置，您可能需要在解压缩 zip 文件后执行以下步骤：

1. 在 **v902FPSMasterData** / **PackageDeployer_FPSDemoData** 文件夹中找到并右键单击 **FPSDemoData.dll** 文件。

2. 选择 **取消阻止**。

3. 选择 **应用**。

4. 选择 **确定**。


## <a name="create-or-configure-users"></a>创建或配置用户

**FPSMasterData** 包需要六个用户，而 **FPSDemoData** 包需要一个用户。 请参阅您的示例数据包的正确说明。

## <a name="create-or-configure-users---setupreference-data-packages"></a>创建或配置用户 - 设置/引用数据包

**FPSMasterData** 包用于通过具有此处所述设置的名为 Spencer Low 的一个用户安装。 若要正确安装包，您需要在环境中创建（或临时重命名）用户以匹配接收的示例数据配置。

若要创建或配置用户，请转到 **设置** > **安全** > **用户** 并执行以下操作：

1. 将 UserFullname="Spencer Low" with username "spencerl"（**小写**）设置为项目经理和实践经理角色。

2. 选择 **Spencer Low** 用户，然后选择 **管理角色**。 找到并选择 **系统管理员** 角色，然后选择 **确定** 为 Spencer Low 授予完全管理员权限。 此步骤是必要的，可以确保创建的示例记录具有正确的用户所有权，因而正确填充视图。

3. 从下载的包，您需要将数据映射文件更新为默认用户上下文的电子邮件地址。 为此，打开 **PkgFolder**，然后找到并在记事本（或 Visual Studio 或其他 XML 编辑器）中打开 **ImportUserMapFile.xml** 文件。 将 **DefaultUserToMapTo=** 字段设置为 Spencer Low 用户的电子邮件地址。

4. 如果不使用用户名为 **spencerl** 的 Spencer Low，您需要更新其他文件。 打开 **DemoDataPreImportConfig.xml** 文件，然后找到 **userstocreateandconfigure** 标记。 将 **\<login\>** 标记更新为 Spencer Low 用户的用户名。 其他详细信息，请参阅[技术说明](#technical-notes)。

## <a name="create-or-configure-users---demo-data-package"></a>创建或配置用户 - 演示数据包

演示数据包需要六个用户。 要正确安装包，请执行以下操作：

 1. 转到 **设置** > **安全** > **用户**，创建或临时重命名现有用户以匹配接收的示例数据配置。
 
    仅基于人员的演示需要这些角色。  
    - 作为 Field Service 技术人员的用户全名="David So"   
    - 作为 Customer Service 和 Field Service 调度员的用户全名="Jamie Reding"   
    - 作为客户经理的用户全名="Molly Clark"   
    - 作为实践经理和项目经理的用户全名="Spencer Low"  
    - 作为团队成员的用户全名="Veronica Quek"   
    - 用户全名="William Contoso"
  
2. 为导入演示数据，请为上述管理员角色分派六个用户，以正确导入示例记录。 

3. 打开 **PkgFolder**，然后找到并打开 **ImportUserMapFile.xml**。 将 **新=** 字段更新为您的系统中对应用户的电子邮件地址。

   > [!div class="mx-imgBorder"]
   > ![UserMapFile 的屏幕截图](media/sample-data-7.png)

4. 如果您的 "Spencer Low" 全名用户的用户 ID 与 **"spencerl"** 不同，则需要更新其他文件。 打开 **DemoDataPreImportConfig.xml**，找到 **userstocreateandconfigure** 标记。 将 **\<login\>** 标记更新为 loginId（区分大小写）。 

5. 第一个用户的日历（在 **userstocreateandconfigure** 标记中）用于在导入演示数据时填充所有可预订资源的工作时间。 导航到 **设置** > **安全** > **用户**，找到您的 "Spencer Low" 用户“，然后打开“工作时间”选项。 编辑现有工作时间，选择 **从开始到结束的所有各周的定期计划** 选项。 确保 **工作时间设置为早晨 8 点 - 下午 5 点（9 小时），星期一至星期五，时区设置为太平洋时间（美国和加拿大）**。 这样可以确保项目和日程安排板正常显示。

**建议：** 如果您需要在安装示例数据期间出现错误时还原到起点，应在现在考虑创建组织的备份。 有关更多信息，请参阅[备份和还原实例](/dynamics365/customer-engagement/admin/backup-restore-instances)。

## <a name="run-the-package-deployer"></a>运行 Package Deployer。

1. 在 **v902FPSMasterData** 或 **PackageDeployer_FPSDemoData** 文件夹中找到并运行 **PackageDeployer.exe**。

2. 接受条款和条件。

3. 在下一个窗口中：

   a. 选择部署类型 **Office 365**。

   b. 使用在“创建或配置用户”中配置的系统管理员用户的用户和密码（用户名为 "spencerl" 的 "Spencer Low"）。

   c. 确保已选择 **显示可用组织列表**。

      > [!div class="mx-imgBorder"]
      > ![选中“显示可用组织列表”的 Package Deployer 窗口的屏幕截图](media/sample-data-2.png)

4. 选择要安装示例数据的组织。

5. 选择 **下一步** 直到您看到 **演示数据设置** 对话框。

   > [!div class="mx-imgBorder"]
   > ![演示数据安装程序状态窗口的屏幕截图](media/sample-data-3.png)

6. 在继续之前，请注意，安装示例数据最多可能需要一个小时（通常约为 10 分钟）。 您需要确保计算机在整个安装过程中保持开启并连接到网络，并确保会话保持活动状态。   

7. 在您准备就绪时，单击 **下一步** 开始示例数据安装过程。 在示例数据加载后，单击 **完成**。

## <a name="verify-the-sample-data-installation"></a>验证示例数据安装

为进行完整性检查，请确认在 Android Fabrikam 虚构场景中列出的实体记录和类型的数量按预期显示。

在完全加载示例数据后，作为 Spencer Low 用户身份登录并确认以下各项：

- 如果已安装 Project Service 应用程序，请转到 **Project Service** > **设置** > **价目表**。 确认数据集中存在记帐费率和成本费率并且具有各个国家/地区的相应货币。

- 如果已安装 Project Service 应用程序，请转到 **Universal Resource Scheduling** > **设置** > **部门**。 确认使用相应货币的成本价目表已与各个部门关联（不包括城市条目）。 如果缺少，找到并关联正确的成本价目表。

- 如果已安装 Field Service 应用程序，请转到 **Project Service** > **设置** > **价目表**。 确认记帐费率和成本费率存在。 转到 **Field Service** > **设置** > **价目表**，检查数据集中是否存在记帐费率和成本比率，且是否使用每个国家/地区的相应货币。

  > [!div class="mx-imgBorder"]
  > ![可用价目表的屏幕截图](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![可用部门的屏幕截图](media/sample-data-5.png)

## <a name="technical-notes"></a>技术说明

请参阅以下内容了解有关此数据安装的更多技术详细信息。

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>在现有数据之上安装示例数据（不推荐）

如果需要在已有数据的现有 Field Service 或 Project Service 试用或演示环境最上层安装示例数据，您需要暂停安装程序执行的安全预检验。

为此，请转到 **PkgFolder** 文件夹，使用记事本（或其他 XML 编辑器）找到并打开 **DemoDataPreImportConfig.xml** 文件。

找到以下值，然后将设置从 true 更改为 false：

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

此更改将使安装程序绕过一些重要的安全检查，包括：

- 确认没有多个可用 **部门** 记录，然后将其重命名为 **Fabrikam US**。

- 确认没有多个可用 **工作模板** 记录。

- 确认没有多个可用 **项目参数** 记录，然后将该条目重命名为 **Parameters**。

### <a name="configuration-components"></a>配置组件

在此预导入配置文件中有其他一些配置组件。 对于技术用户，其中一部分包括：

- **\<RequiredSolutions\>** 指定必备解决方案的安装及其版本号。

- **\<InstallSampleData\>** 控制应用的现成示例数据是否安装。

    - false - 跳过此内置数据（可移除）的安装

    - true - 在安装 FS 和 PSA 示例数据的同时安装内置数据

- **\<PreImportDataCollection\>** 指定要在主要示例数据安装前导入的平面文件数据映射和关联的记录。

- **\<EntitiesToEnableScheduling\>** 指定应该在 Microsoft Dynamics Scheduling（也称为 Universal Resource Scheduling）中为预订启用哪些实体。

- **\<UsersToCreateAndConfigure\>** 指定将在示例数据导入执行前创建的可预订资源（如果尚不存在）。 请注意，源系统示例数据可预订资源与每个资源的全名和登录信息上的目标系统可预订资源记录匹配。 因此，无法更改此预配置文件中的名称，除非您首先使用这些名称将示例数据导入目标系统，然后将可预订资源重命为随“启用的用户”记录设置的您需要的名称，然后再次导出数据以导入您的最终目标系统（相应更新 **ImportUserMapFile.xml** 旧条目和新条目）。

- **\<PluginsToDisable\>** 指定必须在导入示例数据时禁用并在以后重新启用的非常分散的明细项目插件。

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics 虚构场景

Field Service 和 Project Service 示例引用数据包安装 **Fabrikam 制造主数据 (v3.0.0.0) 解决方案**，以及约 4,000 个记录和约 40 个不同实体。 Field Service 或 Project Service 的单独示例数据包包含该应用程序的 **v902FPSMasterData** 示例数据的子集。 **演示数据** 包安装 **Fabrikam 制造演示数据 (v3.0.0.7) 解决方案**，其跨 148 个实体有约 22,000 个记录。

虚构公司 Fabrikam Robotics 是一家电子设备装配线机器人制造商，以其产品质量、创新和可靠的客户服务著称，包括安装计划、实施和持续的维护系统。 Fabrikam 总部设在美国 (Fabrikam US)，并在法国、印度、英国和瑞士有基于项目的服务运营。

Field service 运营集中于美国，大部分是在大西雅图地区。 该公司专注于利用物联网 (IoT) 连接监视客户资产的性能并提供日渐积极的现场服务。

示例数据的高级概述如下：

- 常见示例数据元素（两个应用程序）

    - 1 个用户

    - 71 个帐户

    - 137 个联系人

    - 各种交易类型和类别

    - 使用 1 个产品价目表的 50 种产品

    - 14 个价目表/成本列表

    - 3 个级别（评分值）2 个评分模型 31 个特征（资源技能）

- Project Service

    - 8 个部门

    - 6 个角色特定的利用率级别

    - 2.8k+ 角色价格规范

- Field Service

    - 4 个区域

    - 5 个工作订单类型

    - 22 项客户资产

    - 9 个事件类型，具有一系列关联的资源特征 (9)、服务 (13) 和服务任务 (13)
   
**演示数据** 包安装大约 179 个工作订单、12 个项目和关联的事务数据。 

### <a name="change-the-work-hours-for-sample-resources"></a>更改示例资源的工作时间

默认情况下，所有可预订资源均具有 24 个工作时数的日历。

如果需要更改示例可预订资源的工作时间，请转到 **Universal Resource Scheduling** > **计划** > **资源**。

选择用户（例如，Spencer Low）并将 Spencer 的工作时间更改为要应用于多个用户的时间。 转到 **Universal Resource Scheduling** > **设置** > **工作时间模板** 并编辑 **默认工作模板** 记录。 在 **模板资源** 字段中，选择具有您希望应用到其他资源的工作时间的用户。 转到 **Universal Resource Scheduling** > **计划** > **资源** > **可用的可预订资源**。 选择要更改的资源，然后选择 **设置日历**。 在 **工作模板** 下拉列表上，选择 **默认工作时间** 模板或具有正确模板资源的其他模板。 如果您转到日程安排板，您应该会看到资源现在已经更新了工作时间。

> [!div class="mx-imgBorder"]
> ![可用的可预订资源的屏幕截图](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]