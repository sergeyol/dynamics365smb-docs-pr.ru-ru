---
title: "Управление сервисной ценой | Документы Майкрософт"
description: "В этом разделе описывается, как использовать лучшие цены в сервисных заказах, создавать для клиентов персонализированные соглашения по сервисным ценам, повышать эффективность работы обслуживающего персонала и ускорять процесс выставления счетов."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e9eb165c8ccb196f687c11f4cb4353d88c71de3c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="service-price-management"></a><span data-ttu-id="14896-103">Управление сервисной ценой</span><span class="sxs-lookup"><span data-stu-id="14896-103">Service Price Management</span></span>
<span data-ttu-id="14896-104">Функциональные возможности управления сервисной ценой позволяют использовать лучшие цены в сервисных заказах, создавать для клиентов персонализированные соглашения по сервисным ценам, повышать эффективность работы обслуживающего персонала и ускорять процесс выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="14896-104">The service price management functionality lets you apply the best price to service orders, set up personalized service price agreements for customers, improve service employees' efficiency, and accelerate the invoicing process.</span></span>  
  
<span data-ttu-id="14896-105">Управление сервисной ценой позволяет создавать различные группы сервисных цен, чтобы учитывать сервисный товар или группу сервисных товаров, а также тип неисправности, с которой связана сервисная задача.</span><span class="sxs-lookup"><span data-stu-id="14896-105">Service price management lets you set up different service price groups so you can consider the service item or service item group, in addition to the type of fault that the service task involves.</span></span> <span data-ttu-id="14896-106">Подобные группы можно настраивать на ограниченный срок или для определенного клиента или валюты.</span><span class="sxs-lookup"><span data-stu-id="14896-106">You can set up these groups for a limited period of time, or for a specific customer or currency.</span></span> <span data-ttu-id="14896-107">Можно использовать схемы расчета цен как шаблоны, чтобы соотносить каждую отдельную цену с определенным сервисным заданием.</span><span class="sxs-lookup"><span data-stu-id="14896-107">You can use price calculation structures as templates to assign a specific price to a specific service task.</span></span>  
  
<span data-ttu-id="14896-108">Например, можно назначить определенные товары, которые будут соотноситься с данной сервисной ценой, а также тип необходимых работ.</span><span class="sxs-lookup"><span data-stu-id="14896-108">For example, this makes it possible to assign specific items included in the service price, in addition to the type of work included.</span></span> <span data-ttu-id="14896-109">Аналогично можно использовать различные суммы НДС и суммы скидок для разных ценовых групп сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="14896-109">This also makes it possible to use different VAT and discount amounts for different service price groups.</span></span> <span data-ttu-id="14896-110">Чтобы избежать ошибок при применении цен, можно назначить фиксированную, минимальную или максимальную цену в зависимости от соглашений, заключенных с клиентами.</span><span class="sxs-lookup"><span data-stu-id="14896-110">To make sure that the correct prices are applied, you can assign fixed, minimum, or maximum prices, depending on the agreements that you have with your customers.</span></span>  
  
<span data-ttu-id="14896-111">Перед корректировкой цены для какого-либо сервисного товара по сервисному заказу вам предлагается обзор последствий такой корректировки цены.</span><span class="sxs-lookup"><span data-stu-id="14896-111">Before adjusting the price of a service item on a service order, you are provided with an overview of what the results of the price adjustment will be.</span></span> <span data-ttu-id="14896-112">Можно согласиться с этими результатами или же внести дополнительные изменения, если необходимо получить другой результат.</span><span class="sxs-lookup"><span data-stu-id="14896-112">You can approve of these results, or you can make additional changes, if you want to have a different result.</span></span> <span data-ttu-id="14896-113">Полная коррекция осуществляется построчно, то есть новые строки при этом не создаются.</span><span class="sxs-lookup"><span data-stu-id="14896-113">The whole adjustment is performed line by line, which means that there are no additional lines created.</span></span>  
  
<span data-ttu-id="14896-114">И, наконец, стандартный отчет и статистика группы сервисных цен позволяют следить за прибылью по каждой ценовой группе сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="14896-114">Finally, service price group statistics and standard reports let you keep track of the profitability of each service price group.</span></span>  
  
