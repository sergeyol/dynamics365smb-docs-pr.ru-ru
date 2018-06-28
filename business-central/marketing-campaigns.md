---
title: "Настройка маркетинговых кампаний в Business Central | Документы Майкрософт"
description: "Описывается, как можно настраивать и проводить маркетинговые кампании в Business Central, чтобы помочь выявить и привлечь потенциальных клиентов, а также сохранить существующих."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4c3f0f612c13d9fe84cffc4862641301795bcebd
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="managing-marketing-campaigns"></a>Управление маркетинговыми кампаниями
Наличие эффективного маркетингового плана помогает определять, привлекать и удерживать клиентов. Маркетинговый план состоит из различных кампаний и других видов взаимодействия, связанных с действиями по продажам и маркетингу. Планируя кампанию, необходимо решить, на какие контакты она будет ориентирована, какого она будет типа (скажем, специализированная выставка или прямая почтовая рассылка) и кто из менеджеров будет выполнять каждую задачу.

Каждая кампания состоит из последовательности действий и задач. Вы можете объединять задачи, например отдельные шаги, в действия. Задачи действий связаны друг с другом с помощью формулы даты. Отдельные задачи можно назначать только менеджерам по продажам. Действия можно назначать возможным сделкам, менеджерам по продажам, группам менеджеров и контактам. Дополнительные сведения см. в разделе [Настройка циклов продаж и этапов циклов](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Определение отдельных кампаний
Прежде чем создавать кампанию, необходимо настроить *коды статуса кампаний*. Их использование поможет управлять кампаниями путем назначения им статусов. Переходя от одного этапа кампании к другому, вы сможете видеть, на каком из них вы сейчас находитесь и какой этап следует за ним. Коды статуса кампаний настраиваются в окне **Статус кампании**.

Можно создать карточку кампании для каждой кампании, которую требуется отслеживать. Просмотр карточки кампании позволяет получить общие сведения о ней.
Можно удалить операции кампании, например, если некоторое действие в операции было зарегистрировано, но отменено. Можно удалить только отмененные операции кампаний.

### <a name="selecting-the-target-audience"></a>Выбор целевой аудитории
После создания кампании можно начинать создание сегментов, указывающих целевую аудиторию кампании. Дополнительные сведения см. в разделе [Управление сегментами](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Регистрация процентов скидки
При настройке кампании определите, какие сегменты необходимы при работе с данной кампанией, и настройте дату начала и дату окончания. Затем выполните регистрацию процента скидки, которую получит клиент на отдельные товары в строках окна **Скидки строки продажи**. Можно также зарегистрировать цены продажи для отдельных товаров в строках в окне **Цены продажи**. Доступ к обоим окнам можно получить из карточки кампании.

 При настройке цены продажи/скидки строки и сегментов на карточке кампании необходимо их активизировать для отражения в строках цен/скидок кампании.

> [!NOTE]  
>   Для активации цены продажи/скидки строки необходимо указать, что входит в целевую аудиторию кампании: весь сегмент или только некоторые контакты. Если цены продажи/скидки строки охватывают все контакты в сегменте, выберите поле **Цель кампании** на экспресс-вкладке **Кампания** карточки **Сегмент**.

Если цены продажи/скидки строки предлагаются не всем контактам в сегменте, можно снять флажок в поле **Цель кампании** для соответствующих контактов. Если это поле не отображается, его можно добавить в представление. Дополнительные сведения см. в разделе [Персонализация рабочей области](ui-personalization-user.md).

## <a name="conducting-campaigns"></a>Проведение кампаний
В ходе кампании все взаимодействия с контактами или сегментами записываются. Это позволяет вам получать статистику или другие сведения о затратах и успешности кампании.

Кампании проводятся менеджерами по продажам, поэтому вам нужно создать действия, представляющие каждую задачу, и назначить их соответствующим менеджерам по продажам. Дополнительные сведения см. в разделе [Настройка циклов продаж и этапов циклов](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>См. также
[Управление контактами](marketing-contacts.md)  
[Управление сегментами](marketing-segments.md)  
[Управление возможностями продаж](marketing-manage-sales-opportunities.md)  
[Работа с Business Central](ui-work-product.md)  
