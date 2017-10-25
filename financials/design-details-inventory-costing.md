---
title: "Сведения о проектировании — себестоимость запасов | Документы Майкрософт"
description: "Документация содержит подробные технические сведения о концепциях и принципах, используемых в функциях учета стоимости товаров в [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 38a37a6fb1e3b8a58fd28b3d8e678b93a110683b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="ff8db-103">Сведения о проектировании: себестоимость запасов</span><span class="sxs-lookup"><span data-stu-id="ff8db-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="ff8db-104">Документация содержит подробные технические сведения о концепциях и принципах, используемых в функциях учета стоимости товаров в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ff8db-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ff8db-105">Учет себестоимости запасов, который также называют управлением затратами, связан с записью и отчетностью по текущим бизнес-расходам.</span><span class="sxs-lookup"><span data-stu-id="ff8db-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="ff8db-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="ff8db-106">In This Section</span></span>  
[<span data-ttu-id="ff8db-107">Сведения о проектировании: методы учета себестоимости</span><span class="sxs-lookup"><span data-stu-id="ff8db-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="ff8db-108">Сведения о проектировании: применение товара</span><span class="sxs-lookup"><span data-stu-id="ff8db-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="ff8db-109">Сведения о проектировании: коррекция себестоимости</span><span class="sxs-lookup"><span data-stu-id="ff8db-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="ff8db-110">Сведения о проектировании: учет ожидаемой себестоимости</span><span class="sxs-lookup"><span data-stu-id="ff8db-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="ff8db-111">Сведения о проектировании: средняя себестоимость</span><span class="sxs-lookup"><span data-stu-id="ff8db-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="ff8db-112">Сведения о проектировании: отклонение</span><span class="sxs-lookup"><span data-stu-id="ff8db-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="ff8db-113">Сведения о проектировании: округление</span><span class="sxs-lookup"><span data-stu-id="ff8db-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="ff8db-114">Сведения о проектировании: компоненты себестоимости</span><span class="sxs-lookup"><span data-stu-id="ff8db-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="ff8db-115">Сведения о проектировании: периоды учета запасов</span><span class="sxs-lookup"><span data-stu-id="ff8db-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="ff8db-116">Сведения о проектировании: учет запасов</span><span class="sxs-lookup"><span data-stu-id="ff8db-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="ff8db-117">Сведения о проектировании: учет производственного заказа</span><span class="sxs-lookup"><span data-stu-id="ff8db-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="ff8db-118">Сведения о проектировании: учет заказа на сборку</span><span class="sxs-lookup"><span data-stu-id="ff8db-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="ff8db-119">Сведения о проектировании: выверка с главной книгой</span><span class="sxs-lookup"><span data-stu-id="ff8db-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="ff8db-120">Сведения о проектировании: счета в главной книге</span><span class="sxs-lookup"><span data-stu-id="ff8db-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="ff8db-121">Сведения о проектировании: переоценка</span><span class="sxs-lookup"><span data-stu-id="ff8db-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)
