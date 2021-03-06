---
title: Создание заказа на продажу и продажа продукции | Документация Майкрософт
description: Описывается порядок создания заказа на продажу для записи вашего соглашения с клиентом на продажу продукции или торговлю ею на определенных условиях.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 30976629fbee935ccefb15fafa11e38527eb922c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910634"
---
# <a name="sell-products"></a>Продажа продуктов

Счет продажи или заказ на продажу создаются для записи соглашения с клиентом о продаже определенных товаров на определенных условиях доставки и оплаты.

> [!NOTE]  
> Заказы на продажу используются, если процесс продажи требует, чтобы вы могли отгружать части количества в заказе, например потому, что полное количество недоступно в конкретный момент. Если вы используете счета продажи, то [!INCLUDE [prodshort](includes/prodshort.md)] предполагает, что вы отправляете полное количество при учете счета. Если продажа товаров осуществляется путем непосредственной поставки от поставщика клиенту (прямая поставка), то также необходимо использовать заказы на продажу. Дополнительные сведения см. в разделе [Выполнение прямых поставок](sales-how-drop-shipment.md). Во всех других аспектах заказы на продажу аналогичны счетам продажи. Дополнительные сведения см. в разделе [Выставление счетов продажи](sales-how-invoice-sales.md).

Можно провести переговоры с клиентом, сначала создав предложение по продаже, которое можно преобразовать в заказ на продажу, когда вы договоритесь о продаже. Дополнительные сведения см. в разделе [Создание предложений по продаже](sales-how-make-offers.md).

После подтверждения соглашения клиентом, например после процесса предложения, можно отправить подтверждение заказа, чтобы зафиксировать обязательства по доставке продуктов в соответствии с договоренностью.

При поставке продуктов, полностью или частично, вы учитываете заказы на продажу как отгруженные или как отгруженные и с выставленными счетами для создания соответствующих операций книг товаров и клиентов в своей системе. При учете заказа на продажу вы также можете отправить документ по электронной почте в виде вложения PDF. Тело сообщения электронной почты можно заполнить краткой сводкой информации о заказе и платеже, например включить в него ссылку на PayPal. Дополнительные сведения см. в разделе [Отправка документов по электронной почте](ui-how-send-documents-email.md).

В условиях, где клиент совершает оплату через некоторое время после поставки товара в соответствии с условием оплаты, учтенный счет продажи остается открытым (неоплаченным) до тех пор, пока отдел дебиторской задолженности не проверит, что платеж получен и не применит платеж к учтенному счету продажи. Дополнительные сведения см. в разделе [Выверка платежей с использованием автоматического применения](receivables-how-reconcile-payments-auto-application.md).

В условиях, где клиент совершает оплату немедленно, например с помощью PayPal или наличными, оплата регистрируется сразу же при учете заказа на продажу как заказа, по которому выставлен счет, т. е. учтенный счет продажи закрывается как полностью примененный. Соответствующий способ выбирается в поле **Код способа оплаты** в счете продажи. См. шаг 8. В случае электронных платежей, например с помощью PayPal, необходимо также заполнить поле **Служба платежей**. Дополнительные сведения см. в разделе [Включение платежей клиентов через службу платежей](sales-how-enable-payment-service-extensions.md).

Можно даже создавать заказы с прямой оплатой для незарегистрированных клиентов, сначала настроив карточку клиента, оплачивающего наличными, которая указывается в заказе на продажу. Дополнительные сведения см. в разделе [Настройка клиентов, оплачивающих наличными](finance-how-to-set-up-cash-customers.md).

Вы можете легко исправить или отменить учтенный счет продажи, являющийся результатом заказа на продажу, до его оплаты. Это используется, если нужно исправить опечатку или клиент запрашивает изменение на раннем этапе обработки заказа. Дополнительные сведения см. в разделе [Исправление или отмена неоплаченных счетов продажи](sales-how-correct-cancel-sales-invoice.md). Если учтенный счет продажи оплачен, необходимо создать кредит-ноту продажи для сторнирования продажи. Дополнительные сведения см. в разделе [Обработка возвратов продажи или отмен](sales-how-process-sales-returns-cancellations.md)

Карточка товара может быть типа **Складируемый**, **Сервисный** и **Нескладируемый** и определяет, представляет ли карточка товара физические единицы, единицы измерения времени работы или физические единицы, которые не содержатся в запасах. Дополнительные сведения см. в разделе [Регистрация новых товаров](inventory-how-register-new-items.md). Процедура обработки заказов на продажу такая же для всех трех типов товаров.

