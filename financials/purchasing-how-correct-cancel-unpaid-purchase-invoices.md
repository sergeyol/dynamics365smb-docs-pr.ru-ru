---
title: "Изменение или отмена неоплаченных счетов покупки | Документы Майкрософт"
description: "Описывается, как исправлять и отменять учтенные счета покупки и автоматически создавать кредит-ноты покупки."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53800a9fe42934807c551e81098eda768f4f1542
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="e332f-103">Практическое руководство. Исправление или отмена неоплаченных счетов покупки</span><span class="sxs-lookup"><span data-stu-id="e332f-103">How to: Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="e332f-104">Можно исправить или отменить учтенный счет покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="e332f-105">Это используется, если нужно исправить опечатку либо внести изменение в покупку на раннем этапе обработки заказа.</span><span class="sxs-lookup"><span data-stu-id="e332f-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="e332f-106">Если продукты в учтенном счете покупки уже оплачены, его невозможно откорректировать или отменить из учтенного счета покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="e332f-107">Вместо этого необходимо вручную создать кредит-ноту покупки для сторнирования покупки, при необходимости управляемую заказом на возврат покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="e332f-108">Дополнительные сведения см. в разделе [Практическое руководство. Обработка возвратов покупки или отмен](purchasing-how-process-purchase-returns-cancellations.md)</span><span class="sxs-lookup"><span data-stu-id="e332f-108">For more information, see [How to: Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="e332f-109">В окне **Учтенный счет покупки** можно нажать кнопку **Исправить** или **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="e332f-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="e332f-110">При корректировке или отмене учтенного счета покупки корректирующая кредит-нота покупки применяется ко всем операциям ГК и журнала товаров, созданным при учете первоначального счета покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="e332f-111">При этом сторнируется учтенный счет покупки в финансовых записях и оставляется корректирующая учтенная кредит-нота покупки для аудиторского следа.</span><span class="sxs-lookup"><span data-stu-id="e332f-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="e332f-112">Ниже описано использование кнопок **Исправить** и **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="e332f-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="e332f-113">Коррекция учтенного счета покупки</span><span class="sxs-lookup"><span data-stu-id="e332f-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="e332f-114">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Учтенные счета покупки**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="e332f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e332f-115">Выберите учтенный счет покупки, который требуется откорректировать.</span><span class="sxs-lookup"><span data-stu-id="e332f-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="e332f-116">Если установлен флажок **Отменено**, невозможно откорректировать учтенный счет покупки, поскольку он уже откорректирован или отменен.</span><span class="sxs-lookup"><span data-stu-id="e332f-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="e332f-117">В окне **Учтенный счет покупки** выберите **Исправить**.</span><span class="sxs-lookup"><span data-stu-id="e332f-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="e332f-118">Создается новый счет покупки с теми же сведениями, в который можно внести изменения.</span><span class="sxs-lookup"><span data-stu-id="e332f-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="e332f-119">Дополнительные сведения см. в разделе [Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="e332f-119">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="e332f-120">Значение в поле **Отменено** в исходном учтенном счете покупки изменится на **Да**.</span><span class="sxs-lookup"><span data-stu-id="e332f-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="e332f-121">Автоматически создается кредит-нота покупки, которая учитывается для аннулирования исходного учтенного счета покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="e332f-122">Выберите **Показать корректирующую кредит-ноту**, чтобы просмотреть учтенную кредит-ноту покупки, которая аннулирует исходный учтенный счет покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="e332f-123">Отмена учтенного счета покупки</span><span class="sxs-lookup"><span data-stu-id="e332f-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="e332f-124">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Учтенные счета покупки**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="e332f-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e332f-125">Выберите учтенный счет покупки, который требуется отменить.</span><span class="sxs-lookup"><span data-stu-id="e332f-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="e332f-126">Если установлен флажок **Отменено**, невозможно отменить учтенный счет покупки, поскольку он уже отмене или скорректирован.</span><span class="sxs-lookup"><span data-stu-id="e332f-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="e332f-127">В окне **Учтенный счет покупки** выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="e332f-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="e332f-128">Автоматически создается кредит-нота покупки, которая учитывается для аннулирования исходного учтенного счета покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="e332f-129">Значение в поле **Отменено** в исходном учтенном счете покупки изменится на **Да**.</span><span class="sxs-lookup"><span data-stu-id="e332f-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="e332f-130">Выберите **Показать корректирующую кредит-ноту**, чтобы просмотреть учтенную кредит-ноту покупки, которая аннулирует исходный учтенный счет покупки.</span><span class="sxs-lookup"><span data-stu-id="e332f-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="e332f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e332f-131">See Also</span></span>
[<span data-ttu-id="e332f-132">Покупки</span><span class="sxs-lookup"><span data-stu-id="e332f-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e332f-133">Практическое руководство. Регистрация покупок</span><span class="sxs-lookup"><span data-stu-id="e332f-133">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="e332f-134">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e332f-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
