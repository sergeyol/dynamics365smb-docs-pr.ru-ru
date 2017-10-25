---
title: "Приобретение основных средств | Документы Майкрософт"
description: "Вы можете настроить основное средство, назначить книгу амортизации и записать стоимость приобретения ОС."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 903c1a858fe66482cb4404e8b792abade6106489
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-acquire-fixed-assets"></a><span data-ttu-id="678d5-103">Практическое руководство. Приобретение основных средств</span><span class="sxs-lookup"><span data-stu-id="678d5-103">How to: Acquire Fixed Assets</span></span>
<span data-ttu-id="678d5-104">Для каждого из основных средств необходимо настроить карточку, содержащую сведения об этом активе.</span><span class="sxs-lookup"><span data-stu-id="678d5-104">For each fixed asset, you must set up a card containing information about the asset.</span></span> <span data-ttu-id="678d5-105">Можно настроить здания или производственное оборудование как основное средство со списком компонентов, и их можно группировать разными способами, например по классам, подразделениям или расположению.</span><span class="sxs-lookup"><span data-stu-id="678d5-105">You can set up buildings or production equipment as a main asset with a component list, and you can group them in various ways, such as by class, department, or location.</span></span> <span data-ttu-id="678d5-106">Книгу амортизации следует настроить и назначить каждому основному средству, прежде чем его можно будет приобрести.</span><span class="sxs-lookup"><span data-stu-id="678d5-106">A depreciation book must be set up and assigned to each fixed asset before you can acquire it.</span></span>

<span data-ttu-id="678d5-107">После настройки основного средства и назначения книги амортизации необходимо приобрести основное средство.</span><span class="sxs-lookup"><span data-stu-id="678d5-107">When a fixed asset is set up and a depreciation book assigned, you must acquire the fixed asset.</span></span> <span data-ttu-id="678d5-108">Для приобретения основного средства стоимость его приобретения регистрируется на соответствующем счете ГК, банковском счете или счете поставщика путем учета транзакций приобретения из окна **Журнал ГК учета основных средств**.</span><span class="sxs-lookup"><span data-stu-id="678d5-108">To acquire a fixed asset, you record its acquisition cost in the relevant G/L account, bank account, or vendor by posting an acquisition transaction from the **Fixed Asset G/L Journal** window.</span></span> <span data-ttu-id="678d5-109">Можно использовать окно **Помощь в приобретении основных средств** для автоматического создания и учета необходимых строк финансового журнала.</span><span class="sxs-lookup"><span data-stu-id="678d5-109">You can use the **Assisted Fixed Asset Acquisition** window to create and post the required general journal lines automatically.</span></span>

<span data-ttu-id="678d5-110">Ликвидационная стоимость — это стоимость остатка основного средства на момент, когда оно более не пригодно для использования.</span><span class="sxs-lookup"><span data-stu-id="678d5-110">The salvage value is the residual value of a fixed asset when it can no longer be used.</span></span> <span data-ttu-id="678d5-111">Ликвидационную стоимость можно учесть одновременно с учетом стоимости приобретения.</span><span class="sxs-lookup"><span data-stu-id="678d5-111">You can post the salvage value at the same time as you post the acquisition cost.</span></span> <span data-ttu-id="678d5-112">Дополнительные сведения см. в разделе [Практическое руководство. Амортизация основных средств](fa-how-depreciate-amortize.md).</span><span class="sxs-lookup"><span data-stu-id="678d5-112">For more information, see [How to: Depreciate or Amortize Fixed Assets](fa-how-depreciate-amortize.md).</span></span>

