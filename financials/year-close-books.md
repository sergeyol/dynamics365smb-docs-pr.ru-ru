---
title: "Обзор задач по закрытию книг | Документы Майкрософт"
description: "Узнайте о процессе закрытия книг за финансовый год или период, а также о том, что происходит после закрытия в конце года."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 870f1c6a7f93195e0308a646402d642f6cadd219
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="closing-the-books"></a><span data-ttu-id="2c96f-103">Закрытие книг</span><span class="sxs-lookup"><span data-stu-id="2c96f-103">Closing the Books</span></span>
<span data-ttu-id="2c96f-104">После проверки актуальности всех счетов и распределения затрат и прибылей можно закрыть книги для финансового года или периода.</span><span class="sxs-lookup"><span data-stu-id="2c96f-104">After you ensure that all your accounts are up-to-date, and you allocate costs and income, then you can close the books for a fiscal year or period.</span></span>

<span data-ttu-id="2c96f-105">Закрывать год не требуется, но такая операция облегчит работу в системе, так как вы сможете воспользоваться преимуществами удобной системы фильтров.</span><span class="sxs-lookup"><span data-stu-id="2c96f-105">You are not required to close a year, but doing so will make working in the system easier for you because you will be able to take advantage of the convenient filtering options provided.</span></span> <span data-ttu-id="2c96f-106">Кроме того, в случае закрытия отпадает опасность потерять сведения о транзакциях, так как все сведения сохраняются даже после закрытия года.</span><span class="sxs-lookup"><span data-stu-id="2c96f-106">You also do not have to worry about losing details of transactions when you close because all details are retained, even after you close the year.</span></span>

## <a name="closing-book-process"></a><span data-ttu-id="2c96f-107">Процесс закрытия книги</span><span class="sxs-lookup"><span data-stu-id="2c96f-107">Closing Book Process</span></span>
<span data-ttu-id="2c96f-108">Процесс закрытия книги включает следующие основные задачи:</span><span class="sxs-lookup"><span data-stu-id="2c96f-108">The process for closing the book includes these main tasks:</span></span>

