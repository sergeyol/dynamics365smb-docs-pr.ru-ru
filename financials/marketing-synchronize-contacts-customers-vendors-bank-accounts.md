---
title: "Синхронизация контактов с клиентами и поставщиками | Документы Майкрософт"
description: "Вы можете связать или синхронизировать информацию о контактах, т. е. о клиентах, поставщиках или банковских счетах, чтобы централизованно обновлять эту информацию."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dbb29d9d53618eec69817455d4304da2a6bfe466
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="20be7-103">Синхронизация контактов с клиентами, поставщиками и банковскими счетами</span><span class="sxs-lookup"><span data-stu-id="20be7-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="20be7-104">Если какие-то контакты являются еще и клиентами, поставщиками или банковскими счетами, можно синхронизировать контактную информацию с соответствующим клиентом, поставщиком или банковским счетом.</span><span class="sxs-lookup"><span data-stu-id="20be7-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="20be7-105">Синхронизация делает общую информацию между контактами и клиентами, поставщиками или банковским счетом одинаковой.</span><span class="sxs-lookup"><span data-stu-id="20be7-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

<span data-ttu-id="20be7-106">Прежде чем синхронизировать контакты с клиентами, поставщиками или банковскими счетами, следует указать код делового отношения для клиентов, поставщиков и банковских счетов в окне **Настройка модуля Маркетинг**.</span><span class="sxs-lookup"><span data-stu-id="20be7-106">Before you can synchronize your contacts with customers, vendors, or bank accounts, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="20be7-107">Дополнительные сведения см. в разделе [Настройка управления отношениями](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="20be7-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="20be7-108">Различные способы синхронизации контактов с клиентами, поставщиками и банковскими счетами</span><span class="sxs-lookup"><span data-stu-id="20be7-108">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="20be7-109">Контакты можно синхронизировать с заказчиками, поставщиками или банковскими счетами тремя способами:</span><span class="sxs-lookup"><span data-stu-id="20be7-109">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="20be7-110">Свяжите контакты с имеющимися клиентами, поставщиками или банковскими счетами.</span><span class="sxs-lookup"><span data-stu-id="20be7-110">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="20be7-111">Дополнительные сведения см. в разделе [Практическое руководство. Связывание контактов с клиентами, поставщиками и банковскими счетами](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="20be7-111">For more information, see [How to: Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="20be7-112">Создавайте клиентов, поставщиков или банковские счета из контакта.</span><span class="sxs-lookup"><span data-stu-id="20be7-112">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="20be7-113">Дополнительные сведения см. в разделе [Создание клиента, поставщика или банковского счета из клиента](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="20be7-113">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="20be7-114">Создать контакты из клиентов, поставщиков или банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="20be7-114">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="20be7-115">Дополнительные сведения см. в разделе [Создание контакта организации из клиента, поставщика или банковского счета](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="20be7-115">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="20be7-116">Последствия синхронизации</span><span class="sxs-lookup"><span data-stu-id="20be7-116">Consequences of Synchronization</span></span>
<span data-ttu-id="20be7-117">Когда контакт синхронизирован с клиентом, поставщиком или банковским счетом:</span><span class="sxs-lookup"><span data-stu-id="20be7-117">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="20be7-118">Необходимо обновить информацию только в одном месте.</span><span class="sxs-lookup"><span data-stu-id="20be7-118">You only have to update information in one place.</span></span> <span data-ttu-id="20be7-119">Например, если изменить номер телефона в контакте, те же изменения будут автоматически внесены в запись клиента, поставщика или банковского счета.</span><span class="sxs-lookup"><span data-stu-id="20be7-119">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="20be7-120">Если была указана серия номеров для контактов, при создании карточки клиента, поставщика или банковского счета будет автоматически создана карточка контакта для клиента, поставщика или банковского счета.</span><span class="sxs-lookup"><span data-stu-id="20be7-120">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="20be7-121">Непосредственно из контакта можно создавать предложения и заказы на продажу, а также предложения и заказы на покупку;</span><span class="sxs-lookup"><span data-stu-id="20be7-121">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="20be7-122">Можно регистрировать взаимодействия при выполнении действий, таких как печать заказов и общих заказов, создание сервисных заказов на продажу, отправка сообщений электронной почты и т. д.</span><span class="sxs-lookup"><span data-stu-id="20be7-122">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="20be7-123">При удалении контакта, связанного с клиентом, поставщиком или банковским счетом, удаляется только контакт.</span><span class="sxs-lookup"><span data-stu-id="20be7-123">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="20be7-124">Клиент, поставщик или банковский счет остаются.</span><span class="sxs-lookup"><span data-stu-id="20be7-124">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="20be7-125">При удалении клиента, поставщика или банковского счета, связанного с контактом, контакт сохраняется.</span><span class="sxs-lookup"><span data-stu-id="20be7-125">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="20be7-126">Некоторые подробности, например сведения о счетах и учете, не отображаются в карточке контакта.</span><span class="sxs-lookup"><span data-stu-id="20be7-126">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="20be7-127">Следовательно, может потребоваться добавить их вручную в карточку клиента, поставщика или банковского счета при создании контактов как клиентов, поставщиков или банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="20be7-127">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="20be7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="20be7-128">See Also</span></span>
[<span data-ttu-id="20be7-129">Управление контактами</span><span class="sxs-lookup"><span data-stu-id="20be7-129">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="20be7-130">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20be7-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
