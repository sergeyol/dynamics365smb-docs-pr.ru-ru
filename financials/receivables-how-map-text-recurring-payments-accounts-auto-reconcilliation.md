---
title: "Настройка сопоставления текста со счетами для типовых платежей | Документы Майкрософт"
description: "Связывайте текст в платежах с определенными счетами, чтобы платежи учитывались на счетах при учете журнала выверки платежей."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: deb05c6294edeb892606154b38de2aa406abf6a2
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a><span data-ttu-id="3ad86-103">Практическое руководство. Сопоставление текста на типовых платежах со счетами для автоматической выверки</span><span class="sxs-lookup"><span data-stu-id="3ad86-103">How to: Map Text on Recurring Payments to Accounts for Automatic Reconciliation</span></span>
<span data-ttu-id="3ad86-104">В окне **Сопоставление текста со счетами**, открываемом из окна **Журнал выверки платежей**, можно настроить сопоставления между текстом платежей и конкретными дебетовыми, кредитными и балансовыми счетами, чтобы такие платежи учитывались на заданных счетах при учете в журнале выверки платежей.</span><span class="sxs-lookup"><span data-stu-id="3ad86-104">In the **Text-to-Account Mapping** window, which you open from the **Payment Reconciliation Journal** window, you can set up mappings between text on payments and specific debit, credit, and balancing accounts so that such payments are posted to the specified accounts when you post the payment reconciliation journal.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3ad86-105">Этот раздел также применяется при использовании функции **Определить соответствие текста счетам** из записи входящего документа для упрощения преобразования электронных документов, полученных из внешних служб, в документы в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3ad86-105">The topic also applies to when you use the **Map Text to Account** function from an incoming document record to assist in converting electronic documents received from external services to documents in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3ad86-106">Дополнительные сведения см. в разделе [Практическое руководство. Использование OCR для преобразования PDF-файлов и графических файлов в электронные документы](across-how-use-ocr-pdf-images-files.md)</span><span class="sxs-lookup"><span data-stu-id="3ad86-106">For more information, see [How to: Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>   

<span data-ttu-id="3ad86-107">Аналогичная функция существует для выверки избыточных суммы в строках журнала выверки платежей на произвольной основе.</span><span class="sxs-lookup"><span data-stu-id="3ad86-107">Similar functionality exists to reconcile excess amounts on payment reconciliation journal lines on an ad-hoc basis.</span></span> <span data-ttu-id="3ad86-108">Дополнительные сведения см. в разделе [Практическое руководство. Выверка платежей, которые не могут быть применены автоматически](receivables-how-reconcile-payments-cannot-apply-auto.md).</span><span class="sxs-lookup"><span data-stu-id="3ad86-108">For more information, see [How to: Reconcile Payments That Cannot be Applied Automatically](receivables-how-reconcile-payments-cannot-apply-auto.md).</span></span>

