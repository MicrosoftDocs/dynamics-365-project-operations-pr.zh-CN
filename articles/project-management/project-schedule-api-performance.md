---
title: 项目日程安排 API 性能
description: 本主题提供有关项目日程安排 API 性能基准的信息，并确定优化利用的最佳实践。
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593831"
---
# <a name="project-schedule-api-performance"></a>项目日程安排 API 性能

_**适用于**：基于资源/非库存场景的 Project Operations、精简部署 - 估价交易开单、Project for the Web_

本主题提供有关项目日程安排应用编程接口 (API) 性能基准的信息，并确定优化利用的最佳实践。

## <a name="project-scheduling-service"></a>项目计划服务
项目计划服务是一项在 Microsoft Azure 中运行的多租户服务。 它旨在通过在用户处理项目时提供快速流畅的体验来改善交互。 通过接受更改请求、处理这些请求，然后立即返回结果，从而获得此改进。 该服务异步保留到 Dataverse，并且不会阻止用户执行其他操作。

项目日程安排 API 依赖于项目计划服务来运行本主题后面部分中更详细描述的请求。

项目日程安排 API 旨在处理以下工作分解结构 (WBS) 实体：

  - Project
  - 项目任务
  - 项目任务依赖关系
  - 项目团队成员
  - 资源分派
  
支持现成字段和自定义字段。 除非另有说明，否则支持所有常见操作，例如创建、更新和删除。 有关详细信息，请参阅[使用项目日程安排 API 执行操作和计划实体](schedule-api-preview.md)。

作为项目日程安排 API 的一部分，添加了工作单位模式。 该模式称为 OperationSet，当必须在一个事务中处理多个请求时，可以使用该模式。

下图演示合作伙伴在使用此功能时将体验的流。

![Dataverse 和项目计划服务流。](./media/dataverse-project-scheduling-service-flow.png)

**步骤 1**：客户端对 Dataverse 中的 Open Data Protocol (OData) 终结点进行 API 调用，以创建 OperationSet。

**步骤 2**：新建 OperationSet 后，返回 **OperationSetId** 值。

**步骤 3**：客户端使用 **OperationSetId** 值提出另一个项目日程安排 API 请求。 结果是针对计划实体的一个创建、更新或删除请求。 当提出此请求时，会执行元数据验证。 如果验证失败，将终止请求，并返回错误。

**步骤 4a-4c**：这些步骤表示“接受”阶段。 客户端调用 **ExecuteOperationSetV1** API，在一个批处理任务中将所有更改发送到项目计划服务。 项目计划服务对批处理中的请求运行自己的验证。 任何验证失败都会导致撤消批处理并向调用方返回异常。 如果项目计划服务成功接受该批处理任务，则 OperationSet 状态将更新，以反映项目计划服务正在处理 OperationSet 这一事实。

**步骤 5**：此步骤表示“持续”阶段。 项目计划服务在事务中将批处理异步写入到 Dataverse。 如果写入操作成功，会将 OperationSet 标记为 **已完成**。 任何错误都会回滚事务和批处理，并将 OperationSet 标记为 **失败**。

## <a name="performance-methodology"></a>性能方法
执行时间被定义为从调用 **ExecuteOperationSetV1** API 起到项目计划服务完成写入 Dataverse 的这段时间。 所有操作总共运行 2,200 次，并报告了 P99 执行时间测量值。 测量了单记录操作和批量操作。

对于单记录操作，OperationSet 包含一个请求。 对于批量操作，它包含 20、50 或 100 个请求。 将分别报告每个批量大小。

这些操作在北美中的 UR 15 Project Operations 精简部署上运行。

## <a name="results"></a>结果​​
### <a name="create-operations"></a>创建操作
#### <a name="single-record-create-operations"></a>单记录创建操作
下表显示了创建单个记录的执行时间。 这些时间以秒为单位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">记录&nbsp;&nbsp;&nbsp;类型</th>
    <th class="tg-0lax" colspan="2">时间</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">任务</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">分配</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">团队成员</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">依赖关系</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>批量创建操作
下表显示了创建多个记录的执行时间。 具体而言，Microsoft 测量了在单个 OperationSet 中创建 20、50 和 100 条记录的执行时间。 这些时间以秒为单位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">记录&nbsp;&nbsp;&nbsp;类型</th>
    <th class="tg-0lax" colspan="6">时间</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 条记录</th>
    <th class="tg-0lax" colspan="2">50 条记录</th>
    <th class="tg-0lax" colspan="2">100 条记录</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">任务</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">分配</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">依赖关系</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> 此表中不包括对 **项目** 和 **团队成员** 实体的批量创建操作，因为这些操作的运行时与多次调用用于创建单条记录的 API 时的运行时类似。 这些 API 会在 Dataverse 中立即运行。

