---
title: "Как использовать субподрядное производство | Документы Майкрософт"
description: "После создания заказа на покупку из журнала субподрядчика его можно учесть."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6f8094545431468bd12e231364987e70bda429bb
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-subcontract-manufacturing"></a><span data-ttu-id="7a50c-103">Практическое руководство. Субподрядное производство</span><span class="sxs-lookup"><span data-stu-id="7a50c-103">How to: Subcontract Manufacturing</span></span>
<span data-ttu-id="7a50c-104">Передача определенных операций субподрядчику — это обычная практика во многих производственных организациях.</span><span class="sxs-lookup"><span data-stu-id="7a50c-104">Subcontracting selected operations to vendor is common in many manufacturing companies.</span></span> <span data-ttu-id="7a50c-105">Субподряд может быть редким событием или же может стать важной частью всех производственных процессов.</span><span class="sxs-lookup"><span data-stu-id="7a50c-105">Subcontracting can be a rare occurrence or can be an integral part of all production processes.</span></span>

<span data-ttu-id="7a50c-106">Программа содержит несколько инструментов управления субподрядными работами:</span><span class="sxs-lookup"><span data-stu-id="7a50c-106">The program provides several tools for managing subcontract work:</span></span>  

- <span data-ttu-id="7a50c-107">«Рабочие центры» с назначенным поставщиком: эта функция позволяет настраивать рабочий центр для одного поставщика (субподрядчика).</span><span class="sxs-lookup"><span data-stu-id="7a50c-107">Work Centers with assigned vendor: This feature enables you to set up a work center that is associated with a vendor (subcontractor).</span></span> <span data-ttu-id="7a50c-108">Такой рабочий центр называется субподрядным.</span><span class="sxs-lookup"><span data-stu-id="7a50c-108">This is called a subcontract work center.</span></span> <span data-ttu-id="7a50c-109">Можно указать субподрядный рабочий центр в операции маршрута, что позволяет легко управлять субподрядными операциями.</span><span class="sxs-lookup"><span data-stu-id="7a50c-109">You can specify a subcontract work center on a routing operation, which allows you to easily process the subcontracted activity.</span></span> <span data-ttu-id="7a50c-110">Кроме того, себестоимость операции можно указывать на уровне маршрута или рабочего центра.</span><span class="sxs-lookup"><span data-stu-id="7a50c-110">In addition, the cost of the operation can be designated at the routing or the work center level.</span></span>  
- <span data-ttu-id="7a50c-111">Себестоимость "Рабочего центра" на базе единиц или времени: эта функция позволяет указывать, будут ли расходы, связанные с рабочим центром, определяться на основе времени производства или фиксированной ставки за единицу.</span><span class="sxs-lookup"><span data-stu-id="7a50c-111">Work Center cost based on units or time: This feature enables you to specify whether costs associated with the work center are based on the production time or a flat charge per unit.</span></span> <span data-ttu-id="7a50c-112">Хотя субподрядчики обычно применяют фиксированную ставку за единицу своих услуг, программа поддерживает оба варианта (время производства и фиксированная ставка за единицу).</span><span class="sxs-lookup"><span data-stu-id="7a50c-112">Although subcontractors commonly use a flat charge per unit to charge for their services, the program can handle both options (production time and flat charge per unit).</span></span>  
- <span data-ttu-id="7a50c-113">Журналы субподрядов: эта функция позволяет находить производственные заказы с материалами, готовыми к отправке субподрядчику, и автоматически создавать заказы на покупку для субподрядных операций из маршрутов производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="7a50c-113">Subcontracting Worksheet: This feature allows you to find the production orders with material ready to send to a subcontractor and to automatically create purchase orders for subcontract operations from production order routings.</span></span> <span data-ttu-id="7a50c-114">Затем программа автоматически учитывает стоимость заказа на покупку в производственном заказе при учете заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-114">Then the program automatically posts the purchase order charges to the production order during the posting of the purchase order.</span></span> <span data-ttu-id="7a50c-115">С помощью журнала субподрядов можно просматривать и использовать только производственные заказы, имеющие статус запущенных.</span><span class="sxs-lookup"><span data-stu-id="7a50c-115">Only production orders with a status of released can be accessed and used from a subcontracting worksheet.</span></span>  

