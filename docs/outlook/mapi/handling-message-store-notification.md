---
title: Behandeln von Store-Benachrichtigung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791810"
---
# <a name="handling-message-store-notification"></a><span data-ttu-id="ec03f-103">Behandeln von Store-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="ec03f-103">Handling message store notification</span></span>
  
<span data-ttu-id="ec03f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec03f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec03f-105">Um Benachrichtigungen über Textnachrichten Store zu registrieren, rufen Sie die [IMAPISession::Advise](imapisession-advise.md) oder [IMsgStore::Advise](imsgstore-advise.md) -Methode, und geben Sie einen Nachrichtenspeicher, Ordner oder Eintrags-ID der Nachricht in den Inhalt des Parameters _LpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ec03f-105">To register for message store notifications, call either the [IMAPISession::Advise](imapisession-advise.md) or [IMsgStore::Advise](imsgstore-advise.md) method and specify a message store, folder, or message entry identifier in the contents of the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="ec03f-106">Nachricht Anbieter unterstützen Objekt und Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ec03f-106">Message store providers support both object and table notifications.</span></span> <span data-ttu-id="ec03f-107">Ob Sie registrieren mit bestimmten Nachricht Store-Objekten, die Ordner Hierarchie und der Inhalt der Tabellen, die diese Objekte beschreiben oder beides Objekte und Tabellen hängt von der Benachrichtigungen angezeigt wird, die Anrufe Sie Operationen ausführen, stellen Sie erwarten und wie der Nachricht Speicheranbieter unterstützt die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="ec03f-107">Whether you register with particular message store objects, with the folder hierarchy and contents tables that describe these objects, or with both objects and tables depends on the notifications you expect to see, the calls you make to perform operations, and how the message store provider supports notification.</span></span> 
  
<span data-ttu-id="ec03f-108">Da MAPI Flexibilität bei der Unterstützung von Anbietern wie Benachrichtigungen, beachten Sie, dass Sie nicht immer den gleichen Typ der Benachrichtigung als Antwort auf ein bestimmtes Ereignis alle Nachricht-Anbieter empfängt.</span><span class="sxs-lookup"><span data-stu-id="ec03f-108">Because MAPI allows flexibility in how providers support notifications, be aware that you will not always receive the same type of notification in response to a particular event from all message store providers.</span></span> <span data-ttu-id="ec03f-109">Einige Anbieter Nachricht unterstützen überhaupt keine Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="ec03f-109">Some message store providers do not support notifications at all.</span></span> <span data-ttu-id="ec03f-110">Um festzustellen, ob der Nachrichtenspeicher verwendeten Benachrichtigung, suchen Sie nach der STORE_NOTIFY_OK Bit in der Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec03f-110">To determine if the message store you are using supports notification, look for the STORE_NOTIFY_OK bit in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ec03f-111">An einem Ende des Spektrums des Nachrichtenspeichers sind Anbieter, die Benachrichtigung zu unterstützen die Anbieter, die "rich" Benachrichtigungen generieren. Diese Anbieter senden beschreibende Benachrichtigungen für alle registrierten advise-Quellen.</span><span class="sxs-lookup"><span data-stu-id="ec03f-111">At one end of the spectrum of message store providers that support notification are the providers that generate "rich" notifications; these providers send descriptive notifications for all registered advise sources.</span></span> <span data-ttu-id="ec03f-112">An das andere Ende sind die Nachricht Speicheranbieter, beschränkte Benachrichtigungen zu unterstützen. Diese Anbieter senden allgemeine Benachrichtigungen für eine eingeschränkte Anzahl von Advise-Quellen.</span><span class="sxs-lookup"><span data-stu-id="ec03f-112">At the other end are the message store providers that support limited notifications; these providers send general notifications for a restricted number of advise sources.</span></span> 
  
