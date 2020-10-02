---
title: 产品
description: 此主题提供有关产品目录的信息，您可以使用产品目录向客户提供有关您的组织所提供的产品和定价的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898700"
---
# <a name="products"></a><span data-ttu-id="b2d14-103">产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-103">Products</span></span>

<span data-ttu-id="b2d14-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b2d14-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2d14-105">产品是您的业务支柱。</span><span class="sxs-lookup"><span data-stu-id="b2d14-105">Products are the backbone of your business.</span></span> <span data-ttu-id="b2d14-106">Dynamics 365 Sales Professional 中的产品目录是产品和定价信息的集合。</span><span class="sxs-lookup"><span data-stu-id="b2d14-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="b2d14-107">让您的销售代表轻松地通过快速创建产品目录提高销量。</span><span class="sxs-lookup"><span data-stu-id="b2d14-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="b2d14-108">添加产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-108">Add a product</span></span>

1.  <span data-ttu-id="b2d14-109">确保您拥有 Sales Professional 管理员或系统管理员角色，从而可以在 Dynamics 365 Sales Professional 中添加产品。</span><span class="sxs-lookup"><span data-stu-id="b2d14-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="b2d14-110">在站点地图中，在**设置**下，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="b2d14-111">选择**添加产品**并填写以下信息：</span><span class="sxs-lookup"><span data-stu-id="b2d14-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="b2d14-112">**客户**</span><span class="sxs-lookup"><span data-stu-id="b2d14-112">**Name**</span></span>
    -  <span data-ttu-id="b2d14-113">**产品编号**</span><span class="sxs-lookup"><span data-stu-id="b2d14-113">**Product ID**</span></span>
    -  <span data-ttu-id="b2d14-114">**父级**：为产品选择父产品系列。</span><span class="sxs-lookup"><span data-stu-id="b2d14-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="b2d14-115">如果您在产品系列中创建子产品，父产品系列的名称在此处填充。</span><span class="sxs-lookup"><span data-stu-id="b2d14-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="b2d14-116">在保存记录后这无法更改。</span><span class="sxs-lookup"><span data-stu-id="b2d14-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="b2d14-117">**有效期的开始日期**/**有效期的结束日期**：通过选择**有效期的开始日期**和**有效期的结束日期**日期定义产品的有效期间。</span><span class="sxs-lookup"><span data-stu-id="b2d14-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="b2d14-118">**计价单位组**：选择计价单位组。</span><span class="sxs-lookup"><span data-stu-id="b2d14-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="b2d14-119">计价单位组是销售产品时所采用各个计价单位的集合，并定义各个项目如何被分组到更大的数量。</span><span class="sxs-lookup"><span data-stu-id="b2d14-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="b2d14-120">例如，如果您正在将种子添加为产品，则您可能已创建一个名称为“种子”的计价单位组，且已定义其基本计价单位为“包”。</span><span class="sxs-lookup"><span data-stu-id="b2d14-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="b2d14-121">**默认单位**：选择销售产品最常用的计价单位。</span><span class="sxs-lookup"><span data-stu-id="b2d14-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="b2d14-122">计价单位是您销售产品时使用的数量或测量单位。</span><span class="sxs-lookup"><span data-stu-id="b2d14-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="b2d14-123">例如，如果您将种子添加为产品，则您可以以包、盒或盘为单位对其进行销售。</span><span class="sxs-lookup"><span data-stu-id="b2d14-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="b2d14-124">每个均变为产品的计价单价。</span><span class="sxs-lookup"><span data-stu-id="b2d14-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="b2d14-125">如果种子通常以包为基本计价单位进行销售，则选择包为计价单位。</span><span class="sxs-lookup"><span data-stu-id="b2d14-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="b2d14-126">**默认价目表**：如果这是新产品，则此字段为只读字段。</span><span class="sxs-lookup"><span data-stu-id="b2d14-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="b2d14-127">必须先完成所有必填字段并保存记录，然后才能选择默认价目表。</span><span class="sxs-lookup"><span data-stu-id="b2d14-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="b2d14-128">尽管不需要设置默认价目表，但在保存产品记录之后，最好为每个产品设置一个默认价目表。</span><span class="sxs-lookup"><span data-stu-id="b2d14-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="b2d14-129">这样，如果客户记录未包含价目表，则 Sales 可以使用默认价目表来生成报价单、订单和发票。</span><span class="sxs-lookup"><span data-stu-id="b2d14-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="b2d14-130">**支持小数**：必须输入介于 0 和 5 之间的整数。</span><span class="sxs-lookup"><span data-stu-id="b2d14-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="b2d14-131">如果产品无法拆分成部分数量，请输入 0。</span><span class="sxs-lookup"><span data-stu-id="b2d14-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="b2d14-132">如果产品没有关联的价目表，将根据该字段中的值验证报价单、订单或发票产品记录中**数量**字段的精度。</span><span class="sxs-lookup"><span data-stu-id="b2d14-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="b2d14-133">**主题**：将此产品与主题相关联。</span><span class="sxs-lookup"><span data-stu-id="b2d14-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="b2d14-134">可以使用主题对产品进行分类并筛选报表。</span><span class="sxs-lookup"><span data-stu-id="b2d14-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="b2d14-135">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-135">Select **Save**.</span></span>
