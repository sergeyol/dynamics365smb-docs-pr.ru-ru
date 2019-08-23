---
title: Схема налогового агента поставщика в России
description: Российские усовершенствования включают схемы налоговых агентов поставщиков.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: c4f5f156f025d0ecb916010aba2d006515b06ec2
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738273"
---
# <a name="vendor-tax-agent-scheme"></a><span data-ttu-id="bb531-103">Схема налогового агента поставщика</span><span class="sxs-lookup"><span data-stu-id="bb531-103">Vendor Tax Agent scheme</span></span>

## <a name="vat-from-internal-funds"></a><span data-ttu-id="bb531-104">НДС из внутренних фондов</span><span class="sxs-lookup"><span data-stu-id="bb531-104">VAT from Internal Funds</span></span>

<span data-ttu-id="bb531-105">Заполните поля в карточке поставщика.</span><span class="sxs-lookup"><span data-stu-id="bb531-105">Fill the fields in Vendor Card.</span></span>

1. <span data-ttu-id="bb531-106">На вкладке "Договор":</span><span class="sxs-lookup"><span data-stu-id="bb531-106">On Agreement tab:</span></span> 

    - <span data-ttu-id="bb531-107">Учет договоров - обязательно.</span><span class="sxs-lookup"><span data-stu-id="bb531-107">Agreement posting - mandatory.</span></span>

    - <span data-ttu-id="bb531-108">Номера договоров обязательны.</span><span class="sxs-lookup"><span data-stu-id="bb531-108">Agreement Nos is required.</span></span>

2. <span data-ttu-id="bb531-109">В карточке договора:</span><span class="sxs-lookup"><span data-stu-id="bb531-109">In Agreement card:</span></span>

    - <span data-ttu-id="bb531-110">НДС бизнес-группа</span><span class="sxs-lookup"><span data-stu-id="bb531-110">VAT Bus. Posting Group</span></span> 
    - <span data-ttu-id="bb531-111">НДС товарная группа налогового агента</span><span class="sxs-lookup"><span data-stu-id="bb531-111">VAT Agent Prod. Posting Group</span></span>
    - <span data-ttu-id="bb531-112">Тип источника оплаты НДС - Внутренние фонды</span><span class="sxs-lookup"><span data-stu-id="bb531-112">VAT Payment Source Type - Internal Funds</span></span>

## <a name="prepayment-and-payment-vat"></a><span data-ttu-id="bb531-113">Предоплата и оплата НДС</span><span class="sxs-lookup"><span data-stu-id="bb531-113">Prepayment and Payment VAT</span></span>

1. <span data-ttu-id="bb531-114">Создание и выпуск счета</span><span class="sxs-lookup"><span data-stu-id="bb531-114">Create and release an invoice</span></span>

<span data-ttu-id="bb531-115">Номер договора</span><span class="sxs-lookup"><span data-stu-id="bb531-115">Agreement No.</span></span> <span data-ttu-id="bb531-116">(с настройками для продавца с уплатой НДС из внутренних фондов) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="bb531-116">(with settings for Vendor with VAT Payment from internal funds) should be specified.</span></span>

2. <span data-ttu-id="bb531-117">Создание строки в журнале платежей:</span><span class="sxs-lookup"><span data-stu-id="bb531-117">Create a line in Payment Journal:</span></span>

    - <span data-ttu-id="bb531-118">Тип документа - Платеж</span><span class="sxs-lookup"><span data-stu-id="bb531-118">Document Type - Payment</span></span>
    - <span data-ttu-id="bb531-119">Предоплата - да</span><span class="sxs-lookup"><span data-stu-id="bb531-119">Prepayment - yes</span></span>
    - <span data-ttu-id="bb531-120">Номер документа предоплаты не требуется.</span><span class="sxs-lookup"><span data-stu-id="bb531-120">Prepayment Document No is required.</span></span>

3. <span data-ttu-id="bb531-121">Выполните учет строк журнала.</span><span class="sxs-lookup"><span data-stu-id="bb531-121">Post lines of Journal</span></span>

    <span data-ttu-id="bb531-122">Операции с НДС генерируются автоматически в рублях.</span><span class="sxs-lookup"><span data-stu-id="bb531-122">Operations with VAT are automatically generated in rubles.</span></span>

4. <span data-ttu-id="bb531-123">Создайте и учтите в журнале платежей для налогового органа строку с суммой НДС для предоплаты.</span><span class="sxs-lookup"><span data-stu-id="bb531-123">Create and post line in Payment Journal for Tax Authority with VAT Amount of prepayment.</span></span>

