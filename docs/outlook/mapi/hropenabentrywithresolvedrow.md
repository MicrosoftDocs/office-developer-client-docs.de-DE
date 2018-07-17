---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e39f4edc871b49675f1ffcc1bc541345c8829d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791956"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="dcd6c-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="dcd6c-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="dcd6c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcd6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcd6c-105">Führt die gleiche Funktion wie [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , außer dass automatisch die **EmsabpUID** aus der Zeile aufgelöst wird abgerufen, und die **EntryID öffnet**.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcd6c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dcd6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="dcd6c-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="dcd6c-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="dcd6c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dcd6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dcd6c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dcd6c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dcd6c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dcd6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="dcd6c-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="dcd6c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="dcd6c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcd6c-112">Parameters</span></span>

 <span data-ttu-id="dcd6c-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-113">_prwResolved_</span></span>
  
> <span data-ttu-id="dcd6c-114">[in] Ein Zeiger auf die aufgelöste Zeile, die zum Abrufen der **EmsabpUID** , und öffnen Sie die **Eintrags-ID**verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="dcd6c-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="dcd6c-116">[in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="dcd6c-117">Es darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dcd6c-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="dcd6c-119">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dcd6c-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="dcd6c-121">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="dcd6c-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-122">_lpInterface_</span></span>
  
> <span data-ttu-id="dcd6c-123">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, die den Eintrag open Zugriff auf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="dcd6c-124">Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="dcd6c-125">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="dcd6c-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="dcd6c-126">Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md)und Containern, ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="dcd6c-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="dcd6c-127">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="dcd6c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="dcd6c-129">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="dcd6c-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dcd6c-130">The following flags can be set:</span></span>
    
<span data-ttu-id="dcd6c-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dcd6c-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="dcd6c-132">Fordert, dass der Eintrag mit den maximalen zulässigen Netzwerk- und Client Berechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="dcd6c-133">Wenn der Client über Lese- und Schreibberechtigungen, versucht der Adressbuchanbieter beispielsweise, öffnen Sie den Eintrag mit Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="dcd6c-134">Der Client kann die Zugriffsebene abzurufen, die durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode des Eintrags öffnen und das Abrufen der Eigenschaft PR_ACCESS_LEVEL (PidTagAccessLevel) gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="dcd6c-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="dcd6c-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="dcd6c-136">Verwendet nur das Offlineadressbuch namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="dcd6c-137">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dcd6c-138">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="dcd6c-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="dcd6c-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="dcd6c-140">Ermöglicht den Anruf, potenziell erfolgreich ausgeführt werden kann, bevor der Eintrag vollständig geöffnet und verfügbar ist, dass dies, dass nachfolgende Aufrufe von den Eintrag möglicherweise einen Fehler zurück, ist.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="dcd6c-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="dcd6c-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="dcd6c-142">Verwendet nur die globale Adressliste namensauflösung ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="dcd6c-143">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="dcd6c-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dcd6c-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="dcd6c-145">Anforderungen, denen mit der Eintrag geöffnet werden Lese- und Schreibberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="dcd6c-146">Da die Einträge in der Standardeinstellung mit schreibgeschützten Zugriff geöffnet sind, sollte Clients nicht davon ausgehen, das Lesen und schreiben, dass die Berechtigung erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="dcd6c-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="dcd6c-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="dcd6c-148">Das Offlineadressbuch wird nicht zum Ausführen von namensauflösung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="dcd6c-149">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="dcd6c-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="dcd6c-151">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="dcd6c-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="dcd6c-152">_lppUnk_</span></span>
  
> <span data-ttu-id="dcd6c-153">[out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="dcd6c-153">[out] A pointer to a pointer of the opened entry.</span></span>
    