## <a name="service-price-adjustment-groups"></a><span data-ttu-id="14896-115">Группы коррекции цен на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="14896-115">Service Price Adjustment Groups</span></span>  
<span data-ttu-id="14896-116">Группы коррекции цены обслуживания используются для настройки различных типов коррекции цен.</span><span class="sxs-lookup"><span data-stu-id="14896-116">You use service price adjustment groups to set up the different types of price adjustments.</span></span> <span data-ttu-id="14896-117">Например, можно создать одну группу коррекции сервисной цены, чтобы корректировать цены на запасные части, другую — чтобы корректировать цены на труд, третью — чтобы корректировать цены для себестоимости, и т. д.</span><span class="sxs-lookup"><span data-stu-id="14896-117">For example, you can set up a service price adjustment group that adjusts prices for spare parts, one that adjust prices for labor, one that adjusts prices for costs, and so on.</span></span> <span data-ttu-id="14896-118">Можно также указать, относится ли корректировка сервисных цен только к какому-то одному товару или ресурсу, или ко всем товарам и ресурсам.</span><span class="sxs-lookup"><span data-stu-id="14896-118">You can also specify whether the service price adjustment should be applied to just one specific item or resource, or to all items or resources.</span></span>  
  
<span data-ttu-id="14896-119">Каждая группа коррекции сервисной цены содержит информацию об изменениях, которые надо внести в строки сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-119">Each service price adjustment group holds the information about the adjustments that you want to make on the service lines.</span></span>  
  
<span data-ttu-id="14896-120">Функция коррекции сервисной цены не применяется к сервисным товарам, относящимся к сервисным контрактам.</span><span class="sxs-lookup"><span data-stu-id="14896-120">The service price adjustment function does not apply to service items that belong to service contracts.</span></span> <span data-ttu-id="14896-121">Можно корректировать только сервисные цены на товары, относящиеся к определенному сервисному заказу.</span><span class="sxs-lookup"><span data-stu-id="14896-121">You can only adjust the service prices of items that are part of a service order.</span></span> <span data-ttu-id="14896-122">Невозможно корректировать цену сервисного товара, находящегося на гарантии.</span><span class="sxs-lookup"><span data-stu-id="14896-122">You cannot adjust the price of a service item if it has a warranty.</span></span> <span data-ttu-id="14896-123">Невозможно корректировать цену сервисного товара из сервисного заказа, если связанная с ним сервисная строка была полностью или частично учтена в составе счета.</span><span class="sxs-lookup"><span data-stu-id="14896-123">You cannot adjust the price of a service item on a service order if the service line linked to it has been posted as invoice, either fully or in part.</span></span>  
  
<span data-ttu-id="14896-124">При выполнении функции корректировки сервисной цены все скидки в заказе меняются на значения корректировки сервисной цены.</span><span class="sxs-lookup"><span data-stu-id="14896-124">When you run the service price adjustment function, all of the discounts in the order will be replaced by the values of the service price adjustment.</span></span>  
  
## <a name="service-price-groups"></a><span data-ttu-id="14896-125">Ценовые группы сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="14896-125">Service Price Groups</span></span>  
<span data-ttu-id="14896-126">Можно настроить сервисные ценовые группы, чтобы создавать группы сервисных товаров, получающие определенные сервисные цены.</span><span class="sxs-lookup"><span data-stu-id="14896-126">You can set up service price groups to create groups of service items that receive the same special service pricing.</span></span> <span data-ttu-id="14896-127">После настройки сервисных ценовых групп можно присваивать их сервисным товарам в строках сервисных товаров.</span><span class="sxs-lookup"><span data-stu-id="14896-127">When you have set up service price groups, you can then assign them to service items on service item lines.</span></span> <span data-ttu-id="14896-128">Группам сервисных товаров можно также присвоить ценовые группы сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-128">You can also assign service price groups to service item groups.</span></span>  
  
