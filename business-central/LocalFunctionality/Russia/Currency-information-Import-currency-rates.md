---
title: Информация о валюте в России
description: Российские улучшения включают информацию о валюте для импорта курсов валют.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 2c3b8151598865eac1a3405322e688a1e4df3ab8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921314"
---
# <a name="currency-information-import-currency-rates"></a>Информация о валюте, импорт курсов валют

Информация о местной валюте для печатных форм указана в **Настройка ГК**.

Используемые поля на вкладке **Общее**:

- Код местной валюты
- Описание местной валюты

### <a name="import-currencies"></a>Импорт валют

Выберите **Информация об организации**. Заполните поля:

| Поле                          | Описание                                                  |
| ------------------------------ | ------------------------------------------------------------ |
| **Импорт валютных курсов**   | Определяет, имеется ли возможность выполнить пакетное задание "Импорт курсов валют". |
| **Разрешение конфликтов при импорте** | Определяет, что произойдет, если пользователь выполнит пакетное задание "Импорт курсов валют" и будут обнаружены конфликтующие курсы валют. |

Выберите **Валюта**. На вкладке **Общие** заполните поля для каждой валюты:

| Поле                    | Описание                                                  |
| ------------------------ | ------------------------------------------------------------ |
| **Импорт**               | Определяет, содержит ли валюта импортированный курс валют.     |
| **Код банка (Россия)**         | Определяет код российского банка, который связан с валютой. |
| **Цифровой код банка (Россия)** | Определяет цифровой код российского банка, который связан с валютой. |

##### <a name="import-currency-rates"></a>Импорт курсов валют:

1. Выберите Подразделения -> Финансовый менеджмент -> Периодические операции -> Валюта -> Импорт курсов валют.

2. Введите даты начала и окончания периода, для которого вы хотите скорректировать обменные курсы.

## <a name="see-also"></a>См. также

[Коррекция Курс. Разниц](Adjust-Exchange-Rates.md)  
[Функциональность локальной версии для России](russia-local-functionality.md)  
