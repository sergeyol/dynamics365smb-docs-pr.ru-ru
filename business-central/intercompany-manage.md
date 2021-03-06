---
title: Транзакции между компаниями в одной организации | Документация Майкрософт
description: С помощью функции межфирменного учета можно упростить бизнес-процессы и транзакции между компаниями в пределах одной организации.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 070ffe0a25791f8fee51e0e4279a3886a3f18135
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924032"
---
# <a name="managing-intercompany-transactions"></a>Управление межфирменными транзакциями
Ваша организация может состоять из нескольких компаний, но не иметь соответствующего количества бухгалтерских и административных отделов. Функция межфирменного учета позволяет вести дела с филиалами и внутренними партнерскими организациями таким же образом, как с внешними поставщиками и клиентами. Ввод данных о транзакциях с аффилированной организацией в соответствующих документах осуществляется только один раз. Вы можете использовать уже знакомые функции, например, управление расчетами с клиентами и поставщиками. Средства сопоставления для плана счетов и измерения помогают обеспечить отображение данных в нужных местах.  

Существует четыре основных преимущества использования функции межфирменного учета:  

- Увеличение производительности в результате экономии времени и упрощения транзакций  
- Минимизация вероятности ошибок при однократном вводе информации и автоматических обновлений на системном уровне  
- Полный журнал аудита, полное видение бизнес-процессов и истории транзакций  
- Эффективные, экономичные транзакции с филиалами и дочерними организациями  

Вы полностью контролируете все документы по транзакциям. Например, вы можете отклонить отправленный вам документ и тем самым сторнировать учет в журнале и отменить приходные/расходные накладные, которые оказались неверными. Или, в случае покупки у партнера или дочерней компании, можно обновлять заказ на покупку до тех пор, пока продавец не отгрузит товары.  

При вводе транзакции нет необходимости указывать счета для отдельных наборов журналов, достаточно дать идентификатор организации-партнера. Функция межфирменного учета создает строки финансового журнала, которые обеспечивают балансировку журналов обеих организаций, участвующих в транзакции. В счетах дебиторов и кредиторов пользователь назначает межфирменный код партнера любому клиенту или поставщику. Начиная с этого момента все генерируемые заказы и счета, относящиеся к транзакциям с этими организациями, генерируют документы в партнерской организации с правильным сальдо счетов.  

 Создав в системе бизнес-партнеров в качестве клиентов и поставщиков, и назначив им коды партнеров по межфирменным операциям, можно обмениваться межфирменными документами покупок и продаж, включая товары и номера товарных издержек. Функция межфирменного учета обеспечивает межфирменные транзакции между несколькими базами данных, например в разных странах или регионах, а также в разных валютах, разных планах счетов, разных измерениях и при различной нумерации товаров.  

Консолидация финансовых данных может быть особенно уместна в связи с процессами между организациями. Дополнительные сведения см. в разделе [Консолидация финансовых данных из нескольких организаций](finance-consolidated-company-reporting.md).

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.

 |По |Ссылка|
 |---|---|
 |Создание межфирменных поставщиков и клиентов как так называемых межфирменных партнеров (партнеры МФ) и настройка межфирменного плана счетов.|[Настройка межфирменных взаимодействий](intercompany-how-setup.md)|
 |Использование межфирменных документов или журналов для учета транзакций, выполненных с межфирменными партнерами.|[Работа с межфирменными документами и журналами](intercompany-how-work-documents-journals.md)|
 |Упорядочение и обработка входящих и исходящих транзакций, которыми вы обмениваетесь с межфирменными партнерами.|[Управление межфирменными входящими и исходящими ящиками](intercompany-how-manage-intercompany-inbox.md)|

## <a name="see-also"></a>См. также
[Финансы](finance.md)  
[Настройка финансов](finance-setup-finance.md)  
[Работа с финансовыми журналами](ui-work-general-journals.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
