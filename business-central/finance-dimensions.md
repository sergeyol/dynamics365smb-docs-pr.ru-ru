---
title: Работа с измерениями | Документация Майкрософт
description: Измерения служат для категоризации операций, например по отделам или проектам, чтобы данные было легко отслеживать и анализировать.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b0e5a74db148e0c33eeb87bd006f3c136bc8ee33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917180"
---
# <a name="working-with-dimensions"></a>Работа с измерениями
Чтобы упростить анализ по документам, таким как заказы на продажу, можно использовать измерения. Измерения — это атрибуты и значения, которые классифицируют операции для их отслеживания и анализа. Например, измерения могут указывать проект или отдел, который является источником операции.  

Например, вместо настройки отдельных счетов главной книги для каждого отдела или проекта можно использовать измерения. Это дает прекрасные возможности анализа без создания сложного плана счетов. Дополнительные сведения см. в разделе [Бизнес-аналитика](bi.md)

Еще одним примером является настройка измерения *Отдел* и использование этого измерения при учете документов продажи. Это позволит использовать инструменты бизнес-аналитик для просмотра того, какой отдел продал какие товары.
Чем больше измерений вы используете, чем более подробные отчеты вы будете получать, чтобы принимать на их основе бизнес-решения. Например, одна операция продажи может содержать информацию о нескольких измерениях, например:  

* Счет, на котором был учтен товар.  
* Место продажи товара.
* Лицо, продавшее товар.
* Тип клиента, купившего товар.  

## <a name="analyzing-by-dimensions"></a>Анализ по измерениям
Функция измерений играет важную роль в бизнес-аналитике, например при определении представлений анализа. Дополнительные сведения см. в разделе [Анализ данных по измерениям](bi-how-analyze-data-dimension.md).

> [!TIP]
> Для быстрого анализа транзакционных данных по измерениям можно отфильтровать итоговые суммы в планах счетов и записи на всех страницах **Операции** по измерениям. Найдите действие **Установить фильтр измерений**.

## <a name="dimension-sets"></a>Наборы измерений
Набор измерений — это уникальная комбинация значений измерений. Это храниться как записи набора измерений в базе данных. Каждая запись набора измерений представляет отдельное значение измерения. Набор измерений определяется общим кодом набора измерений, который присваивается каждой операции набора измерений, которая относится к набору измерений.  

При создании строки журнала, заголовка документа или строки документа можно указать комбинации значений измерений. Вместо явного сохранения значения каждого измерения в базе данных, код набора измерений присваивается строке журнала, заголовку документа или строке документа для определения набора измерений.  

## <a name="setting-up-dimensions"></a>Настройка измерений
Можно определить измерения и значения измерений для категоризации журналов и документов, таких как заказы на покупку и заказы на продажу. Измерения можно настроить на странице **Измерения**, в котором создается по одной строке для каждого измерения, таких как *Проект*, *Отдел*, *Область* и *Менеджер по продажам*.

Также можно настроить значения для измерений. Например, значениями могут быть отделы в организации. Значения измерений можно настроить в иерархической структуре подобно плану счетов. После выполнения настройки можно будет разделять данные по нескольким уровням гранулярности, а также подсчитывать итоги по подмножествам значений измерений. Можно задать любое количество измерений и значений измерений, и все пользователи в организации могут их использовать.

