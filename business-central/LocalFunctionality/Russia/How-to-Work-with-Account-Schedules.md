---
title: Работа с финансовыми отчетами в России
description: Российские улучшения включают дополнительные функции, связанные с финансовыми отчетами.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 20e4917fccf73b4cacda4c250411b530dd129ac8
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738276"
---
# <a name="how-to-work-with-account-schedules"></a><span data-ttu-id="6d764-103">Практическое руководство. Работа с финансовыми отчетами</span><span class="sxs-lookup"><span data-stu-id="6d764-103">How to: Work with Account Schedules</span></span>

<span data-ttu-id="6d764-104">Используйте финансовые отчеты для получения сведений о финансовых данных, сохраненных в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="6d764-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="6d764-105">Финансовые отчеты анализируют цифры на счетах главной книги и сравнивают операции главной книги с операциями бюджета главной книги.</span><span class="sxs-lookup"><span data-stu-id="6d764-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="6d764-106">Результаты отображаются на диаграммах на домашней странице, например на диаграмме "Движение денежных средств".</span><span class="sxs-lookup"><span data-stu-id="6d764-106">The results display in charts on your Home page, such as the Cash Flow chart.</span></span> 

[!INCLUDE[prodshort](../../includes/prodshort.md)] <span data-ttu-id="6d764-107">обеспечивает несколько примеров финансовых отчетов, которые можно использовать сразу же, либо можно настроить собственные строки и столбцы для указания цифр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="6d764-107">provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="6d764-108">Например, вы можете создавать финансовые отчеты для вычисления размеров прибыли по таким измерениям, как подразделения или группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="6d764-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="6d764-109">Можно создать столько пользовательских финансовых отчетов, сколько нужно.</span><span class="sxs-lookup"><span data-stu-id="6d764-109">You can create as many customized financial statements as you want.</span></span>