<span data-ttu-id="3ad86-109">Платежи, учитываемые на основе сопоставления текст-счет, не применяются к открытым операциям, но учитываются на заданных счетах помимо создания операций журнала банковского счета.</span><span class="sxs-lookup"><span data-stu-id="3ad86-109">Payments posted based on text-to-account mapping are not applied to open entries, but are merely posted to the specified accounts in addition to creating bank account ledger entries.</span></span> <span data-ttu-id="3ad86-110">Соответственно, сопоставление текст-счет подходит для типовых приходных кассовых ордеров или расходов, например частого приобретения автомобильного топлива или банковских сборов и процентов, которые часто отображаются в банковской выписке и для которых не требуется связанный коммерческий документ.</span><span class="sxs-lookup"><span data-stu-id="3ad86-110">Accordingly, text-to-account mapping is suited for recurring cash receipts or expenses, such as frequent purchases of car fuel or bank fees and interest, that regularly occur on the bank statement and do not need a related business document.</span></span> <span data-ttu-id="3ad86-111">Дополнительные сведения см. в подразделе “Пример. Сопоставление текст-счет для расходов на топливо” этого раздела.</span><span class="sxs-lookup"><span data-stu-id="3ad86-111">For more information, see the “Example - Text-to-Account Mapping for Fuel Expense” section in this topic.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3ad86-112">Платежи в строках журнала выверки настраиваются на учет в соответствии с сопоставлением текст-счет, если функция автоматического применения может обеспечить точность совпадения от **Низкий** до **Средний**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-112">Payments on reconciliation journal lines are only set to posting according to text-to-account mapping if the automatic application function can only provide a match confidence of **Low** or **Medium**.</span></span> <span data-ttu-id="3ad86-113">Если функция автоматического применения обеспечивает достоверность совпадения соответствия "Высокий", платеж автоматически применяется к одной или нескольким открытым операциям и не учитывается на счетах, заданных в окне **Сопоставление текста со счетами**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-113">If the automatic application function provides a match confidence of High, then the payment is automatically applied to one or more open entries, and the payment is not posted to the accounts specified in the **Text-to-Account Mapping** window.</span></span> <span data-ttu-id="3ad86-114">Другими словами, уровень соответствия **Высокий** переопределяет сопоставление текст-счет.</span><span class="sxs-lookup"><span data-stu-id="3ad86-114">In other words, a match confidence of **High** overrules a text-to-account mapping.</span></span>

