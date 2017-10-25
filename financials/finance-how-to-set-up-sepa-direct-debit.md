---
title: "Настройка прямого дебетования SEPA | Документы Майкрософт"
description: "Узнайте, как настроить прямое дебетование SEPA в Dynamics 365 for Financials."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: fea703b804fbc88e5c39f52f72bbda5699237b6b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-set-up-sepa-direct-debit"></a><span data-ttu-id="ab4ff-103">Практическое руководство. Настройка прямого дебетования SEPA</span><span class="sxs-lookup"><span data-stu-id="ab4ff-103">How to: Set Up SEPA Direct Debit</span></span>
<span data-ttu-id="ab4ff-104">Из окна **Коллекции прямого дебетования** можно экспортировать команды для вашего электронного банка, чтобы выполнить погашение прямого дебета с банковского счета клиента на ваш банковский счет.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-104">From the **Direct Debit Collections** window, you can export instructions to your electronic bank to perform a direct debit collection from the customer’s bank account to your bank account.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ab4ff-105"> поддерживает формат прямого дебетования SEPA, но в вашей стране или регионе могут быть доступны другие форматы электронных платежей.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-105"> supports the SEPA direct debit format, but in your country/region,other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="ab4ff-106">Чтобы разрешить экспорт форматов банковских файлов, для которых отсутствует готовая поддержка в [!INCLUDE[d365fin](includes/d365fin_md.md)], можно настроить определение обмена данными при помощи платформы обмена данными.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)] , you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="ab4ff-107">Дополнительные сведения см. в разделе [Практическое руководство. Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ff-107">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="ab4ff-108">Прежде чем выполнять обработку платежей клиента электронным способом путем экспорта команд для прямого дебита в формат SEPA Direct Debit, необходимо выполнить следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-108">Before you can process customer payments electronically by exporting direct debit instructions in the SEPA Direct Debit format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="ab4ff-109">Настройка формат экспорта файла банка, который инструктирует ваш банк выполнить погашение прямого дебета с банковского счета клиента на ваш банковский счет.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-109">Set up the export format of the bank file that instructs your bank to perform a direct debit collection from the customer’s bank account to your bank account.</span></span>  
* <span data-ttu-id="ab4ff-110">Настройка метода оплаты клиента.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-110">Set up the customer’s payment method.</span></span>  
* <span data-ttu-id="ab4ff-111">Настройка мандата прямого дебета, отражающего соглашение с клиентом для получения от него оплаты в определенный срок соглашения.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-111">Set up the direct-debit mandate that reflects your agreement with the customer to collect their payments in a certain agreement period.</span></span>  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><span data-ttu-id="ab4ff-112">Настройка банковского счета для прямого дебета SEPA</span><span class="sxs-lookup"><span data-stu-id="ab4ff-112">To set up your bank account for SEPA direct debit</span></span>  
1. <span data-ttu-id="ab4ff-113">В поле **Поиск** введите **Банковские счета**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-113">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab4ff-114">Откройте банковский счет, который необходимо использовать для прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-114">Open the bank account that you want to use for direct debit.</span></span>  
3. <span data-ttu-id="ab4ff-115">На экспресс-вкладке **Перемещение** в поле **Формат экспорта прямого дебетования SEPA** выберите параметр для прямого дебета SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-115">On the **Transfer** FastTab, in the **SEPA Direct Debit Export Format** field, choose the option for SEPA direct debit.</span></span>  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><span data-ttu-id="ab4ff-116">Настройка способа оплаты клиента при прямом дебете SEPA</span><span class="sxs-lookup"><span data-stu-id="ab4ff-116">To set up the customer’s payment method for SEPA direct debit</span></span>  
1. <span data-ttu-id="ab4ff-117">В поле **Поиск** введите **Способы оплаты**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-117">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab4ff-118">Выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-118">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ab4ff-119">Задайте способ платежа.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-119">Set up a payment method.</span></span> <span data-ttu-id="ab4ff-120">Заполните поля, относящиеся к прямому дебету, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-120">Fill in the direct debit\-specific fields as described in the following table.</span></span>  

    |<span data-ttu-id="ab4ff-121">Поле</span><span class="sxs-lookup"><span data-stu-id="ab4ff-121">Field</span></span>|<span data-ttu-id="ab4ff-122">[Описание</span><span class="sxs-lookup"><span data-stu-id="ab4ff-122">[Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ab4ff-123">**Прямое дебетование**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-123">**Direct Debit**</span></span>|<span data-ttu-id="ab4ff-124">Укажите, используется ли способ оплаты для погашения прямого дебета SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-124">Specify if the payment method is for SEPA direct debit collection.</span></span>|  
    |<span data-ttu-id="ab4ff-125">**Код условий оплаты прямого дебетования**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-125">**Direct Debit Pmt. Terms Code**</span></span>|<span data-ttu-id="ab4ff-126">Укажите условия оплаты, например "НЕ ПЛАТИТЬ", отображаемые в счетах продажи, оплачиваемых по прямому дебету SEPA, чтобы показать клиенту, что платеж будет погашен автоматически.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-126">Specify the payment terms, such as DON’T PAY, that are displayed on sales invoices that are paid with SEPA direct debit to indicate to the customer that the payment will be collected automatically.</span></span> <span data-ttu-id="ab4ff-127">В ином случае оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-127">Alternatively, leave the field empty.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="ab4ff-128">Не вводите значение в поле **Номер баланс. счета**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-128">Do not enter a value in the **Bal. Account No.** field.</span></span>  

4. <span data-ttu-id="ab4ff-129">Нажмите кнопку **OK**, чтобы закрыть окно **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-129">Choose the **OK** button to close the **Payment Methods** window.</span></span>  
5. <span data-ttu-id="ab4ff-130">В поле **Поиск** введите **Клиенты**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-130">In the **Search** box, enter **Customers**, and then choose the related link.</span></span>  
6. <span data-ttu-id="ab4ff-131">Откройте карточку клиента, для которого необходимо настроить погашения прямого дебета SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-131">Open the customer card for the customer that you want to set up for SEPA direct debit collection.</span></span>  
7. <span data-ttu-id="ab4ff-132">Выберите поле **Код способа оплаты**, а затем выберите код способа оплаты, указанный вами на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-132">Choose the **Payment Method Code** field, and then select the payment method code that you specified in step 3.</span></span>  
8. <span data-ttu-id="ab4ff-133">Повторите шаги 6 и 7 для всех клиентов, для которых нужно настроить взыскание прямых дебетов SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-133">Repeat steps 6 and 7 for all customers that you want to set up for SEPA direct debit collection.</span></span>  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><span data-ttu-id="ab4ff-134">Настройка мандата прямого дебета, который представляет соглашение с клиентом</span><span class="sxs-lookup"><span data-stu-id="ab4ff-134">To set up the direct-debit mandate that represents the customer agreement</span></span>  
1. <span data-ttu-id="ab4ff-135">В поле **Поиск** введите **Клиенты**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-135">In the **Search** box, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ab4ff-136">Откройте карточку клиента, для которого необходимо настроить прямые дебеты SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-136">Open the card for the customer that you want to set up for SEPA direct debits.</span></span>  
3. <span data-ttu-id="ab4ff-137">Выберите действие **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-137">Choose the **Bank Accounts** action.</span></span>  
4. <span data-ttu-id="ab4ff-138">В окне **Список банковских счетов клиента** выберите банковский счет клиента, который будет использовать прямые дебеты, и затем на вкладке **Главная** в окне **Процесс** выберите **Поручения на прямое дебетование**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-138">In the **Customer Bank Account List** window, select the customer bank account that will use direct debits, and then, on the **Home** tab, in the **Process** group, choose **Direct Debit Mandates**.</span></span>  
5. <span data-ttu-id="ab4ff-139">В окне **Поручения на прямое дебетование SEPA** заполните поля, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-139">In the **SEPA Direct Debit Mandates** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ab4ff-140">[Поле</span><span class="sxs-lookup"><span data-stu-id="ab4ff-140">[Field</span></span>|<span data-ttu-id="ab4ff-141">Описание]</span><span class="sxs-lookup"><span data-stu-id="ab4ff-141">Description]</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ab4ff-142">**Код банковского счета клиента**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-142">**Customer Bank Account Code**</span></span>|<span data-ttu-id="ab4ff-143">Определяет банковский счет, с которого списываются суммы платежей по прямому дебету.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-143">Specifies the bank account from which direct\-debit payments are collected.</span></span> <span data-ttu-id="ab4ff-144">Это поле заполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-144">This field is filled automatically.</span></span>|  
    |<span data-ttu-id="ab4ff-145">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-145">**Valid From**</span></span>|<span data-ttu-id="ab4ff-146">Укажите дату начала действия мандата прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-146">Specify the date when the direct\-debit mandate starts.</span></span>|  
    |<span data-ttu-id="ab4ff-147">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-147">**Valid To**</span></span>|<span data-ttu-id="ab4ff-148">Укажите дату окончания срока действия мандата прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-148">Specify the date when the direct\-debit mandate ends.</span></span>|  
    |<span data-ttu-id="ab4ff-149">**Дата подписания**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-149">**Date of Signature**</span></span>|<span data-ttu-id="ab4ff-150">Укажите дату подписания клиентом мандата прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-150">Specify the date when the customer signed the direct\-debit mandate.</span></span>|  
    |<span data-ttu-id="ab4ff-151">**Тип последовательности**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-151">**Sequence Type**</span></span>|<span data-ttu-id="ab4ff-152">Укажите, охватывает ли соглашение несколько (**Типовой**) или одно (**Одно**) погашение прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-152">Specify if the agreement covers multiple (**Recurring**) or a single (**One Off**) direct debit collection.</span></span>|  
    |<span data-ttu-id="ab4ff-153">**Ожидаемое число списаний**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-153">**Expected Number of Debits**</span></span>|<span data-ttu-id="ab4ff-154">Укажите планируемое количество погашений прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-154">Specify how many direct debit collections you expect to make.</span></span> <span data-ttu-id="ab4ff-155">Это поле имеет значение, только если выбрано значение **Типовой** в поле **Тип последовательности**.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-155">This field is only relevant if you selected **Recurring** in the **Sequence Type** field.</span></span>|  
    |<span data-ttu-id="ab4ff-156">**Счетчик списаний**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-156">**Debit Counter**</span></span>|<span data-ttu-id="ab4ff-157">Определяет количество погашений прямого дебета, созданных с помощью данного мандата прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-157">Specifies how many direct debit collections have been made using this direct\-debit mandate.</span></span> <span data-ttu-id="ab4ff-158">Это поле обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-158">This field is automatically updated.</span></span>|  
    |<span data-ttu-id="ab4ff-159">**Заблокировано**</span><span class="sxs-lookup"><span data-stu-id="ab4ff-159">**Blocked**</span></span>|<span data-ttu-id="ab4ff-160">Укажите, что погашение прямого дебета невозможно создать с помощью данного мандата прямого дебета.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-160">Specify that direct debit collections cannot be made using this direct\-debit mandate.</span></span>|  

6.  <span data-ttu-id="ab4ff-161">Повторите шаги с 1 по 5 для всех клиентов, которых нужно настроить для прямых дебетов SEPA.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-161">Repeat steps 1 through 5 for all customers that you want to set up for SEPA direct debits.</span></span>  

 <span data-ttu-id="ab4ff-162">Мандат прямого дебета автоматически вставляется в поле **Идентификатор поручения на прямое дебетование** при создании счета продажи для клиента, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="ab4ff-162">The direct-debit mandate is automatically inserted in the **Direct Debit Mandate ID** field when you create a sales invoice for the customer that you selected in step 2.</span></span> <span data-ttu-id="ab4ff-163">Дополнительные сведения см. в разделе [Практическое руководство. Создание типовых строк продажи и покупки](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ff-163">For more information, see [How to: Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab4ff-164">См. также</span><span class="sxs-lookup"><span data-stu-id="ab4ff-164">See Also</span></span>  
[<span data-ttu-id="ab4ff-165">Сбор платежей с прямым дебетом SEPA</span><span class="sxs-lookup"><span data-stu-id="ab4ff-165">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
<span data-ttu-id="ab4ff-166">[Практическое руководство. Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md)
[Практическое руководство. Создание типовых строк продажи и покупки](sales-how-work-standard-lines.md)
[Электронный обмен данными](across-data-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="ab4ff-166">[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md)
[How to: Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md)
[Exchanging Data Electronically](across-data-exchange.md)</span></span>
