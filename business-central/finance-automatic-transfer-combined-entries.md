---
title: "Автоматическое перемещение и объединенные операции | Документы Майкрософт"
description: "В модуле \"Учет затрат\" можно переместить операции Главной книги по типу затрат с помощью комбинированного учета. В поле **Объединить операции** в определении типа затрат можно указать, используются ли для типа затрат объединенные операции. В следующей таблице описаны разные параметры."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4f1bcf009b397438bb302a16a23be2f4638cefc4
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Автоматическое перемещение и объединенные операции
В модуле "Учет затрат" можно переместить операции Главной книги по типу затрат с помощью комбинированного учета. В поле **Объединить операции** в определении типа затрат можно указать, используются ли для типа затрат объединенные операции. В следующей таблице описаны разные параметры.  

|Объединить операции|Описание|  
|---------------------|-----------------|  
|Нет|Каждая операция Главной книги переносится по отдельности на соответствующий тип затрат.|  
|День|Записи Главной книги с одной и той же датой учета переносятся как одна операция на соответствующий тип затрат.|  
|Месяц|Все операции Главной книги в одном и том же календарном месяце переносятся как одна операция на соответствующий тип затрат.|  

> [!IMPORTANT]  
>  Если установлен флажок **Автоматический перенос из ГК** в окне **Настройка учета затрат**, [!INCLUDE[d365fin](includes/d365fin_md.md)] обновляет учет затрат после каждого учета в главной книге. Объединенные операции невозможны.  

## <a name="see-also"></a>См. также  
 [Перенос операций ГК в операции затрат](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Критерии для переноса операций главной книги в операции затрат](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Результаты перемещения](finance-results-of-the-transfer.md)   
 [Перемещение и операции учета затрат](finance-transfer-and-post-cost-entries.md)  
 [Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