Можно заполнить поля клиента в заказе на продажу двумя способами в зависимости от того, зарегистрирован ли уже клиент. См. шаги 2 и 3 в следующей процедуре.

## <a name="to-create-a-sales-order"></a>Создание заказа на продажу
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на продажу**, затем выберите соответствующую ссылку.
2. В поле **Клиент** введите название существующего клиента.

    Остальные поля на странице **Заказ на продажу** заполнятся стандартными сведениями о выбранном клиенте. Если клиент не зарегистрирован, выполните следующие действия.
3. В поле **Клиент** введите название нового клиента.
4. В диалоговом окне регистрации нового клиента нажмите кнопку **Да**.
5. На странице **Выбор шаблона для нового клиента** выберите шаблон для создания новой карточки клиента и нажмите кнопку **ОК**.

    Откроется новая карточка клиента, предварительно заполненная сведениями из выбранного шаблона клиента. Поле **Имя** предварительно заполняется названием нового клиента, введенным в заказ на продажу.
6. Перейдите к заполнению остальных полей в карточке клиента. Дополнительные сведения см. в разделе [Регистрация новых клиентов](sales-how-register-new-customers.md).  
7. Заполнив карточку клиента, нажмите кнопку **ОК**, чтобы вернуться на страницу **Заказ на продажу**.

    Несколько полей в заказе на продажу заполняются сведениями, указанными в новой карточке клиента.
8. Заполните остальные поля на странице **Заказ на продажу** по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Если клиенту разрешается провести оплату немедленно, например с помощью кредитной карты или PayPal, заполните поле **Код способа оплаты**. В этом случае платеж регистрируется, как только вы учтете заказ на продажу как заказ, по которому выставлен счет. Если выбрать вариант НАЛИЧНЫЕ, платеж регистрируется на указанном балансирующем счете.

    Теперь вы готовы к заполнению строк заказа на продажу сведениями о товарах в запасах или услугах, которые вы хотите продать клиенту.

    Если заданы строки типовых продаж для клиента, например ежемесячный заказ пополнения заказов, можно вставить эти строки в заказ выбрав действие **Получить строки типовых продаж**.
9. На экспресс-вкладке **Строки** в поле **Товар** введите номер товара в запасах или услуги.  
10. В поле **Кол-во** укажите количество товаров, которые будут проданы.

    > [!NOTE]  
    >   Количество товаров типа "Услуга" измеряется в единицах времени, например часах, как указано в поле **Код единицы измерения** строки.

    Поле **Сумма строки** обновляется и отображает значение в поле **Цена единицы**, умноженное на значение в поле **Кол-во**.

    Значения цены и суммы строки отображаются с налогом или без него в зависимости от выбранного параметра в поле **Цены с учетом налога** на карточке клиента.
11. В поле **Скидка строки (%)** введите процентное значение, если требуется предоставить клиенту скидку на продукт. Значение в поле **Сумма строки** обновляется соответствующим образом.

    Если настроены специальные цены товара на экспресс-вкладке **Цены продажи и скидки по строкам продаж** в карточке клиента или товара, цена и сумма в строке предложения автоматически обновляются, если выполняются условия согласованных критериев цены. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).
12. Чтобы добавить комментарий о строке предложения, которую клиент может просмотреть в напечатанном предложении по продаже, текст в поле **Описание** нужно записать в пустой строке.  
13. Повторите шаги с 9 по 12 для каждого товара, который требуется продать клиенту.

    Итоги под строками автоматически вычисляются по мере создания или изменения строк.
14. В новой карточке клиента отобразится информация из выбранного шаблона клиента. Заполните остальные поля. Дополнительные сведения см. в разделе [Регистрация новых клиентов](sales-how-register-new-customers.md).  
15. Заполнив карточку клиента, нажмите кнопку **ОК**, чтобы вернуться на страницу **Заказ на продажу**.

    Несколько полей в заказе на продажу заполняются сведениями, указанными в новой карточке клиента.
16. Заполните остальные поля на странице **Заказ на продажу** по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Теперь вы готовы заполнить строки заказа на продажу для продуктов, которые вы продаете клиенту, или для всех транзакций с клиентом, которые необходимо записать на счете ГК.   

    Если заданы строки типовых продаж для клиента, например ежемесячный заказ пополнения заказов, можно вставить эти строки в заказ выбрав действие **Получить строки типовых продаж**.  