以下插图显示了当创建 20、50 和 100 条记录并且使用所有支持的字段时，**任务**、**分配** 和 **依赖项** 实体的执行时间图。

![创建记录执行时间图。](./media/create-record-execution-time.png)

### <a name="update-operations"></a>更新操作
#### <a name="single-record-update-operations"></a>单记录更新操作
下表显示了更新单个记录的执行时间。 这些时间以秒为单位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">记录&nbsp;&nbsp;&nbsp;类型</th>
    <th class="tg-0lax" colspan="2">时间</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填字段 </th>
    <th class="tg-0lax">所有受支持的字段</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">任务</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">团队成员</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支持对 **资源分配** 和 **项目任务依赖关系** 实体执行更新操作。

#### <a name="bulk-update-operations"></a>批量更新操作
下表显示了更新多个记录的执行时间。 具体而言，Microsoft 测量了在单个 OperationSet 中更新 20、50 和 100 条记录的执行时间。 这些时间以秒为单位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">记录&nbsp;&nbsp;&nbsp;类型</th>
    <th class="tg-0lax" colspan="6">时间</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 条记录</th>
    <th class="tg-0lax" colspan="2">50 条记录</th>
    <th class="tg-0lax" colspan="2">100 条记录</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
    <th class="tg-0lax">必填字段</th>
    <th class="tg-0lax">所有受支持的字段</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">任务</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">团队成员</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支持对 **资源分配** 和 **项目任务依赖关系** 实体执行更新操作。

以下插图显示了当更新 20、50 和 100 条记录并且使用所有支持的字段时，“任务”和“团队成员”实体的执行时间图。

![更新记录执行时间图。](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>删除操作
#### <a name="single-record-delete-operations"></a>单记录删除操作
下表显示了删除单个记录的执行时间。 这些时间以秒为单位。

| 记录类型 | 时间  |
|-------------|-------|
| 任务        | 20.12 |
| 分配  | 10.86 |
| 团队成员 | 12.52 |
| 依赖关系  | 20.89 |

> [!NOTE]
> 不支持对 **项目** 实体执行删除操作。

#### <a name="bulk-delete-operations"></a>批量删除操作
下表显示了删除多个记录的执行时间。 具体而言，Microsoft 测量了在单个 OperationSet 中删除 20、50 和 100 条记录的执行时间。 这些时间以秒为单位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">记录&nbsp;&nbsp;&nbsp;类型</th>
    <th class="tg-0lax" colspan="3">时间</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 条记录</th>
    <th class="tg-0lax">50 条记录</th>
    <th class="tg-0lax">100 条记录</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">任务</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">分配</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">团队成员</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">依赖关系</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支持对 **项目** 实体执行删除操作。

以下插图显示了当删除 20、50 和 100 条记录时，**任务**、**分配**、**团队成员** 和 **依赖项** 实体的执行时间图。

![删除记录执行时间图。](./media/delete-record-execution-time.png)

## <a name="observations"></a>观察结果
对于每个记录操作，**ExecuteOperationSet** API 向项目计划服务发送请求大约需要 800 毫秒。 之后，项目计划服务大约需要五秒钟来处理有效负载并调用 Dataverse。 其余执行时间用于运行业务逻辑以及将数据写入 Dataverse 中的数据库。

创建、更新或删除 100 条记录后，**ExecuteOperationSet** API 将请求发送给项目计划服务大约需要三秒钟。 之后，项目计划服务大约需要五秒钟来处理请求并调用 Dataverse。 对于 OperationSet 中的所有记录，批量操作必须一次性支付 **项目计划服务税**。 因此，批量操作的平均执行时间明显低于单记录操作。

## <a name="scenarios"></a>方案
下表显示了使用项目日程安排 API 完成特定方案时的执行时间。 这些时间以秒为单位。

| 方案                                                                   | 时间  |
|----------------------------------------------------------------------------|-------|
| 创建具有 40 个任务的项目。                                      | 36.01 |
| 创建具有 40 个任务和 20 个依赖项的项目。                  | 38.11 |
| 创建具有 40 个任务和 30 项分配的项目。                   | 60.17 |
| 创建具有 40 个任务、20 个依赖项和 30 项分配的项目。 | 60.27 |

## <a name="best-practices"></a>最佳实践
基于前面的方案结果，API 在以下情况下性能更佳：

  - 将尽可能多的操作组合在一起。 批量操作的平均运行时优于单记录操作的平均运行时。 使用的 OperationSets 数越少，平均执行时间越短。
  - 仅设置完成方案所需的最少属性。 对 OperationSet 请求中包括的不必要字段的类型具有选择性。 包含外键或汇总字段的字段将对性能有负面影响。
