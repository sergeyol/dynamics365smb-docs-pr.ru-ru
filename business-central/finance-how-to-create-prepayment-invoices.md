---
title: Практическое руководство. Создание счетов на предоплату | Документация Майкрософт
description: Узнайте, как обрабатывать ситуации, в которых вы или ваш поставщик требует предоплату.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 57284dc738ba35c9865bd25f9c180827d4c59c94
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913375"
---
# <a name="create-prepayment-invoices"></a>Создание счетов на предоплату

Если вы требуете, чтобы ваши клиенты отправили платеж до того, как вы отправите им заказ, вы можете использовать функцию предоплаты. То же самое применимо, если ваш поставщик требует, чтобы вы отправили платеж до того, как он отправит вам заказ.  

При создании заказа продажи или покупки можно начать процесс предоплаты. Если у вас есть процент предоплаты по умолчанию для этого клиента или поставщика, он будет автоматически включен в итоговый счет предоплаты. Вы также можете указать процент предоплаты для всего документа.

После создания заказов продажи или покупки можно создать счет на предоплату. Можно использовать процентные значения по умолчанию для каждой строки продажи или покупки, а также можно корректировать сумму по мере необходимости. Например, можно указать общую сумму для всего заказа.  

В следующей процедуре описывается, как выставлять счета на предоплату для заказов на продажу. Действия для заказов на покупку аналогичны.  

## <a name="to-create-a-prepayment-invoice"></a>Процедура создания счета на предоплату

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на продажу**, затем выберите соответствующую ссылку.  
2. Создать новый заказ на продажу для соответствующего клиента. Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).  

    На Экспресс-вкладка **Предоплата**, в поле **Предоплата (%)** указывается процент, используемый для расчета суммы предоплаты. Поле заполняется автоматически, если в карточке клиента указан процент предоплаты по умолчанию. Процент может быть изменено. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Выбрать поле **Сжать предоплату**, если вы хотите создать в счете на предоплату строки, объединяющие строки из заказа на продажу, если:  

    - Они имеют один и тот же счет главной книги для учета предоплаты, что определяется общей настройкой учета.  
    - Они имеют одинаковые измерения.  

    Не выбирайте поле **Сжать предоплату**, если требуется определить счет на предоплату с отдельным строками для каждой строки заказа продажи, которая имеет процент предоплаты.  

    Срок оплаты предоплаты рассчитывается автоматически на основе значения **Код условий предоплаты**.

3. Заполните строки продажи.  

    Если вы указали процент предоплаты по умолчанию для клиента или на экспресс-вкладке **Предоплата** для этого документа, это значение копируется в каждую строку. Можно изменить содержимое поля **Предоплата (%)** в строке.  

4. Для просмотра общей суммы предоплаты выберите действие **Статистика**.

    Если необходимо скорректировать сумму предоплаты для данного заказа, можно изменить содержимое поля **Сумма предоплаты** на странице **Статистика заказов на продажу**.  

    Если выбрано поле **Цены с учетом НДС**, а поле **Сумма предоплаты включая НДС** доступно для редактирования.  

    При изменении значения поля **Сумма предоплаты** данная сумма будет пропорционально распределяться между всеми строками, за исключением тех строк, у которых значение поля **Предоплата (%)** равно **0**.  

5. Чтобы напечатать тестовый отчет перед учетом счета на предоплату, выберите действие **Предоплата**, затем выберите действие **Тестовый отчет о предоплате**.  
6. Чтобы учесть счет на предоплату, выберите действие **Предоплата**, затем выберите действие **Учет счета на предоплату**.  

    Чтобы учесть и распечатать счет на предоплату, выберите действие **Учет и печать счета на предоплату**.  

Для данного заказа можно создать дополнительные счета на предоплату. Для этого необходимо увеличить сумму предоплаты в одной или нескольких строках, скорректировать дату в случае необходимости и учесть счет на предоплату. Новый счет будет создан на сумму разницы между суммами предоплаты, уже включенными в счет, и новой суммой предоплаты.  

> [!NOTE]  
> Если вы расположены в Северной Америке, вы не можете изменить процент предоплаты после учета счета на предоплату. Это запрещено в североамериканской версии [!INCLUDE[d365fin](includes/d365fin_md.md)], поскольку в противном случае расчет налога будет неверным.  

 Когда все готово для учета остатка по счету, его учет выполняется так же, как и учет любого счета, а сумма предоплаты автоматически вычитается из причитающейся суммы.  

## <a name="see-also"></a>См. также

[Выставление счетов на предоплату](finance-invoice-prepayments.md)  
[Пошаговое руководство. Настройка и выставление счетов на продажу](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Финансы](finance.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