17. На экспресс-вкладке **Строки** в поле **Тип** выберите тип продукта, издержки или транзакцию, которая будет учтена для клиента в строке продажи.

18. В поле **Номер** выберите запись для учета согласно значению в поле **Тип**.

    Поле **Номер** пусто в следующих случаях:

    * Если строка предназначена для комментария. Напишите комментарий в поле **Описание**.
    * Если строка предназначена для товара из каталога. Выберите действие **Выбрать товары из каталога**. Дополнительные сведения см. в разделе [Работа с товарами из каталога](inventory-how-work-nonstock-items.md).

19. В поле **Количество** укажите, сколько единиц продукта, издержек или транзакции будет регистрироваться в этой строке для клиента.  

    > [!NOTE]  
    > Если товар принадлежит к типу **Услуга** или поле **Тип** содержит значение **Ресурс**, количество измеряется в единицах времени, например в часах, как указано в поле **Код единицы измерения** строки. Дополнительные сведения см. в разделе [Настройка единиц измерения товара](inventory-how-setup-units-of-measure.md).

    Значение в поле **Сумма строки** рассчитывается как *Цена единицы* х *Количество*.  

    Значения цены и суммы строки отображаются с налогом или без него в зависимости от выбранного параметра в поле **Цены с учетом налога** в карточке клиента.  
20. Если необходимо предоставлять скидку, введите процент в поле **Скидка строки (%)**. Значение в поле **Сумма строки** обновляется соответствующим образом.  

    Если настроены специальные цены товара на экспресс-вкладке **Цены продажи и скидки по строкам продаж** в карточке клиента или товара, цена и сумма в строке продажи автоматически обновляются, если выполняются условия критериев цены. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Повторите шаги с 9 по 12 для каждого продукта или издержки, которые требуется продать клиенту.  

    Поля с итоговыми значениями под строками автоматически обновляются при создании или изменении строк для отображения сумм, которые будут учитываться в бухгалтерских книгах.

    > [!NOTE]
    > В очень редких случаях учтенные суммы могут отличаться от отображаемых в полях итогов. Обычно это происходит из-за округления расчетов в отношении НДС или налога с продаж.<br /><br />Чтобы проверить суммы, которые будут фактически учтены, вы можете использовать страницу **Статистика**, которая учитывает округления расчетов. Кроме того, если вы выбираете действие **Выпустить**, поля итоговых сумм будут обновлены, чтобы включить вычисления округления.  
22. В поле **Сумма скидки по счету** введите сумму, которую нужно вычесть из значения, отображенного в поле **Всего с учетом налога**.

    Если установлены скидки по счету для клиента, то указанное значение процента автоматически вводится в поле **Скидка по счету, %**, если соблюдены условия, а связанная сумма вводится в поле **Сумма скидки по счету без налога**. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).
23. Для отгрузки только части количества заказа введите это количество в поле **Кол-во для отгрузки**. Значение копируется поля **Кол-во для выставления счета**.
24. Для выставления счета только на часть отгружаемого количества введите это количество в поле **Кол-во выставления счета**. Количество должно быть меньше значения в поле **Кол-во для отгрузки**.   
25. Когда строки заказа на продажу готовы, выберите действие **Учесть и отправить**.

В диалоговом окне **Учесть и отправить подтверждение** отобразится предпочтительный способ получения документов клиента. Можно изменить метод отправки, нажав кнопку поиска у поля **Кому отправить документ**. Дополнительные сведения см. в разделе [Настройка профилей отправки документов](sales-how-setup-document-send-profiles.md).

Связанные операции книги товаров и клиентов будут созданы в вашей системе, а заказ на продажу сформирован в виде PDF-документа. Когда заказ продажи будет полностью учтен, он будет удален из списка заказов на продажу и заменен новыми документами в списке учтенных счетов продажи и учтенных расходных накладных продажи.

## <a name="see-also"></a>См. также
[Продажи](sales-manage-sales.md)  
[Настройка продаж](sales-setup-sales.md)  
[Печать сборочного листа](sales-how-print-picking-list.md)  
[Запасы](inventory-manage-inventory.md)  
[Отправка документов по электронной почте](ui-how-send-documents-email.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
