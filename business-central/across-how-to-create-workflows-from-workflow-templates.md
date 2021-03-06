---
title: Создание рабочих процессов из шаблонов рабочих процессов | Документация Майкрософт
description: Для экономии времени при создании новых рабочих процессов можно создавать рабочие процессы из шаблонов рабочих процессов.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2ee2dcba364f7b89bae49c3f15f098c51d2c5a3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913550"
---
# <a name="create-workflows-from-workflow-templates"></a>Создание рабочих процессов из шаблонов рабочих процессов
Для экономии времени при создании новых рабочих процессов можно создавать рабочие процессы из шаблонов рабочих процессов.  

 Шаблоны рабочих процессов не подлежат редактированию и существуют в универсальной версии [!INCLUDE[d365fin](includes/d365fin_md.md)]. Коды для шаблонов рабочих процессов, добавленных Майкрософт, имеют приставку "MS-".  

 Другой способ быстрого создания рабочего процесса — импорт существующего рабочего процесса из файла за пределами [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Экспорт и импорт рабочих процессов](across-how-to-export-and-import-workflows.md).  

На странице **Рабочий процесс** создайте рабочий процесс, указав в строках связанные с ним шаги. Каждый шаг состоит из события рабочего процесса, ограниченного условиями события, и отклика рабочего процесса, ограниченного параметрами отклика. Шаги рабочего процесса заполняются посредством заполнения полей в строках рабочего процесса из фиксированных списков значений события и отклика, представляющих сценарии, которые поддерживаются кодом приложения. Дополнительные сведения см. в разделе [Создание рабочих процессов](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Создание рабочего процесса из шаблона рабочего процесса  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Рабочие процессы**, затем выберите соответствующую ссылку.  
2.  Выберите действие **Создать рабочий процесс из шаблона**. Открывается страница **Шаблоны рабочих процессов**.  
3.  Выберите рабочий процесс, а затем нажмите кнопку **ОК**.  

     Откроется страница **Рабочий процесс** для нового рабочего процесса, содержащее всю информацию из выбранного шаблона. Значение в поле **Код** дополняется символами, например "01", которые указывают, что это первый рабочий процесс, созданный на основе шаблона рабочего процесса.  
4.  Для продолжения создания потока операций измените шаги рабочего процесса или добавьте новые. Дополнительные сведения см. в разделе [Создание рабочих процессов](across-how-to-create-workflows.md).  

## <a name="see-also"></a>См. также  
 [Создание рабочих процессов](across-how-to-create-workflows.md)   
 [Экспорт и импорт рабочих процессов](across-how-to-export-and-import-workflows.md)   
 [Просмотр архивированных экземпляров шагов рабочих процессов](across-how-to-view-archived-workflow-step-instances.md)   
 [Удаление рабочих процессов](across-how-to-delete-workflows.md)   
 [Пошаговое руководство. Настройка и использование рабочего процесса утверждения покупки](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Настройка рабочих процессов](across-set-up-workflows.md)   
 [Использование рабочих процессов](across-use-workflows.md)   
 [Рабочий процесс](across-workflow.md)   
