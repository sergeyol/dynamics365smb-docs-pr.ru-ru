---
title: "Практическое руководство. Учет потребления в пакетном режиме | Документы Майкрософт"
description: "Если выбран метод списания **Вручную**, учет компонентов производится вручную с использованием журнала потребления."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a><span data-ttu-id="50bf0-103">Практическое руководство. Учет потребления для производства в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="50bf0-103">How to: Batch Post Production Consumption</span></span>
<span data-ttu-id="50bf0-104">Если выбран метод списания **Вручную**, учет компонентов производится вручную с использованием журнала потребления.</span><span class="sxs-lookup"><span data-stu-id="50bf0-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="50bf0-105">Можно также настроить систему для автоматического учета (*списания*) компонентов при запуске или завершении производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="50bf0-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="50bf0-106">Дополнительные сведения см. в разделе [Включение списания компонентов в соответствии с производственным выпуском](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="50bf0-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="50bf0-107">Учет потребления для одной или нескольких строк производственного заказа</span><span class="sxs-lookup"><span data-stu-id="50bf0-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="50bf0-108">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал потребления**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="50bf0-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="50bf0-109">Заполните поля данными производственного заказа и данными о потреблении.</span><span class="sxs-lookup"><span data-stu-id="50bf0-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="50bf0-110">Если склад, на котором хранятся компоненты, настроен на использование ячеек, но не требует обработки подбора, присвойте код ячейки строке журнала для указания места на складе, откуда должны забираться товары.</span><span class="sxs-lookup"><span data-stu-id="50bf0-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="50bf0-111">Дополнительные сведения см. в разделе [Практическое руководство. Подбор для производства или сборки](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="50bf0-111">For more information, see [How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="50bf0-112">Выберите действие **Учесть**, чтобы учесть потребление.</span><span class="sxs-lookup"><span data-stu-id="50bf0-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="50bf0-113">Соответствующие операции в книге товаров уменьшаются.</span><span class="sxs-lookup"><span data-stu-id="50bf0-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="50bf0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="50bf0-114">See Also</span></span>  
<span data-ttu-id="50bf0-115">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="50bf0-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="50bf0-116">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="50bf0-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="50bf0-117">[Планирование](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="50bf0-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="50bf0-118">Наличие</span><span class="sxs-lookup"><span data-stu-id="50bf0-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="50bf0-119">Покупки</span><span class="sxs-lookup"><span data-stu-id="50bf0-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="50bf0-120">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50bf0-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
