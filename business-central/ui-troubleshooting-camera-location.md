---
title: 'Устранение неполадок: доступ к камере и геопозиции'
description: В этой статье описывается, как устранять неполадки с доступом к камере и геопозиции в Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics365-business-central
ms.openlocfilehash: befb7af01ba26512a4b62005e81b5a3ff351b02f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324476"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="08e05-103">Устранение неполадок: доступ к камере и геопозиции</span><span class="sxs-lookup"><span data-stu-id="08e05-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="08e05-104">При попытке доступа к камере и геопозиции устройства из [!INCLUDE[prodshort](includes/prodshort.md)] могут возникнуть некоторые проблемы.</span><span class="sxs-lookup"><span data-stu-id="08e05-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="08e05-105">Ниже перечислены возможные причины этих проблем и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="08e05-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="08e05-106">На устройстве должны быть камера и механизм определения геопозиции</span><span class="sxs-lookup"><span data-stu-id="08e05-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="08e05-107">Для доступа к камере и геопозиции устройства пользователя на устройстве должна быть физическая камера и механизм определения геопозиции.</span><span class="sxs-lookup"><span data-stu-id="08e05-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="08e05-108">Если на вашем устройстве есть камеры и механизм определения геопозиции, однако у вас все равно возникают проблемы, возможно, нужно обновить или переустановить некоторые драйверы.</span><span class="sxs-lookup"><span data-stu-id="08e05-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="08e05-109">Даже если вы не уверены в этом, мы всегда рекомендуем обновить операционную систему устройства, драйверы и браузер до последней версии, чтобы обеспечить максимально эффективную работу.</span><span class="sxs-lookup"><span data-stu-id="08e05-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="08e05-110">Не даны разрешения на доступ</span><span class="sxs-lookup"><span data-stu-id="08e05-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="08e05-111">Необходимо включить доступ к камере и местоположению в настройках конфиденциальности вашего устройства и явно дать [!INCLUDE[prodshort](includes/prodshort.md)] разрешение на доступ к ним.</span><span class="sxs-lookup"><span data-stu-id="08e05-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="08e05-112">Например, чтобы просмотреть или изменить разрешения для устройства с ОС Windows, откройте **Параметры**, выберите **Конфиденциальность** и **Разрешения для приложений**.</span><span class="sxs-lookup"><span data-stu-id="08e05-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="08e05-113">В случае мобильных устройств необходимо предоставить разрешения на доступ к камере и геопозиции мобильном приложению [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="08e05-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="08e05-114">Чтобы сделать это на устройстве с iOS, откройте **Настройки**, выберите **Конфиденциальность**, а затем **Камера** или **Службы геолокации**.</span><span class="sxs-lookup"><span data-stu-id="08e05-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="08e05-115">На устройствах с Android откройте **Настройки**, выберите **Приложения и уведомления**, **Дополнительно**, **Разрешения приложений**, а затем **Камера** или **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="08e05-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="08e05-116">Кроме того, если вы используете [!INCLUDE[prodshort](includes/prodshort.md)] в браузере, вы также должны предоставить сайту [!INCLUDE[prodshort](includes/prodshort.md)] разрешение на доступ к камере или информации о местоположении.</span><span class="sxs-lookup"><span data-stu-id="08e05-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="08e05-117">Чтобы просмотреть или изменить разрешения сайта в браузере Microsoft Edge, откройте **Параметры**, выберите **Разрешения для сайта**, а затем **Камера** или **Расположение**.</span><span class="sxs-lookup"><span data-stu-id="08e05-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="08e05-118">Обратите внимание, что в других браузерах процедура может быть другой.</span><span class="sxs-lookup"><span data-stu-id="08e05-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="08e05-119">По умолчанию на устройстве или в браузере появляется запрос на доступ к этим возможностям, когда пользователь активирует их в первый раз.</span><span class="sxs-lookup"><span data-stu-id="08e05-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="08e05-120">Некоторые старые браузеры не предоставляют доступ к камере и геопозиции.</span><span class="sxs-lookup"><span data-stu-id="08e05-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="08e05-121">Например, камера недоступна в Internet Explorer или в старом браузере Edge.</span><span class="sxs-lookup"><span data-stu-id="08e05-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="08e05-122">Соединение с веб-клиентом небезопасно</span><span class="sxs-lookup"><span data-stu-id="08e05-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="08e05-123">Камера и местоположение доступны только при условии, что доступ к веб-клиенту осуществляется по HTTP-подключениям, работающих по протоколу SSL, со схемой URI `https://`.</span><span class="sxs-lookup"><span data-stu-id="08e05-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="08e05-124">Единственным исключением является подключение к `http://localhost`, которое используется для разработки и тестирования.</span><span class="sxs-lookup"><span data-stu-id="08e05-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="08e05-125">Работа с технологиями виртуализации</span><span class="sxs-lookup"><span data-stu-id="08e05-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="08e05-126">При подключении к [!INCLUDE[prodshort](includes/prodshort.md)] через удаленный рабочий стол или другое решение виртуализации доступ к камере или геопозиции может быть невозможен.</span><span class="sxs-lookup"><span data-stu-id="08e05-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="08e05-127">В этом необходимо использовать физическую систему.</span><span class="sxs-lookup"><span data-stu-id="08e05-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="08e05-128">Антивирусное программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="08e05-128">Antivirus Software</span></span>
<span data-ttu-id="08e05-129">Некоторые антивирусные программы по умолчанию блокируют доступ к камере и геопозиции.</span><span class="sxs-lookup"><span data-stu-id="08e05-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="08e05-130">Не забудьте проверить настройки антивирусного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="08e05-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="08e05-131">См. также</span><span class="sxs-lookup"><span data-stu-id="08e05-131">See Also</span></span>
[<span data-ttu-id="08e05-132">Реализация камеры на AL</span><span class="sxs-lookup"><span data-stu-id="08e05-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="08e05-133">Реализация геопозиции на AL</span><span class="sxs-lookup"><span data-stu-id="08e05-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)