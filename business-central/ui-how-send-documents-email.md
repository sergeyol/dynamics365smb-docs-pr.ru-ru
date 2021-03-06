---
title: Настройка содержимого электронной почты, зависящего от документа | Документация Майкрософт
description: Вы можете определить содержимое для вставки в текст сообщения электронной, например ссылку на PayPal. Вы также можете вкладывать документы в сообщения электронной почты.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72ed1cba131e76eba2020e4cca9c900b9b2ed45c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923424"
---
# <a name="send-documents-by-email"></a>Отправка документов по электронной почте

Для быстрой передачи содержимого деловых документов вашим бизнес-партнерам, например информации о платеже в документах продажи клиентам, можно использовать функцию макетов отчетов, чтобы определять зависящее от вида документа содержимое, которое автоматически вставляется в текст сообщения электронной почты. Дополнительные сведения см. в разделе [Управление макетами отчетов и документов](ui-manage-report-layouts.md).

Чтобы включить сообщения электронной почты в [!INCLUDE[d365fin](includes/d365fin_md.md)], в ролевом центре запустите мастер настройки **Настройка электронной почты**.

Отправлять по электронной почте можно практически все типы документов в виде вложений непосредственно со страницы, содержащего документ. В дополнение к вложениям вы можете включать в текст сообщения электронной почты основную информацию из документа после стандартного текста с обращением к получателю и вводной информации о документе. Чтобы предложить клиентам оплатить покупку с помощью электронной службы платежей, например PayPal, вы можете включить в тело сообщения гиперссылку на PayPal.

Из всех поддерживаемых документов отправка электронной почты инициируется действием **Отправить** для учтенных документов и **Учесть и отправить** для неучтенных документов.

Если в поле **Эл. почта** страницы **Кому отправить документ** установлено значение **Да (запросить настройки)**, то откроется страница **Отправить сообщение эл. почты** с заполненным полем **Кому:** и документом, приложенным в виде PDF-файла. В поле **Содержание** вы можете либо ввести текст вручную или заполнить его настроенным текстом, связанным с типом документа.

Ниже показано, как настроить отчет **Продажи - счет**, чтобы использовать готовый текст при отправке по электронной почте учтенных счетов.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Настройка содержания сообщения электронной почты для счетов продажи

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Выбор отчета - продажи**, затем выберите соответствующую ссылку.
2. На странице **Выбор отчета - продажи** в поле **Использование** выберите **Счет**.
3. В новой строке в поле **Код отчета** выберите, например, стандартный отчет 1306.
4. Установите флажок **Использовать для содержания сообщения электронной почты**.
5. Выберите поле **Код макета содержания сообщения электронной почты**, а затем выберите макет из раскрывающегося списка.

    Макеты отчетов определяют стиль и содержимое сообщений электронной почты, включая стандартный текст, который предшествует информации из основного документа в теле сообщения электронной почты. Можно просмотреть все доступные макеты отчетов, если нажать кнопку **Выбор из полного списка** в раскрывающемся списке.
6. Чтобы просмотреть или изменить макет содержания сообщения электронной почты, выберите макет на странице **Пользовательские макеты отчетов** выберите действие **Изменить макет**.
7. Если вы хотите предложить клиентам оплатить покупку с помощью электронной службы платежей, вы можете настроить электронную службу платежей, например PayPal, и включить в тело сообщения гиперссылку на PayPal. Дополнительные сведения см. в разделе [Включение платежей клиентов через PayPal](sales-how-enable-payment-service-extensions.md).
8. Нажмите кнопку **ОК**.

Теперь, когда вы выбираете, например, действие **Отправить** на странице **Учтенный счет продажи**, содержание сообщения электронной почты будет включать информацию из отчета 1306, перед которой будет расположен стандартный текст в соответствии с макетом отчета, выбранном на шаге 5.

Следующая процедура описывает, как отправить учтенный счет продажи в виде сообщения электронной почты с документом, вложенным в виде файла PDF, и с телом сообщения на базе этого документа.

## <a name="to-send-documents-by-email"></a>Отправка документов по электронной почте

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Учтенные счета продаж**, затем выберите соответствующую ссылку.
2. Укажите соответствующий разнесенный счет продажи и выберите действие **Отправить**. Откроется страница **Кому отправить документ**.
3. В поле **Эл. почта** выберите **Да (запросить настройки)**. Дополнительные сведения см. в разделе [Настройка профилей отправки документов](sales-how-setup-document-send-profiles.md).
4. Нажмите кнопку **ОК**. Откроется страница **Отправить сообщение эл. почты**.
5. В поле **Кому:** введите допустимый адрес электронной почты. Значение по умолчанию — адрес электронной почты клиента.
6. В поле **Тема** введите описательный текст темы. Значение по умолчанию — имя и номер счета клиента.
7. В поле **Вложение** созданный счет по умолчанию прикрепляется как PDF-файл.
8. В поле **Содержание** введите краткое сообщение получателю.

    Если на странице **Выбор отчета - продажи** настроено содержание сообщения электронной почты, связанное с документом, поле **Содержание** заполняется автоматически. Дополнительные сведения см. в разделе [Настройка содержания сообщения электронной почты для счетов продажи](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Нажмите кнопку **ОК** для отправки сообщения электронной почты.

> [!NOTE]  
> Если вам не нужно указывать параметры электронной почты при каждой отправке документа, вы можете выбрать вариант **Да (использовать настройки по умолчанию)** в поле **Эл. почта** на странице **Кому отправить документ**. В этом случае страница **Отправить сообщение эл. почты** открываться не будет. См. шаг 4. Дополнительные сведения см. в разделе [Настройка профилей отправки документов](sales-how-setup-document-send-profiles.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Документы, помеченные как распечатанные при отправке

Некоторые документы в [!INCLUDE[prodshort](includes/prodshort.md)] имеют поле, которое указывает, сколько раз этот документ был напечатан. Это поле также обновляется, если вы не печатаете документ, а отправляете его по электронной почте. Поле даже обновляется, если вы на самом деле не отправляете документ, например, когда ваша организация не настроила электронную почту или если контакт, которому вы хотите отправить документ, не имеет адреса электронной почты в списке. Во всех сценариях с использованием [!INCLUDE[prodshort](includes/prodshort.md)] документ печатается, поскольку создается файл PDF.  

Пользователь может не увидеть этот сгенерированный файл, но именно поэтому поле обновляется.

## <a name="see-also"></a>См. также

[Управление макетами отчетов и документов](ui-manage-report-layouts.md)  
[Настройка электронной почты](admin-how-setup-email.md)  
[Выставление счетов продажи](sales-how-invoice-sales.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
