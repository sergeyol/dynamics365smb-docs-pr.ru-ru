---
title: Создание книг НДС в России
description: Российские улучшения включают работу с книгами НДС.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 1fbdadfdf8b47898c41a5f4543b3bebe571bc898
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738257"
---
# <a name="how-to-create-vat-ledgers"></a><span data-ttu-id="38813-103">Практическое руководство. Создание книг НДС</span><span class="sxs-lookup"><span data-stu-id="38813-103">How to: Create VAT Ledgers</span></span>

<span data-ttu-id="38813-104">Можно создать любое количество книг НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-104">You can create and store any number of VAT ledgers.</span></span> <span data-ttu-id="38813-105">Например, можно создать следующие книги:</span><span class="sxs-lookup"><span data-stu-id="38813-105">For example, you can create the following:</span></span> 

- <span data-ttu-id="38813-106">книги продаж для различных групп клиентов;</span><span class="sxs-lookup"><span data-stu-id="38813-106">Sales ledgers for different groups of customers</span></span>
- <span data-ttu-id="38813-107">дополнительные книги продаж для разниц суммы и предоплат;</span><span class="sxs-lookup"><span data-stu-id="38813-107">Additional sales ledgers for amount differences and prepayments</span></span>
- <span data-ttu-id="38813-108">объединенные книги продаж для компании в целом.</span><span class="sxs-lookup"><span data-stu-id="38813-108">Joint sales ledgers for the whole company</span></span>

## <a name="to-create-a-vat-ledger"></a><span data-ttu-id="38813-109">Создание книги НДС</span><span class="sxs-lookup"><span data-stu-id="38813-109">To create a VAT ledger</span></span>

1. <span data-ttu-id="38813-110">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Список книг покупок и продаж**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="38813-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Ledger List**, and then choose the related link.</span></span>

2. <span data-ttu-id="38813-111">Заполните поля в окне **Список книг покупок и продаж**, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="38813-111">In the **VAT Ledger List** window, fill in the fields as described in the following table.</span></span>

   | <span data-ttu-id="38813-112">Поле</span><span class="sxs-lookup"><span data-stu-id="38813-112">Field</span></span>                 | <span data-ttu-id="38813-113">Описание</span><span class="sxs-lookup"><span data-stu-id="38813-113">Description</span></span>                                                  |
   | :-------------------- | :----------------------------------------------------------- |
   | <span data-ttu-id="38813-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="38813-114">**Type**</span></span>              | <span data-ttu-id="38813-115">Выберите тип книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-115">Select the type of VAT ledger.</span></span>                               |
   | <span data-ttu-id="38813-116">**Код**</span><span class="sxs-lookup"><span data-stu-id="38813-116">**Code**</span></span>              | <span data-ttu-id="38813-117">Введите код серии номеров, который используется для книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-117">Enter the code of the number series that is used for the VAT ledger.</span></span> <span data-ttu-id="38813-118">Доступные коды можно просмотреть в окне **Серии номеров**.</span><span class="sxs-lookup"><span data-stu-id="38813-118">You can view the available codes in the **No. Series** window.</span></span> |
   | <span data-ttu-id="38813-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="38813-119">**Description**</span></span>       | <span data-ttu-id="38813-120">Введите описание книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-120">Enter a description for the VAT ledger.</span></span>                      |
   | <span data-ttu-id="38813-121">**Учетный период**</span><span class="sxs-lookup"><span data-stu-id="38813-121">**Accounting Period**</span></span> | <span data-ttu-id="38813-122">Введите учетный период книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-122">Enter the accounting period of the VAT ledger.</span></span> <span data-ttu-id="38813-123">Доступные учетные периоды можно посмотреть в окне **Учетные периоды**.</span><span class="sxs-lookup"><span data-stu-id="38813-123">You can view the available accounting periods in the **Accounting Periods** window.</span></span> |
   | <span data-ttu-id="38813-124">**Дата начала**</span><span class="sxs-lookup"><span data-stu-id="38813-124">**Start Date**</span></span>        | <span data-ttu-id="38813-125">Определяет дату начала учетного периода книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-125">Specifies the start date of the accounting period of the VAT ledger.</span></span> |
   | <span data-ttu-id="38813-126">**Дата окончания**</span><span class="sxs-lookup"><span data-stu-id="38813-126">**End Date**</span></span>          | <span data-ttu-id="38813-127">Определяет дату окончания учетного периода книги НДС.</span><span class="sxs-lookup"><span data-stu-id="38813-127">Specifies the end date of the accounting period of the VAT ledger.</span></span> |

3. <span data-ttu-id="38813-128">Для добавления строк в книгу НДС выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="38813-128">To add lines to the VAT ledger, choose the **Create** action.</span></span>

4. <span data-ttu-id="38813-129">В окне **Создание книги покупок** или **Создание книги продаж** заполните поля, затем выберите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="38813-129">In the **Create VAT Purchase Ledger** or the **Create VAT Sales Ledger** window, fill in the fields, and then choose the **OK** button.</span></span>

   <span data-ttu-id="38813-130">Книга НДС теперь создана и доступна для использования.</span><span class="sxs-lookup"><span data-stu-id="38813-130">The VAT ledger is now created and available for use.</span></span>

5. <span data-ttu-id="38813-131">Чтобы просмотреть книгу НДС выберите действие **Карточка**.</span><span class="sxs-lookup"><span data-stu-id="38813-131">To view the VAT ledger, choose the **Card** action.</span></span>

<span data-ttu-id="38813-132">Теперь можно напечатать книгу НДС как книгу НДС или как дополнительный лист.</span><span class="sxs-lookup"><span data-stu-id="38813-132">Now, you can print the VAT ledger as a VAT ledger or as an additional sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="38813-133">См. также</span><span class="sxs-lookup"><span data-stu-id="38813-133">See Also</span></span>

[<span data-ttu-id="38813-134">Книги НДС</span><span class="sxs-lookup"><span data-stu-id="38813-134">VAT Ledgers</span></span>](VAT-Ledgers.md)  
[<span data-ttu-id="38813-135">Практическое руководство. Настройка книг НДС</span><span class="sxs-lookup"><span data-stu-id="38813-135">How to: Set Up VAT Ledgers</span></span>](How-to-Set-Up-VAT-Ledgers.md)  
[<span data-ttu-id="38813-136">Практическое руководство. Создание дополнительных листов</span><span class="sxs-lookup"><span data-stu-id="38813-136">How to: Create Additional Sheets</span></span>](How-to-Create-Additional-Sheets.md)  