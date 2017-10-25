---
title: "Планирование поставок | Документы Майкрософт"
description: "Подготовьте подробный выполняемый план и график окончательной сборки продукции для производственного спроса и для продаж."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b2a4a682100b0963b540f6f032c4b90061265cc1
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="planning"></a><span data-ttu-id="02721-103">Планирование</span><span class="sxs-lookup"><span data-stu-id="02721-103">Planning</span></span>
<span data-ttu-id="02721-104">Производственные операции, необходимые для преобразования затраченных ресурсов в готовую продукцию, должны быть запланированы по дням или неделям, в зависимости от объема и характера товаров.</span><span class="sxs-lookup"><span data-stu-id="02721-104">The production operations required to transform inputs into finished goods must be planned daily or weekly depending on the volume and nature of the products.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="02721-105"> предлагает функции снабжения для выполнения ожидаемых и фактических требований, возникающих вследствие продажи, сборки и производства, а также функции распределенного планирования с использованием единиц хранения и перемещений между складами.</span><span class="sxs-lookup"><span data-stu-id="02721-105"> offers features to supply for anticipated and actual demand from sale, assembly, and production as well as features for distribution planning using stockkeeping units and location transfers.</span></span>

> [!NOTE]
> <span data-ttu-id="02721-106">В этом разделе в основном описывается планирование для организаций, участвующих в управлении производством или сборкой, в которых соответствующие заказы на поставку могут быть производственными заказами, заказами на сборку, заказами на перемещение или заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="02721-106">This topic mainly describes planning for companies involved in manufacturing or assembly management where the resulting supply orders can be either production, assembly, transfer, or purchase orders.</span></span> <span data-ttu-id="02721-107">Основной интерфейс для планирования — это окно **Журнал планирования**.</span><span class="sxs-lookup"><span data-stu-id="02721-107">The main interface for this planning work is the **Planning Worksheet** window.</span></span>

> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="02721-108"> также поддерживает планирование поставок для оптовых организаций, в которых соответствующие заказы на поставку могут быть только заказами на перемещение или на покупку.</span><span class="sxs-lookup"><span data-stu-id="02721-108"> also supports supply planning for wholesale companies where the resulting supply orders can only be transfer and purchase orders.</span></span> <span data-ttu-id="02721-109">Основной интерфейс для этой работы планирования — окно **Журнал заявок**, которое неявно описывается в этом разделе, так как большинство функций планирования относятся к обоим журналам.</span><span class="sxs-lookup"><span data-stu-id="02721-109">The main interface for this planning work is the **Requisition Worksheet** window, which is described indirectly in this topic as most planning functionality applies to both worksheets.</span></span>

<span data-ttu-id="02721-110">Чтобы можно было планировать и выполнять производственные заказы, необходимо настроить производственные мощности, например создать производственные календари, маршруты, производственные спецификации и машинные центры.</span><span class="sxs-lookup"><span data-stu-id="02721-110">Before you can plan and execute production orders, you must configure production capacities, such as creating shop calendars, routings, production BOMs, and machine centers.</span></span> <span data-ttu-id="02721-111">Дополнительные сведения см. в разделе [Настройка производства](production-configure-production-processes.md).</span><span class="sxs-lookup"><span data-stu-id="02721-111">For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).</span></span>

<span data-ttu-id="02721-112">Планирование можно рассматривать как подготовку, необходимую для заказов на поставку в отделах сборки или производства для удовлетворения потребностей.</span><span class="sxs-lookup"><span data-stu-id="02721-112">Planning can be seen as the preparation required supply orders in the assembly or manufacturing departments to fulfill demand.</span></span> <span data-ttu-id="02721-113">Дополнительные сведения см. в разделах [Управление сборкой](assembly-assemble-items.md) и [Производство](production-manage-manufacturing.md).</span><span class="sxs-lookup"><span data-stu-id="02721-113">For more information, see [Assembly Management](assembly-assemble-items.md) and [Manufacturing](production-manage-manufacturing.md).</span></span>

