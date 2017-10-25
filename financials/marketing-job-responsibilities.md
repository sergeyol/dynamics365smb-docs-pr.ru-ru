---
title: "Настройка должностных обязанностей для контактов | Документы Майкрософт"
description: "Вы можете определять коды должностной обязанностей и назначать их контактам, чтобы задавать задачи, за которые отвечает контакт в своей организации, например за ИТ или производство."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fd949573e7bfd1b6ce1fc849625a1a3474013f96
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-job-responsibilities-for-contact-persons"></a><span data-ttu-id="49c22-103">Практическое руководство. Настройка должностных обязанностей для контактных лиц</span><span class="sxs-lookup"><span data-stu-id="49c22-103">How to: Set Up Job Responsibilities for Contact Persons</span></span>
<span data-ttu-id="49c22-104">Вы можете добавить информацию о должностных обязанностей контактных лиц, чтобы показать, за что контактное лицо ответственно в своей организации, например ИТ, управление или производство.</span><span class="sxs-lookup"><span data-stu-id="49c22-104">You can add information about the job responsibilities of contact persons to indicate what the contact person is responsible for within their company, for example, IT, management, or production.</span></span> <span data-ttu-id="49c22-105">Эту информацию можно использовать при вводе информации о контактах.</span><span class="sxs-lookup"><span data-stu-id="49c22-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="49c22-106">Использование должностных обязанностей для контактов — это двухэтапный процесс.</span><span class="sxs-lookup"><span data-stu-id="49c22-106">Using job responsibilities on contacts is a two-step process.</span></span> <span data-ttu-id="49c22-107">Сначала вы определяете код должностной обязанности.</span><span class="sxs-lookup"><span data-stu-id="49c22-107">First, you define the job responsibility code.</span></span> <span data-ttu-id="49c22-108">Этот шаг нужно выполнить один раз для каждой должностной обязанности.</span><span class="sxs-lookup"><span data-stu-id="49c22-108">You only have to perform this step one time for each job responsibility.</span></span> <span data-ttu-id="49c22-109">После настройки кода должностной обязанности можно начинать назначение кода контактным лицам.</span><span class="sxs-lookup"><span data-stu-id="49c22-109">Once you have a job responsibility code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-job-responsibility-code"></a><span data-ttu-id="49c22-110">Определение кода должностной обязанности</span><span class="sxs-lookup"><span data-stu-id="49c22-110">to define a job responsibility code</span></span>
<span data-ttu-id="49c22-111">Код должностной обязанности определяет тип или категорию работы, например МАРКЕТИНГ или ЗАКУПКИ.</span><span class="sxs-lookup"><span data-stu-id="49c22-111">The job responsibility code defines the type or category of the job, such a MARKETING or PURCHASE.</span></span> <span data-ttu-id="49c22-112">Допускается наличие нескольких кодов должностных обязанностей.</span><span class="sxs-lookup"><span data-stu-id="49c22-112">You can have several job responsibility codes.</span></span> <span data-ttu-id="49c22-113">Для определения должностной обязанности используется окно **Должностные обязанности**.</span><span class="sxs-lookup"><span data-stu-id="49c22-113">To define the job responsibility, you use the **Job Responsibilities** window.</span></span>

1. <span data-ttu-id="49c22-114">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Должностные обязанности**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="49c22-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Responsibilities**, and then choose the related link.</span></span>
2. <span data-ttu-id="49c22-115">Выберите действие **Создать**, введите код и описание.</span><span class="sxs-lookup"><span data-stu-id="49c22-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="49c22-116">Длина кода не должна превышать 11 знаков (допускается сочетание букв и цифр).</span><span class="sxs-lookup"><span data-stu-id="49c22-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a><span data-ttu-id="49c22-117">Назначение должностных обязанностей контактному лицу</span><span class="sxs-lookup"><span data-stu-id="49c22-117">to assign job responsibilities to a contact person</span></span>
<span data-ttu-id="49c22-118">Должностные обязанности не могут назначаться контактным организациям.</span><span class="sxs-lookup"><span data-stu-id="49c22-118">You cannot assign job responsibilities to contact companies.</span></span>

1. <span data-ttu-id="49c22-119">Откройте контактное лицо.</span><span class="sxs-lookup"><span data-stu-id="49c22-119">Open the contact person.</span></span>
2. <span data-ttu-id="49c22-120">Выберите действие **Лицо**, а затем выберите действие **Должностные обязанности**.</span><span class="sxs-lookup"><span data-stu-id="49c22-120">Choose the **Person** action, and then choose the **Job Responsibilities** action.</span></span> <span data-ttu-id="49c22-121">Откроется окно **Должностные обязанности контакта**.</span><span class="sxs-lookup"><span data-stu-id="49c22-121">The **Contact Job Responsibilities** window opens.</span></span>
3. <span data-ttu-id="49c22-122">В поле **Код должностной обязанности** выберите должностную обязанность, которую требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="49c22-122">In the **Job Responsibility Code** field, select the job responsibility that you want to assign.</span></span>

<span data-ttu-id="49c22-123">Повторите эти шаги для назначения желаемого количества функциональных обязанностей.</span><span class="sxs-lookup"><span data-stu-id="49c22-123">Repeat these steps to assign as many job responsibilities as you want.</span></span> <span data-ttu-id="49c22-124">Также можно назначать должностные обязанности из списка контактов, следуя той же процедуре.</span><span class="sxs-lookup"><span data-stu-id="49c22-124">You can also assign job responsibilities from the contact list by following the same procedure.</span></span>

<span data-ttu-id="49c22-125">Число должностных обязанностей, назначенных контакту, отображается в окне **Контакт** в разделе **Сегментация** в поле **Число должностных обязанностей**.</span><span class="sxs-lookup"><span data-stu-id="49c22-125">The number of job responsibilities you have assigned to the contact is displayed in the **No. of Job Responsibilities** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="49c22-126">После назначения контактам должностных обязанностей можно использовать эту информацию для выбора контактов для сегмента.</span><span class="sxs-lookup"><span data-stu-id="49c22-126">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="49c22-127">Дополнительные сведения см. в разделе [Практическое руководство. Добавление контактов к сегментам](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="49c22-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="49c22-128">См. также</span><span class="sxs-lookup"><span data-stu-id="49c22-128">See Also</span></span>
[<span data-ttu-id="49c22-129">Создание контактных лиц</span><span class="sxs-lookup"><span data-stu-id="49c22-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="49c22-130">Создание контактных организаций</span><span class="sxs-lookup"><span data-stu-id="49c22-130">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="49c22-131">Работа с Financials</span><span class="sxs-lookup"><span data-stu-id="49c22-131">Working with Financials</span></span>](ui-work-product.md)
