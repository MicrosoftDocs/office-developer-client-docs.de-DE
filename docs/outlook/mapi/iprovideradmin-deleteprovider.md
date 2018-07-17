---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792765"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="3a6dc-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="3a6dc-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="3a6dc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a6dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a6dc-105">Löscht einen Dienstanbieter aus der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="3a6dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a6dc-106">Parameters</span></span>

 <span data-ttu-id="3a6dc-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="3a6dc-107">_lpUID_</span></span>
  
> <span data-ttu-id="3a6dc-108">[in, out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner, der den enthält zu löschenden-Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3a6dc-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3a6dc-109">Return value</span></span>

<span data-ttu-id="3a6dc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a6dc-110">S_OK</span></span> 
  
> <span data-ttu-id="3a6dc-111">Der Anbieter wurde aus dem Nachrichtendienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="3a6dc-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3a6dc-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3a6dc-113">Die **MAPIUID** auf den durch den Parameter _LpUID_ verwiesen wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a6dc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a6dc-114">Remarks</span></span>

<span data-ttu-id="3a6dc-115">Die **IProviderAdmin::DeleteProvider** -Methode löscht einen Dienstanbieter aus den Dienst.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="3a6dc-116">**DeleteProvider** bestimmt den Dienstanbieter zu löschen, indem Sie die **MAPIUID** -Struktur, die auf den _LpUID_ mit den IDs durch die aktiv-Dienstanbieter registriert.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="3a6dc-117">Die meisten Message-Dienste können nicht Anbieter gelöscht werden, während das Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="3a6dc-118">Wenn der Anbieter löschen verwendet wird, **DeleteProvider** es zum Löschen, anstatt sie zu entfernen sofort markiert und gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="3a6dc-119">Wenn der Anbieter nicht mehr verwendet wird, wird es gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="3a6dc-120">**DeleteProvider** Ruft die Messagingdiensts Eintrag Point-Funktion, bevor der Anbieter aus dem Dienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="3a6dc-121">Der Parameter _UlContext_ wird auf MSG_SERVICE_PROVIDER_DELETE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="3a6dc-122">Die Nachricht Service Eintrag-Funktion werden die folgenden Aufgaben ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="3a6dc-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="3a6dc-123">Löscht den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="3a6dc-124">Löscht den Dienstanbieter Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="3a6dc-125">Die Nachricht Service Eintrag-Funktion wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3a6dc-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a6dc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a6dc-126">See also</span></span>



[<span data-ttu-id="3a6dc-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3a6dc-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3a6dc-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="3a6dc-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="3a6dc-129">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a6dc-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
