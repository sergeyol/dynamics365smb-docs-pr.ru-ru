---
title: "Обзор задач управления кредиторской задолженностью | Microsoft Docs"
description: "Описываются задачи управления кредиторской задолженностью, например, оплата кредиторам или применение исходящих платежей к операциями книг для закрытия счетов или кредит-нот."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5482579cb453b119be1b6eb5c24d5adc9441ea8b
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a>Управление кредиторской задолженностью
Большая часть управлении кредиторской задолженностью заключается в оплате поставщикам или в возмещении расходов, понесенных сотрудниками. Вы можете использовать функции для добавления строк платежей в счета покупки к оплате в окне **Журнал платежей**. Чтобы отправить транзакции в банк, вы можете экспортировать несколько строк журнала платежей в файл, а затем отправить файл в банк. Кроме того, вы можете осуществлять оплату с помощью платежных документов, в том числе через электронные платежи.

Еще одна типичная задача — применение исходящих платежей к соответствующим операциям книги поставщиков или сотрудников, чтобы закрывать счета, кредит-ноты покупки или счета сотрудников как оплаченные. Эту задачу можно выполнять в окне **Журнал выверки платежей**, импортировав файл банковской выписки для регистрации платежей. Платежи применяются к открытым операциям книги поставщиков, клиентов или сотрудников путем сопоставления текста платежа и информации операции. Существуют различные способы просмотреть и изменить сопоставления перед учетом журнала. Вы можете закрыть любую открытую операцию книги банковских счетов, связанную с примененными операциями книги, при учете журнала. Банковский счет автоматически выверяется после применения всех платежей.

Кроме того, можно применять исходящие платежи вручную в окне **Журнал платежей** или из соответствующих операций книги поставщиков или сотрудников.

В следующей таблице приводится последовательность задач с кредиторской задолженностью со ссылками на разделы, в которых они описываются.

| Действие | Ссылка |
| --- | --- |
| Создавайте причитающиеся выплаты поставщиками или выплаты для возмещения расходов сотрудников, подготавливайте платежи чеками и экспортируйте платежи в банковский файл при учете. |[Осуществление платежей](payables-make-payments.md) |
| Автоматическое применение платежей поставщикам к неоплаченным счетам покупки путем импорта файла банковской выписки. |[Автоматическое применение платежей и выверка банковских счетов](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Применение платежей поставщикам к неоплаченным счетам покупки вручную. |[Выверка платежей поставщикам вручную](payables-how-apply-purchase-transactions-manually.md) |
|Проверьте правильность переоценки запасов, назначив дополнительную себестоимость товаров, например за транспортировку, физическое обращение, страхование и другие расходы, которые вы несли при покупке.|[Использование товарных издержек для учета дополнительных торговых расходов](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>См. также
[Покупки](purchasing-manage-purchasing.md)  
[Управление дебиторской задолженностью](receivables-manage-receivables.md)  
[Использование товарных издержек для учета дополнительных торговых расходов](payables-how-assign-item-charges.md)  
[Общие бизнес-функции](ui-across-business-areas.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
