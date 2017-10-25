---
title: "Как преобразовывать сервисные контракты | Документы Майкрософт"
description: "Так как средство изменения ставки НДС не может преобразовать сервисные контракты, эти контракты необходимо преобразовывать вручную. В этом разделе описывается несколько альтернативных методов, которые можно использовать для преобразования сервисного контракта."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2f62bbae71eac1c0d63df5e352601c0885274066
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-convert-service-contracts-that-include-vat-amounts"></a><span data-ttu-id="fd9f2-104">Практическое руководство. Преобразование сервисных контрактов, которые включают суммы НДС</span><span class="sxs-lookup"><span data-stu-id="fd9f2-104">How to: Convert Service Contracts that Include VAT Amounts</span></span>
<span data-ttu-id="fd9f2-105">Так как средство изменения ставки НДС не может преобразовать сервисные контракты, эти контракты необходимо преобразовывать вручную.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-105">Because the VAT rate change tool cannot convert service contracts, these contracts must be converted manually.</span></span> <span data-ttu-id="fd9f2-106">В этом разделе описывается несколько альтернативных методов, которые можно использовать для преобразования сервисного контракта.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-106">This topic describes several alternative methods that you can use for service contract conversion.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fd9f2-107">В этом разделе дается общий обзор процесса.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-107">This topic provides a high-level workflow.</span></span>  

 <span data-ttu-id="fd9f2-108">Следующая процедура описывает, как исправить счет для контакта с предоплаченным сервисом, который был создан год назад.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-108">The following procedure describes how to correct an invoice for a prepaid service contact that has been created a year in advance.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fd9f2-109">Для данного примера необходимо изменить рабочую дату на 01.01.2017.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-109">For this example, you must change your work date to 01.01.2017.</span></span>  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a><span data-ttu-id="fd9f2-110">Исправление счета для предоплаченного сервисного контракта</span><span class="sxs-lookup"><span data-stu-id="fd9f2-110">To correct an invoice for a prepaid service contract</span></span>  
1. <span data-ttu-id="fd9f2-111">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Управление контрактами**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contract Management**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fd9f2-112">В разделе **Списки** выберите **Сервисные контракты**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-112">Under **Lists**, choose **Service Contracts**.</span></span>  
3. <span data-ttu-id="fd9f2-113">Создайте новый предварительно оплаченный сервисный контракт.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-113">Create a new prepaid service contract.</span></span> <span data-ttu-id="fd9f2-114">Введите начальную дату **01.01.2017** и год периода выставления счета для клиента **20000**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-114">Enter a start date of **01.01.2017** and an invoice period year for customer **20000**.</span></span>  
4. <span data-ttu-id="fd9f2-115">Этот контракт должен быть подписан.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-115">This contract must be signed.</span></span> <span data-ttu-id="fd9f2-116">На вкладке **Главная** в группе **Процесс** выберите **Подписать контракт**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-116">On the **Home** tab, in the **Process** group, choose **Sign Contract**.</span></span>  
5. <span data-ttu-id="fd9f2-117">Создать сервисный счет.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-117">Create a service invoice.</span></span>
6. <span data-ttu-id="fd9f2-118">Счет указывается как неучтенный сервисный счет.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-118">The invoice is listed as an unposted service invoice.</span></span> <span data-ttu-id="fd9f2-119">Для просмотра сервисного счета последовательно выберите **Сервис**, **Управление контрактами**, а затем — **Сервисные счета**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-119">To view the service invoice, choose **Service**, choose **Contract Management**, and then choose **Service Invoices**.</span></span>  
7. <span data-ttu-id="fd9f2-120">Выполните учет сервисного счета.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-120">Post the service invoice.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fd9f2-121">Не изменяйте неучтенный сервисный счет.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-121">Do not change the unposted service invoice.</span></span> <span data-ttu-id="fd9f2-122">Поскольку операции книги сервиса создаются при создании счета, изменение в неучтенном счете не отразится на уже созданных операциях книги сервиса.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-122">Since the service ledger entries are created when the invoice is created, a change in the unposted invoice will not change the already created service ledger entries.</span></span> <span data-ttu-id="fd9f2-123">Операции НДС создаются при учете счета.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-123">However, the VAT entries are created when the invoice is posted.</span></span> <span data-ttu-id="fd9f2-124">Это позволяет изменять общую товарную учетную группу и учетную товарную группу GSP в неучтенном сервисном счете.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-124">This lets you change the general product posting group and the GSP product posting group on the unposted service invoice.</span></span>  

### <a name="to-create-a-credit-memo-for-vat-difference"></a><span data-ttu-id="fd9f2-125">Создание кредит-ноты для разницы НДС</span><span class="sxs-lookup"><span data-stu-id="fd9f2-125">To create a credit memo for VAT difference</span></span>  
<span data-ttu-id="fd9f2-126">В следующей процедуре описывается создание кредит-ноты, которая включает только разницу НДС за период, по которому уже выставлен счет, начиная с **01.07.2017**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-126">The following procedure describes how to create a credit memo that only includes the VAT difference for the already invoiced period starting on **01.07.2017**.</span></span> <span data-ttu-id="fd9f2-127">В этом примере сумма НДС учитывается только в модуле "Финансовый менеджмент", не в модуле "Сервисное управление".</span><span class="sxs-lookup"><span data-stu-id="fd9f2-127">In this example, the VAT amount is only posted to the Financial Management module, not to the Service Management module.</span></span> <span data-ttu-id="fd9f2-128">Операции НДС, связанные с операцией книги сервиса, не будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-128">The VAT entries that are linked to the service ledger entry will not be corrected.</span></span>  

