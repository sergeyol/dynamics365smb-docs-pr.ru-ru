---
title: Настройка расчета налоговых разниц в России
description: Российские усовершенствования включают расчет налоговых разниц по основным средствам.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 5da77cb6a2eb091aee4ba199ed5b54e28229ba3f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919759"
---
# <a name="setting-up-tax-difference-calculation"></a>Настройка расчета налоговых разниц

Расчет налоговых разниц необходимо настроить, если имеется налоговая разница в представлении операций с основными средствами, операций себестоимости товаров или финансовых операций в бухгалтерском и налоговом учете, для которых необходимо зафиксировать расходы, подлежащие списанию. Чтобы настроить налоговую разницу, выберите действие **Настройка**, а затем выберите действие **Налоговые разницы**.

## <a name="setting-up-posting-groups"></a>Настройка учетных групп

В пункте меню **Учетные группы налоговых разниц** необходимо указать финансовые счета из настроенного плана счетов, на которых будут учитываться финансовые транзакции с налоговыми разницами.

Если имеются строки журнала, которые необходимо нормализовать перед списанием расходов, эти журналы невозможно учесть без запуска периодического задания нормализации.

В следующей процедуре показан порядок обработки функции нормализации.

1. В окне **Журнал расходов будущих периодов** выберите **Расчет нормируемой амортизации** .
2. В окне **Расчет аморт. РБП по норм.** на экспресс-вкладке **Налоговая разница** установите фильтр для налоговой разницы.
3. На экспресс-вкладке **Параметры** введите учетный период, для которого выполняется расчет.
4. Для печати отчета выберите действие **Печать**.
5. Выполните операцию учета журнала расходов будущих периодов.

## <a name="see-also"></a>См. также

[Налоговые регистры](Tax-Registers.md)  
[Налоговые разницы](Tax-Differences.md)  
[Регистры налоговых разниц](Tax-Difference-Registers.md)  
[Настройка юрисдикций нормы](How-to-Set-Up-Norm-Jurisdictions.md)  
[Учет налоговых разниц](How-to-Post-Tax-Differences.md)  