<span data-ttu-id="3ad86-115">В строке журнала выверки платежей, где платеж настроен на учет в соответствии с сопоставлением текст-счет, поле **Достоверность совпадения** содержит значение **Высокий – сопоставление текста со счетами**, а поля **Тип счета** и **Номер счета** содержат сопоставленные счета.</span><span class="sxs-lookup"><span data-stu-id="3ad86-115">On a payment reconciliation journal line where the payment has been set to posting according to text-to-account mapping, the **Match Confidence** field contains **High - Text-to-Account Mapping**, and the **Account Type** and **Account No.** fields contain the mapped accounts.</span></span>

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a><span data-ttu-id="3ad86-116">Сопоставление текста на типовых платежах со счетами для автоматической выверки</span><span class="sxs-lookup"><span data-stu-id="3ad86-116">To map text on recurring payments to accounts for automatic reconciliation</span></span>
1. <span data-ttu-id="3ad86-117">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы выверки платежей**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3ad86-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Reconciliation Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="3ad86-118">Откройте журнал выверки платежей.</span><span class="sxs-lookup"><span data-stu-id="3ad86-118">Open a payment reconciliation journal.</span></span> <span data-ttu-id="3ad86-119">Дополнительные сведения см. в разделе [Практическое руководство. Выверка платежей с использованием автоматического применения](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="3ad86-119">For more information, see [How to: Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>
3. <span data-ttu-id="3ad86-120">Выберите действие **Определить соответствие текста счетам**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-120">Choose the **Map Text to Account** action.</span></span> <span data-ttu-id="3ad86-121">Откроется окно **Сопоставление текста со счетами**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-121">The **Text-to-Account Mapping** window opens.</span></span>
4. <span data-ttu-id="3ad86-122">В поле **Текст сопоставления** введите любой текст, который встречается в платежах, которые требуется учесть на заданных счетах без применения к открытой операции.</span><span class="sxs-lookup"><span data-stu-id="3ad86-122">In the **Mapping Text** field, enter any text that occurs on payments that you want to post to specified accounts without applying to an open entry.</span></span> <span data-ttu-id="3ad86-123">Можно ввести до 50-ти символов.</span><span class="sxs-lookup"><span data-stu-id="3ad86-123">You can enter up to 50 characters.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="3ad86-124">Если нет других платежей или входящих документов с рассматриваемым сопоставляемым текстом, сопоставление текста со счетом выполняется даже в том случае, если только часть текста в платеже или входящем документе имеется в сопоставляемом тексте.</span><span class="sxs-lookup"><span data-stu-id="3ad86-124">If no other payments or incoming documents exist with the mapping text in question, then the text-to-account mapping will occur even when only a part of the text on the payment or incoming document exists as a mapping text.</span></span>
5. <span data-ttu-id="3ad86-125">В поле **Номер поставщика** введите поставщика, для которого будут созданы входящие документы, содержащие текст сопоставления, или для которого будут учтены платежи.</span><span class="sxs-lookup"><span data-stu-id="3ad86-125">In the **Vendor No.** field, enter the vendor that incoming documents containing the mapping text will be created for, or that payments will be posted to.</span></span> <span data-ttu-id="3ad86-126">Дополнительные сведения см. в разделе [Практическое руководство. Использование OCR для преобразования PDF-файлов и графических файлов в электронные документы](across-how-use-ocr-pdf-images-files.md)</span><span class="sxs-lookup"><span data-stu-id="3ad86-126">For more information, see [How to: Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>      
6. <span data-ttu-id="3ad86-127">В поле **Номер дебетового счета** введите счет, на котором будут учтены платежи, содержащие текст сопоставления, если это входящие платежи.</span><span class="sxs-lookup"><span data-stu-id="3ad86-127">In the **Debit Acc. No.** field, enter the account that payments containing the mapping text will be posted to if they are incoming payments.</span></span> <span data-ttu-id="3ad86-128">Для входящих платежей знак значения в поле **Сумма по выписке** положительный.</span><span class="sxs-lookup"><span data-stu-id="3ad86-128">For incoming payments, the sign of the value in the **Statement Amount** field is positive.</span></span>
7. <span data-ttu-id="3ad86-129">В поле **Номер кредитового счета** введите счет, на котором будут учтены платежи, содержащие текст сопоставления, если это исходящие платежи.</span><span class="sxs-lookup"><span data-stu-id="3ad86-129">In the **Credit Acc. No.** field, enter the account that payments containing the mapping text will be posted to if they are outgoing payments.</span></span> <span data-ttu-id="3ad86-130">Для исходящих платежей знак значения в поле **Сумма по выписке** отрицательный.</span><span class="sxs-lookup"><span data-stu-id="3ad86-130">For outgoing payments, the sign of the value in the **Statement Amount** field is negative.</span></span>
8. <span data-ttu-id="3ad86-131">В поле **Тип источника сальдо** укажите, будет ли платеж учтен на счете ГК или на счете клиента либо поставщика.</span><span class="sxs-lookup"><span data-stu-id="3ad86-131">In the **Bal. Source Type** field, specify if the payment will be posted to a general ledger account or to a customer or vendor account.</span></span>
9. <span data-ttu-id="3ad86-132">В поле **Номер источника сальдо** укажите счет, на котором будет учтен платеж в зависимости от варианта выбора в поле **Тип источника сальдо**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-132">In the **Bal. Source No.** field, specify the account that the payment will be posted to, depending on your selection in the **Bal. Source Type** field.</span></span>
10. <span data-ttu-id="3ad86-133">Повторите шаги с 4 по 8 для всего текста в платежах, которые требуется соотнести со счетами для непосредственного учета без применения.</span><span class="sxs-lookup"><span data-stu-id="3ad86-133">Repeat steps 4 through 8 for all text on payments that you want to map to accounts for direct posting without application.</span></span>

<span data-ttu-id="3ad86-134">Следующий раз при импорте файла банковской выписки или выборе действия **Применить автоматически** в окне **Журнал выверки платежей** строки журнала платежей, которые содержат определенный текст соответствия, будут содержать сопоставленные счета в полях **Тип счета** и **Номер счета**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-134">Next time you import a bank statement file or choose the **Apply Automatically** action in the **Payment Reconciliation Journal** window, journal lines for the payments that contain the specified mapping text will contain the mapped accounts in the **Account Type** and **Account No.** fields.</span></span> <span data-ttu-id="3ad86-135">Поле **Достоверность совпадения** будет содержать значение **Высокий – сопоставление текста со счетами**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-135">The **Match Confidence** field will contain **High - Text-to-Account Mapping**.</span></span> <span data-ttu-id="3ad86-136">Это при условии, что функция автоматического применения обеспечивает уверенность в совпадении **Низкая** или **Средняя**.</span><span class="sxs-lookup"><span data-stu-id="3ad86-136">This is on the condition that the automatic application function can only provide a match confidence of **Low** or **Medium**.</span></span>

## <a name="example-text-to-account-mapping-for-fuel-expense"></a><span data-ttu-id="3ad86-137">Пример: сопоставление текст-счет для расходов на топливо</span><span class="sxs-lookup"><span data-stu-id="3ad86-137">Example: Text-to-Account Mapping for Fuel Expense</span></span>
<span data-ttu-id="3ad86-138">Чтобы всегда учитывать расходы на топливо, понесенные на заправках Shell, на счету ГК за бензин (счет 8510), заполните строку в окне **Сопоставление текста со счетами** следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3ad86-138">To always post fuel expenses incurred at Shell gas stations to the general ledger account for gasoline (account 8510), fill a line in the **Text-to-Account Mapping** window as follows.</span></span>

| <span data-ttu-id="3ad86-139">Текст сопоставления</span><span class="sxs-lookup"><span data-stu-id="3ad86-139">Mapping Text</span></span> | <span data-ttu-id="3ad86-140">Номер дебетового счета</span><span class="sxs-lookup"><span data-stu-id="3ad86-140">Debit Acc. No.</span></span> | <span data-ttu-id="3ad86-141">Номер кредитового счета</span><span class="sxs-lookup"><span data-stu-id="3ad86-141">Credit Acc. No.</span></span> | <span data-ttu-id="3ad86-142">Тип источника сальдо</span><span class="sxs-lookup"><span data-stu-id="3ad86-142">Bal. Source Type</span></span> | <span data-ttu-id="3ad86-143">Номер источника сальдо</span><span class="sxs-lookup"><span data-stu-id="3ad86-143">Bal. Source No.</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="3ad86-144">Shell</span><span class="sxs-lookup"><span data-stu-id="3ad86-144">Shell</span></span> |<span data-ttu-id="3ad86-145">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="3ad86-145">BLANK</span></span> |<span data-ttu-id="3ad86-146">8510</span><span class="sxs-lookup"><span data-stu-id="3ad86-146">8510</span></span> |<span data-ttu-id="3ad86-147">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="3ad86-147">G/L Account</span></span> |<span data-ttu-id="3ad86-148">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="3ad86-148">BLANK</span></span> |

> [!TIP]  
>   <span data-ttu-id="3ad86-149">Дополнительные сведения о работе с полями и столбцами см. в разделе [Работа с [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md).</span><span class="sxs-lookup"><span data-stu-id="3ad86-149">For more information about how to work with fields and columns, see [Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md).</span></span> <span data-ttu-id="3ad86-150">Дополнительные сведения о поиске определенных страниц см. в разделе [Поиск](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="3ad86-150">For more information about how to find specific pages, see [Search](ui-search.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ad86-151">См. также</span><span class="sxs-lookup"><span data-stu-id="3ad86-151">See Also</span></span>
[<span data-ttu-id="3ad86-152">Управление дебиторской задолженностью</span><span class="sxs-lookup"><span data-stu-id="3ad86-152">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="3ad86-153">Продажи</span><span class="sxs-lookup"><span data-stu-id="3ad86-153">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3ad86-154">Практическое руководство. Настройка службы банковских выписок Envestnet Yodlee</span><span class="sxs-lookup"><span data-stu-id="3ad86-154">How to: Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
<span data-ttu-id="3ad86-155">[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3ad86-155">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="3ad86-156">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3ad86-156">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
