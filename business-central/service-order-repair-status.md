---
title: Настройка статусов для сервисных заказов и ремонтных работ | Документация Майкрософт
description: Необходимо настроить девять параметров статуса ремонта, которые указывают продвижение ремонта и обслуживания сервисных товаров в сервисных заказах.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c4dd1916f60c424d93d4e225aa87830d34a1fff
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915240"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Как настраивать статусы для сервисных заказов и ремонтных работ
Необходимо настроить параметры статуса ремонта, которые указывают продвижение ремонта и обслуживания сервисных товаров в сервисных заказах. Необходимо настроить по крайней мере девять параметров статуса ремонта, указывающих ситуации или действия, производимые с сервисными товарами.  

Можно задать уровень приоритета для параметров статуса сервисного заказа. Имеется четыре приоритета: "Высокий", "Выше Среднего", "Ниже Среднего" и "Низкий".  

При изменении статуса ремонта сервисного товара в сервисном заказе статус сервисного заказа обновляется. Статус ремонта каждого сервисного товара связан со статусом сервисного заказа. Если сервисные товары связаны с двумя или более параметрами статуса сервисного заказа, то выбирается статус сервисного заказа с наиболее высоким приоритетом.  

## <a name="to-set-up-a-repair-status"></a>Настройка статуса ремонта  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Статус ремонта**, затем выберите соответствующую ссылку.
2. Создать новый статус ремонта.  
3. Заполните поля **Код** и **Описание**.  
4. В поле **Статус сервисного заказа** выберите статус заказа, с которым требуется связать статус ремонта. В поле **Приоритет** отображается приоритет выбранного статуса сервисного заказа.  
5. Выберите статус ремонта. Можно выбрать только один.  
6. Выберите поле **Учет разрешен**, чтобы можно было учитывать сервисные заказы с этим статусом ремонта, включая сервисные товары.  
7. Выберите флажок **Статус ожидания разрешен**, чтобы иметь возможность менять вручную параметр статуса сервисного заказа на **Ожидание** в сервисных заказах с этим статусом ремонта, включая сервисные товары.  
8. Выберите флажки **Статус В работе разрешен**, **Статус Завершено разрешен** и **Статус На удержании разрешен** таким же образом.
  
## <a name="to-set-up-service-status-priorities"></a>Настройка приоритетов сервисных статусов  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Статус сервисного заказа**, затем выберите соответствующую ссылку.  
2. Выберите статус сервисного заказа, которому необходимо назначить приоритет.  
3. В поле **Приоритет** выберите тот приоритет, который хотите назначить этому статусу сервисного заказа. Повторите этот шаг для каждого статуса.  

## <a name="see-also"></a>См. также  
[Статус сервисного заказа и ремонта](service-service-order-status-and-repair-status.md)  
[Настройка управления сервисным обслуживанием](service-setup-service.md)  
