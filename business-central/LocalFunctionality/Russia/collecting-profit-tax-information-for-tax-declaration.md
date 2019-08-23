---
title: Сбор информации о налоге на прибыль в России
description: Российские улучшения включают информацию о налоге на прибыль для налоговых деклараций.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: e3502b226a6766115c56ed32d072d13acf00b12c
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738269"
---
# <a name="collecting-profit-tax-information-for-tax-declaration"></a><span data-ttu-id="953c5-103">Сбор сведений о налоге на прибыль для налоговой декларации</span><span class="sxs-lookup"><span data-stu-id="953c5-103">Collecting Profit Tax Information for Tax Declaration</span></span>

<span data-ttu-id="953c5-104">Чтобы уменьшить трудоемкость заполнения декларации по налогу на прибыль и упростить бухгалтерский учет в компании, документ разделен на приложения в соответствии с источником.</span><span class="sxs-lookup"><span data-stu-id="953c5-104">To reduce the labor required to complete a profit tax declaration and to simplify the company bookkeeping, the reporting document is split into supplements in accordance with the source.</span></span> <span data-ttu-id="953c5-105">Для каждого приложения, заполняемого налогоплательщиком, создается синтетический налоговый регистр в модуле налогового учета, где перечисляются все строки декларации и описываются источники данных и правила создания для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="953c5-105">For each supplement, which is filled in by a taxpayer, a synthetic tax register is created in the tax accounting module, where all the declaration lines are stated and data sources and creation rules for each line are described.</span></span> 

<span data-ttu-id="953c5-106">В модуле налогового учета реализованы следующие синтетические регистры документа "Отчет о декларации по налогу на прибыль":</span><span class="sxs-lookup"><span data-stu-id="953c5-106">In the tax accounting module, the following synthetic registers of the Profit Tax Declaration Reporting document are realized:</span></span> 

- <span data-ttu-id="953c5-107">Лист 02 Расчет Налога на прибыль</span><span class="sxs-lookup"><span data-stu-id="953c5-107">Sheet 02 Profit Tax Calculation</span></span>
- <span data-ttu-id="953c5-108">Приложение 1 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-108">Supplement 1 to Sheet 02.</span></span> <span data-ttu-id="953c5-109">Доход с продаж</span><span class="sxs-lookup"><span data-stu-id="953c5-109">Sales Income</span></span>
- <span data-ttu-id="953c5-110">Приложение 2 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-110">Supplement 2 to Sheet 02.</span></span> <span data-ttu-id="953c5-111">Затраты на производство и продажи</span><span class="sxs-lookup"><span data-stu-id="953c5-111">Production and Sales Costs</span></span>
- <span data-ttu-id="953c5-112">Приложение 3 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-112">Supplement 3 to Sheet 02.</span></span> <span data-ttu-id="953c5-113">Особые затраты на производство и продажи</span><span class="sxs-lookup"><span data-stu-id="953c5-113">Special Production and Sales Costs</span></span>
- <span data-ttu-id="953c5-114">Приложение 4 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-114">Supplement 4 to Sheet 02.</span></span> <span data-ttu-id="953c5-115">Расчет суммы убытков или части суммы убытков, на которую будет уменьшена налогооблагаемая база</span><span class="sxs-lookup"><span data-stu-id="953c5-115">Calculation of Loss Amount or Loss Amount Part decreasing the taxation basis</span></span>
- <span data-ttu-id="953c5-116">Приложение 6 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-116">Supplement 6 to Sheet 02.</span></span> <span data-ttu-id="953c5-117">Затраты, не связанные с продажами</span><span class="sxs-lookup"><span data-stu-id="953c5-117">Non – Sales Costs</span></span>
- <span data-ttu-id="953c5-118">Приложение 7 к Листу 02.</span><span class="sxs-lookup"><span data-stu-id="953c5-118">Supplement 7 to Sheet 02.</span></span> <span data-ttu-id="953c5-119">Затраты, не связанные с продажами, и убытки, которые рассматриваются как не связанные с продажами</span><span class="sxs-lookup"><span data-stu-id="953c5-119">Non – Sales Costs and Losses to be understood as non–sale</span></span>

 

## <a name="see-also"></a><span data-ttu-id="953c5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="953c5-120">See Also</span></span> 

[<span data-ttu-id="953c5-121">Налоговый учет</span><span class="sxs-lookup"><span data-stu-id="953c5-121">Tax Accounting</span></span>](Tax-Accounting.md)

[<span data-ttu-id="953c5-122">Практическое руководство. Настройка секций налогового регистра</span><span class="sxs-lookup"><span data-stu-id="953c5-122">How to: Set Up Tax Register Sections</span></span>](How-to-Set-Up-Tax-Register-Sections.md)

 [<span data-ttu-id="953c5-123">Практическое руководство. Создание налоговых регистров</span><span class="sxs-lookup"><span data-stu-id="953c5-123">How to: Create Tax Registers</span></span>](How-to-Create-Tax-Registers.md)

[<span data-ttu-id="953c5-124">Налоговые разницы</span><span class="sxs-lookup"><span data-stu-id="953c5-124">Tax Differences</span></span>](Tax-Differences.md)