<span data-ttu-id="02721-114">В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.</span><span class="sxs-lookup"><span data-stu-id="02721-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="02721-115">**Задача**</span><span class="sxs-lookup"><span data-stu-id="02721-115">**To**</span></span>|<span data-ttu-id="02721-116">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="02721-116">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="02721-117">Краткое введение в использование системы планирования для выявления и определения приоритетов требования и предложения сбалансированного плана снабжения.</span><span class="sxs-lookup"><span data-stu-id="02721-117">Get a brief introduction to how the planning system can be used to detect and prioritize demand and suggest a balanced supply plan.</span></span>|[<span data-ttu-id="02721-118">О функциональности планирования</span><span class="sxs-lookup"><span data-stu-id="02721-118">About Planning Functionality</span></span>](production-about-planning-functionality.md)|
|<span data-ttu-id="02721-119">Сведения о том, как работают все аспекты системы планирования и как скорректировать алгоритмы для выполнения требований планирования в различных средах.</span><span class="sxs-lookup"><span data-stu-id="02721-119">Understand how all aspects of the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="02721-120">Сведения о проектировании: планирование поставок</span><span class="sxs-lookup"><span data-stu-id="02721-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|
|<span data-ttu-id="02721-121">Изучение различий логики планирования для требований на складах в соответствии с настройкой единицы хранения и требований без кодов склада</span><span class="sxs-lookup"><span data-stu-id="02721-121">Learn how the planning logic differentiates between demand at locations according to the SKU setup and demand without location codes.</span></span>|[<span data-ttu-id="02721-122">Планирование со складами и без складов</span><span class="sxs-lookup"><span data-stu-id="02721-122">Planning With or Without Locations</span></span>](production-planning-with-without-locations.md)|
|<span data-ttu-id="02721-123">Прогноз производственного спроса на основании ожидаемых продаж и производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="02721-123">Forecast production demand presented by expected sales and production orders.</span></span>|[<span data-ttu-id="02721-124">Практическое руководство. Создание прогноза производства</span><span class="sxs-lookup"><span data-stu-id="02721-124">How to: Create a Production Forecast</span></span>](production-how-to-create-a-forecast.md)|  
|<span data-ttu-id="02721-125">Автоматическое создание взаимно однозначных производственных заказов на основании заказа на продажу для покрытия конкретного спроса по этой строке заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="02721-125">Create one-to-one production orders automatically from a sales order to cover the exact demand of that sales order line.</span></span>|[<span data-ttu-id="02721-126">Практическое руководство. Создание производственных заказов из заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="02721-126">How to: Create Production Orders from Sales Orders</span></span>](production-how-to-create-production-orders-from-sales-orders.md)|
|<span data-ttu-id="02721-127">Создание проектного производственного заказа непосредственно на основании многострочного заказа на продажу, представляющего рабочий проект</span><span class="sxs-lookup"><span data-stu-id="02721-127">Create a project production order directly from a multiline sales order representing a production project.</span></span>|[<span data-ttu-id="02721-128">Практическое руководство. Планирование заказов проекта</span><span class="sxs-lookup"><span data-stu-id="02721-128">How to: Plan Project Orders</span></span>](production-how-to-plan-project-orders.md)|
|<span data-ttu-id="02721-129">Использование окна **Планирование заказов** для составления вручную плана продаж или требований производства, отдельно для каждого уровня производственной спецификации</span><span class="sxs-lookup"><span data-stu-id="02721-129">Use the **Order Planning** window to manually plan for sales or production demand one production BOM level at a time.</span></span>|[<span data-ttu-id="02721-130">Практическое руководство. Последовательное планирование по каждому заказу</span><span class="sxs-lookup"><span data-stu-id="02721-130">How to: Plan for New Demand Order by Order</span></span>](production-how-to-plan-for-new-demand.md)|
|<span data-ttu-id="02721-131">Использование окна **Журнал планирования** для запуска обоих параметров MPS и MRP для автоматического создания общего или подробного плана поставки на всех уровнях товаров.</span><span class="sxs-lookup"><span data-stu-id="02721-131">Use the **Planning Worksheet** window to run both the MPS and MRP options to automatically create either a high-level or detailed supply plan at all item levels.</span></span>|[<span data-ttu-id="02721-132">Практическое руководство. Выполнение полного планирования, MPS или MRP</span><span class="sxs-lookup"><span data-stu-id="02721-132">How to: Run Full Planning, MPS or MRP</span></span>](production-how-to-run-mps-and-mrp.md)|
|<span data-ttu-id="02721-133">Запуск журнала заявок для автоматического создания подробный план поставки для выполнения требования товаров, которые пополняются только посредством покупки или перемещения</span><span class="sxs-lookup"><span data-stu-id="02721-133">Run the requisition worksheet to automatically create a detailed supply plan to cover demand for items that are replenished by purchase or transfer only.</span></span>|<span data-ttu-id="02721-134">Страница **Журнал заявок**</span><span class="sxs-lookup"><span data-stu-id="02721-134">**Requisition Worksheet** page</span></span>|  
|<span data-ttu-id="02721-135">Создание или обновление производственного заказа как операций с запланированным маршрутом в основном плане производства</span><span class="sxs-lookup"><span data-stu-id="02721-135">Initiate or update a production order as rough-scheduled operations in the master production schedule.</span></span>|[<span data-ttu-id="02721-136">Практическое руководство. Прямое перепланирование или обновление производственных заказов</span><span class="sxs-lookup"><span data-stu-id="02721-136">How to: Replan or Refresh Production Orders Directly</span></span>](production-how-to-replan-refresh-production-orders.md)|
|<span data-ttu-id="02721-137">Перерасчет календарей производственных или машинных центров в связи с изменением планирования.</span><span class="sxs-lookup"><span data-stu-id="02721-137">Recalculate work or machine center calendars due to planning changes.</span></span>|<span data-ttu-id="02721-138">Пункт "Расчет календаря рабочего центра" в разделе [Практическое руководство. Настройка производственных календарей](production-how-to-create-work-center-calendars.md)</span><span class="sxs-lookup"><span data-stu-id="02721-138">"To calculate a work center calendar" section in [How to: Set Up Shop Calendars](production-how-to-create-work-center-calendars.md)</span></span>|
|<span data-ttu-id="02721-139">Трассирование требования по заказу (трассируемое количество), прогноза, общего заказа продажи или параметров планирования (нетрассируемое количество), ставших причиной создания соответствующей строки планирования</span><span class="sxs-lookup"><span data-stu-id="02721-139">Track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>|[<span data-ttu-id="02721-140">Практическое руководство. Отслеживание связей между спросом и предложением</span><span class="sxs-lookup"><span data-stu-id="02721-140">How to: Track Relations Between Demand and Supply</span></span>](production-how-track-demand-supply.md)|
|<span data-ttu-id="02721-141">Просмотрите ожидаемый доступный запас товара различными способами и определите полные потребности, плановые поступления по заказу и другие события, влияющие на него с течением времени.</span><span class="sxs-lookup"><span data-stu-id="02721-141">View an item's projected available inventory by different views and see which gross requirements, planned order receipts, and other events influence it over time.</span></span>|[<span data-ttu-id="02721-142">Практическое руководство. Просмотр наличия товара</span><span class="sxs-lookup"><span data-stu-id="02721-142">How to: View the Availability of Items</span></span>](inventory-how-availability-overview.md)|  
|<span data-ttu-id="02721-143">Выполнение выбранных действий планирования, таких как изменение или добавление строк журнала планирования, в графическом представлении плана поставки.</span><span class="sxs-lookup"><span data-stu-id="02721-143">Perform selected planning activities, such as changing or adding planning worksheet lines, in a graphical view of the supply plan.</span></span>|[<span data-ttu-id="02721-144">Практическое руководство. Изменение предложений по планированию в графическом виде</span><span class="sxs-lookup"><span data-stu-id="02721-144">How to: Modify Planning Suggestions in a Graphical View</span></span>](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a><span data-ttu-id="02721-145">См. также</span><span class="sxs-lookup"><span data-stu-id="02721-145">See Also</span></span>
[<span data-ttu-id="02721-146">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="02721-146">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="02721-147">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="02721-147">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="02721-148">Наличие</span><span class="sxs-lookup"><span data-stu-id="02721-148">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="02721-149">Покупки</span><span class="sxs-lookup"><span data-stu-id="02721-149">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="02721-150">[Сведения о проектировании: планирование поставок](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="02721-150">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="02721-151">Рекомендации по настройке. Планирование поставок</span><span class="sxs-lookup"><span data-stu-id="02721-151">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="02721-152">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02721-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
