---
title: "Как рассчитать пополнение ячейки | Документы Майкрософт"
description: "Если склад настроен для использования направленного подбора и размещения, приоритеты шаблона размещения для данного склада учитываются при размещении приходных накладных."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a683d2f88f8c30d457d44facd21b0068688ad05a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-calculate-bin-replenishment"></a><span data-ttu-id="6da82-103">Практическое руководство. Расчет пополнения ячеек</span><span class="sxs-lookup"><span data-stu-id="6da82-103">How to: Calculate Bin Replenishment</span></span>
<span data-ttu-id="6da82-104">Если склад настроен для использования направленного подбора и размещения, приоритеты шаблона размещения для данного склада учитываются при размещении приходных накладных.</span><span class="sxs-lookup"><span data-stu-id="6da82-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="6da82-105">Приоритеты включают максимальное и минимальное количества содержимого ячеек, которые были зафиксированы для конкретной ячейки, а также рейтинги ячеек.</span><span class="sxs-lookup"><span data-stu-id="6da82-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="6da82-106">Следовательно, если товары поступают равномерно, наиболее часто используемые ячейки подбора будут заполняться по мере их опорожнения.</span><span class="sxs-lookup"><span data-stu-id="6da82-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="6da82-107">Но товары не всегда поступают равномерно.</span><span class="sxs-lookup"><span data-stu-id="6da82-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="6da82-108">Иногда товары закупаются в больших количествах, чтобы организация получила скидку, или производственное подразделение изготавливает большое количество одного товара для уменьшения себестоимости единицы.</span><span class="sxs-lookup"><span data-stu-id="6da82-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="6da82-109">После этого данные товары не будут поступать на склад в течение какого-то времени, и складу необходимо периодически перемещать товары в ячейки подбора из навалочной зоны.</span><span class="sxs-lookup"><span data-stu-id="6da82-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="6da82-110">Иногда на складе ожидается скорое поступление новых товаров, и необходимо освободить навалочную зону до их поступления.</span><span class="sxs-lookup"><span data-stu-id="6da82-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="6da82-111">Наконец, если тип ячейки навалочного хранения содержит только действие **размещения**, т. е. для типа ячейки флажок действия **Подбор** не установлен, то ячейки подбора должны постоянно пополняться, т. к. программа не будет предлагать подбора товаров только из ячеек типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="6da82-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="6da82-112">Пополнение ячеек подбора</span><span class="sxs-lookup"><span data-stu-id="6da82-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="6da82-113">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал перемещения**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6da82-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6da82-114">Выберите действие **Расчет пополнения ячеек**, чтобы открыть страницу запроса отчета.</span><span class="sxs-lookup"><span data-stu-id="6da82-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="6da82-115">Заполните окно запроса пакетного задания для того, чтобы ограничить рамки предложений по пополнению, которые будут рассчитываться.</span><span class="sxs-lookup"><span data-stu-id="6da82-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="6da82-116">Например, может потребоваться обработка только конкретных товаров, зон или ячеек.</span><span class="sxs-lookup"><span data-stu-id="6da82-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="6da82-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6da82-117">Choose the **OK** button.</span></span> <span data-ttu-id="6da82-118">Будут созданы строки для передвижений пополнения, которые необходимо выполнить согласно правилам, настроенным для ячеек и содержимого ячеек (то есть товаров в ячейках).</span><span class="sxs-lookup"><span data-stu-id="6da82-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="6da82-119">Если необходимо выполнить все предложенные пополнения, выберите действие **Создать передвижение**.</span><span class="sxs-lookup"><span data-stu-id="6da82-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="6da82-120">Теперь сотрудники должны найти инструкции в пункте меню **Перемещения**, выполнить и зарегистрировать их.</span><span class="sxs-lookup"><span data-stu-id="6da82-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="6da82-121">Если необходимо выполнить некоторые из предложенных пополнений, удалите менее важные строки и затем создайте передвижение.</span><span class="sxs-lookup"><span data-stu-id="6da82-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="6da82-122">Когда пополнение ячеек будет рассчитываться в следующий раз, удаленные предложения будут созданы заново, если они еще имеют силу.</span><span class="sxs-lookup"><span data-stu-id="6da82-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6da82-123">Если товар соответствует следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="6da82-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="6da82-124">Указан срок годности товара и</span><span class="sxs-lookup"><span data-stu-id="6da82-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="6da82-125">Выбрано поле **Выбрать по методу FEFO** в карточке склада, и</span><span class="sxs-lookup"><span data-stu-id="6da82-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="6da82-126">Вы используете функцию **Расчет пополнения ячеек**</span><span class="sxs-lookup"><span data-stu-id="6da82-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="6da82-127">то поля **Из зоны** и **Из ячейки** будут пусты, потому что алгоритм, рассчитывающий, откуда необходимо переместить товары, запускается при активации функции **Создать передвижение**.</span><span class="sxs-lookup"><span data-stu-id="6da82-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6da82-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6da82-128">See Also</span></span>  
[<span data-ttu-id="6da82-129">Управление складом</span><span class="sxs-lookup"><span data-stu-id="6da82-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6da82-130">Подбор по методу FEFO</span><span class="sxs-lookup"><span data-stu-id="6da82-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="6da82-131">Наличие</span><span class="sxs-lookup"><span data-stu-id="6da82-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6da82-132">[Настройка управления складом](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6da82-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6da82-133">[Управление сборкой](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6da82-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6da82-134">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="6da82-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6da82-135">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6da82-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