<span data-ttu-id="14896-129">Прежде чем приписывать сервисную группу цен какому-либо сервисному товару, необходимо определить, к какой сфере проблем, к какой валюте или группе корректировки сервисной цены относится данная ценовая группа сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="14896-129">Before you can assign a service price group to a service item, you have to determine to which fault area, currency, or service price adjustment group the service price group applies.</span></span> <span data-ttu-id="14896-130">Необходимо указать, до какой суммы можно корректировать сервисную цену, и включает ли эта сумма НДС и скидки.</span><span class="sxs-lookup"><span data-stu-id="14896-130">You have to determine to which amount the service price should be adjusted, and whether this amount should include VAT and discounts.</span></span> <span data-ttu-id="14896-131">Также следует определить, относится ли эта корректировка к фиксированной сумме или применяется только в определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="14896-131">You also have to determine whether this adjustment concerns a fixed amount, or should only be applied under certain conditions.</span></span>  
  
<span data-ttu-id="14896-132">Когда ценовая группа сервисного обслуживания присвоена некоторому сервисному товару, все специализированные сервисные цены, установленные в этой группе, автоматически применяются к данному сервисному товару.</span><span class="sxs-lookup"><span data-stu-id="14896-132">When you assign a service price group to a service item, all the special service pricing that you set up in this group will then apply for this service item.</span></span>  
  
## <a name="service-pricing"></a><span data-ttu-id="14896-133">Сервисные цены</span><span class="sxs-lookup"><span data-stu-id="14896-133">Service Pricing</span></span>  
<span data-ttu-id="14896-134">Фактические типы сервисных цен (тип корректировки цены и цена) устанавливаются для комбинации ценовых групп сервиса и ценовых групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="14896-134">You set up the actual types of service pricing (price adjustment type and price) for a combination of service price groups and customer price groups.</span></span> <span data-ttu-id="14896-135">Для каждого типа сервисной цены выбирается группа корректировки сервисной цены.</span><span class="sxs-lookup"><span data-stu-id="14896-135">For each type of service pricing, you select a service price adjustment group.</span></span> <span data-ttu-id="14896-136">Также определяется тип коррекции сервисной цены: фиксированная, максимальная или минимальная и фактическая цена.</span><span class="sxs-lookup"><span data-stu-id="14896-136">You also specify the service price adjustment type, fixed, maximum, or minimum, and the actual price.</span></span>  
  
<span data-ttu-id="14896-137">Например, можно установить типы сервисных цен для ценовой группы радиосервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-137">For example, you can set up types of service pricing for a radio service price group.</span></span> <span data-ttu-id="14896-138">Для клиентов без ценовой группы можно применить сервисные цены с максимальной ценой работы (группа коррекции цены работы).</span><span class="sxs-lookup"><span data-stu-id="14896-138">For customers without a price group, you can decide to have service pricing with maximum price on labor, which is the labor price adjustment group.</span></span> <span data-ttu-id="14896-139">Для клиентов с отдельной ценовой группой можно применить сервисные цены с фиксированной ценой работы (та же группа коррекции цены работы).</span><span class="sxs-lookup"><span data-stu-id="14896-139">For customers with a particular price group, you can decide to have service pricing with a fixed price on labor, the same labor price adjustment group.</span></span>  
  
## <a name="service-price-adjustment"></a><span data-ttu-id="14896-140">Коррекции цен на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="14896-140">Service Price Adjustment</span></span>  
<span data-ttu-id="14896-141">Коррекция сервисной цены позволяет корректировать цены для товаров, ресурсов, счета Главной книги или себестоимости по сервисному заказу.</span><span class="sxs-lookup"><span data-stu-id="14896-141">Service price adjustment lets you adjust the price of an item, resource, general ledger account, or cost on a service order.</span></span>  
  
<span data-ttu-id="14896-142">После ввода товара в строку сервисного товара нужно ввести все данные о стоимости данного товара по строкам сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-142">After you have entered an item on the service item line, you then enter all information about the costs of this item on the service lines.</span></span> <span data-ttu-id="14896-143">При выполнении функции коррекции сервисной цены следует предварительно просмотреть корректировки цен.</span><span class="sxs-lookup"><span data-stu-id="14896-143">When you run the Adjust Service Price function, you can preview the price adjustments.</span></span> <span data-ttu-id="14896-144">При необходимости можно внести дополнительные изменения.</span><span class="sxs-lookup"><span data-stu-id="14896-144">You can make modifications if you have to.</span></span> <span data-ttu-id="14896-145">Когда все изменения приняты, значения коррекции вычисляются и переводятся в сервисные строки.</span><span class="sxs-lookup"><span data-stu-id="14896-145">When you acknowledge the modifications, the adjustments are calculated, and are then transferred to the service lines.</span></span> <span data-ttu-id="14896-146">После этого можно производить учет сервисного заказа.</span><span class="sxs-lookup"><span data-stu-id="14896-146">You then post the service order.</span></span>  
  
