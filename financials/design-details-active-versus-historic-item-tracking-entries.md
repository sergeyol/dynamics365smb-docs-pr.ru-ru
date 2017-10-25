---
title: "Сведения о проектировании — активные и исторические операции трассировки товаров | Документы Майкрософт"
description: "При учете частей количества, указанного на строке документа, только соответствующее количество переносится в операции журнала товаров и числа трассировки товаров. Однако будет необходимо открыть всю информацию о трассировке товаров непосредственно из активной строки документа. Это означает, что требуется не только просмотреть операции, связанные с остатком, но и сведения о единицах, которые были учтены. При просмотре или изменении окна **Строки трассировки товаров** совместное содержимое таблиц **Спецификация трассировки** (T336) и **Операция резервирования** (T337) представляются во временной версии T336. Это обеспечивает доступ к данным за прошлые периоды и активным данным трассировки товаров как к единому целому."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0b0d49b4f9b9e77b311628c2d88b4891b32f8276
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a><span data-ttu-id="c5db9-107">Сведения о проектировании: активные и исторические операции трассировки товаров</span><span class="sxs-lookup"><span data-stu-id="c5db9-107">Design Details: Active versus Historic Item Tracking Entries</span></span>
<span data-ttu-id="c5db9-108">При учете частей количества, указанного на строке документа, только соответствующее количество переносится в операции журнала товаров и числа трассировки товаров.</span><span class="sxs-lookup"><span data-stu-id="c5db9-108">When parts of a document line quantity are posted, only that particular quantity is transferred to the item ledger entries and its item tracking numbers.</span></span> <span data-ttu-id="c5db9-109">Однако будет необходимо открыть всю информацию о трассировке товаров непосредственно из активной строки документа.</span><span class="sxs-lookup"><span data-stu-id="c5db9-109">However, you will want to access all relevant item tracking information directly from the active document line.</span></span> <span data-ttu-id="c5db9-110">Это означает, что требуется не только просмотреть операции, связанные с остатком, но и сведения о единицах, которые были учтены.</span><span class="sxs-lookup"><span data-stu-id="c5db9-110">That is, not only will you want to see the entries that are related to the remaining quantity, you will also want information about the units that have been posted.</span></span> <span data-ttu-id="c5db9-111">При просмотре или изменении окна **Строки трассировки товаров** совместное содержимое таблиц **Спецификация трассировки** (T336) и **Операция резервирования** (T337) представляются во временной версии T336.</span><span class="sxs-lookup"><span data-stu-id="c5db9-111">When you view or modify the **Item Tracking Lines** window, the collective contents of the **Tracking Specification** table (T336) and **Reservation Entry** table (T337) are presented in a temporary version of T336.</span></span> <span data-ttu-id="c5db9-112">Это обеспечивает доступ к данным за прошлые периоды и активным данным трассировки товаров как к единому целому.</span><span class="sxs-lookup"><span data-stu-id="c5db9-112">This ensures that historic and active item tracking data is accessed as one.</span></span>  

 <span data-ttu-id="c5db9-113">В следующей таблице показано, как T336 и T337 используются в сценарии покупки.</span><span class="sxs-lookup"><span data-stu-id="c5db9-113">The following table shows how T336 and T337 are used in a purchase scenario.</span></span> <span data-ttu-id="c5db9-114">Выделенные полужирным шрифтом цифры представляют значения, которые пользователь вручную вводит в окне **Строки трассировки товаров**.</span><span class="sxs-lookup"><span data-stu-id="c5db9-114">The bold figures represent values that the user manually enters in the **Item Tracking Lines** window.</span></span>  

 <span data-ttu-id="c5db9-115">Шаг 1. Создайте строку заказа покупки для семи штук с номерами трассировки товара.</span><span class="sxs-lookup"><span data-stu-id="c5db9-115">Step 1: Create a purchase order line of seven pieces with item tracking numbers.</span></span>  