## <a name="subcontract-work-centers"></a><span data-ttu-id="7a50c-116">Субподрядные рабочие центры</span><span class="sxs-lookup"><span data-stu-id="7a50c-116">Subcontract Work Centers</span></span>  
<span data-ttu-id="7a50c-117">«Субподрядные рабочие центры» настраиваются так же, как обычные рабочие центры с дополнительными данными.</span><span class="sxs-lookup"><span data-stu-id="7a50c-117">Subcontract Work Centers are set up the same as regular work centers with additional information.</span></span> <span data-ttu-id="7a50c-118">Они назначаются маршрутам таким же образом, как и прочие рабочие центры.</span><span class="sxs-lookup"><span data-stu-id="7a50c-118">They are assigned to routings in the same manner as other work centers.</span></span>  

### <a name="subcontract-work-center-fields"></a><span data-ttu-id="7a50c-119">Поля субподрядных рабочих центров</span><span class="sxs-lookup"><span data-stu-id="7a50c-119">Subcontract Work Center Fields</span></span>  
<span data-ttu-id="7a50c-120">Поле **Код субподрядчика** позволяет обозначить рабочий центр как субподрядный.</span><span class="sxs-lookup"><span data-stu-id="7a50c-120">This **Subcontractor No.** field designates the work center as a subcontract work center.</span></span> <span data-ttu-id="7a50c-121">Можно ввести номер субподрядчика, снабжающего рабочий центр.</span><span class="sxs-lookup"><span data-stu-id="7a50c-121">You can enter the number of a subcontractor who supplies the work center.</span></span> <span data-ttu-id="7a50c-122">Это поле может быть использовано для управления рабочими центрами, которые не находятся на предприятии, а работают по контракту.</span><span class="sxs-lookup"><span data-stu-id="7a50c-122">This field can be used to administer work centers, which are not in-house but perform processing under contract.</span></span>  

<span data-ttu-id="7a50c-123">Если субподряд с поставщиком оформляется по разным ставкам для каждого процесса, установите флажок в поле **Специальная себест. единицы**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-123">If you subcontract with the vendor for a different rate for each process, then select the **Specific Unit Cost** field.</span></span> <span data-ttu-id="7a50c-124">Это позволяет настраивать себестоимость по каждой строке маршрута и экономит время на повторный ввод данных для каждого заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-124">This lets you set up a cost on each routing line and saves the time of re-entering each purchase order.</span></span> <span data-ttu-id="7a50c-125">При обработке используется себестоимость по строке маршрута, а не себестоимость по полям рабочего центра.</span><span class="sxs-lookup"><span data-stu-id="7a50c-125">The cost on the routing line is used in processing instead of the cost on the work center cost fields.</span></span> <span data-ttu-id="7a50c-126">Выбор поля **Специальная себест. единицы** позволяет вычислять себестоимость по поставщику для каждой операции маршрута.</span><span class="sxs-lookup"><span data-stu-id="7a50c-126">Selecting the **Specific Unit Cost** field calculates costs for the vendor by the routing operation.</span></span>  

<span data-ttu-id="7a50c-127">Если используется одна ставка для каждого субподрядчика, оставьте поле **Специальная себест. единицы** пустым.</span><span class="sxs-lookup"><span data-stu-id="7a50c-127">If you subcontract at a single rate per vendor, leave the **Specific Unit Cost** field blank.</span></span> <span data-ttu-id="7a50c-128">Себестоимость будет настраиваться путем заполнения полей **Прямая себестоимость единицы**, **Косвенные затраты (%)** и **Норма накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-128">The costs will be set up by filling in **Direct Unit Cost**, **Indirect Cost %**, and **Overhead Rate** fields.</span></span>  

### <a name="routings-that-use-subcontract-work-centers"></a><span data-ttu-id="7a50c-129">Маршруты, использующие субподрядные рабочие центры</span><span class="sxs-lookup"><span data-stu-id="7a50c-129">Routings that use Subcontract Work Centers</span></span>  
<span data-ttu-id="7a50c-130">Субподрядные рабочие центры можно использовать для операций точно так же, как обычные рабочие центры.</span><span class="sxs-lookup"><span data-stu-id="7a50c-130">Subcontract work centers can be used for operations on routings in the same way as regular work centers.</span></span>  

