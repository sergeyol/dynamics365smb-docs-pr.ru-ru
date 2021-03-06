---
title: Настройка взаимодействия с пользователем для отображения или скрытия расширенных функций | Документация Майкрософт
description: Узнайте о вариантах настройки Essential и Premium — что это значит с точки зрения пользовательского интерфейса, областей приложения и вашей организации.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1e4de0f59788bb49ebaead7a4ee2516ff32147eb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912450"
---
# <a name="change-which-features-are-displayed"></a>Изменение набора отображаемых функций
[!INCLUDE[d365fin](includes/d365fin_md.md)] разработан, чтобы помочь вам вести свой бизнес независимо от размера и сложности. В основе продукта вы найдете такие важные функции, как финансовая отчетность, продажи, закупки и управление запасами. По мере увеличения сложности бизнеса вы можете, например, включить функциональность для управления производством и обслуживанием.

Вы можете определить уровень сложности продукта и, следовательно, к каким функциям пользователи компании получают доступ, изменив настройку **Функциональность** на странице **Информация о компании**. Обратите внимание, что настройку функциональности также можно изменить, добавив определенные расширения из AppSource. Дополнительные сведения см. в разделе [Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md).

В следующей таблице перечислены типы взаимодействия, доступные в настоящий момент.

| Функциональность | Влияние на пользовательский интерфейс |
| --- | --- |
| **Essential** |Отображаются все действия и поля для всех общих функций бизнеса.|
| **Премиум** |Показывает все действия и поля для всех бизнес-функций, включая управление производством и обслуживанием.|

Функциональности, которые можно выбрать в [!INCLUDE[d365fin](includes/d365fin_md.md)], отражают лицензии решения, называемые планами, которые определены для продукта. Сведения о планах Essential и Premium см. в разделе [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) на маркетинговом сайте Microsoft Dynamics 365. См. также [Руководство по лицензированию [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?linkid=2068931) (требуется доступ к CustomerSource или PartnerSource).

> [!IMPORTANT]  
> Все обычным пользователям решения должен быть назначен один и тот же план — Essential или Premium — прежде чем для компании можно будет выбрать соответствующую функциональность. Соответственно, один пользователь не может иметь доступ к функциональным компонентам Premium, если другой пользователь (или несколько других пользователей) имеют доступ только к функциональным компонентам Essential. Это не относится к пользователям типа "Член группы", "Внутренний администратор", "Внешний бухгалтер", "Делегированный администратор", который может быть назначен другой план, не такой, как остальным пользователям в решении.<br /><br /> Только пользователи типа Evaluation или Premium могут изменять значение в поле **Функциональность** с Essential на Premium.

Прежде чем определить настройку взаимодействия с компанией, вы определяете доступ пользователей к определенным функциям и страницам, назначая наборы разрешений. Дополнительные сведения см. в разделе [Назначение разрешений пользователям и группам](ui-define-granular-permissions.md).

Параметр **Функциональность** применяется ко всем пользователям в компании, но каждый пользователь может дополнительно персонализировать свой собственный опыт, изменяя макеты страниц и контент. Дополнительные сведения см. в разделе [Персонализация рабочей области](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Включение функций Premium после перехода на план Premium
Пользователи назначаются планам в Центре администрирования Microsoft 365 в ходе общей работы по созданию пользователей Business Central. Для получения дополнительной информации см. раздел [Добавление пользователей по отдельности или массово Microsoft 365](https://support.office.com/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

### <a name="to-update-plan-changes-in-users-groups"></a>Обновление в соответствии с изменением плана в группах пользователей
После внесения изменения в планы пользователей в Центре администрирования Microsoft 365, например назначения дополнительных пользователей плану Premium, это изменение необходимо отразить в [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Войдите в систему в качестве администратора.
2. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Пользователи**, затем выберите соответствующую ссылку.
3. На странице **Пользователи** выберите действие **Обновить все группы пользователей**.

Вся новая информация о планах пользователей и назначенных им группах пользователей теперь обновляется в соответствии с изменениями в плане.

### <a name="to-select-the-premium-experience"></a>Выбор функциональности Premium
Теперь можно переходить к выбору новой функциональности.
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Информация о компании**, затем выберите соответствующую ссылку.
2. На странице **Информация о компании** на экспресс-вкладке **Опыт пользователя** выберите Premium в поле **Функциональность**.

## <a name="help-assumes-premium-experience"></a>Справка предполагает уровень Premium
Все описания функций в пользовательской документации для [!INCLUDE[d365fin](includes/d365fin_md.md)] предполагают наличие уровня **Premium**, то есть описание охватывает полный набор элементов пользовательского интерфейса.

## <a name="see-also"></a>См. также
[Персонализация рабочей области](ui-personalization-user.md)  
[Настройка Business Central](ui-customizing-overview.md)  
[Назначение разрешений пользователям и группам](ui-define-granular-permissions.md)  
[Создание новых организаций](about-new-company.md)  
[Изменение базовых настроек](ui-change-basic-settings.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Руководство по лицензированию](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
