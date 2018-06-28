---
title: "Выдача, печать, отмена и аннулирование платежных документов | Microsoft Docs"
description: "Далее описывается процедура выдачи платежных документов с помощью журнала платежей, печать платежных документов и их аннулирование или просмотр операций книги платежей в Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: ru-ru
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a>Совершение платежей с помощью платежных документов
Можно выпустить электронные платежные документы или создать их вручную в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Оба метода используют журнал платежей для выпуска платежных документов для поставщиков. Также можно аннулировать платежные документы и просмотреть операции с платежными документами.

Приведенная ниже процедура иллюстрирует порядок совершения оплаты поставщику с помощью компьютерных платежных документов путем применения платежа к соответствующему счету поставщика, печати платежного документа и учета платежа как произведенного. В результате создаются положительные операции в книге поставщиков, примененные к отрицательным операциям банковской книги, также физические платежные документы для обработки в банке.

Для оплаты можно использовать два типа платежных документов. Для обоих типов в поле **Тип баланс. счета** или **Тип счета** должно быть указано **Банковский счет**.

- **Компьютерный**. Выберите эту опцию, если хотите, чтобы программа распечатала платежный документ на сумму из этой строки журнала платежей. Платежные документы нужно печатать до учета строк журнала. Выбрать вариант **Компьютерный** можно только при условии, что
- **Ручной**. Выберите эту опцию, если платежный документ создан вручную и нужно создать соответствующую операцию книги платежных документов на эту сумму. При использовании этого варианта распечатать платежный документ нельзя.

> [!NOTE]  
> Чтобы банк выполнил клиринг только проверенных платежных документов и сумм, ему можно отправить файл, содержащий сведения о поставщике, платежном документе и платеже. Дополнительные сведения см. в разделе [Экспорт файла Positive Pay](finance-how-positive-pay.md).

Ваши принтер должен быть соответствующим образом настроен для использования форм платежных документов, и вы должны определить макеты чеков для использования. Дополнительные сведения см. в разделе [Определение макетов платежных документов](finance-how-define-check-layouts.md)

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Оплата счета поставщика с помощью компьютерного платежного документа
Ниже описано, как совершить оплату поставщику с помощью платежного документа. Действия аналогичны возврату денег клиенту с помощью платежного документа.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы платежей**, а затем выберите соответствующую ссылку.
2. Заполните строки журнала платежей. Дополнительные сведения см. в разделе [Регистрация платежей и возвратов](payables-how-post-payments-refunds.md).
3. В поле **Код способа оплаты** выберите **Платежный документ**.
4. В поле **Тип банковского платежа** выберите **Компьютерный**.
5. Выберите действие **Печать платежного документа**.
6. В окне **Платежный документ** заполните поля по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Нажмите кнопку **Отправить**, выберите вариант **Документ PDF** и нажмите кнопку **ОК**.

    Теперь можно передать физические платежные документы в банк на обработку. Дальше нужно учесть платеж как примененный к поставщику, а следовательно, как совершенный в системе.
8. Выберите действие **Учет**.

Будут созданы полностью примененные операции книги поставщиков и операции банковской книги.

> [!NOTE]  
> Если требуется напечатать и оплатить платежные документы в нескольких валютах с различных банковских счетов, необходимо выполнить пакетное задание **Печать платежного документа** отдельно по каждой валюте и указать соответствующий банковский счет.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Отмена напечатанных платежных документов. которые не учтены
Вы можете отменить неучтенные платежные документы после их печати с помощью действия **Аннулировать платеж. документ** в окне **Журнал платежей**.

1. В окне **Журнал платежей** выберите **Аннулировать платеж. документ**, а затем выберите платежные документы для отмены.

## <a name="to-void-checks"></a>Аннулирование платежных документов
Если платеж с помощью платежного документа учтен, аннулировать (отменять) платежные документы можно только в итоговых операциях книги банка.

1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Банковские счета**, а затем выберите соответствующую ссылку.
2. Выберите соответствующий банковский счет, выберите действие **Изменить**, а затем выберите действие **Книга платежных документов**.
3. В окне **Книга платежных документов** выберите действие **Аннулировать платеж. документ**.
4. Установите флажок **Аннулировать только платеж. документ**.
5. Нажмите кнопку **ОК**.

## <a name="to-view-a-summary-of-posted-checks"></a>Просмотр сводки учтенных платежных документов
Если вы хотите просмотреть учтенные платежные документы, например чтобы проверить несколько платежных документов в адрес одного поставщика, можно использовать отчет **Банк. счет - подробности платежей**.
1. Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Банк. счет - подробности платежей**, а затем выберите соответствующую ссылку.
2. Установите необходимые фильтры, а затем нажмите кнопку **Предварительный просмотр**.

## <a name="see-also"></a>См. также
[Осуществление платежей](payables-make-payments.md)  
[Управление кредиторской задолженностью](payables-manage-payables.md)  
[Настройка банковских операций](bank-setup-banking.md)  
[Экспорт файла Positive Pay](finance-how-positive-pay.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
