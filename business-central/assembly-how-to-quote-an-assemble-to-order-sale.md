---
title: Практическое руководство. Предложения продажи сборки на заказ | Документация Майкрософт
description: Можно использовать функцию управления сборкой, чтобы настроить сборочный элемент по запросу клиента во время процесса продаж.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3710cb0e9d3ca4c9fb699f535a6cb3b0be68cb78
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924482"
---
# <a name="quote-an-assemble-to-order-sale"></a>Предложения продажи сборки на заказ
Можно использовать функцию управления сборкой, чтобы настроить сборочный элемент по запросу клиента во время процесса продаж. Дополнительные сведения см. в разделе [Продажа товара, собранного на заказ](assembly-how-to-sell-items-assembled-to-order.md).  

Как при продаже любого другого типа товара, можно также создать предложение по продаже для настраиваемого сборочного элемента до его преобразования в заказ на продажу. Этот процесс включает несколько дополнительных этапов при его сравнении с созданием обычного предложения по продаже, и он использует разновидность связанного сборочного заказа, которой является предложение по сборке.

> [!NOTE]  
>  Как и во всех типах предложений, количества в предложениях по сборке не используются в расчетах наличия, планирования или резервирования.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Создание предложения по продаже для товара сборки на заказ  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Предложение по продаже**, затем выберите соответствующую ссылку.  
2.  Создайте строку предложения по продаже с одной строкой для сборочного элемента. Дополнительные сведения см. в разделе [Создание предложений по продаже](sales-how-make-offers.md).  
3.  В поле **Количество для сборки на заказ** введите полное количество.

    > [!NOTE]  
    >  Не следует отправлять предложение по частичному количеству. Поэтому необходимо ввести то же количество, введенное в поле **Кол-во**, в строку предложения по продаже.  

4.  На экспресс-вкладке **Строки** выберите **Строка**, выберите **Сборка на заказ**, а затем выберите **Строки сборки на заказ**. В качестве альтернативы выберите поле **Количество для сборки на заказ** в строке.  
5.  На странице **Строки сборки на заказ** просмотрите или измените строки сборочного заказа в соответствии с предложением по продаже, которое запросил клиент. Если необходимо просмотреть дополнительные сведения, выберите действие **Показать документ**, чтобы открыть полный общий предложенный заказ. Изменить содержимое большинства полей и учесть их невозможно.  
6.  При регулировке строк сборочного заказа в соответствии с предложением закройте окно **Строки сборки на заказ**, чтобы вернуться на страницу **Предложение**.  
7.  Если клиент принимает предложение, создайте заказ на продажу оцененного сборочного элемента. Дополнительные сведения см. в разделе [Создание предложений по продаже](sales-how-make-offers.md). Связанное предложение по сборке и все настройки связаны с новым заказом на продажу для подготовки сборки товара или товаров, которые должны быть проданы.  

## <a name="see-also"></a>См. также  
[Управление сборкой](assembly-assemble-items.md)  
[Работа со спецификациями](inventory-how-work-BOMs.md)  
[Запасы](inventory-manage-inventory.md)  
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