5.  <span data-ttu-id="b2d14-136">在**其他详细信息**选项卡上，在**价目表项**部分，选择**更多命令**，然后选择**添加新价目表项**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="b2d14-137">在**其他详细信息**选项卡上的**产品关系**部分，选择**更多命令**图标，然后选择**添加新产品关系**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="b2d14-138">在**新建产品关系**窗体中，输入以下详细信息，然后在命令栏中，选择**保存并关闭**：</span><span class="sxs-lookup"><span data-stu-id="b2d14-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="b2d14-139">**相关产品**：选择要作为相关产品添加到正在处理的现有产品记录中的产品。</span><span class="sxs-lookup"><span data-stu-id="b2d14-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="b2d14-140">**销售关系类型**：选择是否要添加作为追加销售、交叉销售、配件或替代产品的产品。</span><span class="sxs-lookup"><span data-stu-id="b2d14-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="b2d14-141">**方向**：选择产品之间的关系是单向还是双向的。</span><span class="sxs-lookup"><span data-stu-id="b2d14-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="b2d14-142">如果选择单向，您在**相关产品**中选择的产品将显示为现有产品的推荐，但是反过来就不是这样了。</span><span class="sxs-lookup"><span data-stu-id="b2d14-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="b2d14-143">在“产品”窗体中，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="b2d14-144">导入产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-144">Import products</span></span>

<span data-ttu-id="b2d14-145">可以使用导入模板将产品数据批量导入 Dynamics 365 Sales 中。</span><span class="sxs-lookup"><span data-stu-id="b2d14-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="b2d14-146">修改产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-146">Revise a product</span></span>

<span data-ttu-id="b2d14-147">根据需要修改产皮属性，保持产品库存更新，并且重新发布信息，以便您的销售代理能够看到最新的库存变动。</span><span class="sxs-lookup"><span data-stu-id="b2d14-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="b2d14-148">请确保您具有以下安全角色之一或具有等效权限：系统管理员、系统定制员、销售经理、销售副总裁、市场营销副总裁或 CEO 业务经理。</span><span class="sxs-lookup"><span data-stu-id="b2d14-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="b2d14-149">在站点地图中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b2d14-150">打开要更改的可用产品，然后在命令栏上选择**修订**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="b2d14-151">在**确认修订**对话框中，选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="b2d14-152">此操作会将产品状态更改为**正在修改**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="b2d14-153">更改完毕后，在命令栏上选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="b2d14-154">若要撤消更改并继续使用上一个可用产品版本，请选择**还原**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="b2d14-155">这会将产品的状态更改回**可用**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="b2d14-156">克隆产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-156">Clone a product</span></span> 

<span data-ttu-id="b2d14-157">在创建新产品时，通过克隆现有对象可以节省时间。</span><span class="sxs-lookup"><span data-stu-id="b2d14-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="b2d14-158">这可以创建原始记录副本，此副本包含所有详细信息（名称和 ID 除外）。</span><span class="sxs-lookup"><span data-stu-id="b2d14-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="b2d14-159">请确保您具有以下安全角色之一或具有等效权限：系统管理员、系统定制员、销售经理、销售副总裁、市场营销副总裁或 CEO 业务经理。</span><span class="sxs-lookup"><span data-stu-id="b2d14-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="b2d14-160">在站点地图中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b2d14-161">选择要克隆的产品记录，并在命令栏上选择**克隆**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="b2d14-162">出现确认对话框。</span><span class="sxs-lookup"><span data-stu-id="b2d14-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="b2d14-163">选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-163">Select **Confirm**.</span></span>

