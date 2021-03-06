---
title: Использование табелей учета рабочего времени для работ | Документация Майкрософт
description: Описывается процедура создания табеля учета рабочего времени для работы, копирования строк планирования в него, определения видов работ, заполнения табеля учета рабочего времени и его отправки на утверждение.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 68271b7f6f90f88af74cee848af82d28abbf339f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921371"
---
# <a name="use-time-sheets-for-jobs"></a>Использование табелей учета рабочего времени для работ

Используйте пакетное задание **Создать табели учета рабочего времени**, чтобы настроить табели для определенного количества периодов времени или недель. Вы должны иметь права на создание табелей.

Можно скопировать и использовать в табеле строки планирования работы. В этом способе необходимо только ввести информацию для одного места, и информация в строке всегда будет правильной.

После утверждения операций табеля для задания можно выполнять их учет в соответствующем журнале заданий или журнале ресурсов.

Прежде чем использовать табели, необходимо настроить общую информацию и указать администратора и одного или нескольких утверждающих табелей. Дополнительные сведения см. в разделе [Настройка табелей учета рабочего времени](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Создание табеля учета рабочего времени

Можно использовать пакетное задание **Создать табели учета рабочего времени**, чтобы настроить табели для определенного количества периодов времени или недель. Затем владелец табеля может открыть его и записать время, которое было затрачено на задание.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени**, затем выберите соответствующую ссылку.
2. На странице **Список табелей** выберите действие **Создать табели учета рабочего времени**.
3. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Поля **Использовать табель** и **Код пользователя владельца табеля** должны быть заполнены в карте для ресурса табеля.
4. Нажмите кнопку **ОК**.  

Можно просматривать табели, созданные вами, на странице **Список табелей**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Копирование строк планирования работ в табель учета времени
Далее описывается процедура создания быстрого добавления строк планирования работы в табель.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени**, затем выберите соответствующую ссылку.  
2. На странице **Список табелей** выберите табель для соответствующего периода времени, затем выберите действие **Изменить табель**.  
3. Выберите действие **Создать строки из планирования работ**. Все строки планирования заданий в периоде времени табеля копируются в табель для лица или машины в поле **Номер ресурса** табеля учета рабочего времени.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Определение видов работ и добавление вида работ в табель
Можно определить тип работы для всех для строк табелей для заданий. Таким образом можно добавить информацию, которая необходима, чтобы выставить счет клиенту за различные типы работ.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени**, затем выберите соответствующую ссылку.   
2. Откройте соответствующий табель.
3. Выберите поле **Описание**.  
4. На странице **Сведения о работах строк табелей** окне выберите поле **Код вида работы** и выберите вид работы из списка, например **КМ**.  
5. В случае отсутствия видов работ, выберите действие **Создать**.
6. На странице **Виды работ** заполните требуемые поля.
7. Повторите шаг 4 для назначения нового вида работ табелю.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Повторное использование строк табелей в других табелях
Если ваши сведения о табеле учета рабочего времени остаются прежним от периода времени к периоду времени, можно сохранить время, копируя строки из предыдущего периода времени. Затем необходимо просто ввести свое время работы для нового периода.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени**, затем выберите соответствующую ссылку.  
2. Откройте табель дата периода, более позднего, чем период для существующего табеля со строками.  
3. Выберите действие **Копировать строки из предыдущих табелей**.

Строки копируются, включая подробную информацию, такую как тип и описание. Например, если данная строка связана с работой, то поле **Код работы** копируется. Все скопированные строки имеют статус **Открыто**. Теперь строки можно изменять, как требуется.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Заполнение строк табелей и отправка на утверждение
Регистрация табеля отслеживается в часах (стандартной базовой единице измерения для ресурсов). По умолчанию в табеле отображаются общие рабочие дни с понедельника по пятницу.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени**, затем выберите соответствующую ссылку.  
2. Выберите табель для соответствующего периода времени, затем выберите действие **Изменить табель**.  
3. Заполните поля в строке по мере необходимости. Введите количество часов, использованных ресурсом, для каждого дня недели.

    > [!TIP]  
    >   Можно просмотреть общее количество часов, которые вы ввели на информационной панели **Сводка по фактическим и бюджетным суммам**.  
4. Повторите шаг 3 для других видов работ, которые выполняет ресурс.
5. Выберите действие **Передать**, затем выберите действие **Все открытые строки** для передачи всех строк или действие **Только выбранные строки** для передачи только строк, которые выбраны на странице **Табель учета рабочего времени**.  

    > [!NOTE]  
    >   Вы можете отправлять только строки табеля, для которых введено время.  
6. Чтобы изменить информацию в строке, для которой установлено значение **Представляется**, выделите строку и выберите действие **Открыть**.

    > [!NOTE]  
    >   Менеджер может отклонить строку табеля, которая представлена на утверждение. Если строка имеет статус **Отклонено**, вы можете внести изменения в строку, а затем выбрать **Отправить** еще раз.  
7. Нажмите кнопку **ОК**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Утверждение или отклонение табеля
Табель должны быть отправлен для утверждения, прежде чем его можно будет использовать. Можно принимать или отклонять отдельные строки в табеле либо отправлять обратно для выполнения дополнительного действия. Табель может быть утвержден двумя способами:

* Администратор табелей может утвердить любой табель.
* Лицо, указанное в поле **Код пользователя, утверждающего табель** в карточке ресурса, может утвердить табели этого ресурса. Дополнительные сведения см. в разделе [Настройка табелей учета рабочего времени](projects-how-setup-time-sheets.md).

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени для менеджера**, затем выберите соответствующую ссылку.
2. Выберите табель в списке.  
3. На странице **Табель учета рабочего времени** выберите действие **Утвердить**, затем выберите действие **Все отправленные строки** для утверждения всех строк или действие **Только выбранные строки** для утверждения только строк, которые выбраны на странице **Табель учета рабочего времени**.
4. Нажмите кнопку **ОК**.  
5. Можно также выбрать действие **Отклонить** и выполнить шаги с 4 по 5.  

> [!TIP]  
>   Используйте информационные панели **Статус табеля** и **Сводка по фактическим и бюджетным суммам** для общего просмотра сведений о табеле учета рабочего времени.

После утверждения или отклонение табеля его нельзя изменить, пока он не будет повторно открыт. В следующей процедуре объясняется, как повторно открыть утвержденный или отклоненный табель.

## <a name="to-reopen-a-time-sheet"></a>Повторное открытие табеля
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Табели учета рабочего времени для менеджера** или **Табели учета рабочего времени**, затем выберите соответствующую ссылку.
2. Откройте табель из списка.  

    > [!NOTE]  
    >   Повторно можно открыть только строки с состоянием **Одобрено**. Невозможно повторно открыть строки со статусом **Отклонено**. Невозможно повторно открыть табель, если он был учтен.  
3. На странице **Табель учета рабочего времени** выберите действие **Открыть повторно**, затем выберите действие **Все отправленные строки** для повторного открытия всех строк или действие **Только выбранные строки** для повторного открытия только строк, которые выбраны на странице **Табель учета рабочего времени**.
4. Нажмите кнопку **ОК**. Статус строки или строк табелей изменяется на **Представляется**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Просмотр и утверждение табелей учета рабочего времени по работе

Для данной работы можно определить лицо, ответственное за эту работу. Данная информация связана со строками табелей учета рабочего времени и может использоваться для создания списка табелей учета рабочего времени, который менеджер должен просмотреть и утвердить. Например, менеджер команды проекта может быть ответственными за некоторые задачи в вашей организации. В этом случае, менеджер должен быть обозначен как **Ответственное лицо** в карточке работы. В этом представлении сведений о табеле учета рабочего времени можно просмотреть рабочие задания, связанные с задачей и использованное количество часов.

> [!NOTE]
> Чтобы утверждать табели учета времени в окне **Табели учета рабочего времени для менеджера по работам**, необходимо сначала выбрать вариант **Табель учета рабочего времени по утверждению работы** на странице **Настройка модуля "Ресурсы"**. Дополнительные сведения см. в разделе [Настройка ресурсов](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Утверждение или отклонение табеля учета рабочего времени по заданию

1. В поле **Поиск** введите **Управление табелями учета рабочего времени по заданию**, а затем выберите связанную ссылку. Microsoft Dynamics NAV отображает список строк табеля учета рабочего времени, связанных с заданиями, за которые вы отвечаете.
2. На вкладке **Главная** выберите **Утвердить**. Выберите **Все**, чтобы утвердить все строки. Выберите **Выбрано**, чтобы утвердить только выбранные строки.

    > [!NOTE]
    > Можно одобрять только те табели, которые имеют состояние **Отправлено**.

3. Чтобы указать дополнительные сведения об утверждении или отклонении, выберите строку табеля учета рабочего времени и на вкладке **Навигатор** выберите **Комментарии**. В поле **Дата** укажите дату, а затем введите комментарий в поле **Комментарий**.
4. Нажмите кнопку **ОК**.

> [!NOTE]
> После утверждения или отклонение строки табеля по заданию ее нельзя открыть повторно или изменить в окне **Табель учета рабочего времени**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Учет строк табеля в журнале ресурсов
После утверждения операций табеля для ресурса можно выполнять их учет в соответствующем журнале ресурсов.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал ресурсов**, затем выберите соответствующую ссылку.  
2. Выберите действие **Предлагать строки из табелей**.  
3. Заполните соответствующим образом поля.  
4. Нажмите кнопку **ОК**. Операции для использования создаются в журнале ресурсов, в котором можно изменить информацию как нужно.  
5. Выберите действие **Учет**.  
6. Чтобы проверить учет, выберите действие **Книга операций**. Открывается страница **Книга операций по ресурсам** с результатом учета журнала ресурсов.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Учет строк табеля в журнале работ
После утверждения операций табеля для работы можно выполнять их учет в соответствующем журнале работ.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал работ**, затем выберите соответствующую ссылку.  
2. Выберите действие **Предлагать строки из табелей**.  
3. Заполните соответствующим образом поля.  
4. Нажмите кнопку **ОК**. Операции для использования создаются в журнале работ, в котором можно изменить информацию как нужно.  

    > [!NOTE]  
    >   Информация о типе работы и о том, оплачивается ли эта работа, копируется из строки табеля. Если необходимо, можно сократить количество и выполнить частичный учет. Если уменьшить количество, то в следующий раз при выборе действия **Предлагать строки из табелей** создаваемая строка будет содержать остаток часов.  
5. Выберите действие **Учет**.  
6. Чтобы проверить учет, выберите действие **Книга операций**. Открывается страница **Книга операций по работам** с результатом учета журнала ресурсов.

## <a name="to-archive-time-sheets"></a>Архивирование табелей
После учета табелей их можно поместить в архив для обращения в будущем. Все строки табелей необходимо учесть, прежде чем табель можно будет поместить в архив.

> [!NOTE]  
>   Примечание. Когда архивируется табель учета рабочего времени, он удаляется из списков на страницах **Табели учета рабочего времени** и **Управление табелями учета рабочего времени**.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Переместить табели учета рабочего времени в архив**, затем выберите соответствующую ссылку.  
2. Заполните поля, как требуется, и нажмите кнопку **ОК**.  
3. Для просмотра табелей учета рабочего времени из архива выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Архивы табелей учета рабочего времени** или **Архивы табелей учета рабочего времени руководителя**, затем выберите соответствующую ссылку.

## <a name="see-also"></a>См. также
[Управление проектами](projects-manage-projects.md)  
[Настройка управления проектами](projects-setup-projects.md)    
[Финансы](finance.md)  
[Покупки](purchasing-manage-purchasing.md)         
[Продажи](sales-manage-sales.md)     
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