<span data-ttu-id="678d5-113">Переоценка используется для коррекции значений при изменении общего уровня цен.</span><span class="sxs-lookup"><span data-stu-id="678d5-113">Indexation is used to adjust values for general price-level changes.</span></span> <span data-ttu-id="678d5-114">Для вычисления стоимости приобретения и стоимости замены можно использовать пакетное задание **Индекс ОС**.</span><span class="sxs-lookup"><span data-stu-id="678d5-114">The **Index Fixed Assets** batch job can be used to calculate the acquisition costs at replacement costs.</span></span>

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a><span data-ttu-id="678d5-115">Создание основного средства и его автоматическое приобретение</span><span class="sxs-lookup"><span data-stu-id="678d5-115">To create a fixed asset and acquire it automatically</span></span>
<span data-ttu-id="678d5-116">В следующей процедуре описывается, как создать основное средство, а затем приобрести его с помощью окна **Помощь в приобретении основных средств**, чтобы создать и учесть необходимые строки журнала ГК учета основных средств.</span><span class="sxs-lookup"><span data-stu-id="678d5-116">The following procedure describes how to create a fixed asset and then acquire it by using the **Assisted Fixed Asset Acquisition** window to create and post the required fixed asset G/L journal lines.</span></span> <span data-ttu-id="678d5-117">Можно также создавать и учитывать строки журнала вручную.</span><span class="sxs-lookup"><span data-stu-id="678d5-117">You can also create and post the journal lines manually.</span></span> <span data-ttu-id="678d5-118">Дополнительные сведения см. в разделе "Разноска приобретения основного средства вручную с помощью журнала ГК учета основных средств".</span><span class="sxs-lookup"><span data-stu-id="678d5-118">For more information, see the "To post a fixed asset acquisition manually with the fixed asset G/L journal" section.</span></span>

