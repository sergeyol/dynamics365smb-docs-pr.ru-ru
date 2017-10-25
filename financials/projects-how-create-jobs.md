---
title: "Создание карточки работы и указание задач | Документы Майкрософт"
description: "Для нового проекта вы создаете карточку работы, которая содержит рабочие задания и строки планирования, помогающие управлять ходом выполнения бюджетами."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 50ea98d45875fa418d12c5ba378f26208d739126
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-jobs"></a><span data-ttu-id="6e449-103">Практическое руководство. Создание работ</span><span class="sxs-lookup"><span data-stu-id="6e449-103">How to: Create Jobs</span></span>
<span data-ttu-id="6e449-104">В начале нового проекта необходимо создать карту работ с интегрированными рабочими заданиями и строками планирования работ, содержащую два уровня.</span><span class="sxs-lookup"><span data-stu-id="6e449-104">When you start a new project, you must create a job card with integrated job tasks and job planning lines, structured in two layers.</span></span>  

<span data-ttu-id="6e449-105">Первый уровень состоит из рабочих заданий.</span><span class="sxs-lookup"><span data-stu-id="6e449-105">The first layer consists of job tasks.</span></span> <span data-ttu-id="6e449-106">Следует создать по крайней мере одно рабочее задание для каждой работы, поскольку весь учет производится с помощью рабочих заданий.</span><span class="sxs-lookup"><span data-stu-id="6e449-106">You must create at least one job task per job because all posting refers to a job task.</span></span> <span data-ttu-id="6e449-107">Наличие хотя бы одного рабочего задания в работе позволяет настроить строки планирования работ и учесть потребление по работе.</span><span class="sxs-lookup"><span data-stu-id="6e449-107">Having at least one job task in your job enables you to set up job planning lines and to post consumption to the job.</span></span>

<span data-ttu-id="6e449-108">Второй уровень состоит из строк планирования работ, в которых подробно указывается использование ресурсов, товаров и различных расходов из Главной книги.</span><span class="sxs-lookup"><span data-stu-id="6e449-108">The second layer consists of job planning lines, which specify the detailed use of resources, items and various general ledger expenses.</span></span>

