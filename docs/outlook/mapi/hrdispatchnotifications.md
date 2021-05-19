---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348097"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="1dc33-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="1dc33-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="1dc33-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dc33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dc33-105">Erzwingt die Versendung aller Benachrichtigungen in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1dc33-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1dc33-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1dc33-106">Header file:</span></span>  <br/> |<span data-ttu-id="1dc33-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1dc33-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1dc33-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1dc33-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1dc33-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1dc33-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1dc33-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1dc33-110">Called by:</span></span>  <br/> |<span data-ttu-id="1dc33-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1dc33-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1dc33-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dc33-112">Parameters</span></span>

 <span data-ttu-id="1dc33-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1dc33-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1dc33-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="1dc33-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1dc33-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dc33-115">Return value</span></span>

<span data-ttu-id="1dc33-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1dc33-116">S_OK</span></span>
  
> <span data-ttu-id="1dc33-117">Alle Benachrichtigungen in der Warteschlange wurden gesendet.</span><span class="sxs-lookup"><span data-stu-id="1dc33-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="1dc33-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1dc33-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="1dc33-119">WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1dc33-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="1dc33-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="1dc33-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="1dc33-121">MAPI wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1dc33-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1dc33-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1dc33-122">Remarks</span></span>

<span data-ttu-id="1dc33-123">Die **HrDispatchNotifications-Funktion** bewirkt, dass MAPI alle Benachrichtigungen versendet, die derzeit im MAPI-Benachrichtigungsmodul in der Warteschlange stehen, ohne auf einen Nachrichtenversand zu warten.</span><span class="sxs-lookup"><span data-stu-id="1dc33-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="1dc33-124">Dies kann sich positiv auf die Arbeitsspeicherauslastung aus wirken.</span><span class="sxs-lookup"><span data-stu-id="1dc33-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="1dc33-125">Weitere Informationen finden Sie unter [Erzwingen einer Benachrichtigung](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1dc33-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1dc33-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1dc33-126">Notes to callers</span></span>

<span data-ttu-id="1dc33-127">Einige Anwendungen warten mit den Funktionen [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) und [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) in einer Timeoutschleife auf eine Windows Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1dc33-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="1dc33-128">Auf allen bis auf die schnellsten Plattformen kann es zu Leistungsausfällen oder sogar Zusperren von Benachrichtigungen für solche Anwendungen führen.</span><span class="sxs-lookup"><span data-stu-id="1dc33-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="1dc33-129">Die **Verwendung von HrDispatchNotifications** reduziert nicht nur Code, sondern verbessert auch die Leistung.</span><span class="sxs-lookup"><span data-stu-id="1dc33-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