1. <span data-ttu-id="678d5-119">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Основные средства**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="678d5-120">Выберите действие **Создать**, затем требуемым образом заполните поля на экспресс-вкладке **Общее**.</span><span class="sxs-lookup"><span data-stu-id="678d5-120">Choose the **New** action, and then fill in the fields on the **General** FastTab as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="678d5-121">На экспресс-вкладке **Книга амортизации** заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="678d5-121">On the **Depreciation Book** FastTab, fill in the fields as necessary.</span></span> <span data-ttu-id="678d5-122">Этот шаг назначает журнал амортизации основному средству.</span><span class="sxs-lookup"><span data-stu-id="678d5-122">This step assigns a depreciation book to the fixed asset.</span></span>  
4. <span data-ttu-id="678d5-123">Если требуется назначить основному средству более одной книги амортизации, выберите действие **Добавить несколько книг амортизации**.</span><span class="sxs-lookup"><span data-stu-id="678d5-123">If you need to assign more than one depreciation book to the fixed asset, choose the **Add More Depreciation Books** action.</span></span> <span data-ttu-id="678d5-124">Дополнительные сведения см. в пункте "Назначение книги амортизации основному средству" в разделе [Практическое руководство. Настройка амортизации основных средств](fa-how-setup-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="678d5-124">For more information, see the "To assign a depreciation book to a fixed asset" section in [How to: Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).</span></span>

    <span data-ttu-id="678d5-125">После заполнения всех полей, необходимых для приобретения основного средства вверху страницы появляется уведомление **Все готово к приобретению основного средства. Приобрести**.</span><span class="sxs-lookup"><span data-stu-id="678d5-125">When all fields required to acquire a fixed asset are filled in, the **You are ready to acquire the fixed asset. Acquire** notification appears at the top of the page.</span></span>
5. <span data-ttu-id="678d5-126">Выберите в уведомлении действие **Приобрести**.</span><span class="sxs-lookup"><span data-stu-id="678d5-126">Choose the **Acquire** action in the notification.</span></span>
6. <span data-ttu-id="678d5-127">Выполните шаги в окне **Помощь в приобретении основных средств** для выполнения автоматического приобретения основного средства.</span><span class="sxs-lookup"><span data-stu-id="678d5-127">Follow the steps in the **Assisted Fixed Asset Acquisition** window to complete the automatic acquisition of the fixed asset.</span></span>

> [!NOTE]  
>   <span data-ttu-id="678d5-128">Можно также учитывать стоимость приобретения как суммы по кредиту.</span><span class="sxs-lookup"><span data-stu-id="678d5-128">You can also post acquisition cost as credits.</span></span> <span data-ttu-id="678d5-129">В этом случае не забудьте, что значение в поле **Стоимость приобретения с учетом НДС** должно быть отрицательным, чтобы указать кредит.</span><span class="sxs-lookup"><span data-stu-id="678d5-129">In that case, remember that the value in the **Acquisition Cost Incl. VAT** field must be with a minus sign to indicate a credit.</span></span>

<span data-ttu-id="678d5-130">При выборе **Готово** заполняется поле **Балансовая стоимость** в окне **Карточка ОС**, указывая, что основное средство было приобретено по указанной стоимости приобретения.</span><span class="sxs-lookup"><span data-stu-id="678d5-130">When you choose **Finish**, the **Book Value** field in the **Fixed Asset Card** window is filled, indicating that the fixed asset has been acquired at the specified acquisition cost.</span></span>  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a><span data-ttu-id="678d5-131">Настройка списка компонентов для основного средства</span><span class="sxs-lookup"><span data-stu-id="678d5-131">To set up a component list for a main asset</span></span>
<span data-ttu-id="678d5-132">Основные средства можно разделить на комплекты ОС и их компоненты.</span><span class="sxs-lookup"><span data-stu-id="678d5-132">You can group your fixed assets into main assets and their components.</span></span> <span data-ttu-id="678d5-133">Например, может иметься производственный станок, состоящий из множества деталей, которые необходимо разделить таким образом.</span><span class="sxs-lookup"><span data-stu-id="678d5-133">For example, you may have a production machine that consists of many parts that you want to group in this manner.</span></span>  

<span data-ttu-id="678d5-134">Комплект ОС и все его компоненты должны быть настроены как отдельные карточки основных средств.</span><span class="sxs-lookup"><span data-stu-id="678d5-134">Both the main asset and all its components must be set up as individual fixed asset cards.</span></span> <span data-ttu-id="678d5-135">После настройки списка компонентов [!INCLUDE[d365fin](includes/d365fin_md.md)] автоматически заполняет поля **Комплект ОС - компоненты** и **Компоненты комплекта ОС** в карточках основных средств.</span><span class="sxs-lookup"><span data-stu-id="678d5-135">After you have set up a component list, [!INCLUDE[d365fin](includes/d365fin_md.md)] automatically fills in the **Main Assets/Component** and **Components of Main Asset** fields on the fixed asset cards.</span></span>

1. <span data-ttu-id="678d5-136">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Основные средства**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="678d5-137">Выберите основное средство, которое является главным средством, затем выберите действие **Компоненты комплекта ОС**.</span><span class="sxs-lookup"><span data-stu-id="678d5-137">Select the fixed asset that is the main asset, and then choose the **Main Asset Components** action.</span></span>
3. <span data-ttu-id="678d5-138">В окне **Компоненты комплекта ОС** выберите поле **Номер ОС**, затем выберите основное средство, которое требуется добавить как компонент ОС.</span><span class="sxs-lookup"><span data-stu-id="678d5-138">In the **Main Asset Components** window, choose the **FA No**. field, and then select the fixed asset that you want to add as a component of the main asset.</span></span>
4. <span data-ttu-id="678d5-139">Закройте окно.</span><span class="sxs-lookup"><span data-stu-id="678d5-139">Close the window.</span></span>
5. <span data-ttu-id="678d5-140">Повторите шаги 3 и 4 для каждого компонентного основного средства, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="678d5-140">Repeat steps 3 and 4 for each component asset that you want to add.</span></span>
6. <span data-ttu-id="678d5-141">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка модуля ОС**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Asset Setup**, and then choose the related link.</span></span>
7. <span data-ttu-id="678d5-142">Установите флажок **Разрешить учет в комплектах ОС**.</span><span class="sxs-lookup"><span data-stu-id="678d5-142">Select the **Allow Posting to Main Assets** check box.</span></span>

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a><span data-ttu-id="678d5-143">Учет приобретения основного средства вручную с помощью журнала ГК учета основных средств</span><span class="sxs-lookup"><span data-stu-id="678d5-143">To post a fixed asset acquisition manually with the fixed asset G/L journal</span></span>
<span data-ttu-id="678d5-144">Следующая процедура описывает способ приобретения основного средства вручную путем создания и учета строк в окне **Журнал ГК учета основных средств**.</span><span class="sxs-lookup"><span data-stu-id="678d5-144">The following procedure describes how to acquire a fixed asset manually by creating and posting lines in the **Fixed Asset G/L Journal** window.</span></span> <span data-ttu-id="678d5-145">Можно также приобрести основное средство автоматически с помощью окна **Помощь в приобретении основных средств**.</span><span class="sxs-lookup"><span data-stu-id="678d5-145">You can also acquire a fixed asset automatically by using the **Assisted Fixed Asset Acquisition** window.</span></span> <span data-ttu-id="678d5-146">Дополнительные сведения см. в шаге 5 раздела "Создание основного средства и его автоматическое приобретение".</span><span class="sxs-lookup"><span data-stu-id="678d5-146">For more information, see step 5 in the "To create a fixed asset and acquire it automatically" section.</span></span>

> [!NOTE]  
>   <span data-ttu-id="678d5-147">Можно также учитывать стоимость приобретения как суммы по кредиту.</span><span class="sxs-lookup"><span data-stu-id="678d5-147">You can also post acquisition cost as credits.</span></span> <span data-ttu-id="678d5-148">В этом случае не забудьте, что значение в поле **Сумма** должно быть отрицательным, чтобы указать кредит.</span><span class="sxs-lookup"><span data-stu-id="678d5-148">In that case, remember that the value in the **Amount** field must be with a minus sign to indicate a credit.</span></span>

1. <span data-ttu-id="678d5-149">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы ГК ОС**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="678d5-150">В окне **Журнал ГК учета основных средств** в поле **Тип учета ОС** выберите **Стоимость приобретения**.</span><span class="sxs-lookup"><span data-stu-id="678d5-150">In the **Fixed Asset G/L Journal** window, in the **FA Posting Type** field, select **Acquisition Cost**.</span></span>
3. <span data-ttu-id="678d5-151">Заполните соответствующим образом остальные поля.</span><span class="sxs-lookup"><span data-stu-id="678d5-151">Fill in the remaining fields as necessary.</span></span>
4. <span data-ttu-id="678d5-152">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="678d5-152">Choose the **Post** action.</span></span>  

> [!TIP]  
>   <span data-ttu-id="678d5-153">Если заполняется поле **Номер страхования** в ГК журнала ОС при выполнении учета стоимости приобретения, то [!INCLUDE[d365fin](includes/d365fin_md.md)] будет учитывать также стоимость приобретения основного средства в книге страхования.</span><span class="sxs-lookup"><span data-stu-id="678d5-153">If you fill in the **Insurance No.** field in the fixed asset G/L journal when you post an acquisition cost, then [!INCLUDE[d365fin](includes/d365fin_md.md)] will also post the acquisition cost of the fixed asset to the insurance coverage ledger.</span></span> <span data-ttu-id="678d5-154">Дополнительные сведения см. в разделе [Практическое руководство. Страхование основных средств](fa-how-insure.md).</span><span class="sxs-lookup"><span data-stu-id="678d5-154">For more information, see [How to: Insure Fixed Assets](fa-how-insure.md).</span></span>

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a><span data-ttu-id="678d5-155">Отмена учета стоимости приобретения для одного основного средства</span><span class="sxs-lookup"><span data-stu-id="678d5-155">To cancel an acquisition cost posting for one fixed asset</span></span>
<span data-ttu-id="678d5-156">Если при учете стоимости приобретения допущена ошибка, можно удалить операцию с помощью пакетного задания **Отмена операций ОС** и затем учесть правильную стоимость приобретения.</span><span class="sxs-lookup"><span data-stu-id="678d5-156">If you make an error when posting an acquisition cost, you can remove the entry with the **Cancel FA Entries** batch job and then post the correct acquisition entry.</span></span> <span data-ttu-id="678d5-157">Ошибочные операции перемещаются в окно **Ошибочные операции по ОС**.</span><span class="sxs-lookup"><span data-stu-id="678d5-157">The erroneous entries are transferred to the **FA Error Ledger Entries** window.</span></span>

<span data-ttu-id="678d5-158">Например, если приобретение учтено с неправильной датой, это необходимо исправить как можно быстрее, так как дата учета основных средств используется во многих критически важных расчетах.</span><span class="sxs-lookup"><span data-stu-id="678d5-158">For example, if you post an acquisition with the wrong date, you must correct it as soon as possible because the fixed asset posting date is used is many critical calculations.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="678d5-159">Невозможно использовать функцию **Сторнировать транзакции** для операций основного средства.</span><span class="sxs-lookup"><span data-stu-id="678d5-159">You cannot use the **Reverse Transactions** function for fixed asset entries.</span></span>

1. <span data-ttu-id="678d5-160">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Отмена операций ОС**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-160">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cancel FA Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="678d5-161">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="678d5-161">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="678d5-162">Нажмите кнопку **ОК** для запуска пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="678d5-162">Choose the **OK** button to run the batch job.</span></span>
4. <span data-ttu-id="678d5-163">Когда одна или несколько неправильных операций будут отменены, выполните учет правильной стоимости приобретения.</span><span class="sxs-lookup"><span data-stu-id="678d5-163">When the incorrect entry or entries are canceled, proceed to post the correct acquisition cost.</span></span>

<span data-ttu-id="678d5-164">Чтобы отменить операции одновременно для нескольких основных средств, следует использовать пакетное задание **Отменить операции по ОС**.</span><span class="sxs-lookup"><span data-stu-id="678d5-164">To cancel ledger entries for multiple fixed assets at a time, use the **Cancel FA Ledger Entries** batch job.</span></span>

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a><span data-ttu-id="678d5-165">Учет ликвидационной стоимости вместе со стоимостью приобретения</span><span class="sxs-lookup"><span data-stu-id="678d5-165">To post the salvage value together with the acquisition cost</span></span>
<span data-ttu-id="678d5-166">Можно учитывать ликвидационную стоимость вместе со стоимостью приобретения из журнала ГК учета основных средств.</span><span class="sxs-lookup"><span data-stu-id="678d5-166">You can post the salvage value together with the acquisition cost from a fixed asset G/L journal.</span></span>    

1. <span data-ttu-id="678d5-167">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Отмена операций ОС**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="678d5-167">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cancel FA Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="678d5-168">Создайте строку журнала приобретения.</span><span class="sxs-lookup"><span data-stu-id="678d5-168">Create the acquisition journal line.</span></span> <span data-ttu-id="678d5-169">Дополнительные сведения см. в разделе "Разноска приобретения основного средства вручную с помощью журнала ГК учета основных средств".</span><span class="sxs-lookup"><span data-stu-id="678d5-169">For more information, see the "To post a fixed asset acquisition manually with the fixed asset G/L journal" section.</span></span>
3. <span data-ttu-id="678d5-170">В поле **Ликвидационная стоимость** строки журнала введите ликвидационную стоимость как кредит (со знаком минус).</span><span class="sxs-lookup"><span data-stu-id="678d5-170">In the **Salvage Value** field on the journal line, enter the salvage value amount as a credit (with a minus sign).</span></span>
4. <span data-ttu-id="678d5-171">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="678d5-171">Choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="678d5-172">Тип учета **Ликвидационная стоимость** является одним из вариантов только в окне **Журнал учета основных средств**.</span><span class="sxs-lookup"><span data-stu-id="678d5-172">The **Salvage Value** posting type is an option in the **Fixed Asset Journal** window only.</span></span> <span data-ttu-id="678d5-173">Он не доступен в окне **Журнал ГК учета основных средств**, поскольку ликвидационная стоимость никогда не учитывается в главной книге.</span><span class="sxs-lookup"><span data-stu-id="678d5-173">It is not available in the **Fixed Asset G/L Journal** window because salvage value is never posted to the general ledger.</span></span>

## <a name="see-also"></a><span data-ttu-id="678d5-174">См. также</span><span class="sxs-lookup"><span data-stu-id="678d5-174">See Also</span></span>
[<span data-ttu-id="678d5-175">Основные Средства</span><span class="sxs-lookup"><span data-stu-id="678d5-175">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="678d5-176">Настройка основных средств</span><span class="sxs-lookup"><span data-stu-id="678d5-176">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="678d5-177">Финансы</span><span class="sxs-lookup"><span data-stu-id="678d5-177">Finance</span></span>](finance.md)  
<span data-ttu-id="678d5-178">[Добро пожаловать в [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="678d5-178">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="678d5-179">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="678d5-179">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
