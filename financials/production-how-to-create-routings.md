---
title: "Практическое руководство. Создание маршрутов | Документы Майкрософт"
description: "Маршрут содержит основные данные, которые фиксируют требования процесса производства данного товара. После создания производственного заказа для данного товара его маршрут используется для управления графиком производственных операций, представленных в окне **Маршрутизация производственных заказов** под производственным заказом."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 166d85bbcf7d97cb513ba668e41fc4a179d8fcc3
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-routings"></a><span data-ttu-id="c575c-104">Практическое руководство. Создание маршрутов</span><span class="sxs-lookup"><span data-stu-id="c575c-104">How to: Create Routings</span></span>
<span data-ttu-id="c575c-105">Производственные организации используют маршруты, чтобы визуально отображать и направлять процесс производства.</span><span class="sxs-lookup"><span data-stu-id="c575c-105">Manufacturing companies use routings to visualize and direct the manufacturing process.</span></span>

<span data-ttu-id="c575c-106">Данный маршрут является основанием для планирования процесса, производственной мощности, планируемого задания потребности материалов и производственной документации.</span><span class="sxs-lookup"><span data-stu-id="c575c-106">The routing is the basis of process scheduling, capacity scheduling, scheduled assignment of material needs, and manufacturing documents.</span></span>  

<span data-ttu-id="c575c-107">В отношении производственных спецификаций маршруты назначаются производству конечного товара.</span><span class="sxs-lookup"><span data-stu-id="c575c-107">As for production BOMs, the routings are assigned to the manufacturing end item.</span></span> <span data-ttu-id="c575c-108">Маршрут содержит основные данные, которые фиксируют требования процесса производства данного товара.</span><span class="sxs-lookup"><span data-stu-id="c575c-108">A routing holds master data that captures the process requirements of a given produced item.</span></span> <span data-ttu-id="c575c-109">После создания производственного заказа для данного товара его маршрут используется для управления графиком производственных операций, представленных в окне **Маршрутизация производственных заказов** под производственным заказом.</span><span class="sxs-lookup"><span data-stu-id="c575c-109">Once a production order is created for that item, its routing will govern the scheduling of operations as represented in the **Prod. Order Routing** window under the production order.</span></span>  

<span data-ttu-id="c575c-110">Прежде чем можно будет настроить маршрут, необходимо подготовить следующее:</span><span class="sxs-lookup"><span data-stu-id="c575c-110">Before you can set up a routing, the following must be in place:</span></span>  

