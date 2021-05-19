---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Ruft eine automatisch konfigurierte ISocialSession-Schnittstelle ab.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417441"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="cbf97-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="cbf97-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="cbf97-104">Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="cbf97-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="cbf97-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbf97-105">Parameters</span></span>

<span data-ttu-id="cbf97-106">_session_</span><span class="sxs-lookup"><span data-stu-id="cbf97-106">_session_</span></span>
  
> <span data-ttu-id="cbf97-107">[out] Eine **ISocialSession**-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cbf97-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbf97-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbf97-108">Remarks</span></span>

<span data-ttu-id="cbf97-109">Die zurückgegebene **ISocialSession**-Schnittstelle wird basierend auf einer anbieterspezifischen Methode automatisch am Netzwerk angemeldet.</span><span class="sxs-lookup"><span data-stu-id="cbf97-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="cbf97-110">Der Anbieter sollte den Fehler OSC_E_NOT_IMPLEMENTED zurückgeben, wenn das soziale Netzwerk die automatische Konfiguration nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbf97-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="cbf97-111">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cbf97-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbf97-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbf97-112">See also</span></span>

- [<span data-ttu-id="cbf97-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbf97-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

