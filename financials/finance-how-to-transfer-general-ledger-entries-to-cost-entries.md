---
title: "Практическое руководство. Перенос операций ГК в операции затрат | Документы Майкрософт"
description: "Можно перенести операции главной книги в операции затрат."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e68378d7acc789a70caf9c5b0590a81bf874337
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c9fc4-103">Практическое руководство: перенос операций ГК в операции затрат</span><span class="sxs-lookup"><span data-stu-id="c9fc4-103">How to: Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="c9fc4-104">Можно перенести операции главной книги в операции затрат.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="c9fc4-105">Перед запуском процесса перемещения операций Главной книги в операции затрат необходимо подготовить перемещение, чтобы избежать ручного учета коррекции.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="c9fc4-106">Подготовка перемещения</span><span class="sxs-lookup"><span data-stu-id="c9fc4-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="c9fc4-107">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка учета затрат**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c9fc4-108">В окне **Настройка учета затрат** убедитесь, что в поле **Начальная дата для перемещения ГК** установлено нужное значение.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="c9fc4-109">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Диаграмма типов затрат**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="c9fc4-110">В окне **Карта типов затрат** убедитесь, что поле **Диапазон счетов ГК** правильно связано с каждым типом затрат для получения операций из главной книги.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="c9fc4-111">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **План счетов**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="c9fc4-112">Для каждого соответствующего счета главной книги в окне **Карточка счета ГК** убедитесь, что поле **Номер типа затрат**</span><span class="sxs-lookup"><span data-stu-id="c9fc4-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="c9fc4-113">правильно связано с типом затрат.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="c9fc4-114">Дополнительные сведения см. в разделе [Определение отношения между типами затрат и счетами главной книги](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="c9fc4-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="c9fc4-115">Удостоверьтесь, что для всех соответствующих операций главной книги указаны значения измерений, соответствующие месту возникновения затрат или объекту затрат.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c9fc4-116">Перенос операций ГК в операции затрат</span><span class="sxs-lookup"><span data-stu-id="c9fc4-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="c9fc4-117">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Перенести записи ГК в CA**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c9fc4-118">Нажмите кнопку **Да** для запуска перемещения.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="c9fc4-119">Процесс переносит все операции главной книги, которые еще не были переданы.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="c9fc4-120">Во время перемещения процесс создает связи в записях таблиц **Операция затрат** и **Регистр затрат**.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="c9fc4-121">Это позволяет отслеживать источник операций себестоимости.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9fc4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c9fc4-122">See Also</span></span>  
 <span data-ttu-id="c9fc4-123">[Критерии для переноса операций главной книги в операции затрат](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c9fc4-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="c9fc4-124">[Автоматическое перемещение и объединенные операции](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c9fc4-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="c9fc4-125">[Результаты перемещения](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="c9fc4-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="c9fc4-126">[Перемещение и операции учета затрат](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c9fc4-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="c9fc4-127">Определение отношения между типами затрат и счетами главной книги.</span><span class="sxs-lookup"><span data-stu-id="c9fc4-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