<span data-ttu-id="ec03f-113">Beispielsweise kopieren eine Nachricht in einen Ordner mit dem Sie registriert haben, um empfangen beide-Objekt kopiert und Objekt verschoben, Benachrichtigungen oder anzeigen, kann möglicherweise nicht die Benachrichtigung-Objekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="ec03f-113">For example, if you copy a message to a folder with which you have registered to receive both object copied and object moved notifications, you may or may not receive the object copied notification.</span></span> <span data-ttu-id="ec03f-114">Unabhängig davon, ob Sie erhalten hängt:</span><span class="sxs-lookup"><span data-stu-id="ec03f-114">Whether or not you receive it depends on:</span></span>
  
- <span data-ttu-id="ec03f-115">Die Methode, die Sie aufgerufen, um die Kopie auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec03f-115">The method that you called to perform the copy.</span></span> <span data-ttu-id="ec03f-116">Dies kann [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)oder [IMAPIProp::CopyProps](imapiprop-copyprops.md)sein.</span><span class="sxs-lookup"><span data-stu-id="ec03f-116">This could be [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md), or [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="ec03f-117">Wie die Nachricht speichern Anbieter implementiert die Copy-Methode.</span><span class="sxs-lookup"><span data-stu-id="ec03f-117">How the message store provider implements the copy method.</span></span>
    
- <span data-ttu-id="ec03f-118">Unabhängig davon, ob der Nachricht Speicheranbieter-Objekt kopiert Benachrichtigungen für Ordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec03f-118">Whether or not the message store provider supports object copied notifications on folders.</span></span>
    
<span data-ttu-id="ec03f-119">Da vorhanden, dass keine strengen Richtlinien, die zum Implementieren der Benachrichtigung für Nachricht beschreiben Anbieter speichern sind, können keine Clients durchgängigen erwarten.</span><span class="sxs-lookup"><span data-stu-id="ec03f-119">Because there are no strict guidelines that describe how to implement event notification for message store providers, clients cannot expect consistent behavior.</span></span> <span data-ttu-id="ec03f-120">MAPI legt Empfehlungen vor, um wie Nachrichtenspeicher Anbieter implementieren Benachrichtigung und die in der folgenden Tabelle Konturen diesen Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="ec03f-120">MAPI does make recommendations as to how message store providers implement event notification and the following table outlines these recommendations.</span></span> <span data-ttu-id="ec03f-121">Lesen die Tabelle wie folgt: nach dem Ausführen dieses Vorgangs in der ersten Spalte erwarten eine Benachrichtigung über den Typ in der zweiten Spalte aufgeführt werden, wenn Sie für diesen Typ, mit dem Objekt in der dritten Spalte aufgeführt registriert haben.</span><span class="sxs-lookup"><span data-stu-id="ec03f-121">Read the table as follows: after you perform the operation in the first column, expect to receive a notification of the type listed in the second column if you have registered for that type with the object listed in the third column.</span></span> <span data-ttu-id="ec03f-122">Beispielsweise nachdem Sie einen Ordner erstellt haben, erhalten Sie eine _FnevObjectCreated_ Benachrichtigung nur, wenn Sie für _FnevObjectCreated_ Benachrichtigungen, mit dem Nachrichtenspeicher registriert haben.</span><span class="sxs-lookup"><span data-stu-id="ec03f-122">For example, after you have created a folder, you will receive an  _fnevObjectCreated_ notification only if you have registered for  _fnevObjectCreated_ notifications with the message store.</span></span> 
  