||<span data-ttu-id="c5db9-116">**Количество (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-116">**Quantity (Base)**</span></span>|<span data-ttu-id="c5db9-117">**Кол-во для обработки**</span><span class="sxs-lookup"><span data-stu-id="c5db9-117">**Qty. to Handle**</span></span>|<span data-ttu-id="c5db9-118">**Кол-во для выст. счета (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-118">**Qty. to Invoice (Base)**</span></span>|<span data-ttu-id="c5db9-119">**Обработанное кол-во (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-119">**Quantity Handled (Base)**</span></span>|<span data-ttu-id="c5db9-120">**Кол-во по выст. счетам (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-120">**Quantity Invoiced (Base)**</span></span>|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|<span data-ttu-id="c5db9-121">**T337**</span><span class="sxs-lookup"><span data-stu-id="c5db9-121">**T337**</span></span>|<span data-ttu-id="c5db9-122">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-122">7</span></span>|<span data-ttu-id="c5db9-123">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-123">0</span></span>|<span data-ttu-id="c5db9-124">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-124">0</span></span>|<span data-ttu-id="c5db9-125">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-125">0</span></span>|<span data-ttu-id="c5db9-126">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-126">0</span></span>|  
|<span data-ttu-id="c5db9-127">**T336**</span><span class="sxs-lookup"><span data-stu-id="c5db9-127">**T336**</span></span>|<span data-ttu-id="c5db9-128">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-128">0</span></span>|<span data-ttu-id="c5db9-129">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-129">0</span></span>|<span data-ttu-id="c5db9-130">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-130">0</span></span>|<span data-ttu-id="c5db9-131">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-131">0</span></span>|<span data-ttu-id="c5db9-132">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-132">0</span></span>|  

 <span data-ttu-id="c5db9-133">Шаг 2. Получите четыре штуки.</span><span class="sxs-lookup"><span data-stu-id="c5db9-133">Step 2: Receive four pieces.</span></span>  

||<span data-ttu-id="c5db9-134">**Количество (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-134">**Quantity (Base)**</span></span>|<span data-ttu-id="c5db9-135">**Кол-во для обработки**</span><span class="sxs-lookup"><span data-stu-id="c5db9-135">**Qty. to Handle**</span></span>|<span data-ttu-id="c5db9-136">**Кол-во для выст. счета (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-136">**Qty. to Invoice (Base)**</span></span>|<span data-ttu-id="c5db9-137">**Обработанное кол-во (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-137">**Quantity Handled (Base)**</span></span>|<span data-ttu-id="c5db9-138">**Кол-во по выст. счетам (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-138">**Quantity Invoiced (Base)**</span></span>|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|<span data-ttu-id="c5db9-139">Окно **Строки трассировки товаров**</span><span class="sxs-lookup"><span data-stu-id="c5db9-139">**Item Tracking Lines** window</span></span>|<span data-ttu-id="c5db9-140">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-140">7</span></span>|<span data-ttu-id="c5db9-141">**4**</span><span class="sxs-lookup"><span data-stu-id="c5db9-141">**4**</span></span>|<span data-ttu-id="c5db9-142">**0**</span><span class="sxs-lookup"><span data-stu-id="c5db9-142">**0**</span></span>|<span data-ttu-id="c5db9-143">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-143">0</span></span>|<span data-ttu-id="c5db9-144">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-144">0</span></span>|  
|<span data-ttu-id="c5db9-145">**T337**</span><span class="sxs-lookup"><span data-stu-id="c5db9-145">**T337**</span></span>|<span data-ttu-id="c5db9-146">3</span><span class="sxs-lookup"><span data-stu-id="c5db9-146">3</span></span>|<span data-ttu-id="c5db9-147">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-147">0</span></span>|<span data-ttu-id="c5db9-148">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-148">0</span></span>|<span data-ttu-id="c5db9-149">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-149">0</span></span>|<span data-ttu-id="c5db9-150">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-150">0</span></span>|  
|<span data-ttu-id="c5db9-151">**T336**</span><span class="sxs-lookup"><span data-stu-id="c5db9-151">**T336**</span></span>|<span data-ttu-id="c5db9-152">4</span><span class="sxs-lookup"><span data-stu-id="c5db9-152">4</span></span>|<span data-ttu-id="c5db9-153">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-153">0</span></span>|<span data-ttu-id="c5db9-154">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-154">0</span></span>|<span data-ttu-id="c5db9-155">4</span><span class="sxs-lookup"><span data-stu-id="c5db9-155">4</span></span>|<span data-ttu-id="c5db9-156">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-156">0</span></span>|  

 <span data-ttu-id="c5db9-157">Шаг 3. Получите две штук и выставите счет по двум штукам.</span><span class="sxs-lookup"><span data-stu-id="c5db9-157">Step 3: Receive two pieces and invoice two pieces.</span></span>  

||<span data-ttu-id="c5db9-158">**Количество (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-158">**Quantity (Base)**</span></span>|<span data-ttu-id="c5db9-159">**Кол-во для обработки**</span><span class="sxs-lookup"><span data-stu-id="c5db9-159">**Qty. to Handle**</span></span>|<span data-ttu-id="c5db9-160">**Кол-во для выст. счета (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-160">**Qty. to Invoice (Base)**</span></span>|<span data-ttu-id="c5db9-161">**Обработанное кол-во (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-161">**Quantity Handled (Base)**</span></span>|<span data-ttu-id="c5db9-162">**Кол-во по выст. счетам (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-162">**Quantity Invoiced (Base)**</span></span>|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|<span data-ttu-id="c5db9-163">Окно **Строки трассировки товаров**</span><span class="sxs-lookup"><span data-stu-id="c5db9-163">**Item Tracking Lines** window</span></span>|<span data-ttu-id="c5db9-164">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-164">7</span></span>|<span data-ttu-id="c5db9-165">**2**</span><span class="sxs-lookup"><span data-stu-id="c5db9-165">**2**</span></span>|<span data-ttu-id="c5db9-166">**2**</span><span class="sxs-lookup"><span data-stu-id="c5db9-166">**2**</span></span>|<span data-ttu-id="c5db9-167">4</span><span class="sxs-lookup"><span data-stu-id="c5db9-167">4</span></span>|<span data-ttu-id="c5db9-168">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-168">0</span></span>|  
|<span data-ttu-id="c5db9-169">**T337**</span><span class="sxs-lookup"><span data-stu-id="c5db9-169">**T337**</span></span>|<span data-ttu-id="c5db9-170">1</span><span class="sxs-lookup"><span data-stu-id="c5db9-170">1</span></span>|<span data-ttu-id="c5db9-171">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-171">0</span></span>|<span data-ttu-id="c5db9-172">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-172">0</span></span>|<span data-ttu-id="c5db9-173">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-173">0</span></span>|<span data-ttu-id="c5db9-174">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-174">0</span></span>|  
|<span data-ttu-id="c5db9-175">**T336**</span><span class="sxs-lookup"><span data-stu-id="c5db9-175">**T336**</span></span>|<span data-ttu-id="c5db9-176">6</span><span class="sxs-lookup"><span data-stu-id="c5db9-176">6</span></span>|<span data-ttu-id="c5db9-177">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-177">0</span></span>|<span data-ttu-id="c5db9-178">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-178">0</span></span>|<span data-ttu-id="c5db9-179">6</span><span class="sxs-lookup"><span data-stu-id="c5db9-179">6</span></span>|<span data-ttu-id="c5db9-180">2</span><span class="sxs-lookup"><span data-stu-id="c5db9-180">2</span></span>|  

 <span data-ttu-id="c5db9-181">Шаг 4. Получите одну штуку.</span><span class="sxs-lookup"><span data-stu-id="c5db9-181">Step 4: Receive one piece.</span></span>  

||<span data-ttu-id="c5db9-182">**Количество (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-182">**Quantity (Base)**</span></span>|<span data-ttu-id="c5db9-183">**Кол-во для обработки**</span><span class="sxs-lookup"><span data-stu-id="c5db9-183">**Qty. to Handle**</span></span>|<span data-ttu-id="c5db9-184">**Кол-во для выст. счета (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-184">**Qty. to Invoice (Base)**</span></span>|<span data-ttu-id="c5db9-185">**Обработанное кол-во (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-185">**Quantity Handled (Base)**</span></span>|<span data-ttu-id="c5db9-186">**Кол-во по выст. счетам (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-186">**Quantity Invoiced (Base)**</span></span>|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|<span data-ttu-id="c5db9-187">Окно **Строки трассировки товаров**</span><span class="sxs-lookup"><span data-stu-id="c5db9-187">**Item Tracking Lines** window</span></span>|<span data-ttu-id="c5db9-188">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-188">7</span></span>|<span data-ttu-id="c5db9-189">**1**</span><span class="sxs-lookup"><span data-stu-id="c5db9-189">**1**</span></span>|<span data-ttu-id="c5db9-190">**0**</span><span class="sxs-lookup"><span data-stu-id="c5db9-190">**0**</span></span>|<span data-ttu-id="c5db9-191">6</span><span class="sxs-lookup"><span data-stu-id="c5db9-191">6</span></span>|<span data-ttu-id="c5db9-192">2</span><span class="sxs-lookup"><span data-stu-id="c5db9-192">2</span></span>|  
|<span data-ttu-id="c5db9-193">**T336**</span><span class="sxs-lookup"><span data-stu-id="c5db9-193">**T336**</span></span>|<span data-ttu-id="c5db9-194">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-194">7</span></span>|<span data-ttu-id="c5db9-195">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-195">0</span></span>|<span data-ttu-id="c5db9-196">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-196">0</span></span>|<span data-ttu-id="c5db9-197">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-197">7</span></span>|<span data-ttu-id="c5db9-198">2</span><span class="sxs-lookup"><span data-stu-id="c5db9-198">2</span></span>|  

 <span data-ttu-id="c5db9-199">Выставите счет по 5 штукам.</span><span class="sxs-lookup"><span data-stu-id="c5db9-199">Invoice 5 pieces.</span></span>  

||<span data-ttu-id="c5db9-200">**Количество (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-200">**Quantity (Base)**</span></span>|<span data-ttu-id="c5db9-201">**Кол-во для обработки**</span><span class="sxs-lookup"><span data-stu-id="c5db9-201">**Qty. to Handle**</span></span>|<span data-ttu-id="c5db9-202">**Кол-во для выст. счета (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-202">**Qty. to Invoice (Base)**</span></span>|<span data-ttu-id="c5db9-203">**Обработанное кол-во (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-203">**Quantity Handled (Base)**</span></span>|<span data-ttu-id="c5db9-204">**Кол-во по выст. счетам (баз.)**</span><span class="sxs-lookup"><span data-stu-id="c5db9-204">**Quantity Invoiced (Base)**</span></span>|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|<span data-ttu-id="c5db9-205">Окно **Строки трассировки товаров**</span><span class="sxs-lookup"><span data-stu-id="c5db9-205">**Item Tracking Lines** window</span></span>|<span data-ttu-id="c5db9-206">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-206">7</span></span>|<span data-ttu-id="c5db9-207">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-207">0</span></span>|<span data-ttu-id="c5db9-208">**5**</span><span class="sxs-lookup"><span data-stu-id="c5db9-208">**5**</span></span>|<span data-ttu-id="c5db9-209">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-209">7</span></span>|<span data-ttu-id="c5db9-210">2</span><span class="sxs-lookup"><span data-stu-id="c5db9-210">2</span></span>|  
|<span data-ttu-id="c5db9-211">**T336**</span><span class="sxs-lookup"><span data-stu-id="c5db9-211">**T336**</span></span>|<span data-ttu-id="c5db9-212">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-212">7</span></span>|<span data-ttu-id="c5db9-213">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-213">0</span></span>|<span data-ttu-id="c5db9-214">0</span><span class="sxs-lookup"><span data-stu-id="c5db9-214">0</span></span>|<span data-ttu-id="c5db9-215">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-215">7</span></span>|<span data-ttu-id="c5db9-216">7</span><span class="sxs-lookup"><span data-stu-id="c5db9-216">7</span></span>|  

## <a name="see-also"></a><span data-ttu-id="c5db9-217">См. также</span><span class="sxs-lookup"><span data-stu-id="c5db9-217">See Also</span></span>  
 <span data-ttu-id="c5db9-218">[Сведения о проектировании: трассировка товара](design-details-item-tracking.md) </span><span class="sxs-lookup"><span data-stu-id="c5db9-218">[Design Details: Item Tracking](design-details-item-tracking.md) </span></span>  
 [<span data-ttu-id="c5db9-219">Сведения о проектировании: окно "Строки трассировки товаров"</span><span class="sxs-lookup"><span data-stu-id="c5db9-219">Design Details: Item Tracking Lines Window</span></span>](design-details-item-tracking-lines-window.md)