<span data-ttu-id="6e449-109">Структура уровней позволяет поделить работу на более мелкие задачи, и, таким образом, получить более конкретные сведения для бюджетирования, предложений и регистрации.</span><span class="sxs-lookup"><span data-stu-id="6e449-109">The layer structure enables you to divide the job into smaller tasks, and therefore use more specific details in budgeting, quotes, and registration.</span></span> <span data-ttu-id="6e449-110">Кроме того, это позволяет анализировать ход выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-110">In addition, it gives you insight into how a job is progressing.</span></span> <span data-ttu-id="6e449-111">Например, вы можете отследить, соблюдаете ли вы назначенные этапы или вы добились ли вы ожидаемых результатов бюджета.</span><span class="sxs-lookup"><span data-stu-id="6e449-111">For example, you can track whether you are meeting designated milestones or if you are on target to meet budget expectations.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6e449-112">Действие **Создать работу** ролевом центре **Менеджер проекта** запускает сопровождаемую настройку, которая направляет вас по шагам создания работы с интегрированными заданиями и строками планирования.</span><span class="sxs-lookup"><span data-stu-id="6e449-112">The **New Job** action on the **Project Manager** Role Center launches an assisted setup that guides you through the steps of creating a job with integrated tasks and planning lines.</span></span> <span data-ttu-id="6e449-113">Следующая процедура описывает выполнение этих шагов вручную.</span><span class="sxs-lookup"><span data-stu-id="6e449-113">The following procedure describes how to perform the steps manually.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6e449-114">Эта функция требует, чтобы было задано значение **Suite**.</span><span class="sxs-lookup"><span data-stu-id="6e449-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="6e449-115">Дополнительные сведения см. в разделе [Настройка взаимодействия [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="6e449-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-job-card"></a><span data-ttu-id="6e449-116">Создание карточки работы</span><span class="sxs-lookup"><span data-stu-id="6e449-116">To create a job card</span></span>
<span data-ttu-id="6e449-117">Вы создаете карточку работы, затем создаете строки рабочего задания и строки планирования работ для него.</span><span class="sxs-lookup"><span data-stu-id="6e449-117">You create a job card and then create job task lines and job planning lines for it.</span></span>

1. <span data-ttu-id="6e449-118">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работы**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6e449-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6e449-119">Выберите действие **Создать**, затем введите в поля требуемые данные.</span><span class="sxs-lookup"><span data-stu-id="6e449-119">Choose the **New** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6e449-120">Для указания работы с информацией о других работах выберите действие **Копировать работу**, заполните поля по мере необходимости, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e449-120">To specify the job with information on other jobs, choose the **Copy Job** action, fill in the fields as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6e449-121">Если в задании используется табели, то необходимо также указывать ответственное лицо.</span><span class="sxs-lookup"><span data-stu-id="6e449-121">If you are using time sheets with your job, you must also designate a person responsible.</span></span> <span data-ttu-id="6e449-122">Это лицо может утверждать табели для задач сотрудника, связанных с работой.</span><span class="sxs-lookup"><span data-stu-id="6e449-122">This person can approve time sheets for the employee tasks associated with the job.</span></span> <span data-ttu-id="6e449-123">Дополнительные сведения см. в разделе [Практическое руководство. Настройка табелей](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="6e449-123">For more information, see [How to: Set Up Timesheets](projects-how-setup-time-sheets.md).</span></span>

## <a name="to-create-tasks-for-a-job"></a><span data-ttu-id="6e449-124">Создание задач для работы</span><span class="sxs-lookup"><span data-stu-id="6e449-124">To create tasks for a job</span></span>
<span data-ttu-id="6e449-125">Основной задачей при создании работы является определение различных задач, входящих в состав работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-125">A key part of creating a job is to specify the various tasks involved in the job.</span></span> <span data-ttu-id="6e449-126">Это можно сделать, добавив новые строки на экспресс-вкладке **Задачи** в окне **Карточка работы**, по строке для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="6e449-126">You do this by adding new lines on the **Tasks** FastTab in the **Job Card** window, one task per line.</span></span> <span data-ttu-id="6e449-127">Каждая работа должна содержать по крайней мере одно задание.</span><span class="sxs-lookup"><span data-stu-id="6e449-127">Every job must have at least one task.</span></span>

1. <span data-ttu-id="6e449-128">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работы**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6e449-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="6e449-129">Откройте карточку работы для соответствующей работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-129">Open the job card for a relevant job.</span></span>
3. <span data-ttu-id="6e449-130">На экспресс-вкладке **Задачи** заполните требуемые поля в новой строке.</span><span class="sxs-lookup"><span data-stu-id="6e449-130">On the **Tasks** FastTab, fill in the fields as necessary on a new line.</span></span>
4. <span data-ttu-id="6e449-131">Для формирования отступов задач и создания иерархии выберите действие **Задачи**, затем выберите действие **Вложенность раб. зад.**.</span><span class="sxs-lookup"><span data-stu-id="6e449-131">To indent tasks and create a hierarchy, Choose the **Tasks** action, the then choose **Indent Job Tasks** action.</span></span>
5. <span data-ttu-id="6e449-132">Повторите шаги 3 и 4 для всех задач, которые необходимы для работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-132">Repeat steps 3 and 4 for all the tasks that you need for the job.</span></span>
6. <span data-ttu-id="6e449-133">Для указания рабочих задач с информацией о других рабочих задачах выберите действие **Копировать рабочие задания из**, заполните поля по мере необходимости, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e449-133">To specify the job tasks with information on other job tasks, choose the **Copy Job Tasks from** action, fill in the fields as necessary, and then choose the **OK** button.</span></span>

## <a name="to-create-planning-lines-for-a-job"></a><span data-ttu-id="6e449-134">Создание строк планирования для работы</span><span class="sxs-lookup"><span data-stu-id="6e449-134">To create planning lines for a job</span></span>
<span data-ttu-id="6e449-135">Можно уточнить новые рабочие задания в строках планирования работ.</span><span class="sxs-lookup"><span data-stu-id="6e449-135">You can refine your new job tasks on job planning lines.</span></span> <span data-ttu-id="6e449-136">Строку планирования можно использовать для записи любой подлежащей трассировке информации о работе.</span><span class="sxs-lookup"><span data-stu-id="6e449-136">A planning line can be used to capture any information that you want to track for a job.</span></span> <span data-ttu-id="6e449-137">Строки планирования можно использовать для добавления такой информации, как данные о необходимых ресурсах, или записи товаров, необходимых для выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-137">You can use planning lines to add information such as what resources are required or to capture what items are needed to perform the job.</span></span> <span data-ttu-id="6e449-138">Например, если имеется задача для получения одобрения работы клиентом, можно связать эту задачу со строками планирования для товаров, такими как встреча с клиентом и назначение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6e449-138">For example, if you have a task to obtain customer approval of a job, you can associate that task with planning lines for items such as meeting with the customer and assigning a resource.</span></span>  

<span data-ttu-id="6e449-139">Строка планирования работы может быть одного из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="6e449-139">A job planning line can have one of the following types.</span></span>  

| <span data-ttu-id="6e449-140">Тип</span><span class="sxs-lookup"><span data-stu-id="6e449-140">Type</span></span> | <span data-ttu-id="6e449-141">Описание</span><span class="sxs-lookup"><span data-stu-id="6e449-141">Description</span></span> |
| --- | --- |
| <span data-ttu-id="6e449-142">**Бюджет**</span><span class="sxs-lookup"><span data-stu-id="6e449-142">**Budget**</span></span> |<span data-ttu-id="6e449-143">Позволяет определить оценочное потребление и затраты на работу, обычно, в случае проекта с оплатой по факту.</span><span class="sxs-lookup"><span data-stu-id="6e449-143">Provides estimated usage and costs for the job, typically in a time and materials type project.</span></span> <span data-ttu-id="6e449-144">На основании строк планирования с таким типом выставить счет нельзя.</span><span class="sxs-lookup"><span data-stu-id="6e449-144">Planning lines of this type cannot be invoiced.</span></span> |
| <span data-ttu-id="6e449-145">**К оплате**</span><span class="sxs-lookup"><span data-stu-id="6e449-145">**Billable**</span></span> |<span data-ttu-id="6e449-146">Позволяет определить оценочный счет для клиента, обычно в случае проекта с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="6e449-146">Provides estimated invoicing to the customer, typically in a fixed price project.</span></span> |
| <span data-ttu-id="6e449-147">**Бюджет и к оплате**</span><span class="sxs-lookup"><span data-stu-id="6e449-147">**Both Budget and Billable**</span></span> |<span data-ttu-id="6e449-148">Позволяет определить бюджетное потребление, равное сумме, на которую выставляется счет.</span><span class="sxs-lookup"><span data-stu-id="6e449-148">Provides budgeted usage equal to what you want to invoice.</span></span> |

<span data-ttu-id="6e449-149">**Примечание**.</span><span class="sxs-lookup"><span data-stu-id="6e449-149">**Note**.</span></span> <span data-ttu-id="6e449-150">После ввода информации в строки планирования работы данные о себестоимости будут подставлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="6e449-150">As you enter information on job planning lines, cost information is automatically filled in.</span></span> <span data-ttu-id="6e449-151">Например, себестоимость, цена и скидка для ресурсов и товаров определяются на основе информации, заданной в карточках ресурсов и товаров.</span><span class="sxs-lookup"><span data-stu-id="6e449-151">For example, the cost, price, and discount for resources and items are initially based on the information that is defined on the resource and item cards.</span></span>

1. <span data-ttu-id="6e449-152">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работы**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6e449-152">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="6e449-153">Откройте соответствующую карточку работы.</span><span class="sxs-lookup"><span data-stu-id="6e449-153">Open a relevant job card.</span></span>
3. <span data-ttu-id="6e449-154">Выберите рабочее задание, для которого поле **Тип рабочего задания** содержит значение **Учет**, затем выберите действие **Строки планирования работ**.</span><span class="sxs-lookup"><span data-stu-id="6e449-154">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="6e449-155">В окне **Строки планирования работ** на новой строке заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="6e449-155">In the **Job Planning Lines** window, on a new line, fill in the fields as necessary.</span></span>
5. <span data-ttu-id="6e449-156">Повторите шаги 3 и 4 для всех строк планирования, которые необходимы для рабочего задания.</span><span class="sxs-lookup"><span data-stu-id="6e449-156">Repeat steps 3 and 4 for all planning lines that you need for the job task.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e449-157">См. также</span><span class="sxs-lookup"><span data-stu-id="6e449-157">See Also</span></span>
[<span data-ttu-id="6e449-158">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="6e449-158">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="6e449-159">Финансы</span><span class="sxs-lookup"><span data-stu-id="6e449-159">Finance</span></span>](finance.md)  
<span data-ttu-id="6e449-160">[Покупки](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="6e449-160">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="6e449-161">[Продажи](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="6e449-161">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="6e449-162">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e449-162">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
