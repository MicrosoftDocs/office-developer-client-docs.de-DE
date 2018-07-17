---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792067"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="1938f-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="1938f-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="1938f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1938f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1938f-105">Gibt an, dass der MAPI-Client der Client sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1938f-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="1938f-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1938f-106">Return value</span></span>

<span data-ttu-id="1938f-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="1938f-107">S_OK</span></span>
  
> <span data-ttu-id="1938f-108">MAPI-Subsystems hat geladen MAPI-Anbieter angegeben, dass der MAPI-Client wird sofort beendet, und die MAPI-Anbieter bereit für den Client beenden sind.</span><span class="sxs-lookup"><span data-stu-id="1938f-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="1938f-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1938f-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="1938f-110">MAPI-Subsystems bietet keine Unterstützung für schnelle Herunterfahren von Clients.</span><span class="sxs-lookup"><span data-stu-id="1938f-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1938f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1938f-111">Remarks</span></span>

<span data-ttu-id="1938f-112">Verlust von Daten über das schnelle Herunterfahren von einem MAPI-Client zu vermeiden, sollten MAPI-Clients die basierend auf dem S_OK Ergebnis des MAPI-Subsystems in zurückgegebene [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::DoFastShutdown** -Methoden aufrufen. die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1938f-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="1938f-113">Weitere Informationen finden Sie unter [Bewährte Methoden für Schnelles Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="1938f-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1938f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1938f-114">See also</span></span>



[<span data-ttu-id="1938f-115">IMAPIClientShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1938f-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="1938f-116">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="1938f-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
