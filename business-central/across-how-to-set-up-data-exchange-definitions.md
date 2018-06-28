---
title: "Определение порядка электронного обмена данными | Microsoft Docs"
description: "Можно использовать внешнего поставщика служб OCR для преобразования PDF-файлов или файлов изображений в электронные документы."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4828da068f1e17d031300948e930c9685a2f274d
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-data-exchange-definitions"></a>Настройка определений обмена данными
Можно настроить [!INCLUDE[d365fin](includes/d365fin_md.md)] для обмена данными в виде таблиц определенного вида и данных из внешних файлов, например, для отправки и получения электронных документов, импорта и экспорта банковских и иных данных, таких как расчет зарплаты, валютные курсы и каталоги изделий. Дополнительные сведения см. в разделе [Электронный обмен данными](across-data-exchange.md).  

В рамках подготовки к созданию определения обмена данными для файла или потока данных можно использовать связанную XML-схему для определения элементов данных, которые должны быть включены в экспресс-вкладку **Определения столбцов**. См. шаг 6 в разделе “Описание форматирования строк и столбцов в файле”. Для получения дополнительной информации см. раздел [Использование XML-схем SEPA для подготовки определений обмена данными](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Обычно определения обмена данными настраиваются в окне **Определение обмена данными**. Однако при настройке определений обмена данными для службы обновления валютных курсов процесс начинается в упрощенном окне **Карточка настройки обновления валютных курсов**.  

> [!NOTE]  
>  Если файл преобразуется в формат XML, термин *“столбец”* в данном разделе следует интерпретировать как *“XML-элемент, содержащий данные"*.  

Этот раздел содержит следующие процедуры:  

* Создание определения обмена данными  
* Экспорт определения обмена данными в XML-файл для использования другими  
* Импорт XML-файла в существующее определение обмена данными  

## <a name="to-create-a-data-exchange-definition"></a>Создание определения обмена данными  
Создание определения обмена данными включает две задачи:  

1. В окне **Определение обмена данными** опишите форматирование строк и столбцов в файле.  
2. В окне **Сопоставление обмена данными** сопоставьте столбцы в файле данных с полями в [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     Это описано в следующих процедурах.  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Описание форматирования строк и столбцов в файле  
1. В поле **Поиск** введите **Определения обмена данными**, а затем выберите связанную ссылку.  
2. Выберите действие **Создать**.  
3. На экспресс-вкладке **Общее** введите описание определения обмена данными и тип файла данных, заполнив поля, как описано в следующей таблице.  

    |Поле|Описание|  
    |---------------------------------|---------------------------------------|  
    |**Код**|Введите код, чтобы задать определение обмена данными.|  
    |**Название**|Введите имя определения обмена данными.|  
    |**Тип файла**|Укажите тип файла, для которого используется определение обмена данными. Доступны для выбора три типа файлов.<br /><br /> -   **XML**: послойные строки содержимого и разметка, окруженные тегами, которые указывают на функцию.<br />-   **Текст переменной**: записи имеют переменную длину и разделены знаком, например запятой или точкой с запятой. Также называется *файлом с разделителями-запятыми*.<br />-   **Фиксированный текст**: записи имеют одинаковую длину за счет заполнителей, и каждая запись находится на отдельной строке. Также называется *файлом с фиксированной шириной*.|  
    |**Тип**|Укажите тип бизнес-действий, для которого используется определение обмена данными – например, **Экспорт платежей**.|  
    |**Codeunit обработки данных**|Укажите модуль codeunit, который перемещает данные в таблицы в [!INCLUDE[d365fin](includes/d365fin_md.md)] и из них.|  
    |**Codeunit проверки**|Укажите модуль codeunit, который используется для проверки данных в соответствии с предварительно определенными бизнес-правилами.|  
    |**Codeunit чтения/записи**|Укажите модуль codeunit, который обрабатывает импортируемые данные до сопоставления и экспортируемые данные после сопоставления.|  
    |**Чтение/запись XMLport**|Укажите XMLport, с помощью которого поступает импортированный файл данных или служба до сопоставления и с помощью которого существуют экспортированные данных, если они записаны в файл данных или службу после сопоставления.|  
    |**Codeunit обработки внешних данных**|Укажите модуль codeunit, который перемещает внешние данные в структуру обмена данными и из нее.|  
    |**Codeunit обратной связи с пользователем**|Укажите модуль codeunit, выполняющий различные операции очистки после сопоставления – такие как пометка строк экспортированными и удаление временных записей.|  
    |**Кодировка файла**|Укажите шифрование файла. **Примечание.** Это поле релевантно только для импорта.|  
    |**Разделитель столбцов**|Укажите способ разделения столбцов в файле данных, если файл принадлежит типу **Текст переменной**.|  
    |**Строки заголовка**|Укажите количество строк заголовка в файле.<br /><br /> При этом не импортируются данные верхнего колонтитула. **Примечание.** Это поле релевантно только для импорта.|  
    |**Тег заголовка**|Если строка заголовка существует в нескольких местах в файле, введите текст первого столбца в строке заголовка.<br /><br /> При этом не импортируются данные верхнего колонтитула. **Примечание.** Это поле релевантно только для импорта.|  
    |**Тег нижнего колонтитула**|Если строка нижнего колонтитула существует в нескольких местах в файле, введите текст первого столбца в строке нижнего колонтитула.<br /><br /> При этом не импортируются данные нижнего колонтитула. **Примечание.** Это поле релевантно только для импорта.|  

4. На экспресс-вкладке **Определения строки** введите описание форматирования строк в файле данных, заполнив поля, как описано в следующей таблице.  

    > [!NOTE]  
    >  Для импорта банковских выписок следует создать только одну строку для единого формата файла банковской выписки, который требуется импортировать.  
    >   
    >  Для экспорта платежей можно создать строку для каждого типа платежа, который необходимо экспортировать. В этом случае на экспресс-вкладке **Определения столбца** отобразятся различные столбцы для каждого типа платежа.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Код**|Введите код, чтобы определить строку в файле.|  
    |**Название**|Введите имя, описывающее строку в файле.|  
    |**Число столбцов**|Укажите количество столбцов в строке файла данных. **Примечание.** Это поле релевантно только для импорта.|  
    |**Тег строки данных**|Укажите позицию элемента на связанной XML-схеме, представляющего основную запись файла данных. **Примечание.** Это поле релевантно только для импорта.|  
    |**Пространство имен**|Укажите пространство имен, которое ожидается в файле, чтобы включить проверку пространства имен. Можно оставить это поле пустым, если не требуется включать проверку пространства имен.|  

5. Повторите шаг 4, чтобы создать строку для каждого типа файла данных, который необходимо экспортировать.  

     Перейдите к описанию форматирования столбцов файла данных, заполнив поля экспресс-вкладки **Определения столбцов** как описано в следующей таблице. Можно использовать файл структуры – например, формата .XSD – для файла данных, предназначенного для заполнения экспресс-вкладки соответствующими элементами. Для получения дополнительной информации см. раздел [Использование XML-схем SEPA для подготовки определений обмена данными](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. На экспресс-вкладке **Определения столбца** выберите **Получить структуру файла**.  
7. В окне **Получить структуру файла** выберите соответствующий файл структуры и затем нажмите кнопку **ОК**. Строки экспресс-вкладки **Определения столбца** заполняются в соответствии со структурой файла данных.  
8. На экспресс-вкладке **Определения столбца** измените или заполните поля, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Номер столбца**|Укажите номер, который определяет положение столбца в строке в файле.<br /><br /> Для XML-файлов укажите номер, отражающий тип элемента в файле, который содержит данные.|  
    |**Название**|Укажите имя столбца.<br /><br /> Для XML-файлов укажите разметку, которая определяет данные для обмена.|  
    |**Тип данных**|Укажите тип данных для обмена: **Текст**, **Дата** или **Десятичное**.|  
    |**Формат данных**|Укажите формат данных, если есть. Например, **ММ-дд-гггг**, если используется тип данных **Дата**. **Примечание.** Для экспорта укажите формат данных в соответствии с [!INCLUDE[d365fin](includes/d365fin_md.md)]. Для импорта укажите формат данных в соответствии с платформой .NET. Дополнительные сведения см. в разделе [Стандартные строки форматирования даты и времени](http://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Языковой стандарт форматирования данных**|Укажите культуру формата данных, если есть. Например, **en-US**, если используется тип данных **Десятичный**, чтобы гарантировать, что запятая используется в качестве разделителя ,000 в соответствии с форматом США. Дополнительные сведения см. в разделе [Стандартные строки форматирования даты и времени](http://go.microsoft.com/fwlink/?LinkID=323466). **Примечание.** Это поле релевантно только для импорта.|  
    |**Длина**|Укажите длину строки с фиксированной шириной, которая содержит столбец, если файл данных принадлежит типу **Фиксированный текст**.|  
    |**Описание**|Введите описание столбца для информации.|  
    |**Путь**|Укажите позицию элемента в связанной XML-схеме.|  
    |**Идентификатор отрицательного знака**|Введите значение, используемое в файле данных для определения отрицательных сумм, в файлы данных, которые не могут содержать отрицательные знаки. Затем этот идентификатор используется для добавления отрицательных знаков к идентифицированным суммам во время импорта. **Примечание.** Это поле релевантно только для импорта.|  
    |**Константа**|Укажите все данные, которые требуется экспортировать в этом столбце, такие как дополнительные сведения о типе платежа. **Примечание.** Это поле релевантно только для экспорта.|  

9. Повторите шаг 8 для каждого столбца или XML-элемента файла данных, содержащего данные, которыми нужно обменяться с [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Следующим шагом в создании определения обмена данными является принятие решения о том, какие столбцы или XML-элементы на карте файлов данных нужно сопоставить с какими полями [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Конкретное сопоставление зависит от коммерческого назначения обмениваемого файла данных и от местных вариаций. Даже банковский стандарт SEPA отличается в зависимости от региона. [!INCLUDE[d365fin](includes/d365fin_md.md)] изначально поддерживает импорт файлов банковских выписок SEPA в формате CAMT. Он представлен кодом записи определения обмена данными **SEPA CAMT** в окне **Определения обмена данными**. Информацию о сопоставлении конкретных полей данной поддержки SEPA CAMT см. в разделе [Сопоставление полей при импорте файлов SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Сопоставление столбцов в файле данных полям в [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. На экспресс-вкладке **Определения строки** выберите строку, для которой необходимо сопоставить столбцы и поля, а затем выберите **Сопоставление полей**. Откроется окно **Сопоставление обмена данными**.  
2. На экспресс-вкладке **Общее** укажите настройку сопоставления, заполнив поля, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Таблица ID**|Укажите таблицу, в которой содержатся поля с данными, обмен которыми выполняется в соответствии с сопоставлением.|  
    |**Использовать как промежуточную таблицу**|Укажите, является ли таблица, выбранная в поле **Код таблицы**, промежуточной таблицей, в которой импортируемые данные сохраняются перед сопоставлением с целевой таблицей.<br /><br /> Обычно промежуточная таблица используется, когда определение обмена данными применяется для импорта и преобразования электронных документов — например, преобразования счетов от поставщиков в счета покупки в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Электронный обмен данными](across-data-exchange.md).|  
    |**Название**|Ввод имени настройки сопоставления.|  
    |**Codeunit до сопоставления**|Укажите модуль codeunit, который подготавливает сопоставление полей в [!INCLUDE[d365fin](includes/d365fin_md.md)] с внешними данными.|  
    |**Сопоставление Codeunit**|Укажите модуль codeunit, который используется для сопоставления указанных столбцов или XML-элементов данных с полями в [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit после сопоставления**|Укажите модуль codeunit, который завершает сопоставление полей в [!INCLUDE[d365fin](includes/d365fin_md.md)] с внешними данными. **Примечание.** При использовании функции службы преобразования банковских данных модуль codeunit конвертирует экспортированные данные из [!INCLUDE[d365fin](includes/d365fin_md.md)] для получения универсального формата, готового к экспорту. Для импорта модуль codeunit преобразует внешние данные в формат, готовый для импорта в [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  На экспресс-вкладке **Сопоставление полей** определите, какие столбцы будут сопоставлены с какими полями в [!INCLUDE[d365fin](includes/d365fin_md.md)], заполнив поля, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Номер столбца**|Укажите столбец в файле данных, для которого необходимо определить сопоставление.<br /><br /> Можно выбрать только столбцы, представленные строками на экспресс-вкладке **Определения столбца** в окне **Определение обмена данными**.|  
    |**Код поля**|Укажите поле, с которым требуется сопоставить столбец в поле **Номер столбца** .<br /><br /> Можно выбирать только из полей, которые существуют в таблице, заданной в поле **Таблица** на экспресс-вкладке **Общее**.|  
    |**Можно**|Укажите, что сопоставление будет пропущено, если поле не заполнено. **Примечание.** Если этот флажок не установлен, произойдет ошибка экспорта, если поле пустое. **Примечание.** Это поле релевантно только для экспорта.|  
    |**Код целевой таблицы**|Отображается только в том случае, если установлен флажок **Использовать как промежуточную таблицу**.<br /><br /> Определите таблицу, с которой сопоставляется значение в поле **Заголовок столбца**, при использовании промежуточной таблицы для импорта данных.|  
    |**Метка целевой таблицы**|Отображается только в том случае, если установлен флажок **Использовать как промежуточную таблицу**.<br /><br /> Укажите имя таблицы в поле **Код целевой таблицы**, которое задает таблицу, с которой сопоставляется значение в поле **Заголовок столбца**, при использовании промежуточной таблицы для импорта данных.|  
    |**Код целевого поля**|Отображается только в том случае, если установлен флажок **Использовать как промежуточную таблицу**.<br /><br /> Укажите поле в целевой таблице, с которым сопоставляется значение в поле **Заголовок столбца**, при использовании промежуточной таблицы для импорта данных.|  
    |**Заголовок целевого поля**|Отображается только в том случае, если установлен флажок **Использовать как промежуточную таблицу**.<br /><br /> Укажите имя поля в целевой таблице, с которым сопоставляется значение в поле **Заголовок столбца**, при использовании промежуточной таблицы для импорта данных.|  
    |**Можно**|Отображается только в том случае, если установлен флажок **Использовать как промежуточную таблицу**.<br /><br /> Укажите, следует ли пропустить сопоставление, если поле не заполнено. Если этот флажок не установлен, произойдет ошибка экспорта, если поле пустое.|  

Определение обмена данными готово для применения пользователями. Дополнительные сведения см. в разделах [Настройка отправки и получения электронных документов](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Настройка кредитового перевода SEPA](finance-how-to-set-up-sepa-credit-transfer.md), [Настройка прямого дебетования SEPA](finance-how-to-set-up-sepa-direct-debit.md) и [Выполнение платежей с помощью службы конвертации банковских данных или кредитового перевода SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

Если создано определение обмена данными для конкретного файла данных, можно экспортировать определение обмена данными в качестве XML-файла, который можно использовать для того, чтобы быстро включить импорт файла данных. Это описано в следующей процедуре.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Экспорт определения обмена данными в XML-файл для использования другими  
1. В поле **Поиск** введите **Определения обмена данными**, а затем выберите связанную ссылку.  
2. Выберите определение обмена данными, которое требуется экспортировать.  
3. Выберите действие **Экспорт определения обмена данными**.  
4. Сохраните XML-файл, представляющий определение обмена данными, в соответствующем местоположении.  

    Если определение обмена данными уже создано, достаточно импортировать XML-файл в инфраструктуру обмена данными. Это описано в следующей процедуре.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Импорт существующего определения обмена данными  
1. Сохраните XML-файл, представляющий определение обмена данными, в соответствующем местоположении.  
2. В поле **Поиск** введите **Определения обмена данными**, а затем выберите связанную ссылку.  
3. Выберите действие **Создать**. Открывается окно **Определение обмена данными**.  
4. Выберите действие **Импорт определения обмена данными**.  
5. Выберите файл, сохраненный на шаге 1.  

## <a name="see-also"></a>См. также  
[Настройка обмена данными](across-set-up-data-exchange.md)  
[Настройка отправки и получения электронных документов](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Настройка кредитового перевода SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Настройка прямого дебетования SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Выполнение платежей с помощью службы конвертации банковских данных или кредитового перевода SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Входящие документы](across-income-documents.md)  
[Общие бизнес-функции](ui-across-business-areas.md)  
