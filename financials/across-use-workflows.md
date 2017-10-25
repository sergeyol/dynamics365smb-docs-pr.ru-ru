---
title: "Использование рабочих процессов | Документы Майкрософт"
description: "Можно настроить и использовать рабочие процессы, связывающие задачи бизнес-процесса, выполняемые различными пользователями. Системные задачи, такие как автоматический учет, могут включаться в качестве шагов рабочего процесса, предшествующих задачам пользователя или выполняемых после них. Типичные шаги рабочего процесса – запрос и выдача разрешения на создание новых записей."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a42e336dba385cbf24c19702ad64d76b26c15104
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="using-workflows"></a><span data-ttu-id="c0070-105">Использование рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="c0070-105">Using Workflows</span></span>
<span data-ttu-id="c0070-106">Можно настроить и использовать рабочие процессы, связывающие задачи бизнес-процесса, выполняемые различными пользователями.</span><span class="sxs-lookup"><span data-stu-id="c0070-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="c0070-107">Системные задачи, такие как автоматический учет, могут включаться в качестве шагов рабочего процесса, предшествующих задачам пользователя или выполняемых после них.</span><span class="sxs-lookup"><span data-stu-id="c0070-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="c0070-108">Типичные шаги рабочего процесса – запрос и выдача разрешения на создание новых записей.</span><span class="sxs-lookup"><span data-stu-id="c0070-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="c0070-109">Прежде чем начать использование рабочих процессов, необходимо произвести настройку пользователей рабочих процессов, создать рабочие процессы (возможно, перед этим потребуется настройка кода) и определить, как пользователи будут получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0070-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="c0070-110">Дополнительные сведения см. в разделе [Настройка рабочих процессов](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c0070-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c0070-111">Типичные шаги рабочего процесса имеют отношение к пользователям, запрашивающим утверждение задач, и утверждающим лицам, принимающим или отклоняющим запросы на утверждение.</span><span class="sxs-lookup"><span data-stu-id="c0070-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="c0070-112">Таким образом, многие разделы Справки, посвященные рабочим процессам, касаются утверждения.</span><span class="sxs-lookup"><span data-stu-id="c0070-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="c0070-113">В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.</span><span class="sxs-lookup"><span data-stu-id="c0070-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="c0070-114">**Чтобы**</span><span class="sxs-lookup"><span data-stu-id="c0070-114">**To**</span></span>|<span data-ttu-id="c0070-115">**Смотрите**</span><span class="sxs-lookup"><span data-stu-id="c0070-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="c0070-116">Установите начало запуска рабочего процесса на тот момент, когда произойдет первое событие входа.</span><span class="sxs-lookup"><span data-stu-id="c0070-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="c0070-117">Практическое руководство. Включение рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="c0070-117">How to: Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="c0070-118">Запрос утверждения для задачи, утверждение, отклонение или делегирование утверждений утверждающим, отправка или просмотр уведомлений об утверждении.</span><span class="sxs-lookup"><span data-stu-id="c0070-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="c0070-119">Практическое руководство. Использование рабочего процесса утверждения</span><span class="sxs-lookup"><span data-stu-id="c0070-119">How to: Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="c0070-120">Создание шагов рабочего процесса, которые ограничивают использование записей определенного типа до наступления определенного события, например утверждения записи.</span><span class="sxs-lookup"><span data-stu-id="c0070-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="c0070-121">Практическое руководство. Ограничение и разрешение использования записи</span><span class="sxs-lookup"><span data-stu-id="c0070-121">How to: Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="c0070-122">Просмотр экземпляров шагов рабочего процесса в статусе "Завершено".</span><span class="sxs-lookup"><span data-stu-id="c0070-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="c0070-123">Практическое руководство. Просмотр архивированных экземпляров шагов рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="c0070-123">How to: View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="c0070-124">Удаление рабочего процесса, про который известно, что он больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="c0070-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="c0070-125">Практическое руководство. Удаление рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="c0070-125">How to: Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="c0070-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c0070-126">See Also</span></span>  
<span data-ttu-id="c0070-127">[Настройка рабочих процессов](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c0070-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="c0070-128">[Рабочий процесс](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="c0070-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="c0070-129">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0070-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
