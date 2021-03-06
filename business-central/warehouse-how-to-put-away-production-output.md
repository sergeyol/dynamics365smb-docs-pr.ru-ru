---
title: Как размещать выпуск продукции | Документация Майкрософт
description: Каким образом выполняется размещение выпущенной продукции, зависит от того, как настроен склад.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 59830cc2e9b90f9ee6c6fd61cb9715ce60208ad1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923199"
---
# <a name="put-away-production-or-assembly-output"></a>Размещение выпуска производства или сборки
Каким образом выполняется размещение выпущенной продукции, зависит от того, как настроен склад. Дополнительные сведения см. в разделе [Настройка управления складом](warehouse-setup-warehouse.md).  

В базовых конфигурациях склада, в которых склад настроен так, что требуется обработка размещения, но не требуется обработка приемки, то для организации и регистрации размещения выпущенной продукции используется документ **Размещение запасов**.  

В расширенных конфигурациях склада, в которых для склада требуется обработка и размещения, и приемки, для размещения выпущенной продукции можно создать либо документ внутреннего размещения, либо документ передвижения.  

Первым шагом при создании размещения выпущенной продукции является создание входящего складского запроса. Этот запрос уведомляет склад, что выход производственного заказа или заказа на сборку готов для размещения.

## <a name="to-create-the-inbound-warehouse-request"></a>Создание входящего запроса склада  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Запущенный производственный заказ**, затем выберите соответствующую ссылку.  
2.  В производственном заказе, готовом к размещению, выберите действие **Создать входящий складской запрос**.  

> [!NOTE]  
>  Можно также создать входящий запрос склада, если установить флажок **Создать входящий запрос** при обновлении производственного заказа. Дополнительные сведения см. в разделе [Обновление или перепланирование производственных заказов](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Размещение продукции выхода с помощью складского размещения  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Размещение запасов**, затем выберите соответствующую ссылку.  
2.  Создать новое размещение запасов. Дополнительную информацию см. в разделе [Размещение товаров с помощью функции товарного размещения](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Чтобы получить доступ к выходу производственного заказа, выберите действие **Получить исходные документы**, затем выберите запущенный производственный заказ.  
4.  Заполните строки размещения надлежащим образом.
5.  Когда строки будут готовы для учета, выберите действие **Учет**. Во время процедуры учета будут созданы необходимые складские операции и будет учтен выход товаров.  

Можно также создать **Размещение запасов** непосредственно из запущенного производственного заказа. Дополнительную информацию см. в разделе [Размещение товаров с помощью функции товарного размещения](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

При учете размещения запасов предполагается, что все операции учитываются в соответствии со стандартной процедурой, т. е. количество выхода продукции учитывается в соответствии с последней операцией. Журнал выхода продукции можно использовать для учета отклонений в количестве выхода продукции, а также времени настройки и выполнения. Если требуется выполнить частичный учет после создания размещения запасов, это можно сделать в ходе настройки времени и количества для всех операций, кроме последней. В этом случае последняя операция контролируется функцией размещения запасов.  

Если необходимо только учесть время настройки или выполнения в последней операции, установите в последней операции количество выхода продукции равным 0. Кроме того, можно вообще не выполнять учет последней строки, просто удалив ее.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Размещение продукции выхода с помощью внутреннего складского размещения
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Внутреннее складское размещение**, затем выберите соответствующую ссылку.  
2. Выберите действие **Создать**.
3. В заголовке нового внутреннего размещения, как минимум, заполните поле **Код склада**.  
4. Заполните строку для каждого подлежащего передвижению на складе товара. Следует только заполнить поля **Код товара** и **Кол-во**.  

    > [!NOTE]  
    >  При выборе поля **Код товара** откроется **Список содержимого ячейки**, а не **Список товаров**. Это вызвано тем, что необходимо отложить товар, находящийся в определенной ячейке - "Содержимое ячейки", а не просто товар, и вам уже известно, из какой ячейки необходимо взять товар.  

4.  Чтобы в строки журнала ввести содержимое всех ячеек склада или содержимое ячеек, удовлетворяющее условиям фильтра, выберите действие **Получить содержимое ячейки**.  
5.  Выберите действие **Создать размещение**, и подлежащие передвижению с производства товары теперь включены в инструкцию по размещению и ожидают принятия на хранение на склад.  

> [!NOTE]  
>  Если склад настроен на использование расширенного подбора и размещения, он будет связан с производственным оборудованием с помощью производственных ячеек по умолчанию: ячеек входящей и исходящей продукции и ячейки сборочного цеха, все они задаются на экспресс-вкладке **Ячейки** карточки склада. При учете продукции, выпущенной в соответствии с производственным заказом, выпущенная продукция помещается в поле **Ячейка исходящей продукции**. Чтобы разместить выход продукции, необходимо выполнить процедуру, описанную выше, но вместо использования стандартной ячейки товара следует переместить или разместить товары из **Ячейки исходящей продукции** в стандартную ячейку товара.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Определение вручную ячейки для хранения выпущенной из производства продукции  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал перемещения**, затем выберите соответствующую ссылку.  
2.  Заполните заголовок и создайте строку для каждого товара, подлежащего передвижению на складе.  
3.  Заполните поля **Из кода ячейки** и **В код ячейки** и введите количество в поле **Кол-во**.  
4.  Чтобы в строки журнала ввести содержимое всех ячеек склада или содержимое ячеек, удовлетворяющее условиям фильтра, выберите действие **Получить содержимое ячейки**.  
5. Выберите действие **Создать передвижение**. Инструкции по складскому перемещению создаются со строками "Взять" и "Поместить" для работников склада.  

> [!NOTE]  
>  Номер документа-источника, например номер производственного заказа, нельзя ввести в документы внутреннего размещения, размещения или перемещения.  

## <a name="see-also"></a>См. также  
[Управление складом](warehouse-manage-warehouse.md)  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