5. <span data-ttu-id="bb531-124">Выполните отгрузку и учет счета.</span><span class="sxs-lookup"><span data-stu-id="bb531-124">Ship and post invoice.</span></span>

6. <span data-ttu-id="bb531-125">Создайте строку в журнале платежей</span><span class="sxs-lookup"><span data-stu-id="bb531-125">Create a line in Payment Journal</span></span>

    - <span data-ttu-id="bb531-126">Тип документа - Платеж</span><span class="sxs-lookup"><span data-stu-id="bb531-126">Document Type - Payment</span></span>
    - <span data-ttu-id="bb531-127">Номер начального документа - Номер</span><span class="sxs-lookup"><span data-stu-id="bb531-127">Initial Document No. - No.</span></span> <span data-ttu-id="bb531-128">учтенного счета</span><span class="sxs-lookup"><span data-stu-id="bb531-128">of posted invoice</span></span>
    - <span data-ttu-id="bb531-129">Примен. к док. - номер - Номер</span><span class="sxs-lookup"><span data-stu-id="bb531-129">Applies-to Doc. No. - No.</span></span> <span data-ttu-id="bb531-130">учтенного счета</span><span class="sxs-lookup"><span data-stu-id="bb531-130">of posted invoice</span></span>

7. <span data-ttu-id="bb531-131">Создайте и выполните учет платежа в налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="bb531-131">Create and post payment to the Tax Authority.</span></span>
8. <span data-ttu-id="bb531-132">Откройте журнал НДС.</span><span class="sxs-lookup"><span data-stu-id="bb531-132">Go to VAT Settlement Worksheet.</span></span> <span data-ttu-id="bb531-133">Выполните учет НДС (см. [Зачет НДС](Settlement-VAT.md)).</span><span class="sxs-lookup"><span data-stu-id="bb531-133">Post VAT (see [Settlement VAT](Settlement-VAT.md)).</span></span>

## <a name="vat-from-vendor-funds"></a><span data-ttu-id="bb531-134">НДС из фондов поставщика</span><span class="sxs-lookup"><span data-stu-id="bb531-134">VAT from Vendor Funds</span></span>

<span data-ttu-id="bb531-135">Заполните поля в карточке поставщика.</span><span class="sxs-lookup"><span data-stu-id="bb531-135">Fill the fields in Vendor Card.</span></span>

1. <span data-ttu-id="bb531-136">На вкладке "Договор":</span><span class="sxs-lookup"><span data-stu-id="bb531-136">On Agreement tab:</span></span> 

    - <span data-ttu-id="bb531-137">Учет договоров - обязательно.</span><span class="sxs-lookup"><span data-stu-id="bb531-137">Agreement posting - mandatory.</span></span>
    - <span data-ttu-id="bb531-138">Номера договоров обязательны.</span><span class="sxs-lookup"><span data-stu-id="bb531-138">Agreement Nos is required.</span></span>

2. <span data-ttu-id="bb531-139">В карточке договора:</span><span class="sxs-lookup"><span data-stu-id="bb531-139">In Agreement card:</span></span>

    - <span data-ttu-id="bb531-140">НДС бизнес-группа</span><span class="sxs-lookup"><span data-stu-id="bb531-140">VAT Bus. Posting Group</span></span> 
    - <span data-ttu-id="bb531-141">НДС товарная группа налогового агента</span><span class="sxs-lookup"><span data-stu-id="bb531-141">VAT Agent Prod. Posting Group</span></span>
    - <span data-ttu-id="bb531-142">Тип источника оплаты НДС - Фонды поставщика</span><span class="sxs-lookup"><span data-stu-id="bb531-142">VAT Payment Source Type - Vendor Funds</span></span>

## <a name="prepayment-and-payment-vat"></a><span data-ttu-id="bb531-143">Предоплата и оплата НДС</span><span class="sxs-lookup"><span data-stu-id="bb531-143">Prepayment and Payment VAT</span></span>

1. <span data-ttu-id="bb531-144">Создайте и выпустите счет.</span><span class="sxs-lookup"><span data-stu-id="bb531-144">Create and release an invoice.</span></span>