|<span data-ttu-id="ec03f-123">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="ec03f-123">**Operation**</span></span>|<span data-ttu-id="ec03f-124">**Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="ec03f-124">**Event type**</span></span>|<span data-ttu-id="ec03f-125">**Advise-Quelle**</span><span class="sxs-lookup"><span data-stu-id="ec03f-125">**Advise source**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec03f-126">Erstellen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="ec03f-126">Create a folder</span></span>  <br/> | <span data-ttu-id="ec03f-127">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="ec03f-127">_fnevObjectCreated_</span></span> <br/> |<span data-ttu-id="ec03f-128">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ec03f-128">Message store</span></span>  <br/> |
|<span data-ttu-id="ec03f-129">Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="ec03f-129">Delete a folder</span></span>  <br/> | <span data-ttu-id="ec03f-130">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="ec03f-130">_fnevObjectDeleted_</span></span> <br/> |<span data-ttu-id="ec03f-131">Nachrichtenspeicher Ordner gelöscht</span><span class="sxs-lookup"><span data-stu-id="ec03f-131">Message store Deleted folder</span></span>  <br/> |
|<span data-ttu-id="ec03f-132">Verschieben Sie einen Ordner aus einem Ordner in einen anderen</span><span class="sxs-lookup"><span data-stu-id="ec03f-132">Move a folder from one folder to another</span></span>  <br/> | <span data-ttu-id="ec03f-133">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="ec03f-133">_fnevObjectMoved_</span></span> <br/> |<span data-ttu-id="ec03f-134">Nachrichtenspeicher verschobene Ordner</span><span class="sxs-lookup"><span data-stu-id="ec03f-134">Message store Moved folder</span></span>  <br/> |
|<span data-ttu-id="ec03f-135">Kopieren eines Ordners aus einem Ordner in einen anderen</span><span class="sxs-lookup"><span data-stu-id="ec03f-135">Copy a folder from one folder to another</span></span>  <br/> | <span data-ttu-id="ec03f-136">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="ec03f-136">_fnevObjectCopied_</span></span> <br/> |<span data-ttu-id="ec03f-137">Nachricht speichern und kopiert Ordner (keine _FnevObjectCreated_ Benachrichtigung, die für die neue Kopie des Ordners)</span><span class="sxs-lookup"><span data-stu-id="ec03f-137">Message store and copied folder (no  _fnevObjectCreated_ notification sent for the new copy of the folder)</span></span>  <br/> |
|<span data-ttu-id="ec03f-138">Ändern Sie in einem berechnete-Ordnereigenschaft (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec03f-138">Change in a computed folder property (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>  <br/> | <span data-ttu-id="ec03f-139">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="ec03f-139">_fnevObjectModified_</span></span> <br/> |<span data-ttu-id="ec03f-140">Nachrichtenspeicher Changed-Ordner (keine Benachrichtigung an den übergeordneten Ordner)</span><span class="sxs-lookup"><span data-stu-id="ec03f-140">Message store Changed folder (No notification to parent folder)</span></span>  <br/> |
|<span data-ttu-id="ec03f-141">Erstellen Sie eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec03f-141">Create a message</span></span>  <br/> | <span data-ttu-id="ec03f-142">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="ec03f-142">_fnevObjectCreated_</span></span> <br/> |<span data-ttu-id="ec03f-143">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ec03f-143">Message store</span></span>  <br/> |
|<span data-ttu-id="ec03f-144">Löschen einer Nachricht, verursacht eine Änderung in der übergeordneten Ordners **PR_CONTENT_COUNT** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec03f-144">Delete a message, causing a change in the parent folder's **PR_CONTENT_COUNT** property</span></span>  <br/> | <span data-ttu-id="ec03f-145">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="ec03f-145">_fnevObjectDeleted_</span></span> <br/> |<span data-ttu-id="ec03f-146">Nachrichtenspeicher Deleted Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec03f-146">Message store Deleted message</span></span>  <br/> |
|<span data-ttu-id="ec03f-147">Verschieben Sie eine Nachricht von einem Ordner in einen anderen</span><span class="sxs-lookup"><span data-stu-id="ec03f-147">Move a message from one folder to another</span></span>  <br/> | <span data-ttu-id="ec03f-148">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="ec03f-148">_fnevObjectMoved_</span></span> <br/> |<span data-ttu-id="ec03f-149">Nachrichtenspeicher verschobene Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec03f-149">Message store Moved message</span></span>  <br/> |
|<span data-ttu-id="ec03f-150">Kopieren Sie eine Nachricht von einem Ordner in einen anderen</span><span class="sxs-lookup"><span data-stu-id="ec03f-150">Copy a message from one folder to another</span></span>  <br/> | <span data-ttu-id="ec03f-151">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="ec03f-151">_fnevObjectCopied_</span></span> <br/> |<span data-ttu-id="ec03f-152">Nachrichtenspeicher kopierte Nachricht (keine _FnevObjectCreated_ Benachrichtigung für die neue Kopie der Nachricht)</span><span class="sxs-lookup"><span data-stu-id="ec03f-152">Message store Copied message (No  _fnevObjectCreated_ notification for new copy of the message)</span></span>  <br/> |
|<span data-ttu-id="ec03f-153">Speichern einer Nachricht, verursacht eine Änderung in der übergeordneten Ordners **PR_CONTENT_COUNT** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec03f-153">Save a message, causing a change in the parent folder's **PR_CONTENT_COUNT** property</span></span>  <br/> | <span data-ttu-id="ec03f-154">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="ec03f-154">_fnevObjectCreated_</span></span> <br/> |<span data-ttu-id="ec03f-155">Nachrichtenspeicher bei der ersten nur speichern</span><span class="sxs-lookup"><span data-stu-id="ec03f-155">Message store on first save only</span></span>  <br/> |
|<span data-ttu-id="ec03f-156">Speichern einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec03f-156">Save a message</span></span>  <br/> | <span data-ttu-id="ec03f-157">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="ec03f-157">_fnevObjectModified_</span></span> <br/> |<span data-ttu-id="ec03f-158">Nachrichtenspeicher auf speichert nach dem ersten Speichern Changed-Nachricht (keine Benachrichtigung an den übergeordneten Ordner)</span><span class="sxs-lookup"><span data-stu-id="ec03f-158">Message store on saves after the first save Changed message (No notification to parent folder)</span></span>  <br/> |
|<span data-ttu-id="ec03f-159">Führen Sie einen Suchvorgang</span><span class="sxs-lookup"><span data-stu-id="ec03f-159">Complete a search operation</span></span>  <br/> | <span data-ttu-id="ec03f-160">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="ec03f-160">_fnevSearchComplete_</span></span> <br/> |<span data-ttu-id="ec03f-161">Nachrichtenspeicher Suchordner</span><span class="sxs-lookup"><span data-stu-id="ec03f-161">Message store Search folder</span></span>  <br/> |
|<span data-ttu-id="ec03f-162">Neue Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec03f-162">New message</span></span>  <br/> | <span data-ttu-id="ec03f-163">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="ec03f-163">_fnevNewMail_</span></span> <br/> |<span data-ttu-id="ec03f-164">Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ec03f-164">Message store</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ec03f-165">Wenn Sie eine Benachrichtigung geänderten Objekt erhalten, denken Sie daran, dass der Eigenschaft Tag Array-Teil der [OBJECT_NOTIFICATION](object_notification.md) Struktur auf die _LpNotifications_ -Parameter im Aufruf **OnNotify** zeigt möglicherweise oder darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ec03f-165">When you receive an object modified notification, remember that the property tag array portion of the [OBJECT_NOTIFICATION](object_notification.md) structure pointed to by the  _lpNotifications_ parameter in the **OnNotify** call may or may not be NULL.</span></span> <span data-ttu-id="ec03f-166">Nachricht Anbieter sind nicht zum Einfügen von Informationen in diesem Array und am häufigsten nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec03f-166">Message store providers are not required to insert property information in this array and most do not.</span></span> <span data-ttu-id="ec03f-167">Stellen Sie sicher, dass Ihre **OnNotify** -Methode die Groß-/Kleinschreibung verarbeiten kann, auf dem der _LpPropTagArray_ Zeiger NULL ist.</span><span class="sxs-lookup"><span data-stu-id="ec03f-167">Make sure your **OnNotify** method can handle the case where the  _lpPropTagArray_ pointer is NULL.</span></span> 
  
<span data-ttu-id="ec03f-168">Bei den meisten wenn nicht alle Benachrichtigungen-Objekts, aktualisieren Sie die Ansicht der betreffenden Ordner oder Ordner.</span><span class="sxs-lookup"><span data-stu-id="ec03f-168">For most, if not all object notifications, update the view of the affected folder or folders.</span></span>
  
