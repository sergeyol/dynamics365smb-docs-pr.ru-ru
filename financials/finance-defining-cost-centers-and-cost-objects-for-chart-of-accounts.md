---
title: "Определение центров затрат и объектов затрат для плана счетов | Документы Майкрософт"
description: "Можно автоматически передавать операции доходов и расходов из главной книги в модуль учета затрат или для каждого учета главной книги или с помощью пакетного задания. При выполнении перемещения система выполняет перемещение только тех записей, которые уже связаны с центром затрат или объектом затрат. Чтобы настроить содержательное перемещение, необходимо обеспечить, чтобы места возникновения затрат и объекты затрат были правильно определены."
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
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="0bb47-105">Определение центров затрат и объектов затрат для плана счетов</span><span class="sxs-lookup"><span data-stu-id="0bb47-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="0bb47-106">Можно автоматически передавать операции доходов и расходов из главной книги в модуль учета затрат или для каждого учета главной книги или с помощью пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="0bb47-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="0bb47-107">При выполнении перемещения [!INCLUDE[d365fin](includes/d365fin_md.md)] выполняет перемещение только тех записей, которые уже связаны с центром затрат или объектом затрат.</span><span class="sxs-lookup"><span data-stu-id="0bb47-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="0bb47-108">Чтобы настроить содержательное перемещение, необходимо обеспечить, чтобы места возникновения затрат и объекты затрат были правильно определены.</span><span class="sxs-lookup"><span data-stu-id="0bb47-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="0bb47-109">Определение значений измерений по умолчанию для счетов главной книги</span><span class="sxs-lookup"><span data-stu-id="0bb47-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="0bb47-110">Для каждого счета главной книги можно определить значения измерений по умолчанию в таблице **Измерение по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="0bb47-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="0bb47-111">В следующем примере представлен способ определения того, чтобы всегда было место возникновения затрат ПОДРАЗДЕЛЕНИЕ, но никогда — место возникновения затрат ПРОЕКТ, при учете на счете главной книги.</span><span class="sxs-lookup"><span data-stu-id="0bb47-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="0bb47-112">**Код измерения**</span><span class="sxs-lookup"><span data-stu-id="0bb47-112">**Dimension Code**</span></span>|<span data-ttu-id="0bb47-113">**Учет значения**</span><span class="sxs-lookup"><span data-stu-id="0bb47-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="0bb47-114">Отдел</span><span class="sxs-lookup"><span data-stu-id="0bb47-114">Department</span></span>|<span data-ttu-id="0bb47-115">Код обязателен</span><span class="sxs-lookup"><span data-stu-id="0bb47-115">Code Mandatory</span></span>|  
|<span data-ttu-id="0bb47-116">Проект</span><span class="sxs-lookup"><span data-stu-id="0bb47-116">Project</span></span>|<span data-ttu-id="0bb47-117">Нет кода</span><span class="sxs-lookup"><span data-stu-id="0bb47-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="0bb47-118">Определение значений измерений для накладных расходов и прямой себестоимости</span><span class="sxs-lookup"><span data-stu-id="0bb47-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="0bb47-119">Можно перенести накладные расходы в место возникновения затрат и прямую себестоимость в объект затрат.</span><span class="sxs-lookup"><span data-stu-id="0bb47-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="0bb47-120">В следующей таблице представлена оптимальная комбинация значений набора измерений.</span><span class="sxs-lookup"><span data-stu-id="0bb47-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="0bb47-121">Переместить в</span><span class="sxs-lookup"><span data-stu-id="0bb47-121">Transfer To</span></span>|<span data-ttu-id="0bb47-122">Учет места возникновения затрат</span><span class="sxs-lookup"><span data-stu-id="0bb47-122">Cost Center Posting</span></span>|<span data-ttu-id="0bb47-123">Учет объектов затрат</span><span class="sxs-lookup"><span data-stu-id="0bb47-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="0bb47-124">Место возникновения затрат</span><span class="sxs-lookup"><span data-stu-id="0bb47-124">Cost Center</span></span>|<span data-ttu-id="0bb47-125">Код обязателен</span><span class="sxs-lookup"><span data-stu-id="0bb47-125">Code Mandatory</span></span>|<span data-ttu-id="0bb47-126">Нет кода</span><span class="sxs-lookup"><span data-stu-id="0bb47-126">No Code</span></span>|  
|<span data-ttu-id="0bb47-127">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="0bb47-127">Cost Object</span></span>|<span data-ttu-id="0bb47-128">Нет кода</span><span class="sxs-lookup"><span data-stu-id="0bb47-128">No Code</span></span>|<span data-ttu-id="0bb47-129">Код обязателен</span><span class="sxs-lookup"><span data-stu-id="0bb47-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="0bb47-130">Чтобы убедиться в том, что предопределенный центр затрат и объект затрат, настраиваемые в главной книге, автоматически перенесены в модуль учета затрат, установите флажок **Проверка разносок ГК** в окне "Настройка учета затрат".</span><span class="sxs-lookup"><span data-stu-id="0bb47-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0bb47-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0bb47-131">See Also</span></span>  
[<span data-ttu-id="0bb47-132">Учет по затратам</span><span class="sxs-lookup"><span data-stu-id="0bb47-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="0bb47-133">[Практическое руководство. Настройка центров затрат](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="0bb47-133">[How to: Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="0bb47-134">Практическое руководство. Настройка объектов затрат</span><span class="sxs-lookup"><span data-stu-id="0bb47-134">How to: Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="0bb47-135">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0bb47-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
