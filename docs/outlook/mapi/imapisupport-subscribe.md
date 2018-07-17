---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792448"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="3dd55-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="3dd55-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="3dd55-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3dd55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3dd55-105">Registriert ein Advise-Empfänger Erhalt von Benachrichtigungen über MAPI an.</span><span class="sxs-lookup"><span data-stu-id="3dd55-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3dd55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dd55-106">Parameters</span></span>

 <span data-ttu-id="3dd55-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="3dd55-107">_lpKey_</span></span>
  
> <span data-ttu-id="3dd55-108">[in] Ein Zeiger auf eine Benachrichtigung-Schlüssel, der Advise-Source-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3dd55-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="3dd55-109">Der Parameter _LpKey_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3dd55-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3dd55-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="3dd55-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="3dd55-111">[in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dd55-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="3dd55-112">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3dd55-112">The following values are valid:</span></span>
    
 <span data-ttu-id="3dd55-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="3dd55-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="3dd55-114">Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3dd55-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="3dd55-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="3dd55-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="3dd55-116">Speicheranbieter Register für Benachrichtigungen über Ereignisse, die speziell für die bestimmten Adressbuch oder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3dd55-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="3dd55-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="3dd55-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="3dd55-118">Register für die Benachrichtigung über den Empfang von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3dd55-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="3dd55-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="3dd55-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="3dd55-120">Register für die Benachrichtigung über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="3dd55-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="3dd55-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="3dd55-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="3dd55-122">Register für Benachrichtigungen zu einem Objekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="3dd55-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="3dd55-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="3dd55-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="3dd55-124">Register für Benachrichtigungen zu einem Objekt, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3dd55-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="3dd55-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="3dd55-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="3dd55-126">Register für Benachrichtigungen zu einem Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3dd55-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="3dd55-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="3dd55-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="3dd55-128">Register für Benachrichtigungen zu einem Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="3dd55-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="3dd55-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="3dd55-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="3dd55-130">Register für die Benachrichtigung über den Abschluss der Suchvorgang.</span><span class="sxs-lookup"><span data-stu-id="3dd55-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="3dd55-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3dd55-131">_ulFlags_</span></span>
  
> <span data-ttu-id="3dd55-132">[in] Eine Bitmaske aus Flags, die steuert, wie die Benachrichtigung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dd55-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="3dd55-133">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3dd55-133">The following flag can be set:</span></span>
    
<span data-ttu-id="3dd55-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="3dd55-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="3dd55-135">Wenn der Anrufer die [IMAPISupport::Notify](imapisupport-notify.md) -Methode zum Generieren von Benachrichtigungen für diese Advise-Empfänger aufruft, sollten **Benachrichtigen** alle erforderlichen Aufrufe advise-senken, vor der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="3dd55-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="3dd55-136">Wenn dieses Flag nicht festgelegt ist, Benachrichtigung ist asynchron und Rückrufe werden in der Warteschlange für die Prozesse, die sich dafür angemeldet haben und gestartet, wenn die Prozesse der CPU Kontrolle.</span><span class="sxs-lookup"><span data-stu-id="3dd55-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="3dd55-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="3dd55-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="3dd55-138">[in] Ein Zeiger auf eine Advise-Empfängerobjekt.</span><span class="sxs-lookup"><span data-stu-id="3dd55-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="3dd55-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="3dd55-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="3dd55-140">[out] Ein Zeiger auf eine Verbindung ungleich NULL-Zahl, die Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3dd55-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3dd55-141">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3dd55-141">Return value</span></span>

<span data-ttu-id="3dd55-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dd55-142">S_OK</span></span> 
  
> <span data-ttu-id="3dd55-143">Die benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3dd55-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dd55-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3dd55-144">Remarks</span></span>

<span data-ttu-id="3dd55-145">Die **IMAPISupport::Subscribe** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="3dd55-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="3dd55-146">Dienstanbieter Aufrufen **Abonnieren** von einem ihrer **Advise** -Methoden, um MAPI, um die Benachrichtigungen verwalten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3dd55-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3dd55-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3dd55-147">Notes to callers</span></span>

<span data-ttu-id="3dd55-148">Um die Methoden des MAPI-Unterstützung für die Benachrichtigung zu verwenden, erstellen Sie einen Product Key für die Advise-Quelle das Objekt über welche Benachrichtigungen generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dd55-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="3dd55-149">Der Wert des Schlüssels muss eindeutig sein und auf einfache Weise neu generiert werden sollte jeder Änderung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3dd55-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="3dd55-150">MAPI verwendet den Benachrichtigung Schlüssel um zu suchenden alle Callback-Funktionen, die über die [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion für die entsprechenden Advise-Quelle registriert.</span><span class="sxs-lookup"><span data-stu-id="3dd55-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="3dd55-151">Übergeben Sie dieser Schlüssel an **IMAPISupport::Notify** , wenn Sie eine Benachrichtigung für die entsprechenden Advise-Quelle erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="3dd55-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="3dd55-152">Das Flag NOTIFY_SYNC wirkt sich auf den Betrieb von nachfolgende Aufrufe **benachrichtigt werden soll**.</span><span class="sxs-lookup"><span data-stu-id="3dd55-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="3dd55-153">Wenn Sie NOTIFY_SYNC festlegen, gibt **Benachrichtigen** bis zum Abschluss aller erforderlichen Mitteilungen senden keine zurück.</span><span class="sxs-lookup"><span data-stu-id="3dd55-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="3dd55-154">Wenn Sie nicht NOTIFY_SYNC festlegen, arbeitet **Benachrichtigen** asynchron möglicherweise zurückgeben, bevor alle die Benachrichtigungen gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="3dd55-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dd55-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd55-155">See also</span></span>



[<span data-ttu-id="3dd55-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3dd55-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="3dd55-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3dd55-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3dd55-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="3dd55-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="3dd55-159">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3dd55-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="3dd55-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="3dd55-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="3dd55-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3dd55-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
