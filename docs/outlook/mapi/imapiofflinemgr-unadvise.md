---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404855"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="25839-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="25839-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="25839-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25839-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25839-105">Bricht Rückrufe für ein Offlineobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="25839-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="25839-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25839-106">Parameters</span></span>

 <span data-ttu-id="25839-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25839-107">_ulFlags_</span></span>
  
> <span data-ttu-id="25839-108">[in] Flags zum Abbrechen des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="25839-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="25839-109">Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25839-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="25839-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="25839-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="25839-111">[in] Ein Ratentoken, das die Rückrufregistrierung identifiziert, die abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="25839-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="25839-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25839-112">Return value</span></span>

<span data-ttu-id="25839-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="25839-113">S_OK</span></span>
  
> <span data-ttu-id="25839-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="25839-114">The call was successful.</span></span> <span data-ttu-id="25839-115">Dieser Aufruf muss eine S_OK.</span><span class="sxs-lookup"><span data-stu-id="25839-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25839-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25839-116">Remarks</span></span>

<span data-ttu-id="25839-117">Entfernt die Registrierung für den Rückruf, der *ulAdviseToken* zugeordnet war, die aus einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise zurückgegeben wurde.](imapiofflinemgr-advise.md)**</span><span class="sxs-lookup"><span data-stu-id="25839-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="25839-118">Bewirkt, **dass das IMAPIOfflineMgr-Objekt** seinen Verweis auf das **[IMAPIOfflineNotify-Objekt](imapiofflinenotifyiunknown.md)** frei gibt, das *ulAdviseToken zugeordnet ist.*</span><span class="sxs-lookup"><span data-stu-id="25839-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25839-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25839-119">See also</span></span>



[<span data-ttu-id="25839-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="25839-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="25839-121">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="25839-121">MAPI Constants</span></span>](mapi-constants.md)