<span data-ttu-id="7a50c-131">Можно настроить маршрут, использующий внешний рабочий центр, в качестве стандартного операционного шага.</span><span class="sxs-lookup"><span data-stu-id="7a50c-131">You can set up a routing that uses an outside work center as a standard operational step.</span></span> <span data-ttu-id="7a50c-132">Другой вариант - изменить маршрут для конкретного производственного заказа, включив внешнюю операцию.</span><span class="sxs-lookup"><span data-stu-id="7a50c-132">Alternatively, you can modify the routing for a particular production order to include an outside operation.</span></span> <span data-ttu-id="7a50c-133">Это может понадобиться в экстренной ситуации, например при неправильной работе сервера или при временном периоде повышенного спроса, когда работа, обычно выполняемая собственными силами, передается субподрядчику.</span><span class="sxs-lookup"><span data-stu-id="7a50c-133">This might be needed in an emergency such as a server not working correctly, or during a temporary period of higher demand, where the work generally performed in-house must be sent to a subcontractor.</span></span>  

<span data-ttu-id="7a50c-134">Дополнительные сведения см. в разделе [Практическое руководство. Создание маршрутов](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="7a50c-134">For more information, see [How to: Create Routings](production-how-to-create-routings.md).</span></span>  

## <a name="subcontracting-worksheet"></a><span data-ttu-id="7a50c-135">Журнал субподрядов</span><span class="sxs-lookup"><span data-stu-id="7a50c-135">Subcontracting Worksheet</span></span>  
<span data-ttu-id="7a50c-136">После расчета журнала субподряда создается соответствующий документ, в данном случае заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-136">Once you have calculated the subcontracting worksheet, the relevant document, in this case a purchase order, is created.</span></span>  

# <a name="how-to-calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a><span data-ttu-id="7a50c-137">Практическое руководство. Вычисление листов субподрядов и создание заказов на покупку для субподряда</span><span class="sxs-lookup"><span data-stu-id="7a50c-137">How to: Calculate Subcontracting Worksheets and Create Subcontract Purchase Orders</span></span>
<span data-ttu-id="7a50c-138">Окно **Журнал субподрядов** работает как **Журнал планирования**, вычисляя необходимую поставку, в данном случае — заказы на покупку, которые можно сначала просмотреть в журнале, а затем создать с помощью функции **Выполнить указание**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-138">The **Subcontracting Worksheet** window functions like the **Planning Worksheet** by calculating the needed supply, in this case purchase orders, which you review in the worksheet and then create with the **Carry Out Action Message** function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7a50c-139">С помощью журнала субподрядов можно просматривать и использовать только производственные заказы со статусом **Выпущено**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-139">Only production orders with status **Released** can be accessed and used from a subcontracting worksheet.</span></span>  

### <a name="to-calculate-the-subcontracting-worksheet"></a><span data-ttu-id="7a50c-140">Вычисление листа субподряда</span><span class="sxs-lookup"><span data-stu-id="7a50c-140">To calculate the subcontracting worksheet</span></span>  
1.  <span data-ttu-id="7a50c-141">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал субподрядов**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Subcontracting Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a50c-142">Для расчета журнала выберите действие **Расчет субподрядов**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-142">To calculate the worksheet, choose the **Calculate Subcontracts** action.</span></span>  
3.  <span data-ttu-id="7a50c-143">В окне **Расчет субподрядов** задайте фильтры для субподрядных операций или для производственных центров, в которых они выполняются, чтобы вычислить только соответствующие производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="7a50c-143">In the **Calculate Subcontracts** window, set filters for the subcontracted operations, or the work centers where they are performed, to calculate only the relevant production orders.</span></span>  
4.  <span data-ttu-id="7a50c-144">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-144">Choose the **OK** button.</span></span>  

    <span data-ttu-id="7a50c-145">Просмотрите строки в окне **Журнал субподрядов**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-145">Review the lines in the **Subcontracting Worksheet** window.</span></span> <span data-ttu-id="7a50c-146">Данные в этот журнал поступают из строк производственного заказа и маршрута производственного заказа, и передаются в заказ на покупку при создании этого документа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-146">The information in this worksheet comes from the production order and production order routing lines and flows to the purchase order when that document is created.</span></span> <span data-ttu-id="7a50c-147">Как и в случае с другими журналами, удаление строки в этом журнале не влияет на исходные данные.</span><span class="sxs-lookup"><span data-stu-id="7a50c-147">You can delete a row from the worksheet without affecting the original information, just as you can with the other worksheets.</span></span> <span data-ttu-id="7a50c-148">Информация появится снова при следующем использовании функции **Расчет субподрядов**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-148">The information will reappear the next time you run the **Calculate Subcontracts** function.</span></span>  

### <a name="to-create-the-subcontract-purchase-order"></a><span data-ttu-id="7a50c-149">Создание заказа на покупку для субподряда</span><span class="sxs-lookup"><span data-stu-id="7a50c-149">To create the subcontract purchase order</span></span>  
1.  <span data-ttu-id="7a50c-150">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал субподрядов**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-150">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Subcontracting Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a50c-151">На вкладке **Действия** в группе **Процесс** выберите **Выполнить указание**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-151">On the **Actions** tab, in the **Process** group, choose **Carry Out Action Message**.</span></span>  
3.  <span data-ttu-id="7a50c-152">Выберите поле **Печатать заказы**, чтобы распечатать заказ на покупку после его создания.</span><span class="sxs-lookup"><span data-stu-id="7a50c-152">Select the **Print Orders** field to print the purchase order as it is created.</span></span>  
4.  <span data-ttu-id="7a50c-153">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-153">Choose the **OK** button.</span></span>  

<span data-ttu-id="7a50c-154">Если все операции субподряда будут передаваться на один склад поставщика, создается только один заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-154">If all subcontracted operations are sent to the same vendor location, then only one purchase order is created.</span></span>  

<span data-ttu-id="7a50c-155">Строка журнала, преобразованная в заказ на покупку, удаляется из журнала.</span><span class="sxs-lookup"><span data-stu-id="7a50c-155">The worksheet line that was turned into a purchase order is deleted from the worksheet.</span></span> <span data-ttu-id="7a50c-156">После того как заказ на покупку создан, он не будет отображен в журнале повторно.</span><span class="sxs-lookup"><span data-stu-id="7a50c-156">Once a purchase order is created, it will not appear in the worksheet again.</span></span>  

## <a name="posting-subcontract-purchase-orders"></a><span data-ttu-id="7a50c-157">Учет субподрядных заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="7a50c-157">Posting Subcontract Purchase Orders</span></span>  
<span data-ttu-id="7a50c-158">После создания субподрядных заказов на покупку их можно учитывать.</span><span class="sxs-lookup"><span data-stu-id="7a50c-158">Once the Subcontractor Purchase Orders have been created, they can be posted.</span></span> <span data-ttu-id="7a50c-159">При получении заказа операция из книги производственных мощностей учитывается в производственном заказе, а выставление счета по заказу учитывает прямые затраты заказа на покупку в производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="7a50c-159">Receiving the order posts a Capacity Ledger Entry to the production order and invoicing the order posts the direct cost of the purchase order to the production order.</span></span>  

<span data-ttu-id="7a50c-160">Если покупка учитывается как полученная, выполняется автоматически учет операции журнала выхода для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-160">When the purchase is posted as received, then an output journal entry is automatically posted for the production order.</span></span> <span data-ttu-id="7a50c-161">Это справедливо, только если операция субподряда является последней операцией в маршруте производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-161">This only applies if the subcontract operation is the last operation on the production order routing.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="7a50c-162">Автоматически учет выхода будущих производственных заказов, когда получение субподрядных товаров не желательно.</span><span class="sxs-lookup"><span data-stu-id="7a50c-162">Posting output automatically for an ongoing production order when subcontracted items are received may not be desired.</span></span> <span data-ttu-id="7a50c-163">Причиной этого может быть то, что учтенное ожидаемое количество выпуска может отличаться от фактического количества и дата учета автоматической отгрузки может быть неверной.</span><span class="sxs-lookup"><span data-stu-id="7a50c-163">Reasons for this could be that the expected output quantity that is posted may be different from the actual quantity and that the posting date of the automatic output is misleading.</span></span>  
>   
>  <span data-ttu-id="7a50c-164">Чтобы избежать учета результатов выполнения производственного заказа при получении покупок по субподряду, убедитесь, что операция субподряда не является последней.</span><span class="sxs-lookup"><span data-stu-id="7a50c-164">To avoid that the expected output of a production order is posted when subcontract purchases are received, make sure the subcontracted operation is not the last one.</span></span> <span data-ttu-id="7a50c-165">В качестве альтернативы вставьте новую последнюю операцию для окончательного количества выхода.</span><span class="sxs-lookup"><span data-stu-id="7a50c-165">Alternatively, insert a new last operation for the final output quantity.</span></span>

## <a name="to-post-a-subcontract-purchase-order"></a><span data-ttu-id="7a50c-166">Учет заказа на покупку по субподряду</span><span class="sxs-lookup"><span data-stu-id="7a50c-166">To post a subcontract purchase order</span></span>  
1.  <span data-ttu-id="7a50c-167">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на покупку**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7a50c-167">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then select the related link.</span></span>  
2.  <span data-ttu-id="7a50c-168">Откройте заказ на покупку, созданный из журнала субподрядов.</span><span class="sxs-lookup"><span data-stu-id="7a50c-168">Open a purchase order that is created from the subcontracting worksheet.</span></span>  

    <span data-ttu-id="7a50c-169">В строках заказа покупки содержится та же информация, которая была в журнале.</span><span class="sxs-lookup"><span data-stu-id="7a50c-169">On the purchase order lines, you see the same information that was in the worksheet.</span></span> <span data-ttu-id="7a50c-170">Поля **Номер производственного заказа**, **Номер строки произв. заказа**, **Номер произв. операции** и **Номер производственного центра**</span><span class="sxs-lookup"><span data-stu-id="7a50c-170">The **Prod. Order No.**, **Prod. Order Line No.**, **Operation No.**, and **Work Center No.**</span></span> <span data-ttu-id="7a50c-171">заполняются информацией из исходного производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-171">fields are filled in with the information from the source production order.</span></span>  

3.  <span data-ttu-id="7a50c-172">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="7a50c-172">Choose the **Post** action.</span></span>  

<span data-ttu-id="7a50c-173">Если покупка учитывается как полученная, выполняется автоматически учет операции журнала выхода для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-173">When the purchase is posted as received, then an output journal entry is automatically posted for the production order.</span></span> <span data-ttu-id="7a50c-174">Это справедливо, только если операция субподряда является последней операцией в маршруте производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7a50c-174">This only applies if the subcontract operation is the last operation on the production order routing.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="7a50c-175">Автоматически учет выхода будущих производственных заказов, когда получение субподрядных товаров не желательно.</span><span class="sxs-lookup"><span data-stu-id="7a50c-175">Posting output automatically for an ongoing production order when subcontracted items are received may not be desired.</span></span> <span data-ttu-id="7a50c-176">Причиной этого может быть то, что учтенное ожидаемое количество выпуска может отличаться от фактического количества и дата учета автоматической отгрузки может быть неверной.</span><span class="sxs-lookup"><span data-stu-id="7a50c-176">Reasons for this could be that the expected output quantity that is posted may be different from the actual quantity and that the posting date of the automatic output is misleading.</span></span>  
>   
>  <span data-ttu-id="7a50c-177">Чтобы избежать учета результатов выполнения производственного заказа при получении покупок по субподряду, убедитесь, что операция субподряда не является последней.</span><span class="sxs-lookup"><span data-stu-id="7a50c-177">To avoid that the expected output of a production order is posted when subcontract purchases are received, make sure the subcontracted operation is not the last one.</span></span> <span data-ttu-id="7a50c-178">В качестве альтернативы вставьте новую последнюю операцию для окончательного количества выхода.</span><span class="sxs-lookup"><span data-stu-id="7a50c-178">Alternatively, insert a new last operation for the final output quantity.</span></span>  

<span data-ttu-id="7a50c-179">Если заказ на покупку учитывается как заказ с выставленным счетом, прямая себестоимость заказа на покупку учитывается в производстве.</span><span class="sxs-lookup"><span data-stu-id="7a50c-179">When the purchase order is posted as invoiced, then the direct cost of the purchase order is posted to the production.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a50c-180">См. также</span><span class="sxs-lookup"><span data-stu-id="7a50c-180">See Also</span></span>  
<span data-ttu-id="7a50c-181">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7a50c-181">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7a50c-182">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="7a50c-182">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7a50c-183">[Планирование](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="7a50c-183">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="7a50c-184">Наличие</span><span class="sxs-lookup"><span data-stu-id="7a50c-184">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7a50c-185">Покупки</span><span class="sxs-lookup"><span data-stu-id="7a50c-185">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7a50c-186">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a50c-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