1. <span data-ttu-id="2c96f-109">Закрытие учетного периода.</span><span class="sxs-lookup"><span data-stu-id="2c96f-109">Closing the accounting period.</span></span>

    <span data-ttu-id="2c96f-110">Финансовый год определяется как один или несколько открытых периодов, перечисленных в окне **Учетные периоды**.</span><span class="sxs-lookup"><span data-stu-id="2c96f-110">A fiscal year is defined as one or more open periods as defined in the **Accounting Periods** window.</span></span> <span data-ttu-id="2c96f-111">Стандартный финансовый год содержит 12 периодов, состоящих из одного месяца каждый, при этом допускается выбор другого метода определения года.</span><span class="sxs-lookup"><span data-stu-id="2c96f-111">A typical fiscal year contains 12 periods of one month each, but you can also choose another method of defining a year.</span></span>

    <span data-ttu-id="2c96f-112">Дополнительные сведения см. в разделе [Практическое руководство. Закрытие учетных периодов](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="2c96f-112">For more information, see [How to: Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="2c96f-113">Регистрация операций предыдущего года.</span><span class="sxs-lookup"><span data-stu-id="2c96f-113">Registering prior-year entries.</span></span>

    <span data-ttu-id="2c96f-114">При закрытии финансового года необходимо ввести ряд административных транзакций, например предоплаченные товары и начисленные суммы за товары.</span><span class="sxs-lookup"><span data-stu-id="2c96f-114">When you close a fiscal year, you must enter a number of administrative transactions (such as prepaid and accrued items).</span></span> <span data-ttu-id="2c96f-115">Эти транзакции называются корректирующими операциями.</span><span class="sxs-lookup"><span data-stu-id="2c96f-115">These transactions are called adjusting entries.</span></span> <span data-ttu-id="2c96f-116">Не существует специальных правил для учета этих операций, и они (как и другие операции) содержат флажки в поле **Операция прошлого года**, если они учитываются на дату в закрытом финансовом году.</span><span class="sxs-lookup"><span data-stu-id="2c96f-116">There are no special rules for posting these entries, and they (like other entries) contain a check mark in the **Prior-Year Entry** field if they are posted on a date in a closed fiscal year.</span></span> <span data-ttu-id="2c96f-117">Несмотря на то, что финансовый год закрыт, можно по-прежнему производить учет ГК операций по нему.</span><span class="sxs-lookup"><span data-stu-id="2c96f-117">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span>
3. <span data-ttu-id="2c96f-118">Перенос сальдо со счетов отчета о прибылях и убытках на балансовые счета.</span><span class="sxs-lookup"><span data-stu-id="2c96f-118">Transferring balances from the income statement accounts to the balance sheet.</span></span>

    <span data-ttu-id="2c96f-119">После закрытия финансового года и учета всех прошлогодних операций счета отчета о прибылях и убытках должны быть закрыты, а чистая прибыль за год должна быть перенесена на балансовый счет собственных средств владельца.</span><span class="sxs-lookup"><span data-stu-id="2c96f-119">After a fiscal year has been closed and all prior-year entries have been posted, the income statement accounts must be closed and the net income for the year must be transferred to an account under owners' equity on the balance sheet.</span></span> <span data-ttu-id="2c96f-120">Для этого можно воспользоваться пакетным заданием Закрытие отчета о прибылях и убытках.</span><span class="sxs-lookup"><span data-stu-id="2c96f-120">Use the Close Income Statement batch job for this purpose.</span></span> <span data-ttu-id="2c96f-121">Данное пакетное задание обрабатывает все счета главной книги типа Отчет о прибылях и убытках и создает операции, сторнирующие их сальдо.</span><span class="sxs-lookup"><span data-stu-id="2c96f-121">The batch job processes all general ledger accounts of the type Income Statement and creates entries that reverse their balances.</span></span> <span data-ttu-id="2c96f-122">Эти операции помещаются в журнал, из которого они могут быть учтены.</span><span class="sxs-lookup"><span data-stu-id="2c96f-122">These entries are placed in a journal from which they can be posted.</span></span> <span data-ttu-id="2c96f-123">Данное пакетное задание не учитывает их автоматически за исключением случаев, когда используется дополнительная отчетная валюта.</span><span class="sxs-lookup"><span data-stu-id="2c96f-123">The batch job does not post them automatically, except when an additional reporting currency is used.</span></span> <span data-ttu-id="2c96f-124">При использовании дополнительной отчетной валюты данное пакетное задание производит учет прямо в главной книге.</span><span class="sxs-lookup"><span data-stu-id="2c96f-124">When an additional reporting currency is used, the batch job posts directly to the general ledger.</span></span>

    <span data-ttu-id="2c96f-125">Дополнительные сведения см. в разделе [Закрытие отчета о прибылях и убытках](year-close-income-statement.md).</span><span class="sxs-lookup"><span data-stu-id="2c96f-125">For more information, see [Close Income Statement](year-close-income-statement.md).</span></span>
4. <span data-ttu-id="2c96f-126">Учет закрывающей операции с операциями корреспондирующего счета собственных средств.</span><span class="sxs-lookup"><span data-stu-id="2c96f-126">Posting the year-end closing entry along with the offsetting equity account entries.</span></span>

    <span data-ttu-id="2c96f-127">После завершения пакетного задания "Закрытие отчета о прибылях и убытках" вы учитываете операции, сформированные этим заданием.</span><span class="sxs-lookup"><span data-stu-id="2c96f-127">When the Close Income Statement batch job is finished, you post the entries generated by the job.</span></span> <span data-ttu-id="2c96f-128">Если счет нераспределенной прибыли не указывается в пакетном задании, следует ввести одну строку с балансирующей операцией, которая учитывает чистую прибыль на правильном счету главной книги, входящем в число балансовых счетов собственных средств владельца.</span><span class="sxs-lookup"><span data-stu-id="2c96f-128">If you did not specify a retained earnings account in the batch job, then enter one line with a balancing entry that posts the net income to the correct general ledger account under owners' equity on the balance sheet.</span></span> <span data-ttu-id="2c96f-129">Наконец, выполните операцию учета журнала.</span><span class="sxs-lookup"><span data-stu-id="2c96f-129">Finally, post the journal.</span></span>

    <span data-ttu-id="2c96f-130">Дополнительные сведения см. в разделе [Практическое руководство. Учет операции закрытия года](year-how-post-year-end-close-entry.md).</span><span class="sxs-lookup"><span data-stu-id="2c96f-130">For more information, see [How to: Post Year-End Closing Entry](year-how-post-year-end-close-entry.md).</span></span>

## <a name="what-happens-when-you-close"></a><span data-ttu-id="2c96f-131">Что произойдет после закрытия</span><span class="sxs-lookup"><span data-stu-id="2c96f-131">What Happens When You Close</span></span>
<span data-ttu-id="2c96f-132">В результате закрытия на конец года прибыли перемещаются из расчетных прибылей на счет нераспределенной прибыли.</span><span class="sxs-lookup"><span data-stu-id="2c96f-132">When you close at the end of the year, the system moves your earnings from calculated earnings to the Retained Earnings account.</span></span> <span data-ttu-id="2c96f-133">Кроме того, финансовый год помечается как «закрытый», а все последующие записи для закрытого года — как «прошлогодние записи».</span><span class="sxs-lookup"><span data-stu-id="2c96f-133">The system also marks the fiscal year as "closed," and marks all subsequent entries for the closed year as "prior year entries."</span></span>

<span data-ttu-id="2c96f-134">Система затем генерирует закрывающую операцию, но не учитывает операцию автоматически.</span><span class="sxs-lookup"><span data-stu-id="2c96f-134">The system then generates a closing entry, but it does not post the entry automatically.</span></span> <span data-ttu-id="2c96f-135">Пользователь получает возможность создать одну или несколько операций корреспондирующего счета собственных средств, который позволяет определить метод выделения закрывающей операции.</span><span class="sxs-lookup"><span data-stu-id="2c96f-135">You are given the opportunity to make the offsetting equity account entry or entries, which allows you to decide how to allocate your closing entry.</span></span> <span data-ttu-id="2c96f-136">Например, если ваша организация имеет несколько отделений, система может создать одну закрывающую операцию для всех отделений, после чего можно создать корреспондирующую операцию для счета собственных средств каждого отделения.</span><span class="sxs-lookup"><span data-stu-id="2c96f-136">For example, if your company has several divisions, you can let the system generate a single closing entry for all the divisions, and you can then make an offsetting entry for each division's equity account.</span></span>

<span data-ttu-id="2c96f-137">Можно выполнять учет в предыдущем финансовом году даже после закрытия счетов прибылей и убытков; для этого следует выполнить пакетное задание Закрытие отчета о прибылях и убытках.</span><span class="sxs-lookup"><span data-stu-id="2c96f-137">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the Close Income Statement batch job again afterward.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c96f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2c96f-138">See Also</span></span>
[<span data-ttu-id="2c96f-139">Практическое руководство. Открытие нового финансового года</span><span class="sxs-lookup"><span data-stu-id="2c96f-139">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="2c96f-140">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c96f-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
