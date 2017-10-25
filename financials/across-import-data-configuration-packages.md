---
title: "Использование Excel для импорта данных в Financials | Документы Майкрософт"
description: "Используйте пакет конфигурации по умолчанию для добавления данных в Excel и импорта данных обратно в Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="c2d1a-103">Импорт данных из устаревшего ПО учета с использованием пакета конфигурации</span><span class="sxs-lookup"><span data-stu-id="c2d1a-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="c2d1a-104">Можно импортировать основные данные и некоторые транзакционные данные из других финансовых систем на основе пакета конфигурации по умолчанию в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2d1a-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c2d1a-105">В окне **Пакеты конфигураций** можно использовать пакет для импорта и проверки данных перед применением пакета.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="c2d1a-106">Если вам знакомы службы RapidStart для Microsoft Dynamics, вам также знакомы пакеты конфигураций.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="c2d1a-107">Пакет конфигурации по умолчанию поддерживает наиболее распространенные типы данных, которые требуется импортировать из устаревшей системы.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="c2d1a-108">Затем в Excel можно добавить данные устаревшей системы и настроить их согласно бизнес-логике [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2d1a-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="c2d1a-109">Кроме того, можно использовать мастеры миграции данных для импорта данных из QuickBooks или Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="c2d1a-110">Дополнительные сведения см. в разделе [Миграция данных QuickBooks](ui-extensions-quickbooks-data-migration.md) или [Миграция данных Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="c2d1a-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="c2d1a-111">Работа с данными в Excel</span><span class="sxs-lookup"><span data-stu-id="c2d1a-111">Working with Data in Excel</span></span>
<span data-ttu-id="c2d1a-112">При экспорте пакета конфигурации по умолчанию в Excel созданная книга содержит лист для каждой таблицы в пакете.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="c2d1a-113">Чтобы упростить задачи, можно воспользоваться преимуществами инструментов управления XML, которые встроены в Excel.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="c2d1a-114">Также можно воспользоваться встроенными функциями Excel, чтобы помочь с форматом данных и поместить данные в правильную ячейку.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="c2d1a-115">Например, добавьте пустой лист и скопируйте в него устаревшие данные.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="c2d1a-116">Затем создайте формулу Excel для сопоставления данных в листе преобразования между полями в экспортированном листе и устаревшими данными клиента.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="c2d1a-117">После сопоставления всех данных скопируйте диапазон данных в табличный журнал.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c2d1a-118">Не изменяйте столбцы в журналах.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="c2d1a-119">Если они перемещаются, изменяются или удаляются, то импортировать лист в [!INCLUDE[d365fin](includes/d365fin_md.md)] невозможно.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="c2d1a-120">Таблицы в пакете конфигурации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c2d1a-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="c2d1a-121">Пакет конфигурации по умолчанию поддерживает следующие таблицы:</span><span class="sxs-lookup"><span data-stu-id="c2d1a-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="c2d1a-122">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="c2d1a-122">Payment Terms</span></span>
-   <span data-ttu-id="c2d1a-123">Ценовая группа клиента</span><span class="sxs-lookup"><span data-stu-id="c2d1a-123">Customer Price Group</span></span>
-   <span data-ttu-id="c2d1a-124">Метод поставки</span><span class="sxs-lookup"><span data-stu-id="c2d1a-124">Shipment Method</span></span>
-   <span data-ttu-id="c2d1a-125">Менеджер по продажам/закупкам</span><span class="sxs-lookup"><span data-stu-id="c2d1a-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="c2d1a-126">Склады</span><span class="sxs-lookup"><span data-stu-id="c2d1a-126">Location</span></span>
-   <span data-ttu-id="c2d1a-127">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="c2d1a-127">GL Account</span></span>
-   <span data-ttu-id="c2d1a-128">Клиент</span><span class="sxs-lookup"><span data-stu-id="c2d1a-128">Customer</span></span>
-   <span data-ttu-id="c2d1a-129">Поставщик</span><span class="sxs-lookup"><span data-stu-id="c2d1a-129">Vendor</span></span>
-   <span data-ttu-id="c2d1a-130">Пункт меню</span><span class="sxs-lookup"><span data-stu-id="c2d1a-130">Item</span></span>
-   <span data-ttu-id="c2d1a-131">Заголовок продажи</span><span class="sxs-lookup"><span data-stu-id="c2d1a-131">Sales Header</span></span>
-   <span data-ttu-id="c2d1a-132">Строка продажи</span><span class="sxs-lookup"><span data-stu-id="c2d1a-132">Sales Line</span></span>
-   <span data-ttu-id="c2d1a-133">Заголовок покупки</span><span class="sxs-lookup"><span data-stu-id="c2d1a-133">Purchase Header</span></span>
-   <span data-ttu-id="c2d1a-134">Строка покупки</span><span class="sxs-lookup"><span data-stu-id="c2d1a-134">Purchase Line</span></span>
-   <span data-ttu-id="c2d1a-135">Строка финансового журнала</span><span class="sxs-lookup"><span data-stu-id="c2d1a-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="c2d1a-136">Строка журнала товаров</span><span class="sxs-lookup"><span data-stu-id="c2d1a-136">Item Journal Line</span></span>
-   <span data-ttu-id="c2d1a-137">Учетная группа клиента</span><span class="sxs-lookup"><span data-stu-id="c2d1a-137">Customer Posting Group</span></span>
-   <span data-ttu-id="c2d1a-138">Учетная группа поставщика</span><span class="sxs-lookup"><span data-stu-id="c2d1a-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="c2d1a-139">Учетная группа товаров</span><span class="sxs-lookup"><span data-stu-id="c2d1a-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="c2d1a-140">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="c2d1a-140">Unit of Measure</span></span>
-   <span data-ttu-id="c2d1a-141">Общая бизнес-группа</span><span class="sxs-lookup"><span data-stu-id="c2d1a-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="c2d1a-142">Общая товарная группа</span><span class="sxs-lookup"><span data-stu-id="c2d1a-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="c2d1a-143">Общая настройка учета</span><span class="sxs-lookup"><span data-stu-id="c2d1a-143">General Posting Setup</span></span>
-   <span data-ttu-id="c2d1a-144">Территория</span><span class="sxs-lookup"><span data-stu-id="c2d1a-144">Territory</span></span>
-   <span data-ttu-id="c2d1a-145">Категория товара</span><span class="sxs-lookup"><span data-stu-id="c2d1a-145">Item Category</span></span>
-   <span data-ttu-id="c2d1a-146">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="c2d1a-146">Sales Price</span></span>
-   <span data-ttu-id="c2d1a-147">Цена покупки</span><span class="sxs-lookup"><span data-stu-id="c2d1a-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="c2d1a-148">Импорт данных клиента</span><span class="sxs-lookup"><span data-stu-id="c2d1a-148">Importing Customer Data</span></span>
<span data-ttu-id="c2d1a-149">После ввода данных клиента в Excel вам следует импортировать данные в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2d1a-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c2d1a-150">В окне **Пакеты конфигураций** импортируйте данные из файлов Excel и проверьте соответствие данных с [!INCLUDE[d365fin](includes/d365fin_md.md)] перед применением пакета.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d1a-151">См. также</span><span class="sxs-lookup"><span data-stu-id="c2d1a-151">See Also</span></span>
[<span data-ttu-id="c2d1a-152">Импорт бизнес-данных из других финансовых систем</span><span class="sxs-lookup"><span data-stu-id="c2d1a-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="c2d1a-153">Миграция данных QuickBooks</span><span class="sxs-lookup"><span data-stu-id="c2d1a-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="c2d1a-154">Миграция данных Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="c2d1a-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
