---
title: 'ОС: местоположения и ответственные сотрудники в России'
description: Российские улучшения включают местоположения и ответственных сотрудников для основных средств.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 99c9eb7e4f4b6028f934b978999e59a48dadfeeb
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738267"
---
# <a name="fixed-asset-locations-and-employees"></a><span data-ttu-id="f7724-103">ОС: местоположения и ответственные сотрудники</span><span class="sxs-lookup"><span data-stu-id="f7724-103">Fixed Asset Locations and Employees</span></span>

<span data-ttu-id="f7724-104">Функция местоположений и ответственных сотрудников для основных средств позволяет:</span><span class="sxs-lookup"><span data-stu-id="f7724-104">The fixed assets locations and the fixed assets employees feature enable you to:</span></span> 

- <span data-ttu-id="f7724-105">управлять движением основных средств и хранить историю перемещений ОС между различными местоположениями и подотчетными лицами;</span><span class="sxs-lookup"><span data-stu-id="f7724-105">Control the movement of fixed assets and to keep the history of the movements of fixed assets between locations and responsible employees.</span></span>
- <span data-ttu-id="f7724-106">указывать местоположение и подотчетное лицо для ОС в документах и журналах для учета основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-106">Enter the fixed assets location and responsible employee in documents and journals for fixed asset posting.</span></span> <span data-ttu-id="f7724-107">Эти данные будут отражены в операциях основных средств;</span><span class="sxs-lookup"><span data-stu-id="f7724-107">This information is reflected in fixed assets operations.</span></span>
- <span data-ttu-id="f7724-108">создавать отчеты и расчеты, в которых используется история перемещений основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-108">Create reports and calculations that use the history of the movements of fixed assets.</span></span> <span data-ttu-id="f7724-109">Кроме того, можно связать сотрудников (по умолчанию), местоположения (склад товара) и регионы в официальной классификации (код ОКАТО) с любым местоположением основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-109">You can also connect employees (by default), locations (item location), and regions in an official classification (OKATO code) to any fixed assets location.</span></span>

 

## <a name="setup"></a><span data-ttu-id="f7724-110">Настройка</span><span class="sxs-lookup"><span data-stu-id="f7724-110">Setup</span></span> 

<span data-ttu-id="f7724-111">Ниже показано, как обеспечить, чтобы поля **Код местонахождения ОС** и **Код сотрудника**</span><span class="sxs-lookup"><span data-stu-id="f7724-111">The following procedure shows how to make sure the **FA Location Code** and **Employee No.**</span></span> <span data-ttu-id="f7724-112">были всегда заполнены для основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-112">fields are always filled in for fixed assets.</span></span> 

1. <span data-ttu-id="f7724-113">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите \**Настройка ОС*, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f7724-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter \**FA Setup*, and then choose the related link.</span></span>
2. <span data-ttu-id="f7724-114">На экспресс-вкладке **Общие** установите флажок **Местонахождение ОС обязательно**.</span><span class="sxs-lookup"><span data-stu-id="f7724-114">On the **General** FastTab, select the **FA Location Mandatory** check box.</span></span>

 

> :speech_balloon: <span data-ttu-id="f7724-115">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f7724-115">**Note**</span></span>
>
> <span data-ttu-id="f7724-116">Если этот флажок установлен, процедуры учета основных средств управляются, пока они генерируют операции ОС с ненулевым значением в поле **Кол-во**.</span><span class="sxs-lookup"><span data-stu-id="f7724-116">When this field is selected, fixed asset posting procedures are controlled as long as they generate fixed asset operations with a non-zero value in the **Quantity** field.</span></span>



1. <span data-ttu-id="f7724-117">Установите флажок **Код сотрудника обязателен**.</span><span class="sxs-lookup"><span data-stu-id="f7724-117">Select the **Employee No. Mandatory** check box.</span></span>

 

> :speech_balloon: <span data-ttu-id="f7724-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f7724-118">**Note**</span></span>
>
> <span data-ttu-id="f7724-119">Если этот флажок установлен, процедуры учета основных средств управляются, пока они генерируют операции ОС с ненулевым значением в поле **Кол-во**.</span><span class="sxs-lookup"><span data-stu-id="f7724-119">When this field is selected, fixed asset posting procedures are controlled as long as they generate fixed asset operations with a non-zero value in the **Quantity** field.</span></span>

 

## <a name="added-fields"></a><span data-ttu-id="f7724-120">Добавленные поля</span><span class="sxs-lookup"><span data-stu-id="f7724-120">Added Fields</span></span> 

<span data-ttu-id="f7724-121">Поля со ссылками на местоположения и подотчетных лиц для ОС были добавлены к следующим элементам:</span><span class="sxs-lookup"><span data-stu-id="f7724-121">Fields with references to fixed asset locations and responsible employees have been added to the following:</span></span> 

- <span data-ttu-id="f7724-122">строки документов покупки;</span><span class="sxs-lookup"><span data-stu-id="f7724-122">Lines of purchase documents</span></span>
- <span data-ttu-id="f7724-123">журналы основных средств;</span><span class="sxs-lookup"><span data-stu-id="f7724-123">Fixed asset journals</span></span>
- <span data-ttu-id="f7724-124">финансовые журналы основных средств;</span><span class="sxs-lookup"><span data-stu-id="f7724-124">Fixed asset G/L journals</span></span>
- <span data-ttu-id="f7724-125">журналы реклассификации основных средств;</span><span class="sxs-lookup"><span data-stu-id="f7724-125">Fixed asset reclassification journals</span></span>
- <span data-ttu-id="f7724-126">акты основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-126">Fixed asset acts</span></span> 

<span data-ttu-id="f7724-127">Если установлен флажок **Код сотрудника обязателен** или **Местонахождение ОС обязательно** в окне **Настройка основных средств**, поля со ссылками на соответствующие таблицы должны быть заполнены для операций с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="f7724-127">If the **Employee No. Mandatory** or the **FA Location Mandatory** check box is selected in the **Fixed Asset Setup** window, then the fields with references to corresponding tables must be filled in for fixed asset operations.</span></span> <span data-ttu-id="f7724-128">Вы вводите значение в поле **Код местоположения ОС** в строке, затем поля **Код сотрудника**</span><span class="sxs-lookup"><span data-stu-id="f7724-128">If you enter a value in the **FA Location Code** field in a line, then the **Employee No.**</span></span> <span data-ttu-id="f7724-129">и **Код склада** (если оно существует в строке) заполняются соответствующими значениями по умолчанию из таблицы местоположения основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-129">field and **Location Code** field (if it exists in the line) are filled with the corresponding default values from the Fixed Asset Location table.</span></span> <span data-ttu-id="f7724-130">Затем значения этих полей можно изменить вручную.</span><span class="sxs-lookup"><span data-stu-id="f7724-130">Then the values of the fields can be changed manually.</span></span>

<span data-ttu-id="f7724-131">При учете документов и журналов значения в этих полях переносятся в соответствующие новые операции ОС и в соответствующие поля в карточках основных средств.</span><span class="sxs-lookup"><span data-stu-id="f7724-131">When posting the documents and journals, the values of these fields are transferred to the corresponding new fixed asset operations and to corresponding fields in the Fixed Asset cards.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f7724-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f7724-132">See Also</span></span> 

[<span data-ttu-id="f7724-133">Инвентаризация основных средств</span><span class="sxs-lookup"><span data-stu-id="f7724-133">Fixed Asset Inventory</span></span>](Fixed-Asset-Inventory.md)