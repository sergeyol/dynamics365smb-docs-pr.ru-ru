---
title: Как осуществить трассировку посылок | Документация Майкрософт
description: Используйте службу отслеживания экспедиторов для контроля хода доставки.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b0cf72609a180d271604dd276f840efbc6b1aa6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910659"
---
# <a name="track-packages"></a>Трассировка посылок

Некоторые экспедиторы предоставляют через Интернет услуги, позволяющие отслеживать упаковки, переданные этому агенту. Если организация пользуется услугами одного или нескольких таких экспедиторов, в программе можно настроить определенную базовую информацию и использовать функцию автоматической трассировки для учтенных отгрузок, учтенных счетов продажи, учтенных кредит-нот продажи и учтенных возвратных приходных накладных. Дополнительные сведения см. в разделе [Настройка экспедиторов](sales-how-to-set-up-shipping-agents.md).  

В следующей процедуре показано, как отслеживать пакет из учтенной расходной накладной продажи, но те же шаги применяются для включения отслеживания пакетов со страниц "Учтенный счет продажи", "Учтенная кредит-нота продажи" и "Учтенная возвратная приходная накладная".  

## <a name="to-track-a-package"></a>Трассировка посылки

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Учтенная расх. накладная продажи**, затем выберите соответствующую ссылку.
2. Откройте соответствующую расходную накладную.
3. Выберите действие **Обновить документ**.
4. В поле **Номер трасс. посылки** укажите номер посылки, полученный от экспедитора. При необходимости обновите значение в поле **Экспедитор** и закройте страницу.
5. Выберите действие **Трассировать пакет**.

Браузер по умолчанию открывает страницу отслеживания экспедитора.

## <a name="see-also"></a>См. также

[Настройка экспедиторов](sales-how-to-set-up-shipping-agents.md)  
[Продажи](sales-manage-sales.md)  
[Настройка продаж](sales-setup-sales.md)  
[Отправка документов по электронной почте](ui-how-send-documents-email.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
