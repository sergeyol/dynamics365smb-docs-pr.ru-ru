---
title: Предоплата для поставщиков и клиентов в России
description: Российские усовершенствования включают управление предоплатой поставщиков и клиентов.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 01bd229187652a9cb4718202d159b820e15257a4
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738229"
---
# <a name="prepayments-vendor-and-customers"></a><span data-ttu-id="acff5-103">Предоплаты поставщиков и клиентов</span><span class="sxs-lookup"><span data-stu-id="acff5-103">Prepayments Vendor and Customers</span></span>

<span data-ttu-id="acff5-104">В российской версии предоплаты работают не так, как в стандартной версии [!INCLUDE[prodshort](../../includes/prodshort.md)],</span><span class="sxs-lookup"><span data-stu-id="acff5-104">In the Russian version, prepayments work in a different way compared to the standard version of [!INCLUDE[prodshort](../../includes/prodshort.md)].</span></span> <span data-ttu-id="acff5-105">Когда мы получаем предоплату, по правилам бухгалтерского учета необходимо учесть ее на отдельном счете, поэтому в учетных группах поставщиков и клиентов есть поле "Счет предоплаты".</span><span class="sxs-lookup"><span data-stu-id="acff5-105">When we receive a prepayment, it is necessary by accounting rules to post prepayment on separate account, that way Vendor and Customer Posting groups have field - Prepayment Account</span></span>

[!INCLUDE[prodshort](../../includes/prodshort.md)] <span data-ttu-id="acff5-106">использует эти счета для операций предоплаты — платежей с отметкой "Предоплата".</span><span class="sxs-lookup"><span data-stu-id="acff5-106">uses this accounts for prepayment entries- Payment with Prepayment check mark.</span></span>

## <a name="posting-a-prepayment"></a><span data-ttu-id="acff5-107">Учет предоплаты</span><span class="sxs-lookup"><span data-stu-id="acff5-107">Posting a prepayment</span></span>

<span data-ttu-id="acff5-108">На странице **Финансовый журнал** выберите тип документа — "Оплата и Предоплата" — да.</span><span class="sxs-lookup"><span data-stu-id="acff5-108">In the **General Journal** page, choose Document type - Payment and Prepayment - yes.</span></span>

<span data-ttu-id="acff5-109">Укажите тип и номер счета, тип и номер балансового счета.</span><span class="sxs-lookup"><span data-stu-id="acff5-109">Specify the account type and account number, the balance account type, and the balance account number.</span></span>

<span data-ttu-id="acff5-110">Выполните учет финансового журнала.</span><span class="sxs-lookup"><span data-stu-id="acff5-110">Post the general journal.</span></span>

## <a name="applying-prepayments"></a><span data-ttu-id="acff5-111">Применение предоплат</span><span class="sxs-lookup"><span data-stu-id="acff5-111">Applying prepayments</span></span>

1. <span data-ttu-id="acff5-112">Выберите **операции книги поставщиков** или **операции книги клиентов**.</span><span class="sxs-lookup"><span data-stu-id="acff5-112">Go to the **vendor ledger entries** or **customer ledger entries**.</span></span>
2. <span data-ttu-id="acff5-113">Выберите строку с учтенной предоплатой.</span><span class="sxs-lookup"><span data-stu-id="acff5-113">Select a line with a posted prepayment.</span></span>
3. <span data-ttu-id="acff5-114">На вкладке **Главная** нажмите "Применить операции".</span><span class="sxs-lookup"><span data-stu-id="acff5-114">On the **Home** tab, click apply operations.</span></span>
4. <span data-ttu-id="acff5-115">Выберите строку со счетом, к которому вы хотите применить предоплату.</span><span class="sxs-lookup"><span data-stu-id="acff5-115">Select the line with the invoice to which you want to apply the prepayment.</span></span>
5. <span data-ttu-id="acff5-116">Нажмите **Установить код применения**.</span><span class="sxs-lookup"><span data-stu-id="acff5-116">Press **Set applies-to ID**.</span></span>
6. <span data-ttu-id="acff5-117">Нажмите **Учет применения**.</span><span class="sxs-lookup"><span data-stu-id="acff5-117">Press **Post Application**.</span></span>

## <a name="see-also"></a><span data-ttu-id="acff5-118">См. также</span><span class="sxs-lookup"><span data-stu-id="acff5-118">See Also</span></span>

[<span data-ttu-id="acff5-119">Функциональность локальной версии для России</span><span class="sxs-lookup"><span data-stu-id="acff5-119">Russia Local Functionality</span></span>](russia-local-functionality.md)  