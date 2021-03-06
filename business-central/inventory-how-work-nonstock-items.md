---
title: Создание и управление товарами из каталога | Документация Майкрософт
description: Далее описывается процедура торговли товарами, которые находятся в списке поставщиков товаров, но не в вашем списке товаров.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7d9950d550f614ba7cc0e422d919d9f8e8bf8390
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921800"
---
# <a name="work-with-catalog-items"></a>Работа с товарами из каталога
Для удобства клиентов можно предлагать им некоторые товары, которые вы не хотите обрабатывать в своей системе до начала торговли ими. Когда вы решите начать управлять такими товарами в своей системе, можно будет преобразовать их в обычные карточки товаров одним из двух способов.

* Из карточки товара из каталога создайте новую карточку товара на основе шаблона.
* Из строки заказа на продажу с типом **Товар** с пустым полем **Номер** выберите товар из каталога. Карточка товара затем будет автоматически создана для товара из каталога.

> [!NOTE]  
> Невозможно выбрать товар из каталога на странице **Счет продажи**.<br /><br />
> Можно выбрать товар из каталога на странице **Предложение по продаже**, но товар из каталога не будет преобразован в обычный товар при использовании функции **Создать заказ**.

Товар из каталога обычно содержит номер товара поставщика, который поставляет его. Чтобы включить преобразование карточки товара из каталога в карточку обычного товара, следует сначала настроить преобразование нумерации товаров поставщика в вашу собственную нумерацию товаров.   

> [!Important]
> Товары из каталога не следует путать с нескладируемыми товарами, являющимися обычными товарами, которым присвоен тип **Нескладируемый**, чтобы они, например, не участвовали в расчетах наличия и себестоимости, так как они предназначены только для внутреннего использования и имеют низкую себестоимость. Дополнительные сведения см. в разделе [О типах товаров](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Создание товара из каталога
Карточки товара из каталога содержат намного меньше информации, чем карточки обычного товара, так как они используются только в предложениях с ценами и другим образом. По этой причине их необходимо преобразовать в карточки обычного товара, прежде чем можно будет учитывать для них транзакции продажи.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Товары из каталога**, затем выберите соответствующую ссылку.
2. Выберите действие **Создать**.
3. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Настройка порядка преобразования номеров товара из каталога в вашу собственную нумерацию
Чтобы включить преобразование карточки товара из каталога в карточку обычного товара, следует сначала настроить преобразование нумерации товаров поставщика в ваш собственный формат нумерации товаров.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка товара из каталога**, затем выберите соответствующую ссылку.
2. Заполните соответствующим образом поля.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Преобразование товара из каталога в обычный товар
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Товары из каталога**, затем выберите соответствующую ссылку.
2. Откройте карточку товара из каталога, который требуется преобразовать в обычный товар.
3. На странице **Карточка товара из каталога** выберите действие **Создать товар**.

Создается новая карточка товара с уже внесенной информацией из товара из каталога и соответствующего шаблона товара. Затем можно заполнить или отредактировать поля в новой карточке товара, как требуется. Дополнительные сведения см. в разделе [Регистрация новых товаров](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Продажа товара из каталога и его преобразование в обычный товар
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на продажу**, затем выберите соответствующую ссылку.
2. Выберите действие **Создать**. Заполните поля на экспресс-вкладке **Общее**, как и для любого другого заказа на продажу. Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).
3. В новой строке продажи в поле **Тип** выберите **Товар**, но оставьте поле **Номер** незаполненным.
4. Выберите действие **Строк**, а затем выберите действие **Выбрать товары из каталога**.

    Товар из каталога преобразуется в обычный товар. Создается новая карточка товара с уже внесенной информацией из товара из каталога и соответствующего шаблона товара.
5. На странице **Товары из каталога** выберите товар из каталога, который требуется продать, затем нажмите кнопку **ОК**.
6. Когда заказ на продажу будет готов, выберите действие **Учет**.

Затем можно заполнить или отредактировать поля в новой карточке товара, как требуется. Дополнительные сведения см. в разделе [Регистрация новых товаров](inventory-how-register-new-items.md).

> [!NOTE]  
>   Для поставщика товара автоматически создается запись перекрестной ссылки между номером товара у поставщика и вашим новым номером товара. Дополнительные сведения см. в разделе [Использование перекрестных ссылок по товару](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>См. также
[Регистрация новых товаров](inventory-how-register-new-items.md)  
[Создание специальных заказов](sales-how-to-create-special-orders.md)|  
[Запасы](inventory-manage-inventory.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
