---
title: "Использование расширения для миграции данных QuickBooks | Документы Майкрософт"
description: "Описывает, как использовать расширение для импорта клиентов, поставщиков, товаров и счетов из QuickBooks Desktop в Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="d449f-103">Расширение для миграции данных QuickBooks для Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="d449f-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="d449f-104">Это расширение облегчает миграцию клиентов, поставщиков, товаров и счетов из QuickBooks Desktop в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d449f-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks Desktop to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d449f-105">Если сейчас ваша компания использует QuickBooks, вы можете экспортировать требуемую информацию, а затем открыть руководство по сопровождаемой настройке, чтобы загрузить данные в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d449f-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="d449f-106">Дополнительные сведения см. в разделе [Импорт бизнес-данных из других финансовых систем](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="d449f-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="d449f-107">Экспорт данных из QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="d449f-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="d449f-108">Вы должны были экспортировать часть или всех ваших существующих клиентов, поставщиков, складские товары и счета в файл Intuit Interchange Format (IIF).</span><span class="sxs-lookup"><span data-stu-id="d449f-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="d449f-109">Расширение для миграции данных QuickBooks содержит сопоставление данных QuickBooks по умолчанию, чтобы вы могли использовать собственные данные для тестирования новой организации [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d449f-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="d449f-110">Сопоставления по умолчанию будет в большинстве случаев достаточно, но можно изменить его с помощью руководства по настройке.</span><span class="sxs-lookup"><span data-stu-id="d449f-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="d449f-111">В QuickBooks в меню "Файл" есть служебная программа для экспорта списков.</span><span class="sxs-lookup"><span data-stu-id="d449f-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="d449f-112">Для целей [!INCLUDE[d365fin](includes/d365fin_md.md)] можно экспортировать следующие списки:</span><span class="sxs-lookup"><span data-stu-id="d449f-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="d449f-113">Список клиентов</span><span class="sxs-lookup"><span data-stu-id="d449f-113">Customer List</span></span>  
* <span data-ttu-id="d449f-114">Список поставщиков</span><span class="sxs-lookup"><span data-stu-id="d449f-114">Vendor List</span></span>  
* <span data-ttu-id="d449f-115">Список товаров</span><span class="sxs-lookup"><span data-stu-id="d449f-115">Item List</span></span>  
* <span data-ttu-id="d449f-116">Список счетов</span><span class="sxs-lookup"><span data-stu-id="d449f-116">Account List</span></span>  

<span data-ttu-id="d449f-117">Экспортируемые данные сохраняются в виде файла IIF, который затем можно загрузить в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d449f-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="d449f-118">Поиск расширения для миграции данных QuickBooks</span><span class="sxs-lookup"><span data-stu-id="d449f-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="d449f-119">Расширение миграции данных QuickBooks установлено и готово к работе как составная часть мастер настройки миграции данных.</span><span class="sxs-lookup"><span data-stu-id="d449f-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="d449f-120">Если вы готовы начать прямо сейчас и уже экспортировали свои данные из QuickBooks, выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Мастер настройки**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="d449f-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="d449f-121">Выберите **Миграция бизнес-данных**, затем выполните шаги в руководстве.</span><span class="sxs-lookup"><span data-stu-id="d449f-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d449f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d449f-122">See Also</span></span>
[<span data-ttu-id="d449f-123">Импорт бизнес-данных из других финансовых систем</span><span class="sxs-lookup"><span data-stu-id="d449f-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d449f-124">[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d449f-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
