---
title: "Закрытие счетов отчета о прибылях и убытках | Документы Майкрософт"
description: "При закрытии года вы должны выполнить пакетное задание \"Закрытие отчета о прибылях и убытках\", чтобы закрыть отчетные периоды, составляющие финансовый год."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6ddd7b504f6faa856e92c336f889ad08db0b3d8b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-income-statement-accounts"></a><span data-ttu-id="0dfa3-103">Практическое руководство. Закрытие счетов отчета о прибылях и убытках</span><span class="sxs-lookup"><span data-stu-id="0dfa3-103">How to: Close Income Statement Accounts</span></span>
<span data-ttu-id="0dfa3-104">При завершении финансового года следует завершить периоды, которые его образуют.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-104">When a fiscal year is over, you must close the periods that comprise it.</span></span> <span data-ttu-id="0dfa3-105">Для этого выполните пакетное задание **Закрытие отчета о прибылях и убытках**.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-105">To do this, you run the **Close Income Statement** batch job.</span></span> <span data-ttu-id="0dfa3-106">Это задание переносит результат года на балансовый счет и закрывает счета отчета о прибылях и убытках.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-106">This job transfers the year's result to an account in the balance sheet and closes the income statement accounts.</span></span> <span data-ttu-id="0dfa3-107">Это осуществляется путем создания строк в журнале, который затем можно учесть.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-107">You do this by creating lines in a journal, which you then can post.</span></span>

## <a name="to-run-the-close-income-statement-batch-job"></a><span data-ttu-id="0dfa3-108">Запуск пакетного задания "Закрытие отчета о прибылях и убытках".</span><span class="sxs-lookup"><span data-stu-id="0dfa3-108">To run the Close Income Statement batch job</span></span>
1. <span data-ttu-id="0dfa3-109">Закройте финансовый год.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-109">Close the fiscal year.</span></span> <span data-ttu-id="0dfa3-110">Пакетное задание можно запустить только после закрытия финансового года.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-110">The fiscal year must closed before the batch job can be run.</span></span> <span data-ttu-id="0dfa3-111">Дополнительные сведения см. в разделе [Практическое руководство. Закрытие учетных периодов](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="0dfa3-111">For more information, see [How to: Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="0dfa3-112">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Закрытие отчета о прибылях и убытках**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>
3. <span data-ttu-id="0dfa3-113">Нажмите кнопку **ОК** для запуска пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-113">Choose the **OK** button to run the batch job.</span></span>

## <a name="about-the-close-income-statement-batch-job"></a><span data-ttu-id="0dfa3-114">О пакетном задании "Закрытие отчета о прибылях и убытках".</span><span class="sxs-lookup"><span data-stu-id="0dfa3-114">About the Close Income Statement Batch Job</span></span>
<span data-ttu-id="0dfa3-115">При выполнении этого пакетного задания обрабатываются все счета главной книги типа "Отчет о прибылях и убытках" и создаются операции, отменяющие соответствующие балансы.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-115">The batch job processes all general accounts of the income statement type and creates entries that cancel out their respective balances.</span></span> <span data-ttu-id="0dfa3-116">То есть каждая операция является суммой всех операций главной книги по счету в финансовом году.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-116">That is, each entry is the sum of all the general ledger entries on the account in the fiscal year.</span></span> <span data-ttu-id="0dfa3-117">Эти новые операции помещают в журнал, где в балансовом отчете перед учетом необходимо указать балансирующий счет и счет нераспределенной прибыли.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-117">These new entries are placed in a journal in which you must specify a balancing account and retained earnings account in the balance sheet before you post.</span></span> <span data-ttu-id="0dfa3-118">Когда журнал учитывается, операция учитывается на каждом счете отчета о прибылях и убытках таким образом, что ее баланс становится равным нулю, и в это же время годовой результат перемещается в балансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-118">When you post the journal, an entry is posted to each income statement account so that its balance becomes zero and at the same time the year's result is transferred to the balance sheet.</span></span>

<span data-ttu-id="0dfa3-119">Следует самостоятельно вести учет в журнале.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-119">You must post the journal yourself.</span></span> <span data-ttu-id="0dfa3-120">При выполнении этого пакетного задания операции не учитываются автоматически за исключением случаев, когда используется дополнительная отчетная валюта.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-120">The batch job does not post the entries automatically, except when an additional reporting currency is being used.</span></span> <span data-ttu-id="0dfa3-121">В этом случае, пакетное задание учитывает операции непосредственно в главной книге.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-121">When an additional reporting currency is being used, the batch job posts entries directly to the general ledger.</span></span>

<span data-ttu-id="0dfa3-122">Дата в строках, которые вставляются в журнал при выполнении пакетного задания, всегда будет датой закрытия для финансового года.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-122">The date on the lines that the batch job inserts in the journal is always a closing date for the fiscal year.</span></span> <span data-ttu-id="0dfa3-123">Дата начала — это вымышленная дата между последним днем старого финансового года и первым днем нового года.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-123">The closing date is a fictitious date between the last day of the old fiscal year and the first day of the new year.</span></span> <span data-ttu-id="0dfa3-124">Преимущество учета на дату закрытия состоит в том, что сохраняются правильные балансы для обычных дат финансового года.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-124">The advantage of posting on a closing date is that you maintain the correct balances for the ordinary dates of the fiscal year.</span></span>

<span data-ttu-id="0dfa3-125">Пакетное задание **Закрытие отчета о прибыли и убытках** можно использовать несколько раз.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-125">The **Close Income Statement** batch job can be used several times.</span></span> <span data-ttu-id="0dfa3-126">Даже после закрытия счетов прибылей и убытков имеется возможность учета в предыдущем финансовом году, если снова запустить пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="0dfa3-126">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the batch job again.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dfa3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0dfa3-127">See Also</span></span>
[<span data-ttu-id="0dfa3-128">Закрытие книг</span><span class="sxs-lookup"><span data-stu-id="0dfa3-128">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="0dfa3-129">Практическое руководство: учет операции закрытия года</span><span class="sxs-lookup"><span data-stu-id="0dfa3-129">How to: Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="0dfa3-130">Практическое руководство. Открытие нового финансового года</span><span class="sxs-lookup"><span data-stu-id="0dfa3-130">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="0dfa3-131">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0dfa3-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
