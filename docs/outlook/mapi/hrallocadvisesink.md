---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428900"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="f62a5-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f62a5-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="f62a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f62a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f62a5-105">Erstellt ein Advise-Sink-Objekt, das einen durch die aufrufende Implementierung angegebenen Kontext und eine Rückruffunktion, die durch eine Ereignisbenachrichtigung ausgelöst werden soll, angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f62a5-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f62a5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f62a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f62a5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f62a5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f62a5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f62a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f62a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f62a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f62a5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f62a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="f62a5-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f62a5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="f62a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f62a5-112">Parameters</span></span>

 <span data-ttu-id="f62a5-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="f62a5-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="f62a5-114">[in] Zeiger auf eine Rückruffunktion basierend auf dem [NOTIFCALLBACK-Prototyp,](notifcallback.md) den MAPI aufrufen soll, wenn ein Benachrichtigungsereignis für die neu erstellte Hinweissenke auftritt.</span><span class="sxs-lookup"><span data-stu-id="f62a5-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="f62a5-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="f62a5-115">_lpvContext_</span></span>
  
> <span data-ttu-id="f62a5-116">[in] Zeiger auf Aufruferdaten, die an die Rückruffunktion übergeben werden, wenn MAPI sie aufruft.</span><span class="sxs-lookup"><span data-stu-id="f62a5-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="f62a5-117">Die Anruferdaten können eine Adresse darstellen, die für den Client oder Anbieter von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="f62a5-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="f62a5-118">In der Regel stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf die Adresse eines Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="f62a5-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="f62a5-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f62a5-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="f62a5-120">[out] Zeiger auf einen Zeiger auf ein Advise Sink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f62a5-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f62a5-121">Return value</span><span class="sxs-lookup"><span data-stu-id="f62a5-121">Return value</span></span>

<span data-ttu-id="f62a5-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="f62a5-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f62a5-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f62a5-123">Remarks</span></span>

<span data-ttu-id="f62a5-124">Um die **HrAllocAdviseSink-Funktion** zu verwenden, erstellt eine Clientanwendung oder ein Dienstanbieter ein Objekt zum Empfangen von Benachrichtigungen, erstellt eine Benachrichtigungsrückruffunktion basierend auf dem [NOTIFCALLBACK-Funktionsprototyp,](notifcallback.md) der mit diesem Objekt verwendet wird, und übergibt einen Zeiger auf das Objekt in der **HrAllocAdviseSink-Funktion** als _lpvContext-Wert._</span><span class="sxs-lookup"><span data-stu-id="f62a5-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="f62a5-125">Dies führt eine Benachrichtigung aus. und im Rahmen des Benachrichtigungsprozesses ruft MAPI die Rückruffunktion mit dem Objektzeiger als Kontext auf.</span><span class="sxs-lookup"><span data-stu-id="f62a5-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="f62a5-126">MAPI implementiert sein Benachrichtigungsmodul asynchron.</span><span class="sxs-lookup"><span data-stu-id="f62a5-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="f62a5-127">In C++ kann der Benachrichtigungsrückruf eine Objektmethode sein.</span><span class="sxs-lookup"><span data-stu-id="f62a5-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="f62a5-128">Wenn das Objekt, das die Benachrichtigung generiert, nicht vorhanden ist, muss der Client oder Anbieter, der eine Benachrichtigung anfordert, eine separate Referenzanzahl für dieses Objekt für die Hinweissenke des Objekts behalten.</span><span class="sxs-lookup"><span data-stu-id="f62a5-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="f62a5-129">**HrAllocAdviseSink** sollte sparsam verwendet werden. Es ist sicherer für Kunden, eigene Ratensenken zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f62a5-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

