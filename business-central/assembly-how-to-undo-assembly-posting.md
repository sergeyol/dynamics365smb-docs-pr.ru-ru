---
title: Практическое руководство. Отмена учета сборки | Документация Майкрософт
description: Иногда может возникнуть необходимость отменить учтенный сборочный заказ, например в случае учете заказа с ошибками, которые нужно исправить, или потому, что он вообще не должен был быть учтен, и его нужно откатить.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9d483d104b0dee148dfc4a15bea6737d505730cc
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913867"
---
# <a name="undo-assembly-posting"></a>Отмена учета сборки
Иногда может возникнуть необходимость отменить учтенный сборочный заказ, например в случае учете заказа с ошибками, которые нужно исправить, или потому, что он вообще не должен был быть учтен, и его нужно откатить.

При отмене учтенного сборочного заказа комплект корректирующих операций книги товаров создается для сторнирования исходных операций. Каждая положительная операция выхода для сборочного элемента сторнируется отрицательной операцией выхода. Каждая отрицательная операция потребления для сборочного компонента сторнируется положительной операцией потребления. Приложение постоянных затрат создается автоматически между корректирующими и исходными операциями для обеспечения точного возврата себестоимости.  

При отмене полностью учтенного сборочного заказа можно выбрать, требуется ли воссоздать исходное состояние сборочного заказа, например для корректировки перед повторным учетом. Кроме того, можно вообще не воссоздавать сборочный заказ.  

При отмене частично учтенного сборочного заказа все поля количества, такие как **Собранное кол-во**, **Потребленное кол-во** и **Остаток** восстанавливают значения, которые они имели до соответствующего учета.  

Чтобы повторно создать или восстановить сборочные заказы, следующие условия должны применяться к сборочному элементу, выпущенному при первоначальном учете:  

-   Он должен быть еще в наличии на складе, то есть не продан и не потреблен другим способом в исходящих транзакциях.  
-   Это не должно быть зарезервировано.  
-   Это должно существовать в ячейке, в которую выводятся данные.  

Кроме того, существующие сборочные заказы можно восстановить, если число строк и последовательность строк в исходном сборочном заказе не менялись.  

> [!TIP]  
>  Чтобы разрешить конфликты из-за изменения строк, можно вручную отменить изменения в строках под вопросом перед отменой связанного разнесенного сборочного заказа. В качестве альтернативы можно учесть сборочный заказ полностью, а затем выбрать повторное его создание в ходе отмены учета.  

Далее описывается процедура отмены учтенных сборочных заказов, где товары были собраны на склад. Если требуется отменить разнесенные сборочные заказы, в которых были отгружены товары, собранные в заказ на продажу, следует использовать функцию **Отменить расх. накладную** в разнесенной расходной накладной, которая относится к учтенному сборочному заказу. Дополнительные сведения см. в разделе [Сторнирование учета в журнале и отмена приходных/расходных накладных](finance-how-reverse-journal-posting.md). Отмена учтенного сборочного заказа затем выполняется автоматически таким же образом, как описано в этом разделе.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Отмена учета сборочного заказа  
1.  Чтобы отменить полностью или частично разнесенный сборочный заказ, выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Разнесенные заказы на сборку** и выберите связанную ссылку.  

    Открывается страница **Разнесенные сборочные заказы**, где показаны один или более учтенных сборочных заказов, которые учитываются из рассматриваемого сборочного заказа. Каждый частичный учет создает отдельно учитываемый сборочный заказ.  
2.  Откройте учтенный сборочный заказ, который нужно отменить, а затем выберите действие **Отменить сборку**.  

    Если учтенный сборочный заказ, который необходимо отменить, связан с полностью учтенным сборочным заказом, который сейчас удален, есть возможность повторно создать его, обычно потому что необходимо его еще раз обработать.  
3.  Если необходимо повторно создать сборочный заказ, то нажмите кнопку **Да**. Чтобы отменить учет без восстановления связанного сборочного заказа, нажмите кнопку **Нет**.  

Поле **Сторнировано** в заголовке сборочного заказа изменяется на **Да**. Теперь учет сборочного заказа сторнируется, и можно перейти к обработке всего сборочного заказа, если требуется повторно создать его или открытый сборочный заказ, исходное состояние которого было восстановлено.  

> [!NOTE]  
>  Для восстановления значений количества из нескольких частичных операций учета в сборочном заказе, необходимо отменить все разнесенные сборочные заказы под вопросом, выполнив указанные выше действия с 1 по 3 для каждого разнесенного сборочного заказа.  

## <a name="see-also"></a>См. также  
[Управление сборкой](assembly-assemble-items.md)  
[Сторнирование учета в журнале и отмена приходных/расходных накладных](finance-how-reverse-journal-posting.md)  
[Обработка возвратов продажи или отмен](sales-how-process-sales-returns-cancellations.md)    
[Работа со спецификациями](inventory-how-work-BOMs.md)  
[Запасы](inventory-manage-inventory.md)  
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
