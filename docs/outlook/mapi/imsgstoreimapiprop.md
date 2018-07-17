---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792651"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="dffd4-103">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dffd4-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="dffd4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dffd4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dffd4-105">Bietet Zugriff auf Informationen zu Märkten Nachricht und Nachrichten und Ordnern.</span><span class="sxs-lookup"><span data-stu-id="dffd4-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dffd4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dffd4-106">Header file:</span></span>  <br/> |<span data-ttu-id="dffd4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dffd4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dffd4-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="dffd4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dffd4-109">Objekt "Message" store</span><span class="sxs-lookup"><span data-stu-id="dffd4-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="dffd4-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dffd4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dffd4-111">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="dffd4-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="dffd4-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dffd4-112">Called by:</span></span>  <br/> |<span data-ttu-id="dffd4-113">Clientanwendungen, die MAPI-Warteschlange und MAPI</span><span class="sxs-lookup"><span data-stu-id="dffd4-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="dffd4-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="dffd4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dffd4-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="dffd4-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="dffd4-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="dffd4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dffd4-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="dffd4-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="dffd4-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="dffd4-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="dffd4-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="dffd4-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dffd4-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="dffd4-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dffd4-121">Beraten</span><span class="sxs-lookup"><span data-stu-id="dffd4-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="dffd4-122">Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Nachrichtenspeicher registriert.</span><span class="sxs-lookup"><span data-stu-id="dffd4-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-123">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="dffd4-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="dffd4-124">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode **IMsgStore::Advise** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="dffd4-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="dffd4-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="dffd4-126">Vergleicht zwei Eintragsbezeichner, um festzustellen, ob sie auf dieselbe Rechtsgrundlage in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="dffd4-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dffd4-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="dffd4-128">Öffnet einen Ordner oder eine Nachricht, und gibt einen Schnittstellenzeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="dffd4-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="dffd4-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="dffd4-130">Stellt einen Ordner als Ziel für eingehende Nachrichten von einer bestimmten Nachrichtenklasse her.</span><span class="sxs-lookup"><span data-stu-id="dffd4-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="dffd4-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="dffd4-132">Ruft den Ordner, der als Ziel für eingehende Nachrichten von einer angegebenen Nachrichtenklasse oder als Standard Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="dffd4-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="dffd4-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="dffd4-134">Bietet Zugriff auf die empfangen Ordnertabelle eine Tabelle mit Informationen zu allen der Ordner für den Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="dffd4-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="dffd4-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="dffd4-136">Ermöglicht das ordnungsgemäße Abmelden des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="dffd4-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="dffd4-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="dffd4-138">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dffd4-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="dffd4-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="dffd4-140">Bietet Zugriff auf ausgehende Warteschlangentabelle eine Tabelle mit Informationen über alle Nachrichten in der Nachrichtenspeicher ausgehenden Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="dffd4-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="dffd4-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="dffd4-142">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dffd4-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="dffd4-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="dffd4-144">Aktiviert den Nachricht-Speicher-Anbieter für die Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dffd4-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="dffd4-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="dffd4-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="dffd4-146">Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="dffd4-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="dffd4-147">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="dffd4-147">**Required properties**</span></span>|<span data-ttu-id="dffd4-148">**Zugriffsebene**</span><span class="sxs-lookup"><span data-stu-id="dffd4-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dffd4-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-150">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="dffd4-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="dffd4-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-152">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-154">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-156">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-158">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-160">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-162">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="dffd4-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dffd4-164">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dffd4-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="dffd4-165">Die folgenden Eigenschaften sind für Nachrichtenspeicher zwischen Personen Nachricht (IPM):</span><span class="sxs-lookup"><span data-stu-id="dffd4-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="dffd4-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dffd4-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dffd4-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dffd4-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dffd4-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dffd4-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="dffd4-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="dffd4-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="dffd4-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dffd4-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dffd4-172">See also</span></span>



[<span data-ttu-id="dffd4-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dffd4-173">MAPI Properties</span></span>](mapi-properties.md)
