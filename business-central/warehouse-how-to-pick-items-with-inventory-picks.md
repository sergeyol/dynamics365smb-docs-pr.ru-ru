---
title: "Как подбирать товары с помощью подбора запасов | Документы Майкрософт"
description: "Если настройки склада требуют обработку подбора, а не обработку отгрузки, то для регистрации и учета информации о подборе и отгрузке для документов-источников следует использовать документы подбора запасов."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8d7fe65a719c7337e0c72435b4ee157c829f7f78
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="pick-items-with-inventory-picks"></a>Подбор товаров с помощью подбора запасов
Если настройки склада требуют обработку подбора, а не обработку отгрузки, то для регистрации и учета информации о подборе и отгрузке для документов-источников следует использовать окно **Подбор запасов**. Исходящий документ-источник может быть заказом продажи, возвратом покупки, исходящим заказом перемещения или производственным заказом, компоненты которого готовы для подбора.

> [!NOTE]  
> Компоненты для сборочных заказов нельзя выбрать или учесть со складскими подборами. Вместо этого используйте окно **Перемещение запасов**. Дополнительные сведения см. в разделе [Перемещение компонентов в производственную зону на основном складе](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

>  При подборе и отгрузке количеств строк продаж, которые собраны для заказа, вы должны следовать определенным правилам при создании строк подбора запасов. Дополнительные сведения см. в разделе "Обработка сборок на заказ в подборах запасов".  

Складской подбор можно создать тремя способами:  

- Создайте подбор в два шага, сначала запросив складской подбор посредством выпуска документа-источника. Это сообщает складу, что документ-основание готов и его можно забирать. После этого складской подбор можно создавать в окне **Подбор запасов** на основании документа-источника.  
- Создание складского подбора непосредственно из самого документа-источника.  
- С помощью пакетного задания можно создавать складские подборы одновременно для нескольких документов-источников.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Запрос складского подбора путем выпуска документа-источника  
В случае заказов на продажу, возвратов покупок и исходящих заказов на перемещение складской запрос создается путем выпуска заказа. Ниже описано, как это делать из заказа на продажу.

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.
2. Выберите заказ на продажу, который требуется выпустить, затем выберите действие **Выпустить**.

Для производственных заказов запрос склада для подбора компонентов, называемый *списанием*, создается автоматически при изменении статуса производственного заказа на **Выпущено** или при создании запущенного производственного заказа. Дополнительные сведения см. в разделе [Подбор для производства или сборки](warehouse-how-to-pick-for-production.md).

После того как складской запрос создан, работник склада, которому поручено создавать подборы, может видеть, что документ-источник готов для выполнения подбора, и может создавать новый документ подбора на основе складского запроса.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Создание складского подбора на основе документа-источника
Теперь, если запрос создан, работник склада может создать новый складской подбор на основании выпущенного документа-источника.
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Товарные подборы**, а затем выберите связанную ссылку.  
2.  Выберите действие **Создать**.  
3. В поле **Документ-источник** выберите тип документа-источника, для которого выполняется подбор.  
4. В поле **Номер источника** выберите документ.  
5. В качестве альтернативы выберите действие **Получить источник документа**, чтобы выбрать документ из списка исходящих документов-источников, готовых к подбору на складе.  
6. Нажмите кнопку **ОК**, чтобы заполнить строки подбора в соответствии с выбранными документом-источником.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Создание документа складского подбора из документа-источника  
1.  В документе-источнике, который может быть заказом на продажу, возвратом покупки, исходящим заказом на перемещение или производственным заказом, выберите действие **Создать размещение/подбор запасов**.
2.  Установите флажок **Создать товарный подбор**.  
3.  Нажмите кнопку **ОК**. Будет создан новый подбор запасов.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Создание нескольких складских подборов с помощью пакетного задания  
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Создать товарное размещение/подбор**, затем выберите связанную ссылку.  
2.  На экспресс-вкладке **Запрос склада** с помощью полей **Документ-источник** и **Номер источника** отфильтруйте данные по определенному типу документов или диапазонам номеров документов. Например, можно создать подборы только для заказов на продажу.  
3. На экспресс-вкладке **Параметры** установите флажок **Создать подбор запасов**.
4. Нажмите кнопку **ОК**. Создаются указанные подборы запасов.

> [!NOTE]  
>  При подборе и отгрузке количеств строк продаж, которые собраны для заказа, вы должны следовать определенным правилам при создании строк подбора запасов. Дополнительные сведения см. в разделе "Обработка сборок на заказ в подборах запасов".  
>   
>  В рамках базовых конфигураций склада товары, собранные для заказов на продажу, скомплектованы из связанных заказов на продажу, как описано в этом разделе. Дополнительные сведения см. в разделе "Обработка сборок на заказ в подборах запасов" в статье "Подбор запасов".  

## <a name="to-record-the-inventory-picks"></a>Регистрация подборок запасов  
1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Подбор запасов**, а затем выберите связанную ссылку.  
2. В поле **Код ячейки** в строках подбора, ячейка, из которой требуется скомплектовать товары, предлагается в соответствии с ячейкой товара по умолчанию. При необходимости данную ячейку можно изменить в этом окне.  
3. Произведите подбор и введите в поле **Кол-во для обработки** информацию о реальном количестве размещенного товара.

    Если товары для одной строки необходимо подобрать из несколько ячеек, например из-за того, что они недоступны в назначенной ячейке, то воспользуйтесь функцией **Разделить строку** на экспресс-вкладке **Строки**. Дополнительные сведения о разделении строк см. в разделе [Разделение строк складских заданий](warehouse-how-to-split-warehouse-activity-lines.md).  
4. По завершении подбора выберите действие **Учет**.    

В процессе учета будет учтена отгрузка товара, подобранного в соответствии со строками документа-источника, или (в случае производственных заказов) будет учтено потребление. Если на складе используются ячейки, в процессе учета создаются также складские операции, чтобы учесть изменения количества в ячейках.  

## <a name="to-delete-inventory-pick-lines"></a>Удаление строк подбора запасов  
Если товары подбора запасов недоступны, вы можете удалить эти строки подбора запасов после учета, а затем удалить документ подбора запасов. Документ-источник, такой как заказ на продажу или производственный заказ, будет включать в себя оставшиеся товары, которые необходимо подобрать, которые затем можно получить путем нового складского подбора, когда товары становятся доступными.  

> [!WARNING]  
>  Этот процесс невозможен, если серийные номера или номера партии указаны в исходном документе. Например, если строка заказа на продажу содержит серийный номер или номер партии, то данные отслеживания товара будут удалены, если строка складского подбора для серийного номера/номера партии также удаляется.  
>   
>  Если в строках подбора запасов содержатся недоступные серийные номера и номера партий, не следует удалять строки в вопросе. Вместо этого, необходимо изменить величину в поле **Кол-во для обработки** на нуль, выполнить учет реальных подборов, а затем удалить документ подбора запасов. Это гарантирует, что строки подбора запасов для этих серийных номеров или номеров партий можно позже повторно создать из заказа на продажу.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Обработка товаров сборки на заказ со складскими подборками
Окно **Подбор запасов** также используется для подбора и отгрузки для продажи, когда товары необходимо собрать до их отгрузки. Дополнительные сведения см. в разделе [Продажа товара, собранного на заказ](assembly-how-to-sell-items-assembled-to-order.md).

Товары, которые должны быть поставлены, физически не присутствуют в ячейке до тех пор, пока они не будут собраны и учтены как исходящие в ячейке в области сборки. Это означает, что подбор товаров сборки на заказ для отгрузки выполняется согласно специальной процедуре. Работники склада берут из ячейки сборочные элементы для склада отгружаемых товаров, а затем учитываются складской подбор. Учтенный складской подбор затем учитывает производительность сборки, потребление компонентов и отгрузки продаж.

Можно настроить [!INCLUDE[d365fin](includes/d365fin_md.md)] для автоматического создания перемещения запасов при создании складского подбора для сборочного элемента. Чтобы включить это, необходимо выбрать поле **Создавать перемещения автоматически** в окне **Настройка сборки**. Дополнительные сведения см. в разделе [Перемещение компонентов в производственную зону на основном складе](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Строки складского подбора для продаваемых товаров создаются разными способами в зависимости от того, какое количество строк продажи собирается на заказ.

Обычные продажи, в которых используются складские подборы, чтобы учесть отгрузку количества запасов, для каждой строки заказа на продажу создается одна строка складского подбора или несколько строк, если товар помещен в различные ячейки. Эта строка подбора основана на количестве в поле **Кол-во для отгрузки**.

В документах продаж сборки на заказ, где все количество в строке заказа на продажу собрано на заказ, создается одна строка складского подбора для этого количества товара. Это означает, что значение "Количество для сборки" совпадает со значение в поле **Кол-во для отгрузки**. В строке выбрано поле **Сборка на заказ**.

Если выход сборки настроен для данного склада, то значение в поле **Код ячейки сборки на заказ** либо значение в поле **Код исходящей сборочн. ячейки** в этом заказе вставляется в поле **Код ячейки** в строке складского подбора.

Если в строке заказа на продажу не указан код ячейки и не настроен поток сборки для склада, поле **Код ячейки** строки складского подбора останется пустым. Работник склада должен открыть окно **Содержимое ячейки** и выбрать ячейку, где собираются сборочные элементы.

В составных сценариях, согласно которым часть количества нужно сначала собрать, а другую отобрать из запасов, создаются минимум две строки подбора запасов. Одна строка складского подбора предназначена для количества сборки на заказ. Другая строка подбора зависит от того, какие ячейки могут пополнить остаток со склада. Коды ячеек в двух строках заполняются по-разному, как описано соответственно для двух разных типов продажи. Дополнительные сведения см. в подразделе "Сценарии комбинации" в разделе [Сборка на заказ и сборка на склад](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>См. также  
[Управление складом](warehouse-manage-warehouse.md)  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