<span data-ttu-id="14896-147">В зависимости от типа коррекции сервисной цены общая сумма коррекции вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14896-147">Depending on the type of service price adjustment, the total amount of the adjustments is calculated.</span></span>  
  
<span data-ttu-id="14896-148">В следующей таблице приводится описание расчетов.</span><span class="sxs-lookup"><span data-stu-id="14896-148">The following table describes the calculations.</span></span>  
  
|<span data-ttu-id="14896-149">Параметр</span><span class="sxs-lookup"><span data-stu-id="14896-149">Option</span></span> | <span data-ttu-id="14896-150">Описанием</span><span class="sxs-lookup"><span data-stu-id="14896-150">Description</span></span> |  
|----------------------------------|---------------------------------------|  
|<span data-ttu-id="14896-151">**Фиксированная цена**</span><span class="sxs-lookup"><span data-stu-id="14896-151">**Fixed Price**</span></span>|<span data-ttu-id="14896-152">Это означает, что для сервисного товара, ресурса, счета главной книги или себестоимости запрашивается фиксированная цена, которая не зависит от реальной себестоимости или стандартной оплаты.</span><span class="sxs-lookup"><span data-stu-id="14896-152">This means that you charge a fixed price for the service item, resource, general ledger account, or cost, regardless of the real costs or regular charges.</span></span> <span data-ttu-id="14896-153">Если выбран этот параметр, коррекция сервисной цены не выйдет за пределы суммы, определенной ценовой группы сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-153">Selecting this option means that the service price adjustment will reach the exact amount specified in the service price group.</span></span>|  
|<span data-ttu-id="14896-154">**Максимум**</span><span class="sxs-lookup"><span data-stu-id="14896-154">**Maximum**</span></span>|<span data-ttu-id="14896-155">Это означает, что для клиента устанавливается верхняя граница издержек, независимо от реальной себестоимости или стандартной оплаты.</span><span class="sxs-lookup"><span data-stu-id="14896-155">This means that you put an upper limit on the charge to your customer, regardless of the real costs or regular charges.</span></span> <span data-ttu-id="14896-156">Если выбран этот параметр, коррекция сервисной цены производится только тогда, когда общая цена превышает сумму, указанную для ценовой группы сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-156">Selecting this option means that the service price adjustment will only be performed if the total price exceeds the amount specified in the service price group.</span></span>|  
|<span data-ttu-id="14896-157">**Минимум**</span><span class="sxs-lookup"><span data-stu-id="14896-157">**Minimum**</span></span>|<span data-ttu-id="14896-158">Это означает, что для клиента устанавливается нижняя граница издержек, независимо от реальной себестоимости или стандартной оплаты.</span><span class="sxs-lookup"><span data-stu-id="14896-158">This means that you put a lower limit on the charge to your customer, regardless of the real costs or regular charges.</span></span> <span data-ttu-id="14896-159">Если выбран этот параметр, коррекция сервисной цены производится только тогда, когда общая сумма оказывается ниже суммы, указанной для ценовой группы сервиса.</span><span class="sxs-lookup"><span data-stu-id="14896-159">Selecting this option means that the service price adjustment will only be performed if the total amount is less than the amount specified on the service price group.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="14896-160">См. также</span><span class="sxs-lookup"><span data-stu-id="14896-160">See Also</span></span>  
[<span data-ttu-id="14896-161">Практическое руководство. Настройка цен и дополнительных издержек для сервисов</span><span class="sxs-lookup"><span data-stu-id="14896-161">How to: Set Up Pricing and Additional Costs for Services</span></span>](service-how-setup-service-costs-pricing.md)  
[<span data-ttu-id="14896-162">Настройка управления сервисным обслуживанием</span><span class="sxs-lookup"><span data-stu-id="14896-162">Setting Up Service Management</span></span>](service-setup-service.md)  