- <span data-ttu-id="c575c-111">Должны быть созданы карточки товара для родительских товаров, которые участвуют в производстве.</span><span class="sxs-lookup"><span data-stu-id="c575c-111">Item cards are created for parent items that take part in manufacturing.</span></span> <span data-ttu-id="c575c-112">Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых продуктов](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-112">For more information, see [How to: Register New Products](inventory-how-register-new-items.md).</span></span>
- <span data-ttu-id="c575c-113">Производственные ресурсы настроены.</span><span class="sxs-lookup"><span data-stu-id="c575c-113">Production resources are set up.</span></span> <span data-ttu-id="c575c-114">Дополнительные сведения см. в разделе [Практическое руководство. Настройка производственных и машинных центров](production-how-to-set-up-work-and-machine-centers.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-114">For more information, see [How to: Set Up Work Centers and Machine Centers](production-how-to-set-up-work-and-machine-centers.md).</span></span>

## <a name="to-create-a-routing"></a><span data-ttu-id="c575c-115">Создание маршрута</span><span class="sxs-lookup"><span data-stu-id="c575c-115">To create a routing</span></span>  
1.  <span data-ttu-id="c575c-116">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Маршруты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c575c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c575c-117">Выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c575c-117">Choose the **New** action.</span></span>  
3. <span data-ttu-id="c575c-118">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="c575c-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="c575c-119">В поле **Тип** выберите **Последовательный**, чтобы вычислить производственный маршрут согласно значению в поле **Номер произв. операции**</span><span class="sxs-lookup"><span data-stu-id="c575c-119">In the **Type** field, select **Serial** to calculate the production routing according to the value in the **Operation No.**</span></span> <span data-ttu-id="c575c-120">.</span><span class="sxs-lookup"><span data-stu-id="c575c-120">field.</span></span>   
    <span data-ttu-id="c575c-121">Выберите **Параллельный** для расчета операций в соответствии со значением в поле **Номер след. произв. операции**</span><span class="sxs-lookup"><span data-stu-id="c575c-121">Select **Parallel** to calculate the operations according to the value in the **Next Operation No.**</span></span> <span data-ttu-id="c575c-122">.</span><span class="sxs-lookup"><span data-stu-id="c575c-122">field.</span></span>  
5.  <span data-ttu-id="c575c-123">Для редактирования маршрута задайте в поле **Статус** значение **Новый** или **В разработке**.</span><span class="sxs-lookup"><span data-stu-id="c575c-123">To edit the routing, set the **Status** field to **New** or **Under Development**.</span></span> <span data-ttu-id="c575c-124">Чтобы его активировать, задайте в поле **Статус** значение **Сертифицировано**.</span><span class="sxs-lookup"><span data-stu-id="c575c-124">To activate it, set the **Status** field to **Certified**.</span></span>  

    <span data-ttu-id="c575c-125">Переходите к заполнению строк маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-125">Proceed to fill in the routing lines.</span></span>
6.  <span data-ttu-id="c575c-126">В поле **Номер произв. операции**</span><span class="sxs-lookup"><span data-stu-id="c575c-126">In the **Operation No.**</span></span> <span data-ttu-id="c575c-127">введите номер первой операции, например **10**.</span><span class="sxs-lookup"><span data-stu-id="c575c-127">field, enter the number of the first operation, for example,  **10**.</span></span>  
7.  <span data-ttu-id="c575c-128">В поле **Тип** укажите тип используемого ресурса, например **Рабочий центр**.</span><span class="sxs-lookup"><span data-stu-id="c575c-128">In the **Type** field, specify which kind of resource is used, for example, **Work Center**.</span></span>  
8.  <span data-ttu-id="c575c-129">В поле **Номер**</span><span class="sxs-lookup"><span data-stu-id="c575c-129">In the **No.**</span></span> <span data-ttu-id="c575c-130">выберите или введите требуемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="c575c-130">field, select the resource to be used, or type it in the field.</span></span>  
9.  <span data-ttu-id="c575c-131">В поле **Код связи маршрута** введите код для соединения компонента с определенной операцией.</span><span class="sxs-lookup"><span data-stu-id="c575c-131">In the **Routing Link Code** field, enter a code to connect the component to a specific operation.</span></span> <span data-ttu-id="c575c-132">Дополнительные сведения см. в разделе "Создание связей маршрута".</span><span class="sxs-lookup"><span data-stu-id="c575c-132">For more information, see the "To create routing links" section.</span></span>
10.  <span data-ttu-id="c575c-133">В поля **Время работы** и **Время настройки** введите время, необходимое для выполнения производственной операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-133">In the **Run Time** and **Setup Time** fields, enter the process times needed to perform the operation.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c575c-134">Время настройки вычисляется для каждого производственного заказа, в то время как время работы – для каждого изготавливаемого товара.</span><span class="sxs-lookup"><span data-stu-id="c575c-134">Setup time is calculated per production order, whereas run time is calculated per produced item.</span></span>  

11.  <span data-ttu-id="c575c-135">В поле **Одновременные произв. мощности** укажите количество единиц выбранного ресурса, используемых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-135">In the **Concurrent Capacities** field, specify how many units of the selected resource are used to perform the operation.</span></span> <span data-ttu-id="c575c-136">Например, если два человека назначены для выполнения одной упаковочной операции, время работы делится пополам.</span><span class="sxs-lookup"><span data-stu-id="c575c-136">For example, two people allocated to one packing operation will halve the run time.</span></span>  
12.  <span data-ttu-id="c575c-137">Заполните таким же образом строки для всех операций, необходимых для создания данного товара.</span><span class="sxs-lookup"><span data-stu-id="c575c-137">Continue to fill in lines for all operations involved in producing the item in question.</span></span>  
13.  <span data-ttu-id="c575c-138">Строки можно скопировать из существующего маршрута, выбрав действие **Копировать маршрут**, чтобы выбрать готовые строки.</span><span class="sxs-lookup"><span data-stu-id="c575c-138">To copy lines from an existing routing, choose the **Copy Routing** action to select existing lines.</span></span>  
14. <span data-ttu-id="c575c-139">Сертифицируйте маршрут.</span><span class="sxs-lookup"><span data-stu-id="c575c-139">Certify the routing.</span></span>  
15. <span data-ttu-id="c575c-140">Теперь можно присоединить новый маршрут к карточке данного изготавливаемого товара, заполнив поле **Номер маршрута**.</span><span class="sxs-lookup"><span data-stu-id="c575c-140">You can now attach the new routing to the card of the production item in question, by filling in the **Routing No.** field.</span></span> <span data-ttu-id="c575c-141">Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых продуктов](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-141">For more information, see [How to: Register New Products](inventory-how-register-new-items.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c575c-142">Не забудьте пересчитать стандартную себестоимость товара в карточке **Товар**: выберите действие **Производство**, выберите действие **Расчет станд. себестоимости**, затем выберите действие **Все уровни**.</span><span class="sxs-lookup"><span data-stu-id="c575c-142">Remember also to recalculate the item’s standard cost from the **Item** card: Choose the **Manufacturing** action, select the **Calc. Standard Cost** action, and then select the **All Levels** action.</span></span>  

## <a name="to-create-routing-links"></a><span data-ttu-id="c575c-143">Создание связей маршрута</span><span class="sxs-lookup"><span data-stu-id="c575c-143">To create routing links</span></span>
<span data-ttu-id="c575c-144">Можно создавать связи маршрутов для соединения компонентов с определенными операциями и сохранения их связи даже при изменении производственной спецификации или маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-144">You can create routing links to connect components to specific operations in order to retain their relationship even though the production BOM or routing is modified.</span></span> <span data-ttu-id="c575c-145">Связи маршрутов также дают возможность своевременно очищать компоненты, а именно, при запуске не целого производственного заказа, а определенных связанных операций.</span><span class="sxs-lookup"><span data-stu-id="c575c-145">It also facilitates just-in-time flushing of components, namely when the specific linked operation starts, not when the complete production order is released.</span></span> <span data-ttu-id="c575c-146">Дополнительные сведения см. в разделе [Практическое руководство. Списание компонентов в соответствии с производственным выпуском](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-146">For more information see [How to: Flush Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>  

<span data-ttu-id="c575c-147">Другое важное преимущество связей заключается в том, что при использовании окна **Производственный журнал** для учета выхода и потребления эти связанные компоненты и операции отображаются в виде логической структуры процесса.</span><span class="sxs-lookup"><span data-stu-id="c575c-147">Another important benefit is that linked components and operations are displayed in a logical process structure when you use the **Production Journal** window for output and consumption posting.</span></span>  

1.  <span data-ttu-id="c575c-148">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Маршруты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c575c-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c575c-149">Откройте маршрут, содержащий операции, которые необходимо связать.</span><span class="sxs-lookup"><span data-stu-id="c575c-149">Open the routing that contains the operations that you want to link.</span></span>  

    <span data-ttu-id="c575c-150">Убедитесь, что статус маршрутизации — **В разработке**.</span><span class="sxs-lookup"><span data-stu-id="c575c-150">Make sure the routing status is **Under Development**.</span></span>  

3.  <span data-ttu-id="c575c-151">В нужной строке маршрута в поле **Код связи маршрута** выберите код.</span><span class="sxs-lookup"><span data-stu-id="c575c-151">On the relevant routing line, in the **Routing Link Code** field, select a code.</span></span>  
4.  <span data-ttu-id="c575c-152">При необходимости добавьте другие коды связей маршрута к другим операциям маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-152">Proceed to add different routing link codes to other operations in the routing, if relevant.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c575c-153">Не следует использовать один код связи маршрута в разных операциях маршрута, так как компонент может быть неправильно связан с двумя разными операциями, которые, таким образом, будут выполнены дважды.</span><span class="sxs-lookup"><span data-stu-id="c575c-153">You should not use the same routing link code in different operations on a routing because you may incorrectly link a component to two different operations, so that it is consumed two times.</span></span>  
    >   
    >  <span data-ttu-id="c575c-154">Чтобы по связям маршрута можно было определить операцию, с которой они связаны, рекомендуется перед именем кода связи маршрута добавлять имя операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-154">It is a good idea to name the routing link code after the operation in order to ensure operation-specific routing links.</span></span>

5.  <span data-ttu-id="c575c-155">Установите для маршрута статус **Сертифицировано**.</span><span class="sxs-lookup"><span data-stu-id="c575c-155">Set the routing status to **Certified**.</span></span>  

    <span data-ttu-id="c575c-156">Теперь коды маршрутных ссылок назначены операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-156">Routing link codes are now assigned to operations.</span></span> <span data-ttu-id="c575c-157">Далее следует создать фактическую связь путем присвоения одинаковых кодов определенным компонентам в соответствующей производственной спецификации.</span><span class="sxs-lookup"><span data-stu-id="c575c-157">Next, you must create the actual link by assigning the same codes to specific components in the relevant production BOM.</span></span>  

6.  <span data-ttu-id="c575c-158">Откройте **Производственную спецификацию**, содержащую компоненты, которые требуется связать с указанными операциями.</span><span class="sxs-lookup"><span data-stu-id="c575c-158">Open the **Production BOM** that contains the components that you want to link to the above operations.</span></span> <span data-ttu-id="c575c-159">Дополнительные сведения см. в разделе [Практическое руководство. Создание производственных спецификаций](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-159">For more information, see [How to: Create Production BOMs](production-how-to-create-production-boms.md).</span></span>
7.  <span data-ttu-id="c575c-160">Убедитесь, что статус спецификации — **В разработке**.</span><span class="sxs-lookup"><span data-stu-id="c575c-160">Make sure the BOM status is **Under Development**.</span></span>  
8.  <span data-ttu-id="c575c-161">В нужной строке производственной спецификации в поле **Код связи маршрута** выберите код, назначенный соответствующей операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-161">On the relevant production BOM line, in the **Routing Link Code** field, select the code that you have just assigned to the relevant operation.</span></span>  
9. <span data-ttu-id="c575c-162">Добавьте коды связи маршрута к другим компонентам в уникальных операциях, в которых они используются.</span><span class="sxs-lookup"><span data-stu-id="c575c-162">Proceed to add routing link codes to other components according to the unique operations where they are used.</span></span>  
10. <span data-ttu-id="c575c-163">Установите для производственной спецификации статус **Сертифицировано**.</span><span class="sxs-lookup"><span data-stu-id="c575c-163">Set the production BOM status to **Certified**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c575c-164">Чтобы применить связи маршрута к существующему производственному заказу, необходимо сначала обновить этот производственный заказ.</span><span class="sxs-lookup"><span data-stu-id="c575c-164">To enable the routing links on an existing production order, you must refresh the productio1n order.</span></span> <span data-ttu-id="c575c-165">Дополнительные сведения см. в разделе [Практическое руководство. Создание производственных заказов](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c575c-165">For more information, see [How to: Create Production Orders](production-how-to-create-production-orders.md).</span></span>  

<span data-ttu-id="c575c-166">Теперь при создании или обновлении производственного заказа, в котором используется рассматриваемые производственная спецификация и маршрут, выбранные компоненты будут связаны с выбранными операциями.</span><span class="sxs-lookup"><span data-stu-id="c575c-166">The selected components will now be linked to the selected operations when you create or refresh a production order using the production BOM and routing in question.</span></span> <span data-ttu-id="c575c-167">Это видно в окне **Произв. заказ - компоненты** в разделе производственного заказа. Здесь же можно в любой момент удалить и добавить определенные коды связи маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-167">This is visible in the **Prod. Order Components** window under the production order, and here you can also remove and add the defined routing link codes at any time.</span></span>

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a><span data-ttu-id="c575c-168">Чтобы назначить персонал, инструменты и измерения качества операциям маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-168">To assign personnel, tools, and quality measures to routing operations.</span></span>
<span data-ttu-id="c575c-169">При необходимости операции можно назначить персонал, обладающий требуемыми квалификациями, специальными знаниями или полномочиями.</span><span class="sxs-lookup"><span data-stu-id="c575c-169">If you require personnel with qualifications, special knowledge, or special authorization for an operation, you can assign these personnel to the operation.</span></span> <span data-ttu-id="c575c-170">Кроме того, можно назначить инструменты и требования к качеству для операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-170">In addition, you can assign tools and quality requirements to the operation.</span></span> <span data-ttu-id="c575c-171">В этой процедуре описано, как назначить персонал.</span><span class="sxs-lookup"><span data-stu-id="c575c-171">This procedure describes how to assign personnel.</span></span> <span data-ttu-id="c575c-172">Шаги аналогичны для различных типов информации об операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-172">The steps are similar for other types of operation information.</span></span>

1.  <span data-ttu-id="c575c-173">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Маршруты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c575c-173">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c575c-174">Откройте соответствующий маршрут.</span><span class="sxs-lookup"><span data-stu-id="c575c-174">Open the relevant routing.</span></span>  
3.  <span data-ttu-id="c575c-175">На экспресс-вкладке **Строки** выберите строку, которую требуется обработать, затем выберите действие **Персонал**.</span><span class="sxs-lookup"><span data-stu-id="c575c-175">On the **Lines** FastTab, select the line that you want to process, and then choose the **Personnel** action.</span></span>  
4.  <span data-ttu-id="c575c-176">Заполните поля в окне **Персонал маршрута**.</span><span class="sxs-lookup"><span data-stu-id="c575c-176">Fill in the fields in the **Routing Personnel** window.</span></span>  
5.  <span data-ttu-id="c575c-177">Нажмите кнопку **OK** для выхода из окна.</span><span class="sxs-lookup"><span data-stu-id="c575c-177">Choose the **OK** button to exit the window.</span></span> <span data-ttu-id="c575c-178">Введенные значения копируются и присваиваются операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-178">The entered values are copied and assigned to the operation.</span></span>    

## <a name="to-create-a-new-versions-of-a-routing"></a><span data-ttu-id="c575c-179">Создание новых версий маршрута</span><span class="sxs-lookup"><span data-stu-id="c575c-179">To create a new versions of a routing</span></span>  
<span data-ttu-id="c575c-180">Принцип версии позволяет управлять несколькими версиями одного маршрута.</span><span class="sxs-lookup"><span data-stu-id="c575c-180">The version principle enables you to manage several versions of a routing.</span></span> <span data-ttu-id="c575c-181">Структура версии маршрута соответствует структуре маршрута, состоящего из заголовка версии маршрута и ее строк.</span><span class="sxs-lookup"><span data-stu-id="c575c-181">The structure of the routing version corresponds to the structure of the routing consisting of the routing version header and the routing version lines.</span></span> <span data-ttu-id="c575c-182">Основное отличие определяется по дате начала.</span><span class="sxs-lookup"><span data-stu-id="c575c-182">The basic difference is defined by the starting date.</span></span>  

1.  <span data-ttu-id="c575c-183">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Маршруты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c575c-183">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c575c-184">Выберите маршрут для копирования, затем выберите действие **Версии**.</span><span class="sxs-lookup"><span data-stu-id="c575c-184">Select the routing to be copied, and then choose the **Versions** action.</span></span>  
3. <span data-ttu-id="c575c-185">В окне **Версии маршрута** выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c575c-185">In the **Routing Versions** window, choose the **New** action.</span></span>
4. <span data-ttu-id="c575c-186">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="c575c-186">Fill in the fields as necessary.</span></span>
5.  <span data-ttu-id="c575c-187">В поле **Код версии** введите уникальный идентификатор версии.</span><span class="sxs-lookup"><span data-stu-id="c575c-187">In the **Version Code** field, enter the unique identification of the version.</span></span> <span data-ttu-id="c575c-188">Можно использовать любую комбинацию цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="c575c-188">Any combination of numbers and letters is permitted.</span></span>  

    <span data-ttu-id="c575c-189">Вновь созданной версии автоматически присваивается статус **Новая**.</span><span class="sxs-lookup"><span data-stu-id="c575c-189">The newly created version is automatically assigned the status **New**.</span></span>  
6.  <span data-ttu-id="c575c-190">Для создания строк операций выберите первую пустую строку, затем заполните **Номер операции**</span><span class="sxs-lookup"><span data-stu-id="c575c-190">To create operation lines, select the first blank line, and then fill in the **Operation No.**</span></span> <span data-ttu-id="c575c-191">в соответствии с порядком операций.</span><span class="sxs-lookup"><span data-stu-id="c575c-191">field according to the sequence of operations.</span></span>

    <span data-ttu-id="c575c-192">Строки операций сортируются в порядке возрастания по номерам операций.</span><span class="sxs-lookup"><span data-stu-id="c575c-192">The operation lines are sorted in ascending order by operation numbers.</span></span> <span data-ttu-id="c575c-193">Рекомендуется выбирать достаточную ширину подзадачи для того, чтобы обеспечить возможность последующих изменений.</span><span class="sxs-lookup"><span data-stu-id="c575c-193">To be able to make changes later, we recommend you to select adequate step widths.</span></span> <span data-ttu-id="c575c-194">Поле **Номер след. произв. операции**</span><span class="sxs-lookup"><span data-stu-id="c575c-194">The **Next Operation No.**</span></span> <span data-ttu-id="c575c-195">относится к следующей операции.</span><span class="sxs-lookup"><span data-stu-id="c575c-195">field refers to the following operation.</span></span> <span data-ttu-id="c575c-196">Номер операции можно ввести непосредственно.</span><span class="sxs-lookup"><span data-stu-id="c575c-196">The number of the operation can be entered directly.</span></span>

7. <span data-ttu-id="c575c-197">Когда версия маршрута готова, установив в поле **Статус** значение **Сертифицировано**.</span><span class="sxs-lookup"><span data-stu-id="c575c-197">When the routing version is completed, setting the **Status** field to **Certified**.</span></span>

<span data-ttu-id="c575c-198">Время действия версии определяется полем **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="c575c-198">The time validity of the version is specified by the **Starting Date** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c575c-199">См. также</span><span class="sxs-lookup"><span data-stu-id="c575c-199">See Also</span></span>  
[<span data-ttu-id="c575c-200">Практическое руководство. Создание производственных спецификаций</span><span class="sxs-lookup"><span data-stu-id="c575c-200">How to: Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="c575c-201">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="c575c-201">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c575c-202">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c575c-202">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="c575c-203">[Планирование](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="c575c-203">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="c575c-204">Наличие</span><span class="sxs-lookup"><span data-stu-id="c575c-204">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c575c-205">Покупки</span><span class="sxs-lookup"><span data-stu-id="c575c-205">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c575c-206">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c575c-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
