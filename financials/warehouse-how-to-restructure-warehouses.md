---
title: "Как изменять структуру складов | Документы Майкрософт"
description: "Может возникнуть необходимость реструктуризации склада и введения новых кодов и характеристик ячеек."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: da5928be8280bad2eac379a5f0e5b19ddc2d12bc
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-restructure-warehouses"></a><span data-ttu-id="476ed-103">Практическое руководство. Изменение структуры складов</span><span class="sxs-lookup"><span data-stu-id="476ed-103">How to: Restructure Warehouses</span></span>
<span data-ttu-id="476ed-104">Может возникнуть необходимость реструктуризации склада и введения новых кодов и характеристик ячеек.</span><span class="sxs-lookup"><span data-stu-id="476ed-104">You may want to restructure your warehouse with new bin codes and new bin characteristics.</span></span> <span data-ttu-id="476ed-105">Этот род действий применяется не слишком часто, но иногда для достижения или обеспечения более эффективной работы склада необходима реклассификация.</span><span class="sxs-lookup"><span data-stu-id="476ed-105">You will not undertake this kind of activity very often, but situations can occur where a reclassification is necessary to achieve or maintain a more efficient operation.</span></span> <span data-ttu-id="476ed-106">Например:</span><span class="sxs-lookup"><span data-stu-id="476ed-106">For example:</span></span>  

- <span data-ttu-id="476ed-107">Необходимо включить в коды ячеек, которые поддерживают использование автоматизированных систем сбора данных, переносные мониторы.</span><span class="sxs-lookup"><span data-stu-id="476ed-107">You might want to switch to bin codes that support the use of automatic data capture, for example, with hand-held devices.</span></span>  
- <span data-ttu-id="476ed-108">Склад закупил новую систему стеллажей, предоставляющую новые возможности для хранения товаров.</span><span class="sxs-lookup"><span data-stu-id="476ed-108">The warehouse may have purchased a new rack system that gives new possibilities in item storage.</span></span>  
- <span data-ttu-id="476ed-109">Организация изменила ассортимент товаров и в связи с этим перевела склад на новое место.</span><span class="sxs-lookup"><span data-stu-id="476ed-109">The company may have altered its item assortment and moved the warehouse to a new physical location to accommodate this change.</span></span>  

<span data-ttu-id="476ed-110">Если склад настроен на использование ячеек, но расширенный подбор и размещение не используются, выполните реструктуризацию склада, создав новые ячейки для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="476ed-110">If your warehouse is set up to use bins but not directed put-away and pick, restructure your warehouse by creating the new bins that you want to use in the future.</span></span>  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a><span data-ttu-id="476ed-111">Изменение структуры основного склада, для которого используются только ячейки</span><span class="sxs-lookup"><span data-stu-id="476ed-111">To restructure a basic warehouse that uses bins only</span></span>  
1.  <span data-ttu-id="476ed-112">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="476ed-113">На экспресс-вкладке **Склад** в поле **Выбор ячейки по умолчанию** установите значение **Последняя использовавшаяся ячейка**.</span><span class="sxs-lookup"><span data-stu-id="476ed-113">On the **Warehouse** FastTab, set the **Default Bin Selection** field to **Last-Used Bin**.</span></span>  
3.  <span data-ttu-id="476ed-114">Переместите все содержимое текущих ячеек в новые, только что созданные ячейки.</span><span class="sxs-lookup"><span data-stu-id="476ed-114">Move all the contents of your current bins to the new bins that you have just created.</span></span>  

    1.  <span data-ttu-id="476ed-115">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал реклассификации товаров**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclassification Journal**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="476ed-116">Выберите строку журнала, затем выберите действие **Получить содержимое ячейки**.</span><span class="sxs-lookup"><span data-stu-id="476ed-116">Select a journal line, and then choose the **Get Bin Content** action.</span></span>  
    3.  <span data-ttu-id="476ed-117">На экспресс-вкладке **Содержимое ячейки** настройте фильтры в полях **Код склада**, **Код ячейки** и **Код товара**, чтобы определить содержимое, которое необходимо переместить.</span><span class="sxs-lookup"><span data-stu-id="476ed-117">On the **Bin Content** FastTab, set filters in the **Location Code**, **Bin Code**, and **Item No.** fields to specify the content that you want to move.</span></span>  
    4.  <span data-ttu-id="476ed-118">Нажмите кнопку **OK** чтобы заполнить строку журнала.</span><span class="sxs-lookup"><span data-stu-id="476ed-118">Choose the **OK** button to fill a journal line.</span></span>  
    5.  <span data-ttu-id="476ed-119">В поле **Код новой ячейки** выберите ячейку, в которую следует переместить товары.</span><span class="sxs-lookup"><span data-stu-id="476ed-119">In the **New Bin Code** field, select the bin to which the items should be moved.</span></span>  
    6.  <span data-ttu-id="476ed-120">Повторите шаги с b по e для всего содержимого ячейки, которое необходимо переместить.</span><span class="sxs-lookup"><span data-stu-id="476ed-120">Repeat steps b through e for all bin content that you want to move.</span></span>  
    7.  <span data-ttu-id="476ed-121">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="476ed-121">Choose the **Post** action.</span></span>  