Если настроены измерения и значения, можно определить глобальные измерения и ярлыки измерений на странице **Настройка ГК**, которые будет всегда доступны для выбора в качестве полей в строках журналов и документов, не открывая сначала страницу **Измерения**. Дополнительную информацию см. в разделе [Настройка глобальных измерений и ярлыков измерений](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Глобальные измерения** используются в качестве фильтров, например в отчетах, пакетных заданиях и XMLport. Можно использовать только два глобальных измерения, поэтому выберите измерения, которые будут использоваться наиболее часто.
* **Ярлыки измерений** доступны как поля в строках журналов и документов. Можно создать до шести ярлыков измерений.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Настройка измерений по умолчанию для клиентов, поставщиков и других счетов
Для конкретного счета можно назначить измерение по умолчанию. Измерение будет копироваться в журнал или документ при вводе номера счета в строку, но вы сможете удалить или изменить код в строке в случае необходимости. Можно также создать измерение, необходимое для учета операции с определенным типом счета.  

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Измерения**, затем выберите соответствующую ссылку.  
2.  На странице **Измерения** выберите соответствующее измерение, а затем выберите действие **Измерение по умолчанию для типа счета**.  
4.  Заполните строку для каждого нового измерения по умолчанию, которое требуется настроить. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Чтобы сделать измерение обязательным без назначения ему значения по умолчанию, оставьте поле **Код значения измерения** пустым, после чего выберите значение **Обязательный код** в поле **Учет значения**.  

> [!WARNING]  
>  Если счет используется в пакетном задании **Коррекция валютных курсов** или в пакетном задании **Учет себест. запасов в ГК**, не выбирайте **Код обязателен** или **Единый код**. Эти пакетные задания не могут использовать коды измерений.  

> [!NOTE]  
>  Если для счета должно быть задано не уже настроенное стандартное для типа счета, а другое измерение, следует для этого счета настроить стандартное измерение. В этом случае стандартное измерение для отдельного счета заменит стандартное измерение для типа счета.  

### <a name="to-set-up-default-dimension-priorities"></a>Настройка приоритетов измерений по умолчанию  
Различные типы счетов, например счет клиента и счет товара, могут иметь разные стандартные измерения. В результате этого, операция может иметь несколько предлагаемых стандартных измерений. Для того, чтобы избежать подобных конфликтов, можно настроить правила приоритетов для различных источников.  

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Приоритеты измерения по умолчанию**, затем выберите соответствующую ссылку.  
2.  На странице **Приоритеты измерения по умолчанию** в поле **Код источника** введите код источника для таблицы операций, к которой будут применяться приоритеты измерения по умолчанию.  
3.  Заполните строку для каждого приоритета измерения по умолчанию, необходимого для выбранного кода источника.
4.  Повторите процедуру для каждого кода источника, для которого требуется настроить приоритеты измерения по умолчанию.  

> [!IMPORTANT]  
>  Если настроены две таблицы с одинаковыми приоритетами для одинаковых кодов источников, в [!INCLUDE[d365fin](includes/d365fin_md.md)] всегда будет выбираться таблица с наименьшим кодом.  

### <a name="to-set-up-dimension-combinations"></a>Настройка комбинаций измерений  
Для того, чтобы избежать учета операций с противоречивыми или неуместными измерениями, можно заблокировать или ограничить определенные комбинации двух измерений. Заблокированная комбинация измерений означает, что невозможно произвести учет двух измерений для одной и той же операции вне зависимости от значений измерений. Ограниченная комбинация измерений позволяет производить учет обоих измерений в одну и ту же операцию, но только при определенных сочетаниях значений этих измерений.

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Комбинации измерений**, затем выберите соответствующую ссылку.  
2.  На странице **Комбинации измерений** перейдите к полю комбинации измерений и выберите один из следующих параметров.  

    |Поле|Описание|
    |----------------------------------|---------------------------------------|  
    |**Без ограничения**|Эта комбинация измерений не имеет ограничений. Все значения измерений разрешены.|  
    |**Ограничено**|Данная комбинация измерений имеет ограничения в зависимости от того, какое значение измерения указано. Ограничения следует определить на странице **Комбинация значений измерения**.|  
    |**Заблокировано**|Такая комбинация измерений не разрешена.|  

3.  Если выбран параметр **Ограничено**, следует определить, какие комбинации значений измерений будут блокироваться. Для этого выберите поле, чтобы определить сочетание измерений.  
4.  Теперь можно выбрать заблокированную комбинацию значений измерений и ввести в поле значение **Заблокировано**. Пустое поле указывает на то, что комбинация значений измерений разрешена. Повторите данные действия, если заблокировано несколько комбинаций.  

> [!NOTE]  
>  Одни и те же измерения отображаются как в строках, так и в столбцах, вследствие чего все комбинации измерений появляются дважды. [!INCLUDE[d365fin](includes/d365fin_md.md)] автоматически отображает настройки в обоих полях. В полях, расположенных в левом верхнем углу и ниже нет возможности выбрать что-либо, т.к. эти поля имеют одинаковые измерения как в строках, так и в столбцах.  
>   
>  Выбранный параметр невидим перед тем, как выйти из поля.  
>   
>  Чтобы вместо кодов измерений показать их названия, установите флажок в поле **Показать название столбца**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Настройка глобальных измерений и ярлыков измерений
Глобальные измерения и ярлыки измерений можно использовать в качестве фильтра в любом месте в [!INCLUDE[d365fin](includes/d365fin_md.md)], включая отчеты, пакетные задания и аналитические отчеты. Глобальные измерения и ярлыки измерений всегда доступны для вставки непосредственно без предварительного открытия страницы **Измерения**. В строках журналов и документов можно выбрать глобальные измерения или ярлыки измерений в поле в строке. Можно настроить два глобальных измерения и восемь ярлыков измерений. Выберите измерения, которые чаще всего используются.

> [!Important]  
> Для изменения глобального измерения или ярлыка измерения требуется, чтобы были обновлены все записи, учтенные с измерением. Эту задачу можно выполнить с помощью функции **Изменить глобальные измерения**, но это может занять много времени и отрицательно сказаться на производительности; кроме того, во время обновления таблицы могут быть заблокированы. Поэтому тщательно выбирайте свои глобальные измерения и ярлыки измерений, чтобы не потребовалось изменять их в дальнейшем. <br /><br />
> Дополнительные сведения см. в разделе [Изменение глобальных измерений](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> При добавлении или изменении глобального измерения или ярлыка измерения производится автоматический выход и обратный вход, чтобы новое значение было подготовлено к применению по всему приложению.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка ГК**, затем выберите соответствующую ссылку.
2. На экспресс-вкладке **Измерения** заполните поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Для изменения глобальных измерений
При изменении глобального измерения или ярлыка измерения все операции, учтенные с этим измерением, обновляются. Поскольку этот процесс может занимать много времени и отрицательно влиять на производительность, предусмотрены два разных режима для адаптации этого процесса к размеру базы данных.  

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка ГК**, затем выберите соответствующую ссылку.
2. Выберите действия **Изменить глобальные измерения**.
3. В верхней части страницы выберите один из следующих вариантов, чтобы определить, в каком режиме будет запущено пакетное задание.

    |Параметр|Описание|
    |-|-|
    |**Последовательный**|(По умолчанию) Изменение измерений целиком выполняется в виде одной транзакции, и все операции возвращаются к измерениям, которые были у них перед изменением.<br /><br />Этот режим рекомендуется, если в организации относительно немного учтенных операций, так как в этом случае он будет быстрее. Процесс блокирует несколько таблиц и блокирует других пользователей, пока не будет завершен. Обратите внимание, что в больших базах данных процесс может вообще не завершиться в этом режиме. В таком случае используйте вариант **Параллельный**.|
    |**Параллельный**|(Установите флажок **Параллельная обработка**.) Изменение измерений выполняется в виде нескольких фоновых сеансов, и операция разбивается на несколько транзакций.<br /><br />Этот режим рекомендуется для больших баз данных или организаций с большим количеством учтенных операций, так как в этом случае он будет быстрее. Обратите внимание, что в этом режиме процесс обновления не запустится, если будет более одного активного сеанса базы данных.|  

4. В полях **Код глобального измерения 1** и/или **Код глобального измерения 2** введите новые измерения. Текущие измерения отображаются серым цветом за полями.
5. Если вы выбрали режим **Последовательный**, выберите действие **Запуск**.
6. Если вы выбрали режим **Параллельный**, выберите действие **Подготовка**.

    Вкладка **Записи журнала** заполняется информация об измерениях, которые будут изменены.
7. Выйдите из [!INCLUDE[d365fin](includes/d365fin_md.md)], а затем войдите снова.
8. Выберите действие **Запуск**, чтобы начать параллельную обработку изменений измерений.

### <a name="example-of-dimension-setup"></a>Пример настройки измерений
Допустим, ваша организация желает отслеживать транзакции на основе организационной структуры и географического расположения. Для этого можно настроить два измерения на странице **Измерения**:

* **ОБЛАСТЬ**  
* **ОТДЕЛ**  

| Код | Name | Метка кода | Метка фильтра |
| --- | --- | --- | --- |
| РЕГИОН |Регион |Код области |Фильтр области |
| ОТДЕЛ |Отдел |Код подразделения |Фильтр по отделу |

Для измерения **ОБЛАСТЬ** вы добавляете следующие значения измерения:

| Код | Name | Тип значения измерения |
| --- | --- | --- |
| 10 |Центральная и Южная Америка |Сумма (от) |
| 20 |Северная Америка |Стандартная |
| 30 |Тихоокеанский регион |Стандартная |
| 40 |Южная Америка |Стандартная |
| 50 |Центральная и Южная Америка, всего |Сумма (до) |
| 60 |Европа |Сумма (от) |
| 70 |ЕС |Стандартная |
| 80 |Страны-не члены ЕС |Стандартная |
| 90 |Европа, всего |Сумма (до) |

Для двух основных географических областей (Центральная и Южная Америка и Европа) добавьте подкатегории для регионов, создав отступы значений измерения. Это позволит создавать отчеты по продажам или расходам в регионах и получать итоги по более крупным географическим областям. Также можно использовать страны или регионы в качестве значений измерения или районы и города в зависимости от сферы деятельности организации.

> [!NOTE]  
>   Чтобы настроить иерархию, коды должны быть расположены в алфавитном порядке. Это включает коды значений измерений, предоставленных в [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Для измерения **ОТДЕЛ** вы добавляете следующие значения измерения:

| Код | Name | Тип значения измерения |
| --- | --- | --- |
| АДМИНИСТРАТОР |Администрация |Стандартная |
| ПРОИЗВ |Зона производства |Стандартная |
| ПРОДАЖИ |Продажи |Стандартная |

В этой настройке вы можете добавить два измерения в качестве глобальных измерений на странице **Настройка ГК**. Это означает, что можно использовать ОБЛАСТЬ и ОТДЕЛ в качестве фильтров для операций главной книги, а также для всех отчетов и финансовых отчетов. Оба глобальных измерения автоматически становятся доступными для использования в качестве ярлыков измерений в строках операций и заголовках документов.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Обзор измерений, используемых несколько раз
На странице **Измерения по умолчанию - несколько** указывается, как группа учетных записей использует измерения и значения измерений. Это можно сделать путем выделения на экране нескольких счетов с последующим определением стандартных измерений для всех счетов, которые выделены в списке счетов. Если для выделенных счетов определены стандартные измерения, приложение предлагает эти измерения и значения измерений всякий раз, когда один из этих счетов используется, — например, в строке журнала. Это упрощает учет операций пользователем, поскольку поля измерений заполняются автоматически. Однако прежлагаемые значения измерений могут быть изменены, например в строке журнала.

Страница **Измерения по умолчанию - несколько** содержит следующие поля:

|Поле|Описание|
|-----|-----------|  
|**Код измерения**|Отображает все измерения, которые были определены как измерения по умолчанию на одном или нескольких выделенных счетах. При выборе поля отображается список всех доступных измерений. При выборе измерения это измерение задается как используемое по умолчанию для всех выделенных счетов.|
|**Код Значения Измерения**|Показывает одно значение измерения или условие (конфликтное). Если значение измерения показано в поле, то всем выделенным на экране счетам будет соответствовать одно и то же стандартное значение измерения. Если в поле показано условие (конфликтное), то не всем выделенным на экране счетам будет соответствовать одно и то же стандартное значение измерения. При выборе поля отображается список всех возможных значений измерения. При выборе измерения это измерение задается как используемое по умолчанию для всех выделенных счетов.|
|**Учет значения**|Показывает или одно правило учета значения, или правило условия (конфликтного). Если в поле показано правило учета значения, то всем выделенным на экране счетам будет соответствовать одно и то же правило учета значения измерения. Если в поле показано условие (конфликтное), то не всем выделенным на экране счетам будет соответствовать одно и то же правило учета значения измерения. При выборе поля Учет значения отображается список правил учета значений. Если выбрать правило учета измерения, оно будет применено ко всем выделенным счетам.|

## <a name="using-dimensions"></a>Использование измерений
В документе, например в заказе на продажу, вы можете добавить сведения об измерении как для отдельной строки документа так и для самого документа. Например, на странице **Заказ на продажу** можно ввести значения измерений для первых двух ярлыков измерений в отдельных строках продажи, а затем добавить дополнительные измерения, нажав кнопку **Измерения**.  

При работе в журнале вы можете добавлять в операцию информацию об измерениях аналогичным образом, если непосредственно в строках журнала в качестве полей были заданы ярлыки измерений.  

Можно настроить измерения по умолчанию для счетов или типов счетов, чтобы измерения и значения измерений заполнялись автоматически.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Для просмотра глобальных измерений на страницах книги операций  
Глобальные измерения всегда определяются и именуются на уровне организации. Чтобы просмотреть глобальные измерения для организации, откройте страницу **Настройка ГК**.  

На странице книги операций можно увидеть, поставлены ли в соответствие операциям глобальные измерения. Два глобальных измерения отличаются от остальных, поскольку их можно использовать в качестве фильтров в любой области [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **План счетов**, затем выберите соответствующую ссылку.  
2.  На странице **План счетов** выберите действие **Операции книги**.  
3.  Для отображения только требуемых операций установите на странице один или несколько фильтров.  
4.  Для отображения всех измерений для операции выберите операцию и выберите действие **Измерения**.  

> [!NOTE]  
>  Страница **Измерения операции в книге** отображает измерения для одной операции книги на текущий момент времени. По мере перемещения по операциям книги, содержимое страницы **Измерения операции в книге** меняется соответствующим образом.

## <a name="troubleshooting-dimensions-errors"></a>Устранение ошибок измерений
При учете строк документов или журнала, которые содержат измерения, могут возникать различные ошибки, которые обычно связаны с ошибочной настройкой или назначением измерений.

> [!NOTE]
> В следующем списке потенциальных сообщений об ошибках, коды *%X* являются заполнителями для переменных данных, которые фактическое сообщение будет содержать в пользовательском интерфейсе в зависимости от контекста. Например, *%1 %2 заблокировано.* может отображаться в пользовательском интерфейсе как "ОБЛАСТЬ кода измерения заблокировано".  

|Проблема|Сообщение об ошибке|Возможное решение|
|-----|-------------|-----------------|
|Заблокированное измерение|%1 %2 заблокировано.|-Найдите неучтенные документы, содержащие набор измерений с заблокированным измерением, и разблокируйте его.<br />-Удалите строку набора измерений для заблокированного измерения.|
|Удаленное измерение|Не удается найти %1 %2.|-Восстановите отсутствующее измерение.<br />-Найдите неучтенные документы, содержащие набор измерений с отсутствующим измерением и добавьте его.<br />-Удалите строку набора измерений для отсутствующего измерения.|
|Заблокированное значение измерения|%1 %2 - %3 заблокировано.|-Найдите неучтенные документы, содержащие набор измерений с заблокированным значением измерения, и разблокируйте его.<br />-Удалите строку набора измерений для заблокированного значения измерения.|
|Удаленное значение измерения|   %1 для %2 отсутствует.|-Восстановите отсутствующее значение измерения.<br />-Найдите неучтенные документы, содержащие набор измерений с отсутствующим значением измерения и добавьте его.<br />-Удалите строку набора измерений для отсутствующего значения измерения.|
|Запрещенное значение измерения|Тип значения измерения для %1 %2 - %3 не должен иметь значение %4.|-Измените поле **Тип значения измерения** на странице **Значения измерения** на **Стандарт** или **Сумма (от)**.<br />-Удалите строку набора измерений для заблокированного значения измерения.|
|Заблокированная комбинация измерений|Измерения %1 и %2 нельзя использовать одновременно.|-Найдите неучтенные документы, содержащие набор измерений с заблокированной комбинацией измерений, и разблокируйте ее.<br />-Измените один из конфликтующих наборов разрешений для комбинации измерений.|
|Заблокированная комбинация значений измерений|Комбинации измерений %1 - %2 и %3 - %4 нельзя использовать одновременно.|-Найдите неучтенные документы, содержащие набор измерений с заблокированной комбинацией значений измерений, и разблокируйте ее.<br />-Измените один из конфликтующих наборов разрешений для комбинации значений измерений.|
|Пустой код значений измерений для измерения по умолчанию, где поле **Учет значения** содержит **Код обязателен**|-Выберите %1 для %2 %3.<br />-Выберите %1 для %2 %3 для %4 %5.|-Измените поле **Учет значения** на странице **Измерение по умолчанию**.<br />-Введите непустое значение измерения для конфликтующего измерения в наборе измерений.|
|Неправильный код значений измерений для измерения по умолчанию, где поле **Учет значения** содержит **Единый код**|-Выберите %1 %2 для %3 %4.<br />-Выберите %1 %2 для %3 %4 для %5 %6|-Измените поле **Учет значения** на странице **Измерение по умолчанию**.<br />-Введите требуемое значение измерения для конфликтующего измерения в наборе измерений.|
|Непустой код значений измерений для пустого измерения по умолчанию, где поле **Учет значения** содержит **Единый код**|-%1 %2 должно быть пусто.<br />-%1 %2 должно быть пусто для %3 %4.|-Измените поле **Учет значения** на странице **Измерение по умолчанию**.<br />-Введите пустой код значений измерения для конфликтующего измерения в наборе измерений.|
|Непредусмотренное значение измерения для измерения по умолчанию, где поле **Учет значения** содержит **Нет кода**|-%1 %2 не должно упоминаться.<br />-%1 %2 не должно упоминаться для %3 %4|-Измените поле **Учет значения** на странице **Измерение по умолчанию**.<br />-Удалите конфликтующую строку из набора измерений.|

## <a name="see-related-training-at-microsoft-learn"></a>См. соответствующее обучение на странице [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>См. также
[Бизнес-аналитика](bi.md)  
[Финансы](finance.md)  
[Анализ данных по измерениям](bi-how-analyze-data-dimension.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