2. <span data-ttu-id="bb531-145">Для оплаты в валюте для банка и в рублях для поставщика необходимо создать две строки в **журнале платежей**.</span><span class="sxs-lookup"><span data-stu-id="bb531-145">For the payment in the currency for the bank and in rubles for the vendor it is necessary to create two lines in the **payment journal**.</span></span>

    <span data-ttu-id="bb531-146">**Для поставщика:**</span><span class="sxs-lookup"><span data-stu-id="bb531-146">**For vendor:**</span></span>

        - Posting Date,
        - Document Type - Payment
        - Prepayment - yes
        - Account Type - Vendor
        - Account No.
        - Agreement No.
        - Bal. Account Type - G/L Account
        - Bal. Account - “ ”
        - Currency Code - “ “
        - Prepayment Document No. is required
        - Amount - in rubles

    <span data-ttu-id="bb531-147">**Для банка:**</span><span class="sxs-lookup"><span data-stu-id="bb531-147">**For Bank:**</span></span>

        - Posting Date,
        - Document Type - Payment
        - Prepayment - yes
        - Account Type - Bank Account
        - Account No.
        - Agreement No.
        - Bal. Account Type -  G/L Account
        - Bal. Account - “ ”
        - Currency Code 
        - Amount - in USD/EUR

3. <span data-ttu-id="bb531-148">Выполните учет строк журнала.</span><span class="sxs-lookup"><span data-stu-id="bb531-148">Post the lines of Journal.</span></span>
4. <span data-ttu-id="bb531-149">Выполните отгрузку.</span><span class="sxs-lookup"><span data-stu-id="bb531-149">Ship.</span></span>

    <span data-ttu-id="bb531-150">Вы можете изменить код валюты и сумму в счете.</span><span class="sxs-lookup"><span data-stu-id="bb531-150">You can change the Currency Code and Amount in the Invoice.</span></span>

5. <span data-ttu-id="bb531-151">Учет счета.</span><span class="sxs-lookup"><span data-stu-id="bb531-151">Post the invoice.</span></span>

6. <span data-ttu-id="bb531-152">Примените операцию.</span><span class="sxs-lookup"><span data-stu-id="bb531-152">Apply Entry.</span></span>

7. <span data-ttu-id="bb531-153">Откройте журнал НДС.</span><span class="sxs-lookup"><span data-stu-id="bb531-153">Go to VAT Settlement Worksheet.</span></span> <span data-ttu-id="bb531-154">Выполните учет НДС (см. [Зачет НДС](Settlement-VAT.md)).</span><span class="sxs-lookup"><span data-stu-id="bb531-154">Post VAT (see [Settlement VAT](Settlement-VAT.md)).</span></span>

    <span data-ttu-id="bb531-155">В конце периода будут формироваться операции в результате переоценки задолженности.</span><span class="sxs-lookup"><span data-stu-id="bb531-155">At the end of the period will be formed entries as a result of revaluation of debt.</span></span>

8. <span data-ttu-id="bb531-156">Создайте строки в журнале платежей и учтите их.</span><span class="sxs-lookup"><span data-stu-id="bb531-156">Create and post lines in Payment Journal.</span></span>

    <span data-ttu-id="bb531-157">Для оплаты в валюте для банка и в рублях для поставщика необходимо создать две строки в журнале платежей.</span><span class="sxs-lookup"><span data-stu-id="bb531-157">For the payment in the currency for the bank and in rubles for the vendor it is necessary to create two lines in the payment journal.</span></span>

    <span data-ttu-id="bb531-158">**Для поставщика:**</span><span class="sxs-lookup"><span data-stu-id="bb531-158">**For vendor:**</span></span>

        - Posting Date
        - Document Type - Payment
        - Account Type - Vendor
        - Account No.
        - External Document No.
        - Internal Document No.
        - Agreement No.
        - Bal. Account Type - G/L Account
        - Bal. Account - “ ”
        - Currency Code - “ “
        - Prepayment Document No. is required
        - Amount - in rubles

    <span data-ttu-id="bb531-159">**Для банка:**</span><span class="sxs-lookup"><span data-stu-id="bb531-159">**For Bank:**</span></span>

        - Posting Date,
        - Document Type - Payment
        - Account Type - Bank Account
        - Account No.
        - Agreement No.
        - Bal. Account Type -  G/L Account
        - Bal. Account - “ ”
        - Currency Code 
        - Amount - in USD/EUR

## <a name="see-also"></a><span data-ttu-id="bb531-160">См. также</span><span class="sxs-lookup"><span data-stu-id="bb531-160">See Also</span></span>

[<span data-ttu-id="bb531-161">Функциональность локальной версии для России</span><span class="sxs-lookup"><span data-stu-id="bb531-161">Russia Local Functionality</span></span>](russia-local-functionality.md)  