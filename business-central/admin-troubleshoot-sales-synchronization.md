---
title: Устранение ошибок синхронизации | Документация Майкрософт
description: Предоставляет некоторые рекомендации по выявлению и устранению ошибок синхронизации.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: db8b05aa74583d8ba74fcfeb8fae1d3c28893fac
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922396"
---
# <a name="troubleshooting-synchronization-errors"></a>Устранение ошибок синхронизации
Интеграция [!INCLUDE[d365fin](includes/d365fin_md.md)] с Common Data Service — сложный процесс, и иногда что-то идет не так. В этом разделе рассказывается о некоторых типичных ошибках, которые могут возникнуть, и даются советы о том, как их исправить.

Ошибки часто возникают либо из-за того, что пользователь что-то сделал со связанными записями, либо из-за неправильной настройки интеграции. Ошибки, относящиеся к связанным записям, пользователи могут устранить самостоятельно. Эти ошибки вызваны такими действиями, как удаление записи в одном, но не в обоих бизнес-приложениях, с последующей синхронизацией. Для получения дополнительной информации см. раздел [Просмотр статуса синхронизации](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Пример
В этом видео показан пример устранения ошибок, возникших при синхронизации с Sales. Процесс будет одинаковым для любой интеграции. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Ошибки, связанные с настройкой интеграции, обычно требуют участия администратора. Вы можете просмотреть эти ошибки на странице **Ошибки синхронизации интеграции**. Примеры некоторых типичных проблем:  
  
* Права и роли, назначенные пользователям, неверны.  
* Учетная запись администратора была указана в качестве пользователя интеграции.  
* Пароль пользователя интеграции настроен так, чтобы требовать смены при входе пользователя в систему.  
* Курсы обмена валют не указаны ни в одном, ни в другом приложении.  
  
Вы должны вручную устранить эти ошибки, но эта страница также может оказаться полезной. Например:  

* Поля **Источник** и **Назначение** могут содержать ссылки на запись, в которой была обнаружена ошибка. Нажмите на ссылку, чтобы открыть запись и изучить проблему.  
* Действия **Удалить записи старше 7 дней** и **Удалить все записи** помогут очистить список. Как правило, эти действия используются после устранения причины ошибки, которая влияет на многие записи. При этом следует соблюдать осторожность. Эти действия могут удалить ошибки, которые все еще актуальны.

Иногда временные метки в записях могут вызывать конфликты. В таблице "Запись интеграции CDS" хранятся временные метки "Время последнего изменения операции синхронизации" и "Время последнего изменения CDS операции синхронизации" для последней интеграции, выполненной в обоих направлениях для записи. Эти временные метки сравниваются с временными метками в записях Business Central и Sales. В Business Central временная метка находится в таблице записей интеграции.

Вы можете фильтровать записи, которые должны быть синхронизированы, сравнивая временные метки записей в таблице "Сопоставление таблиц интеграции" с полями "Синхронизировать измененные по фильтру" и "Синхр. внутр. табл. изм. по флтр."

Сообщение об ошибке конфликта "Невозможно обновить запись клиента, так как у нее более поздняя дата обновления, чем у записи организации." или "Невозможно обновить запись организации, так как у нее более поздняя дата обновления, чем у записи клиента" может произойти, если запись имеет метку времени, которая больше, чем IntegrationTableMapping."Синхронизировать измененные по фильтру", но это не более поздняя версия, чем отметка времени в записи интеграции Sales. Это означает, что исходная запись была синхронизирована вручную, а не записью очереди заданий. 

Конфликт возникает потому, что запись назначения также была изменена — отметка времени записи более поздняя, чем отметка времени в записи интеграции Sales. Проверка назначения происходит только для двунаправленных таблиц. 

Эти записи теперь перемещены на страницу "Пропущенные синхронизированные записи", которую можно найти на странице "Настройка подключения Microsoft Dynamics" в Business Central. Там вы можете указать изменения, которые нужно сохранить, а затем снова синхронизировать записи.

## <a name="remove-couplings-between-records"></a>Удаление связей между записями
Когда что-то пойдет не так с вашей интеграцией и вам нужно разъединить записи, чтобы прекратить их синхронизацию, вы можете сделать это для одной или нескольких записей за раз. На странице **Сопоставления таблиц интеграции** вы можете выбрать **Отмена связывания**, а потом **Удалить связь**. Как вариант, на странице **Ошибки синхронизации связанных данных** вы можете выбрать ошибки, а затем выбрать **Удалить связи**. 

## <a name="see-also"></a>См. также
[Интеграция с Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Настройка учетных записей пользователя для интеграции с Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Настройка подключения к Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Связывание и синхронизация записей вручную](admin-how-to-couple-and-synchronize-records-manually.md)  
[Просмотр статуса синхронизации](admin-how-to-view-synchronization-status.md)  
