---
title: Настройка запасов в России
description: Российские улучшения включают работу с запасами.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 5878b0443e6310af67d86013dd93c05b22c468ca
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738245"
---
# <a name="inventory-setup"></a><span data-ttu-id="281b0-103">Настройка запасов</span><span class="sxs-lookup"><span data-stu-id="281b0-103">Inventory Setup</span></span>

<span data-ttu-id="281b0-104">Как часть управление запасами, можно настроить запасы, чтобы:</span><span class="sxs-lookup"><span data-stu-id="281b0-104">As part of inventory management, you can set up inventory to:</span></span> 

- <span data-ttu-id="281b0-105">Назначать товарные издержки при покупках из зарубежных стран или регионов на основе веса или объема</span><span class="sxs-lookup"><span data-stu-id="281b0-105">Assign item charges on purchases from foreign countries/regions based on weight or volume</span></span>
- <span data-ttu-id="281b0-106">Использовать один и тот же столбец для первоначального учета и корректировок</span><span class="sxs-lookup"><span data-stu-id="281b0-106">Use the same column for original and corrective postings</span></span>

## <a name="item-charge-assignment-in-purchase-documents"></a><span data-ttu-id="281b0-107">Назначение товарных издержек в документах покупки</span><span class="sxs-lookup"><span data-stu-id="281b0-107">Item Charge Assignment in Purchase Documents</span></span>

<span data-ttu-id="281b0-108">В России [!INCLUDE[prodshort](../../includes/prodshort.md)] может назначать товарные издержки при покупках из зарубежных стран или регионов на основе веса или объема.</span><span class="sxs-lookup"><span data-stu-id="281b0-108">In Russia, [!INCLUDE[prodshort](../../includes/prodshort.md)] can assign item charges on purchases from foreign countries/regions based on weight or volume.</span></span> <span data-ttu-id="281b0-109">Для каждого товара в окне **Карточка товара** на экспресс-вкладке **Внешняя торговля** если установлены флажки **Вес брутто обязателен** и **Объем единицы обязателен**, необходимо заполнить поля **Вес брутто** и **Объем единицы**.</span><span class="sxs-lookup"><span data-stu-id="281b0-109">For each item, in the **Item Card** window, on the **Foreign Trade** FastTab, if the **Gross Weight Mandatory** and **Unit Volume Mandatory** check boxes are selected, you must fill in the **Gross Weight** and **Unit Volume** fields.</span></span> <span data-ttu-id="281b0-110">Когда вы предлагаете назначение товарных издержек по заказу на покупку, необходимо указать, что принцип распределения, вес и объем добавляются в параметры для выбора.</span><span class="sxs-lookup"><span data-stu-id="281b0-110">When you suggest an item charge assignment on a purchase order, you must specify that the distribution principle, weight, and volume are added to the options to choose from.</span></span> <span data-ttu-id="281b0-111">Дополнительные сведения см. в разделе [Практическое руководство. Использование товарных издержек для учета дополнительных торговых расходов](../../payables-how-assign-item-charges.md).</span><span class="sxs-lookup"><span data-stu-id="281b0-111">For more information, see [How to: Use Item Charges to Account for Additional Trade Costs](../../payables-how-assign-item-charges.md).</span></span>

## <a name="item-corrections"></a><span data-ttu-id="281b0-112">Корректировки товара</span><span class="sxs-lookup"><span data-stu-id="281b0-112">Item Corrections</span></span>

<span data-ttu-id="281b0-113">Можно настраивать склад на использование одного столбца для первоначального и корректирующего учета.</span><span class="sxs-lookup"><span data-stu-id="281b0-113">You can set up inventory to use the same column for original and corrective postings.</span></span> <span data-ttu-id="281b0-114">Эта функция часто называется *красный сторно*.</span><span class="sxs-lookup"><span data-stu-id="281b0-114">This is often referred to as *red storno*.</span></span>

<span data-ttu-id="281b0-115">Можно использовать учет "красный сторно" для учета корректировок следующих операций склада:</span><span class="sxs-lookup"><span data-stu-id="281b0-115">You can use red storno posting to post corrections for the following inventory entries:</span></span>

- <span data-ttu-id="281b0-116">Корректирующие операции в журнале товаров</span><span class="sxs-lookup"><span data-stu-id="281b0-116">Corrective entries in the item journal</span></span>
- <span data-ttu-id="281b0-117">Сторнирование товарных документов, таких как акты оприходования и акты списания товаров</span><span class="sxs-lookup"><span data-stu-id="281b0-117">Reversal of item documents such as item receipts and item shipments</span></span>
- <span data-ttu-id="281b0-118">Учет журналов переоценки или реклассификации товаров</span><span class="sxs-lookup"><span data-stu-id="281b0-118">Posting item revaluation or item reclassification journals</span></span>
- <span data-ttu-id="281b0-119">Периодические корректировки себестоимости товара</span><span class="sxs-lookup"><span data-stu-id="281b0-119">Periodic adjustments of item costs</span></span>

<span data-ttu-id="281b0-120">Дополнительные сведения см. в разделе [Практическое руководство. Учет корректировок "красный сторно"](How-to-Post-Red-Storno-Corrections.md).</span><span class="sxs-lookup"><span data-stu-id="281b0-120">For more information, see [How to: Post Red Storno Corrections](How-to-Post-Red-Storno-Corrections.md).</span></span>

### <a name="adjusting-item-cost"></a><span data-ttu-id="281b0-121">Корректировка себестоимости товаров</span><span class="sxs-lookup"><span data-stu-id="281b0-121">Adjusting Item Cost</span></span>

<span data-ttu-id="281b0-122">Если выбрано поле "Применять красное сторно" в окне **Настройка модуля "Запасы"**, то отрицательные отклонения учитываются в соответствии с "красным сторно" при исполнении пакетного задания **Коррекция себест. запасов**.</span><span class="sxs-lookup"><span data-stu-id="281b0-122">If you select the Enable Red Storno field in the **Inventory Setup** window, then negative deviations are posted according to red storno when you run the **Adjust Cost - Item Entries** batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="281b0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="281b0-123">See Also</span></span>

[<span data-ttu-id="281b0-124">Товарные документы</span><span class="sxs-lookup"><span data-stu-id="281b0-124">Item Documents</span></span>](Item-Documents.md)  
[<span data-ttu-id="281b0-125">Акты обязательств по товару</span><span class="sxs-lookup"><span data-stu-id="281b0-125">Item Obligatory Acts</span></span>](Item-Obligatory-Acts.md)  
[<span data-ttu-id="281b0-126">Практическое руководство. Учет коррекций "красный сторно"</span><span class="sxs-lookup"><span data-stu-id="281b0-126">How to: Post Red Storno Corrections</span></span>](How-to-Post-Red-Storno-Corrections.md)  
[<span data-ttu-id="281b0-127">Практическое руководство. Использование товарных издержек для учета дополнительных торговых расходов</span><span class="sxs-lookup"><span data-stu-id="281b0-127">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](../../payables-how-assign-item-charges.md)  