<span data-ttu-id="6d764-110">Настройка финансовых отчетов требует понимания финансовых данных в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="6d764-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="6d764-111">Например, можно рассматривать операции главной книги как процент от бюджетных операций.</span><span class="sxs-lookup"><span data-stu-id="6d764-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="6d764-112">Для этого необходимо создать бюджеты.</span><span class="sxs-lookup"><span data-stu-id="6d764-112">This requires that budgets are created.</span></span> <span data-ttu-id="6d764-113">Дополнительные сведения см. в разделе [Практическое руководство. Создание бюджетов](../../finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="6d764-113">For more information, see [How to: Create Budgets](../../finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="6d764-114">Категории счетов и финансовые отчеты</span><span class="sxs-lookup"><span data-stu-id="6d764-114">Account Categories and Account Schedules</span></span>

<span data-ttu-id="6d764-115">Дл изменения макетов финансовых отчетов можно использовать категории счетов.</span><span class="sxs-lookup"><span data-stu-id="6d764-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="6d764-116">После настройки категорий счетов в окне **Категории счетов ГК** и выбора действия **Создать финансовые отчеты** соответствующие финансовые отчеты для основных финансовых отчетов будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="6d764-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="6d764-117">При следующем выполнении одного из этих отчетов, например балансового отчета, будут добавлены новые итоговые значения и вложенные операции на основании внесенных изменений.</span><span class="sxs-lookup"><span data-stu-id="6d764-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> 

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="6d764-118">Создание новых финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="6d764-118">To create new account schedules</span></span>

<span data-ttu-id="6d764-119">Использование финансовых отчетов для анализа числовых значений на счетах главной книги или для сравнения операций главной книги с операциями бюджета главной книги.</span><span class="sxs-lookup"><span data-stu-id="6d764-119">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="6d764-120">Например, можно рассматривать операции ГК как процент от бюджетных операций.</span><span class="sxs-lookup"><span data-stu-id="6d764-120">For example, you can view the general ledger entries as percentages of the budget entries.</span></span> 

1. <span data-ttu-id="6d764-121">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6d764-121">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>

2. <span data-ttu-id="6d764-122">В окне **Названия финансовых отчетов** выберите действие **Создать**, чтобы создать новое название финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="6d764-122">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>

3. <span data-ttu-id="6d764-123">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="6d764-123">Fill in the fields as necessary.</span></span> <span data-ttu-id="6d764-124">Выберите поле для чтения краткого описания поля или ссылки на дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="6d764-124">Choose a field to read a short description of the field or link to more information.</span></span>

4. <span data-ttu-id="6d764-125">Выберите действие **Изменение финансового отчета**.</span><span class="sxs-lookup"><span data-stu-id="6d764-125">Choose the **Edit Account Schedule** action.</span></span>

5. <span data-ttu-id="6d764-126">В окне **Финансовый отчет** заполните все поля соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="6d764-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>

   <span data-ttu-id="6d764-127">После создания нового финансового отчета и настройки строк следует настроить столбцы.</span><span class="sxs-lookup"><span data-stu-id="6d764-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="6d764-128">Настройку можно производить либо вручную, либо предварительно задать для финансового отчета раскладку столбцов.</span><span class="sxs-lookup"><span data-stu-id="6d764-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>

6. <span data-ttu-id="6d764-129">Выберите действие **Изменить настройку макета столбца**.</span><span class="sxs-lookup"><span data-stu-id="6d764-129">Choose the **Edit Column Layout Setup** action.</span></span>

7. <span data-ttu-id="6d764-130">В окне **Раскладка столбцов** заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="6d764-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]
> <span data-ttu-id="6d764-131">Если финансовому отчету не назначена используемая по умолчанию раскладка столбцов, необходимо настроить столбцы вручную.</span><span class="sxs-lookup"><span data-stu-id="6d764-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="6d764-132">Создание столбца для вычисления процентов</span><span class="sxs-lookup"><span data-stu-id="6d764-132">To create a column that calculates percentages</span></span>

<span data-ttu-id="6d764-133">Иногда может возникать потребность включить столбец в финансовый отчет для расчета процентов по итоговой сумме.</span><span class="sxs-lookup"><span data-stu-id="6d764-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="6d764-134">Например, если имеется несколько строк, разбивающих продажи по измерениям, может потребоваться столбец с указанием процента от общих продаж для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="6d764-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span> 

1. <span data-ttu-id="6d764-135">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6d764-135">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="6d764-136">В окне **Названия финансовых отчетов** выберите финансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="6d764-136">In the **Account Schedule Names** window, select an account schedule.</span></span>
3. <span data-ttu-id="6d764-137">Выберите действие **Изменение финансового отчета**, чтобы настроить строку финансового отчета для вычисления общей суммы, на которой будет основан процент.</span><span class="sxs-lookup"><span data-stu-id="6d764-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>
4. <span data-ttu-id="6d764-138">Вставьте строку непосредственно перед первой строкой, для которой необходимо отобразить проценты.</span><span class="sxs-lookup"><span data-stu-id="6d764-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>
5. <span data-ttu-id="6d764-139">Заполните поля в строке следующим образом: В поле **Тип группировки** укажите **Задать базу для процентов**.</span><span class="sxs-lookup"><span data-stu-id="6d764-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="6d764-140">В поле **Подсчет итога** введите формулу для итога, на которой будет основан расчет процента.</span><span class="sxs-lookup"><span data-stu-id="6d764-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="6d764-141">Например, если строка 11 показывает итоговые продажи, введите **11**.</span><span class="sxs-lookup"><span data-stu-id="6d764-141">For example, if row 11 contains the total sales, enter **11**.</span></span>
6. <span data-ttu-id="6d764-142">Выберите действие **Изменить настройку макета столбца**.</span><span class="sxs-lookup"><span data-stu-id="6d764-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>
7. <span data-ttu-id="6d764-143">Заполните поля в строке следующим образом: В поле **Тип столбца** выберите **Формула**.</span><span class="sxs-lookup"><span data-stu-id="6d764-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="6d764-144">В поле **Формула** введите формулу для суммы, для которой необходимо вычислить процент, добавив в конце символ %.</span><span class="sxs-lookup"><span data-stu-id="6d764-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="6d764-145">Например, если столбец с номером N содержит чистое изменение, то введите **N%**.</span><span class="sxs-lookup"><span data-stu-id="6d764-145">For example, if column number N contains the net change, enter **N%**.</span></span>
8. <span data-ttu-id="6d764-146">Повторите шаги с 4 по 7 для каждой группы строк, по которым требуется получить процент.</span><span class="sxs-lookup"><span data-stu-id="6d764-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="6d764-147">Настройка финансовых отчетов с обзорами</span><span class="sxs-lookup"><span data-stu-id="6d764-147">To set up account schedules with overviews</span></span>

<span data-ttu-id="6d764-148">Финансовый отчет можно использовать для создания отчета, содержащего сравнение цифр главной книги с цифрами бюджета главной книги.</span><span class="sxs-lookup"><span data-stu-id="6d764-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span> 

1. <span data-ttu-id="6d764-149">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6d764-149">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>

2. <span data-ttu-id="6d764-150">В окне **Названия финансовых отчетов** выберите финансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="6d764-150">In the **Account Schedule Names** window, select an account schedule.</span></span>

3. <span data-ttu-id="6d764-151">Выберите действие **Изменение финансового отчета**.</span><span class="sxs-lookup"><span data-stu-id="6d764-151">Choose the **Edit Account Schedule** action</span></span>

4. <span data-ttu-id="6d764-152">В окне **Финансовый отчет** в поле **Имя** выберите название финансового отчета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d764-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>

5. <span data-ttu-id="6d764-153">Выберите действие **Вставить счета**.</span><span class="sxs-lookup"><span data-stu-id="6d764-153">Choose the **Insert Accounts** action.</span></span>

6. <span data-ttu-id="6d764-154">Выделите счета, по которым необходимо составить отчет, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6d764-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

   <span data-ttu-id="6d764-155">Теперь счета вставлены в финансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="6d764-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="6d764-156">При желании можно изменить также раскладку столбцов.</span><span class="sxs-lookup"><span data-stu-id="6d764-156">If you want you can also change the column layout.</span></span>

7. <span data-ttu-id="6d764-157">Выберите действие **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="6d764-157">Choose the **Overview** action.</span></span>

8. <span data-ttu-id="6d764-158">На экспресс-вкладке **Фильтры измерения** задайте фильтр по бюджету с требуемым названием фильтра.</span><span class="sxs-lookup"><span data-stu-id="6d764-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>

9. <span data-ttu-id="6d764-159">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6d764-159">Choose the **OK** button.</span></span>

<span data-ttu-id="6d764-160">Теперь можно копировать и вставлять бюджетные отчеты в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6d764-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d764-161">См. также</span><span class="sxs-lookup"><span data-stu-id="6d764-161">See Also</span></span>

[<span data-ttu-id="6d764-162">Финансы</span><span class="sxs-lookup"><span data-stu-id="6d764-162">Finance</span></span>](../../finance.md)  
[<span data-ttu-id="6d764-163">Настройка финансов</span><span class="sxs-lookup"><span data-stu-id="6d764-163">Setting Up Finance</span></span>](../../finance-setup-finance.md)  
[<span data-ttu-id="6d764-164">Главная книга и план счетов</span><span class="sxs-lookup"><span data-stu-id="6d764-164">The General Ledger and the Chart of Accounts</span></span>](../../finance-general-ledger.md)  