<span data-ttu-id="476ed-122">Теперь ячейки, где ранее были указаны товары, очищены.</span><span class="sxs-lookup"><span data-stu-id="476ed-122">You have now emptied the bins where the items used to be.</span></span> <span data-ttu-id="476ed-123">Теперь ячейки по умолчанию для товаров заменены на новые ячейки.</span><span class="sxs-lookup"><span data-stu-id="476ed-123">The default bins for your items have now been changed to the new bins.</span></span>  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a><span data-ttu-id="476ed-124">Изменение структуры склада расширенной конфигурации, для которого используются расширенные подбор и размещение</span><span class="sxs-lookup"><span data-stu-id="476ed-124">To restructure an advanced warehouse that uses directed put-away and pick</span></span>  

1.  <span data-ttu-id="476ed-125">Создать новые ячейки, которые будут использоваться в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="476ed-125">Create the new bins that you want to use in the future.</span></span> <span data-ttu-id="476ed-126">Дополнительные сведения см. в разделе [Практическое руководство. Создание ячеек](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="476ed-126">For more information, see [How to: Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  
2.  <span data-ttu-id="476ed-127">Переместите все содержимое имеющихся ячеек в новые, только что созданные ячейки.</span><span class="sxs-lookup"><span data-stu-id="476ed-127">Move all the contents of your current bins to the new bins that you just created.</span></span>  

    1.  <span data-ttu-id="476ed-128">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал реклассификации склада**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Reclassification Journal**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="476ed-129">Для ячеек, в которых реального движения товаров не происходит, создайте для каждой из текущих ячеек в **Журнале реклассификации склада** по строке со старым кодом ячейки (**Из кода ячейки**) и новым кодом ячейки (**В код ячейки**).</span><span class="sxs-lookup"><span data-stu-id="476ed-129">For the bins where no real movement of items is involved, create a line for each of your current bins in the **Warehouse Reclassification Journal** with the old bin code, **From Bin Code**, and the new bin code, **To Bin Code**.</span></span>  
    3.  <span data-ttu-id="476ed-130">Если некоторые передвижения включают физическое передвижение товаров, которое будет выполнено работниками склада, то для подготовки инструкций по передвижению вместо использования журнала реклассификации складов использовать **Журналы перемещений**.</span><span class="sxs-lookup"><span data-stu-id="476ed-130">If some of the movements involve actual physical movements that you want employees to perform, use **Movement Worksheets** to prepare movement instructions instead of using the warehouse reclassification journal.</span></span> <span data-ttu-id="476ed-131">Дополнительные сведения см. в разделе [Практическое руководство. Перемещение товаров в расширенных конфигурациях склада](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="476ed-131">For more information, see [How to: Move Items in Advanced Warehouse Configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

3.  <span data-ttu-id="476ed-132">Когда старые ячейки очищаются, выполняется их реклассификация с присвоением ячейкам типа **КОНКАЧ**, чтобы предотвратить их включение в товарные потоки.</span><span class="sxs-lookup"><span data-stu-id="476ed-132">When the old bins are emptied, reclassify them as **QC** type bins to ensure that they are not included in item flows.</span></span>  

    1.  <span data-ttu-id="476ed-133">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="476ed-134">Выберите строку со складом, затем выберите действие **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="476ed-134">Select the line with the location, and then choose the **Bins** action.</span></span>  
    3.  <span data-ttu-id="476ed-135">В окне **Ячейки** в поле **Код типа ячейки** введите **QC** для каждой из старых ячеек, которые вы опорожнили на шаге 3 в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="476ed-135">In the **Bins** window, in the **Bin Type Code** field, enter **QC** for each of the old bins that you emptied in step 3 in the previous procedure.</span></span>  

<span data-ttu-id="476ed-136">Теперь ячейки исключены из складского потока и повторно классифицированы как ячейки типа QC. Ячейки типа QC не содержат полей действий в выбранном окне **Типы ячеек** и поэтому не учитываются в потоке товаров.</span><span class="sxs-lookup"><span data-stu-id="476ed-136">You have now removed the bins from the warehouse flow, and reclassified them as QC bins. QC bins have none of the activity fields in the **Bin Types** window selected and are therefore not considered by the item flow.</span></span> <span data-ttu-id="476ed-137">Дополнительные сведения см. в разделе [Практическое руководство. Настройка типов ячеек](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="476ed-137">For more information, see [How to: Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="to-delete-a-bin"></a><span data-ttu-id="476ed-138">Удаление ячейки</span><span class="sxs-lookup"><span data-stu-id="476ed-138">To delete a bin</span></span>  

1.  <span data-ttu-id="476ed-139">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="476ed-140">Выберите склад, где необходимо удалить ячейки. Выберите действие **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="476ed-140">Select the location where you want to delete bins. Choose the **Bins** action.</span></span>  
3.  <span data-ttu-id="476ed-141">Выберите строки для ячеек, которые необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="476ed-141">Select the lines for the bins that you want to delete.</span></span>  
4.  <span data-ttu-id="476ed-142">Выберите действие **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="476ed-142">Choose the **Delete** action.</span></span>  

<span data-ttu-id="476ed-143">Если нажать кнопку **Да**, ячейка удаляется, но код ячейки в складских операциях остается прежним.</span><span class="sxs-lookup"><span data-stu-id="476ed-143">If you choose the **Yes** button, the bin is deleted for use in the future, but the bin code in all warehouse entries remains the same.</span></span>  

<span data-ttu-id="476ed-144">Если ячейка переименовывается так, что переименовываются также все записи, связанные с этой ячейкой, включая содержимое ячейки, строки складских действий, строки зарегистрированных складских действий, строки складских журналов, строки складских приемок, строки учтенных складских приемок, строки складских отгрузок, строки учтенных складских отгрузок и складские операции, то это выполняется в окне **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="476ed-144">If you want to rename a bin so that all records associated with the bin are also renamed, including bin contents, warehouse activity lines, registered warehouse activity lines, warehouse worksheet lines, warehouse receipt lines, posted warehouse receipt lines, warehouse shipment lines, posted warehouse shipment lines, and warehouse entries, you can do so in the **Bins** window.</span></span>  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a><span data-ttu-id="476ed-145">Удаление ячейки и изменение кода ячейки во всех записях</span><span class="sxs-lookup"><span data-stu-id="476ed-145">To rename a bin and change the bin code in all records</span></span>  

1.  <span data-ttu-id="476ed-146">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="476ed-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="476ed-147">Выберите склад, где необходимо переименовать ячейку или изменить код ячейки, затем выберите действие **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="476ed-147">Select the location where you want to rename a bin or change the bin code, and then choose the **Bins** action.</span></span>  
3.  <span data-ttu-id="476ed-148">Выберите ячейку, которую необходимо изменить, и введите новый код ячейки в поле **Код**.</span><span class="sxs-lookup"><span data-stu-id="476ed-148">Select the bin that you want to change and enter a new bin code in the **Code** field.</span></span>  
4.  <span data-ttu-id="476ed-149">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="476ed-149">Choose the **Yes** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="476ed-150">Если выбрано значение **Да** и имеется множество операций в отношении этой ячейки, например, поскольку складские документы не были удалены в течение какого-то времени, переименование всех записей может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="476ed-150">If you choose **Yes** and there are many entries concerning this bin, for example, because you have not deleted warehouse documents for some time, it may take some time to rename all the records.</span></span> <span data-ttu-id="476ed-151">Следовательно, при использовании этого метода рассмотрите возможность выполнения пакетного задания **Удалить зарег. склад. документы** перед началом процесса переименования.</span><span class="sxs-lookup"><span data-stu-id="476ed-151">Therefore, if you use this method, consider running the batch job **Delete Registered Whse. Documents** before you start the renaming process.</span></span> <span data-ttu-id="476ed-152">Обратите также внимание, что единственными удаляемыми документами в этом пакетном задании являются размещения, подборы и перемещения.</span><span class="sxs-lookup"><span data-stu-id="476ed-152">Also note that the only documents that are deleted in this batch job are put-aways, picks, and movements.</span></span>  
>   
>  <span data-ttu-id="476ed-153">Если происходит переименование ячейки получения или ячейка поставки, все учтенные приемки или отгрузки, которые ссылаются на указанную ячейку, будут переименованы.</span><span class="sxs-lookup"><span data-stu-id="476ed-153">If you are renaming a receiving bin or a shipping bin, all the posted receipts or shipments that refer to the bin in question are renamed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="476ed-154">См. также</span><span class="sxs-lookup"><span data-stu-id="476ed-154">See Also</span></span>  
[<span data-ttu-id="476ed-155">Управление складом</span><span class="sxs-lookup"><span data-stu-id="476ed-155">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="476ed-156">Наличие</span><span class="sxs-lookup"><span data-stu-id="476ed-156">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="476ed-157">[Настройка управления складом](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="476ed-157">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="476ed-158">[Управление сборкой](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="476ed-158">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="476ed-159">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="476ed-159">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="476ed-160">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="476ed-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
