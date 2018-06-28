---
title: "Связывание заказа на продажу с заказом на покупку для прямой поставки | Документы Майкрософт"
description: "Рассматривается создание заказа на покупку, связанного с заказом на продажу, для обеспечения прямой поставки от поставщика клиенту."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4840cde44374f17dcbd2befb167bfdf6110fe6fe
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="make-drop-shipments"></a>Выполнение прямых поставок
Прямая поставка — это поставка товаров одним из ваших поставщиков непосредственно одному из ваших клиентов.

Когда заказ на продажу отмечен для прямой поставки и вы создаете заказ на покупку, указав клиента в поле **Код клиента (покупателя)**, можно связать эти два документа, дав таким образом поставщику инструкцию для поставки непосредственно в адрес клиента.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Создание заказа на продажу по прямой поставке
Для подготовки прямой поставки следует создать заказы на продажу для товара, как обычно, но необходимо указать в строке продажи, что продажа требует прямой поставки.

1. Создайте заказ на продажу для товара. Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).
2. В строке заказа на продажу для прямой поставки установите флажок **Прямая поставка**. Используйте функцию **Выбрать столбцы**, если поле не отображается. Дополнительные сведения см. в разделе [Персонализация рабочей области](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Создание заказа на покупку для прямой поставки
Для подготовки прямой поставки для продаваемого товара следует создать обычный заказ на покупку, но необходимо указать в заказе на покупку, что он должен быть доставлен клиенту, а не вам.

1. Создайте заказ покупки. Не заполняйте никакие поля в строках. Дополнительные сведения см. в разделе [Регистрация покупок](purchasing-how-record-purchases.md).
2. В поле **Код клиента (покупателя)** выберите клиента, которому осуществляется продажа.
3. Выберите действие **Прямые поставки**, затем выберите действие **Получить заказ на продажу**.
4. В окне **Список продаж** выберите заказ на продажу, который был подготовлен в разделе "Создание заказа на продажу по прямой поставке".
5. Нажмите кнопку **ОК**.

Информация строки в заказе на продажу будет вставлена в строки заказа на покупку.

Теперь можно проинструктировать поставщика, чтобы он отгрузил товары клиенту, например, переслав заказ на покупку в виде файла PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Просмотр связанного заказа на покупку из заказа на продажу
* Выберите строку заказа на продажу с прямой поставкой, выберите действие **Заказ**, выберите действие **Прямая поставка**, затем выберите действие **Заказ на покупку**.

## <a name="to-post-a-drop-shipment"></a>Учет прямой поставки
После отгрузки товаров поставщиком можно учесть заказ на продажу как отгруженный. Можно также учесть заказ на покупку, но только с параметром **Получить**, пока не будет выставлен счет по заказу на продажу.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.
2. Откройте заказ на продажу, созданный в разделе "Создание заказа на продажу по прямой поставке".
3. В поле **Кол-во для отгрузки** укажите, какое количество из заказа следует доставить, полное или частичное количество по заказу.
4. Выберите действие **Учесть** или **Учесть и отправить**.
5. Выберите вариант **Отгрузить** (чтобы счет был выставлен позже) или вариант **Отгрузить и выставить счет** (чтобы счет был выставлен незамедлительно).

## <a name="see-also"></a>См. также
[Создание специальных заказов](sales-how-to-create-special-orders.md)|  
[Продажа продуктов](sales-how-sell-products.md)  
[Регистрация покупок](purchasing-how-record-purchases.md)  
[Продажи](sales-manage-sales.md)  
[Наличие](inventory-manage-inventory.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
