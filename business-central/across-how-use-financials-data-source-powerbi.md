---
title: "Настройка отчетов для Business Central в Power BI | Документы Майкрософт"
description: "Можно сделать данные Financials доступными в качестве источника данных в Power BI и создать мощные отчеты о состоянии вашего бизнеса."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/03/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: c7782d6f74a56f72b40dfb6cfd59a44ab4a33ae7
ms.contentlocale: ru-ru
ms.lasthandoff: 05/17/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Использование [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] как источника данных Power BI для создания отчетов
Можно сделать данные [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] доступными в качестве источника данных в Power BI и создать мощные отчеты о состоянии вашего бизнеса.  

Вы должны иметь допустимую учетную запись в [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] и в Power BI. Кроме того, необходимо загрузить [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Добавление [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] как источника данных в Power BI Desktop
1. В Power BI Desktop в левой области навигации выберите **Получить данные**.
2. В окне **Получить данные** выберите **Веб-службы**, выберите **Microsoft Dynamics 365 Business Central**, затем нажмите кнопку **Подключиться**.
3. Power BI отобразит мастер с руководством по [процессу подключения](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Будет предложено выполнить вход в службу. Выберите **Войти** и выберите учетную запись для входа. Это должна быть та же учетная запись, которая использовалась для входа в [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Нажмите кнопку **Подключиться**, чтобы продолжить. Мастер Power BI отобразит список организаций и источников данных Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Эти источники данных представляют все веб-службы, которые вы опубликовали из каждой организации в Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Либо создайте новый URL-адрес веб-службы в [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], используя действие **Создать набор данных** на странице **Веб-службы** с помощью руководства по сопровождаемой настройке **Настройка отчетов** либо используя действие **Изменить в Excel** в любом списке.
6. Укажите данные, которые требуется добавить в модель данных, а затем нажмите кнопку **Загрузить**.
7. Повторите предыдущие шаги для добавления дополнительных данных Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] или других данных в модель данных Power BI.

> [!NOTE]  
> После успешного подключения к Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] выполнять повторный вход не требуется.

После загрузки данные отобразятся в правой области навигации на странице. На этом шаге вы успешно подключились с данным Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] и готовы начать создание отчета Power BI. 

Перед построением отчета рекомендуется импортировать файлы темы Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Файл темы создаст цветовую палитру, чтобы можно было создавать отчеты с таким же цветовым стилем, что и пакет содержимого Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] без необходимости определения настраиваемых цветов для каждого визуального элемента.

Дополнительные сведения см. в разделе [Документация Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>См. также
[Бизнес-аналитика](bi.md)  
[Приступая к работе](product-get-started.md)  
[Импорт бизнес-данных из других финансовых систем](across-import-data-configuration-packages.md)  
[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Финансы](finance.md)  
[Подключение Power BI к [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
