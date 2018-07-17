---
title: Kanonische PidTagStoreUnicodeMask-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795223"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="243e0-103">Kanonische PidTagStoreUnicodeMask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="243e0-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="243e0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="243e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="243e0-105">Enthält eine Bitmaske aus Flags, die Clientanwendungen abgefragt werden sollen, um die Eigenschaften eines Nachrichtenspeichers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="243e0-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="243e0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="243e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="243e0-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="243e0-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="243e0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="243e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="243e0-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="243e0-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="243e0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="243e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="243e0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="243e0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="243e0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="243e0-112">Area:</span></span>  <br/> |<span data-ttu-id="243e0-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="243e0-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="243e0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="243e0-114">Remarks</span></span>

<span data-ttu-id="243e0-115">Diese Eigenschaft gibt die Funktionen des einen Nachrichtenspeicher für Clientanwendungen, Planen sie eine Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="243e0-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="243e0-116">Die Kennzeichen erleichtern Entscheidungen durch einen Client oder einem anderen Speicher, z. B., ob **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="243e0-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="243e0-117">Ein Client sollten diese Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="243e0-117">A client should never set this property.</span></span> <span data-ttu-id="243e0-118">Ein Versuch gibt **MAPI_E_COMPUTED**zurück.</span><span class="sxs-lookup"><span data-stu-id="243e0-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="243e0-119">Für diese Eigenschaft kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="243e0-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="243e0-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="243e0-121">(131072, 0 x 00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die amerikanischen National Standards Institute (ANSI) (8-Bit) Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="243e0-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="243e0-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="243e0-123">(32, 0 x 00000020) Der Nachrichtenspeicher unterstützt Object Linking und Embedding (OLE) oder nicht-OLE-Anlagen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="243e0-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="243e0-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="243e0-125">(1024, 0 x 00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="243e0-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="243e0-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="243e0-127">(16, 0 x 00000010) Der Nachrichtenspeicher unterstützt die Erstellung von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="243e0-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="243e0-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="243e0-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="243e0-129">(1, 0 x 00000001) Für die Objekte im Nachrichtenspeicher Eintragsbezeichner sind eindeutig, d. h., während der Lebensdauer des Speichers niemals wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="243e0-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="243e0-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="243e0-131">(65536, 0 x 00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der Eigenschaft **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="243e0-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="243e0-132">Beachten Sie, dass **STORE_HTML_OK** in Versionen von MAPIDEFS nicht definiert ist. H, die und früher mit Microsoft Exchange 2000 Server enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="243e0-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="243e0-133">Wenn Ihre Entwicklungsumgebung ein MAPIDEFS verwendet wird. H-Datei, die nicht **STORE_HTML_OK**enthalten, verwenden Sie stattdessen den Wert "0 x 00010000".</span><span class="sxs-lookup"><span data-stu-id="243e0-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="243e0-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="243e0-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="243e0-135">(2097152, 0x00200000) Gibt an, dass beim Empfang einer neuen Nachricht im Speicher der Speicher funktioniert Regeln und Spam Filtern Verarbeitung der Nachricht getrennt, in einem gepackten PST-Speicher.</span><span class="sxs-lookup"><span data-stu-id="243e0-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="243e0-136">Der Informationsspeicher ruft [IMAPISupport::Notify](imapisupport-notify.md), Einstellung **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und klicken Sie dann die Details der neuen Nachricht an dem listening Client übergibt.</span><span class="sxs-lookup"><span data-stu-id="243e0-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="243e0-137">Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="243e0-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="243e0-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="243e0-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="243e0-139">(524288, 0x00080000) Dieses Kennzeichen ist reserviert und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="243e0-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="243e0-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="243e0-141">(8, 0 x 00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="243e0-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="243e0-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="243e0-143">(512, 0 x 00000200) Der Nachrichtenspeicher mehrwertige Eigenschaften unterstützt, die Stabilität der Reihenfolge der Wert in einer mehrwertigen Eigenschaft in der gesamten Speichervorgang garantiert Vorgang und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen.</span><span class="sxs-lookup"><span data-stu-id="243e0-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="243e0-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="243e0-145">(256, 0 x 00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="243e0-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="243e0-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="243e0-147">(64, 0 x 00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen.</span><span class="sxs-lookup"><span data-stu-id="243e0-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="243e0-148">OLE-Daten ist wie über eine Schnittstelle **IStorage** zugänglich über die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="243e0-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="243e0-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="243e0-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="243e0-150">(16384, 0x00004000) Der Ordner in diesem Zertifikatspeicher sind öffentliche (mehrere Benutzer) wird nicht private (möglicherweise mit mehreren Instanzen, aber nicht mehrere Benutzer).</span><span class="sxs-lookup"><span data-stu-id="243e0-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="243e0-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="243e0-152">(8388608, 0 x 00800000) Der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher wird zum Pushen von Änderungen durch Benachrichtigungen auf die Indizierung Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="243e0-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="243e0-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="243e0-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="243e0-154">(2, 0 x 00000002) Alle Schnittstellen für den Nachrichtenspeicher verfügen über eine nur-Lese-Zugriffsebene.</span><span class="sxs-lookup"><span data-stu-id="243e0-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="243e0-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="243e0-156">(4096, 0 x 00001000) Der Nachrichtenspeicher unterstützt Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="243e0-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="243e0-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="243e0-158">(2048, 0x00000800) Der Nachrichtenspeicher unterstützt Rich Text Format (RTF)-Nachrichten, die in der Regel komprimiert und der Informationsspeicher selbst behält **PR_BODY** **PR_RTF_COMPRESSED** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="243e0-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="243e0-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="243e0-160">(4, 0 x 00000004) Der Nachrichtenspeicher unterstützt Suchergebnisse Ordner.</span><span class="sxs-lookup"><span data-stu-id="243e0-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="243e0-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="243e0-162">(8192, 0 x 00002000) Der Nachrichtenspeicher unterstützt Sortierung Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="243e0-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="243e0-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="243e0-164">(128, 0x00000080) Der Nachrichtenspeicher unterstützt Markierens einer Nachricht für die Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="243e0-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="243e0-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="243e0-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="243e0-166">(32768, 0x00008000) Der Nachrichtenspeicher unterstützt die Speicherung Versionsfähige-Format (RTF)-Text-Nachrichten nicht komprimierten Format.</span><span class="sxs-lookup"><span data-stu-id="243e0-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="243e0-167">Ein nicht komprimierter RTF-Stream wird durch den Wert **DwMagicUncompressedRTF** im Streamheader identifiziert.</span><span class="sxs-lookup"><span data-stu-id="243e0-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="243e0-168">Der Wert **DwMagicUncompressedRTF** ist in der RTFLIB definiert. H-Datei.</span><span class="sxs-lookup"><span data-stu-id="243e0-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="243e0-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="243e0-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="243e0-170">(262144, 0 x 00040000) Der Nachrichtenspeicher unterstützt Eigenschaften, die Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="243e0-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="243e0-171">Eine RTF-Version einer Nachricht kann immer gespeichert werden, selbst wenn der Nachrichtenspeicher RTF nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="243e0-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="243e0-172">Wenn das Bit STORE_RTF_OK für einen bestimmten Speicher nicht festgelegt ist, müssen einen Client RTF-Versionen verwalten die [RTFSync](rtfsync.md) -Funktion, um die **PR_BODY** und **PR_RTF_COMPRESSED** Versionen für Textinhalt synchronisiert halten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="243e0-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="243e0-173">RTF wird immer in **PR_RTF_COMPRESSED**, gespeichert, ob es tatsächlich oder nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="243e0-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="243e0-174">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="243e0-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="243e0-175">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="243e0-175">Header files</span></span>

<span data-ttu-id="243e0-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="243e0-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="243e0-177">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="243e0-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="243e0-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="243e0-178">Mapitags.h</span></span>
  
> <span data-ttu-id="243e0-179">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="243e0-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="243e0-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="243e0-180">See also</span></span>



[<span data-ttu-id="243e0-181">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="243e0-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="243e0-182">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="243e0-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="243e0-183">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="243e0-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="243e0-184">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="243e0-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
