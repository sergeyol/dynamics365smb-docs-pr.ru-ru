---
title: Настройка регистрации электронной почты | Документация Майкрософт
description: Узнайте, как превратить взаимодействие по электронной почте между продавцами и клиентами в реальные возможности продаж.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: e325cce98256b723c6fcfdf4d16068f852a2b032
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308744"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="1bdd1-103">Отслеживание обмена сообщениями электронной почты между продавцами и контактами</span><span class="sxs-lookup"><span data-stu-id="1bdd1-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="1bdd1-104">Получите больше от общения между продавцами и вашими существующими или потенциальными клиентами, отслеживая обмен сообщениями электронной почты, затем превращая их в реальные возможности.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1bdd1-105">может работать с Exchange Online, чтобы вести журнал входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="1bdd1-106">Вы можете просматривать и анализировать содержимое каждого сообщения на странице **Журналы взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a><span data-ttu-id="1bdd1-107">Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] для регистрации сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="1bdd1-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="1bdd1-108">Начните работать с регистрацией электронной почты за два простых шага:</span><span class="sxs-lookup"><span data-stu-id="1bdd1-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="1bdd1-109">Соедините [!INCLUDE[d365fin](includes/d365fin_md.md)] с Exchange Online для подписки Office 365.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="1bdd1-110">Exchange Online обрабатывает ваши сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="1bdd1-111">Мы упростили этот шаг, предоставив мастер настройки.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="1bdd1-112">Вам просто нужны ваши учетные данные администратора для вашей учетной записи администратора в Office 365.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="1bdd1-113">Чтобы запустить руководство, выберите **Мастер настройки**, затем выберите **Настройка регистрации электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="1bdd1-114">Убедитесь, что действительные адреса электронной почты были введены в [!INCLUDE[d365fin](includes/d365fin_md.md)] для ваших продавцов и контактов, в зависимости от того, являются ли они потенциальными или существующими клиентами.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="1bdd1-115">Для этого для каждого клиента или продавца откройте карточку **Контакт** или **Менеджер по продажам/закупкам** и посмотрите в поле **Адрес эл. почты**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="1bdd1-116">После выполнения шагов в руководстве вы можете проверить, было ли соединение успешным.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="1bdd1-117">Выполните поиск **Настройка модуля "Маркетинг"**, выберите **Процесс**, затем **Функции**, потом **Проверить настройку регистрации эл. почты**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="1bdd1-118">Просмотр обмена сообщениями электронной почты в журнале взаимодействия</span><span class="sxs-lookup"><span data-stu-id="1bdd1-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1bdd1-119">создает запись на странице **Журнал взаимодействия** каждый раз, когда продавец и контакт обмениваются сообщениями электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="1bdd1-120">Чтобы просмотреть журнал взаимодействия, откройте карточку **Контакт** или **Менеджер по продажам/закупкам** для человека, затем выберите **Навигатор**, **История**, затем выберите **Журналы взаимодействий**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="1bdd1-121">Есть несколько вещей, которые мы можем сделать с каждой записью в журнале, например:</span><span class="sxs-lookup"><span data-stu-id="1bdd1-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="1bdd1-122">Просмотрите содержимое сообщения электронной почты, которым обменялись собеседники, нажав действие **Показать вложения**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="1bdd1-123">Превратите обмен электронной почтой в возможность продажи — если запись выглядит многообещающей, вы можете превратить ее в возможность, а затем управлять ее продвижением к продаже.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="1bdd1-124">Для этого выберите запись, затем выберите действие **Создать возможность**.</span><span class="sxs-lookup"><span data-stu-id="1bdd1-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="1bdd1-125">Дополнительные сведения см. в разделе [Управление возможностями продаж](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="1bdd1-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1bdd1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1bdd1-126">See Also</span></span>
[<span data-ttu-id="1bdd1-127">Управление отношениями</span><span class="sxs-lookup"><span data-stu-id="1bdd1-127">Managing Relationships</span></span>](marketing-relationship-management.md)
