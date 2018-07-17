---
title: BENACHRICHTIGUNG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793306"
---
# <a name="notification"></a><span data-ttu-id="b3749-103">BENACHRICHTIGUNG</span><span class="sxs-lookup"><span data-stu-id="b3749-103">NOTIFICATION</span></span>
 
<span data-ttu-id="b3749-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3749-105">Enthält Informationen über ein Ereignis, das aufgetreten ist und die Daten, die das Ereignis betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="b3749-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3749-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b3749-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3749-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3749-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="b3749-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3749-108">Members</span></span>

<span data-ttu-id="b3749-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="b3749-109">**ulEventType**</span></span>
  
> <span data-ttu-id="b3749-110">Typ der Benachrichtigungsereignis, das aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b3749-110">Type of notification event that occurred.</span></span> <span data-ttu-id="b3749-111">Der Wert des Elements **UlEventType** entspricht der Struktur, die in der Union **Info** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b3749-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="b3749-112">Das Element **UlEventType** kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b3749-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="b3749-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="b3749-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="b3749-114">Ein globaler Fehler ist aufgetreten, wie eine Sitzung Herunterfahren ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3749-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="b3749-115">Das **Info** -Element enthält eine [ERROR_NOTIFICATION](error_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="b3749-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="b3749-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="b3749-117">Ein internes Ereignis von einem bestimmten Dienstanbieter definierten ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b3749-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="b3749-118">Das **Info** -Element enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="b3749-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="b3749-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="b3749-120">Eine Nachricht übermittelt wurde, um den entsprechenden Ordner für die Nachrichtenklasse empfangen und wartet auf Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b3749-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="b3749-121">Das **Info** -Element enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="b3749-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="b3749-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="b3749-123">Ein MAPI-Objekt wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="b3749-123">A MAPI object has been copied.</span></span> <span data-ttu-id="b3749-124">Das **Info** -Element enthält eine [OBJECT_NOTIFICATION](object_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="b3749-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="b3749-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="b3749-126">Ein MAPI-Objekt wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3749-126">A MAPI object has been created.</span></span> <span data-ttu-id="b3749-127">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="b3749-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="b3749-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="b3749-129">Ein MAPI-Objekt wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b3749-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="b3749-130">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="b3749-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="b3749-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="b3749-132">Ein MAPI-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b3749-132">A MAPI object has changed.</span></span> <span data-ttu-id="b3749-133">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="b3749-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="b3749-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="b3749-135">Einen Nachrichtenspeicher oder Adresse Adressbuch-Objekt verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="b3749-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="b3749-136">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="b3749-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="b3749-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="b3749-138">Suchvorgang beendet wurde, und die Ergebnisse verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b3749-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="b3749-139">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="b3749-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="b3749-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="b3749-141">Die Informationen in einer Tabelle wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="b3749-141">Information in a table has changed.</span></span> <span data-ttu-id="b3749-142">Das **Info** -Element enthält eine [TABLE_NOTIFICATION](table_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3749-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="b3749-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="b3749-143">**info**</span></span>
  
> <span data-ttu-id="b3749-144">Union der Benachrichtigung Strukturen zur Beschreibung der betreffenden Daten für einen bestimmten Typ des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="b3749-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="b3749-145">Die Struktur im **Info** -Member enthalten, hängt von den Wert des Elements **UlEventType** ab.</span><span class="sxs-lookup"><span data-stu-id="b3749-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b3749-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3749-146">Remarks</span></span>

<span data-ttu-id="b3749-147">Ein oder mehrere **Benachrichtigung** Strukturen werden als Eingabeparameter mit jedem Aufruf einer registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3749-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b3749-148">Die **Benachrichtigung** Strukturen enthalten Informationen zu den bestimmte Ereignisse, die aufgetreten sind, und der betroffene Objekte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b3749-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="b3749-149">Bevor Clients oder -Dienstanbieter erhalten eine Benachrichtigung die Struktur verwenden können Verarbeitung des Ereignisses, müssen sie den Ereignistyp überprüfen, wie im **UlEventType** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="b3749-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="b3749-150">Beispielsweise druckt das Codebeispiel, das hier gezeigte überprüft, ob das Eintreffen einer neuen Nachricht und beim Erkennen eines Ereignisses dieser Art, die Nachrichtenklasse der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b3749-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="b3749-151">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b3749-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b3749-152">**Thema**</span><span class="sxs-lookup"><span data-stu-id="b3749-152">**Topic**</span></span>|<span data-ttu-id="b3749-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3749-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3749-154">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="b3749-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b3749-155">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="b3749-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b3749-156">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b3749-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b3749-157">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3749-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b3749-158">Benachrichtigung bei unterstützenden</span><span class="sxs-lookup"><span data-stu-id="b3749-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b3749-159">Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b3749-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3749-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3749-160">See also</span></span>


- [<span data-ttu-id="b3749-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="b3749-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="b3749-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="b3749-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="b3749-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="b3749-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3749-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="b3749-167">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b3749-167">MAPI Structures</span></span>](mapi-structures.md)