1. <span data-ttu-id="fd9f2-129">Создайте новый счет Главной книги для разницы НДС.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-129">Create a new general ledger account for the VAT difference.</span></span> <span data-ttu-id="fd9f2-130">Этот счет будет использоваться для непосредственного учета коррекции НДС.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-130">This account will be used for direct posting of the VAT correction.</span></span>  
2. <span data-ttu-id="fd9f2-131">Добавьте новую строку в настройку учета НДС.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-131">Add a new line to the VAT posting setup.</span></span>  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a><span data-ttu-id="fd9f2-132">Создание дат завершения контрактов по строкам контрактов</span><span class="sxs-lookup"><span data-stu-id="fd9f2-132">To create contract expiration dates in contract lines</span></span>  
<span data-ttu-id="fd9f2-133">Далее описывается процедура создания новых контрактов с использованием дат завершения контакта в строках сервисного контракта.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-133">The following procedure describes how to create new contracts by working with contact expiration dates in service contract lines.</span></span>  

1. <span data-ttu-id="fd9f2-134">В окне **Сервисный контракт** установите дату завершения контракта равной **30.06.2017**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-134">In the **Service Contract** window, set the contract expiration date to **30.06.2017**.</span></span>  
2. <span data-ttu-id="fd9f2-135">Выберите действие **Создать кредит-ноту**, чтобы автоматически создать кредит-ноту с июля 2017 до декабря 2017.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-135">Choose the **Create Credit Memo** action to automatically create a credit memo for July 2017 to December 2017.</span></span>  
3. <span data-ttu-id="fd9f2-136">Поскольку срок действия контракта истек, необходимо создать новый контракт на период с новой ставкой НДС для с 1 июля 2017 по 31 декабря 2017.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-136">Because the contract has expired, you need to create a new contract for the period with the new VAT rate for July 1, 2017 to December 31, 2017.</span></span>  

### <a name="to-create-a-new-credit-memo"></a><span data-ttu-id="fd9f2-137">Создание новой кредит-ноты</span><span class="sxs-lookup"><span data-stu-id="fd9f2-137">To create a new credit memo</span></span>  
<span data-ttu-id="fd9f2-138">В следующей процедуре описывается создание новой кредит-ноты с помощью пакетного задания **Получить операции предоплаты по контракту**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-138">The following procedure describes how to create a new credit memo using the **Get Prepaid Contract Entries** batch job.</span></span> <span data-ttu-id="fd9f2-139">Операции, которые не следует исправлять, с января 2017 по июнь 2017 будут удалены.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-139">Entries that you do not want to correct from January 2017 to June 2017 will be deleted.</span></span>  

1. <span data-ttu-id="fd9f2-140">Запустите средство изменения ставки НДС для 1 июля 2017 года.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-140">Run the VAT rate change tool on July 1, 2017.</span></span> <span data-ttu-id="fd9f2-141">Общая группа учета товаров или группа учета товаров с НДС изменится.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-141">The general product posting group or the VAT product posting group is changed.</span></span> <span data-ttu-id="fd9f2-142">Дополнительные сведения см. в разделе [Практическое руководство. Работа с НДС по продажам и покупкам](finance-work-with-vat.md).</span><span class="sxs-lookup"><span data-stu-id="fd9f2-142">For more information, see [How to: Work with VAT on Sales and Purchases](finance-work-with-vat.md).</span></span>  
2. <span data-ttu-id="fd9f2-143">После запуска средства изменения ставки НДС введите дату завершения сервисного контракта.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-143">After running the VAT rate change tool, enter a contract expiration date for the service contract.</span></span> <span data-ttu-id="fd9f2-144">Теперь можно удалять строки сервисного контракта и создавать новую строку, идентичную старой.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-144">You can now delete the service contract line and create a new line that is identical to the old one.</span></span>  
3. <span data-ttu-id="fd9f2-145">Создайте новый счет за период с января 2017 по декабрь 2012 с использованием новой ставки НДС.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-145">Create a new invoice for the period of January 2017 to December 2012 using the new VAT rate.</span></span>  
4. <span data-ttu-id="fd9f2-146">Чтобы создать другую кредит-ноту, в окне **Сервисные кредит-ноты** выберите **Создать**, чтобы создать новую сервисную кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-146">To create another credit memo, in the **Service Credit Memos** window, choose **New** to create a new service credit memo.</span></span>  
5. <span data-ttu-id="fd9f2-147">Выберите действие **Получение операции предопл. по контр.**.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-147">Choose the **Get Prepaid Contract Entries** action.</span></span>  
6. <span data-ttu-id="fd9f2-148">После завершения преобразование операции НДС и книги сервиса будут скорректированы.</span><span class="sxs-lookup"><span data-stu-id="fd9f2-148">After the conversion is complete, VAT and service ledger entries will be correct.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd9f2-149">См. также</span><span class="sxs-lookup"><span data-stu-id="fd9f2-149">See Also</span></span>  
[<span data-ttu-id="fd9f2-150">Практическое руководство. Работа с сервисными контрактами и предложениями по сервисным контрактам</span><span class="sxs-lookup"><span data-stu-id="fd9f2-150">How to: Work with Service Contracts and Service Contract Quotes</span></span>](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[<span data-ttu-id="fd9f2-151">Финансы</span><span class="sxs-lookup"><span data-stu-id="fd9f2-151">Finance</span></span>](finance.md)  
[<span data-ttu-id="fd9f2-152">Практическое руководство. Подача отчета об НДС в налоговые органы</span><span class="sxs-lookup"><span data-stu-id="fd9f2-152">How to: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)  
[<span data-ttu-id="fd9f2-153">Практическое руководство. Работа с НДС по продажам и покупкам</span><span class="sxs-lookup"><span data-stu-id="fd9f2-153">How to: Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  
