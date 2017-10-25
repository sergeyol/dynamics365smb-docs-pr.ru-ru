---
title: "Настройка предпочтительных способов отправки документов продажи | Документы Майкрософт"
description: "Описывается порядок настройки предпочитаемого способа отправки документов продажи, например электронная почта, PDF, электронные документы и т. д."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a><span data-ttu-id="7a2a8-103">Практическое руководство. Настройка профилей отправки документов</span><span class="sxs-lookup"><span data-stu-id="7a2a8-103">How to: Set Up Document Sending Profiles</span></span>
<span data-ttu-id="7a2a8-104">Для каждого клиента можно настроить предпочтительный способ отправки документов продажи, так что не придется каждый раз выбирать вариант отправки при выборе действия **Учесть и отправить**.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="7a2a8-105">В окне **Профили отправки документов** можно настроить различные профили отправки, которые затем можно будет выбирать в поле **Профиль отправки документов** в карточке клиента.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="7a2a8-106">Вы можете установить флажок **По умолчанию**, чтобы указать, что профиль отправки документа является профилем по умолчанию для всех клиентов, кроме тех, у которых в поле **Профиль отправки документов** указан иной профиль.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="7a2a8-107">При выборе действия **Учесть и отправить** в документе продажи появляется диалоговое окно **Учесть и отправить подтверждение**, в котором отображается используемый профиль отправки — либо установленный для данного клиента, либо профиль по умолчанию для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="7a2a8-108">В этом диалоговом окне можно изменить профиль отправки для конкретного документа продаж.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="7a2a8-109">Дополнительные сведения см. в разделе [Практическое руководство. Выставление счетов продажи](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="7a2a8-109">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="7a2a8-110">Настройка профиля отправки документов</span><span class="sxs-lookup"><span data-stu-id="7a2a8-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="7a2a8-111">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Профили отправки документов**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a2a8-112">В окне **Профили отправки документов** выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="7a2a8-113">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="7a2a8-114">Определение профиля отправки в карточке клиента</span><span class="sxs-lookup"><span data-stu-id="7a2a8-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="7a2a8-115">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Клиенты**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a2a8-116">Откройте карточку клиента, для которого нужно настроить профиль отправки.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="7a2a8-117">В поле **Профиль отправки документов** выберите профиль, настроенный, как описано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="7a2a8-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a2a8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7a2a8-118">See Also</span></span>
[<span data-ttu-id="7a2a8-119">Настройка продаж</span><span class="sxs-lookup"><span data-stu-id="7a2a8-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="7a2a8-120">Продажи</span><span class="sxs-lookup"><span data-stu-id="7a2a8-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="7a2a8-121">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a2a8-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