<span data-ttu-id="b2d14-164">将打开新产品记录及其与原产品相同的详细信息（名称和 ID 除外）。</span><span class="sxs-lookup"><span data-stu-id="b2d14-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="b2d14-165">停用产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-165">Retire a product</span></span> 

<span data-ttu-id="b2d14-166">如果组织不再销售某产品，请停用该产品，以便不再向您的销售代理提供该产品。</span><span class="sxs-lookup"><span data-stu-id="b2d14-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="b2d14-167">请确保您具有系统管理员或 Sales Professional 管理员角色或等效权限。</span><span class="sxs-lookup"><span data-stu-id="b2d14-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="b2d14-168">在站点地图中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b2d14-169">打开要停用的可用产品，然后在命令栏上选择**停用**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="b2d14-170">在**确认停用**对话框中，选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="b2d14-171">删除产品</span><span class="sxs-lookup"><span data-stu-id="b2d14-171">Delete a product</span></span>

<span data-ttu-id="b2d14-172">若要停止销售产品，请将其删除。</span><span class="sxs-lookup"><span data-stu-id="b2d14-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2d14-173">无法恢复已删除的记录。</span><span class="sxs-lookup"><span data-stu-id="b2d14-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="b2d14-174">请确保您具有系统管理员或 Sales Professional 管理员角色或等效权限。</span><span class="sxs-lookup"><span data-stu-id="b2d14-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="b2d14-175">在站点地图中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b2d14-176">选择要删除的产品记录，并在命令栏上选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="b2d14-177">在**确认删除**对话框中，选择**继续**。</span><span class="sxs-lookup"><span data-stu-id="b2d14-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="b2d14-178">产品的数量因子</span><span class="sxs-lookup"><span data-stu-id="b2d14-178">Quantity factors for products</span></span>

<span data-ttu-id="b2d14-179">数量因子支持基于订阅的产品的销售。</span><span class="sxs-lookup"><span data-stu-id="b2d14-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="b2d14-180">对于基于订阅的产品，报价单或项目合同子项中的数量表示为用户的月数。</span><span class="sxs-lookup"><span data-stu-id="b2d14-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="b2d14-181">通常，订阅软件的价格以每用户每月价格的形式存储在目录中。</span><span class="sxs-lookup"><span data-stu-id="b2d14-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="b2d14-182">但是，可改用其他时间描述。</span><span class="sxs-lookup"><span data-stu-id="b2d14-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="b2d14-183">销售阶段中，报价单明细中的价格通常为与 IT 销售代表协商并达成折扣的每用户每月价格。</span><span class="sxs-lookup"><span data-stu-id="b2d14-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="b2d14-184">每笔交易的用户数量和订阅月数不同。</span><span class="sxs-lookup"><span data-stu-id="b2d14-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="b2d14-185">用于计算报价单明细金额的数量是用户数与订阅月数的乘积。</span><span class="sxs-lookup"><span data-stu-id="b2d14-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="b2d14-186">数量因子依赖于产品属性。</span><span class="sxs-lookup"><span data-stu-id="b2d14-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="b2d14-187">为产品配置特定属性时，您可以将这些属性中的一小部分或全部标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="b2d14-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="b2d14-188">系统将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="b2d14-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="b2d14-189">将为其配置了数量因子的产品添加到报价单明细时，报价单明细中的**数量**字段将成为只读字段。</span><span class="sxs-lookup"><span data-stu-id="b2d14-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="b2d14-190">为充当数量因子的产品属性输入值之后，将计算报价单明细的数量。</span><span class="sxs-lookup"><span data-stu-id="b2d14-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="b2d14-191">例如，如果存在以下属性：</span><span class="sxs-lookup"><span data-stu-id="b2d14-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="b2d14-192">**用户数**：用户的数量</span><span class="sxs-lookup"><span data-stu-id="b2d14-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="b2d14-193">**月数**：订阅的月数</span><span class="sxs-lookup"><span data-stu-id="b2d14-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="b2d14-194">**产品 SKU**</span><span class="sxs-lookup"><span data-stu-id="b2d14-194">**Product SKU**</span></span> 

<span data-ttu-id="b2d14-195">可以通过编辑产品明细的属性，将**用户数**和**月数**属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="b2d14-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 
