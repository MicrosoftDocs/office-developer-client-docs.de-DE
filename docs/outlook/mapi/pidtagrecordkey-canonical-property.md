---
title: PidTagRecordKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355265"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="d656f-103">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d656f-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="d656f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d656f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d656f-105">Enthält einen eindeutigen binär-vergleichbaren Bezeichner für ein bestimmtes Objekt.</span><span class="sxs-lookup"><span data-stu-id="d656f-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d656f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d656f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d656f-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="d656f-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="d656f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d656f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d656f-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="d656f-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="d656f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d656f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d656f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d656f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d656f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d656f-112">Area:</span></span>  <br/> |<span data-ttu-id="d656f-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d656f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d656f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d656f-114">Remarks</span></span>

<span data-ttu-id="d656f-115">Diese Eigenschaft erleichtert das Suchen von Verweisen auf ein Objekt, z. B. das Suchen der Zeile in einer Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="d656f-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="d656f-116">Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. verwenden Sie zu diesem Zweck die Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="d656f-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="d656f-117">Ein Anlagenunterobjekt sollte innerhalb einer Nachricht durch diese Eigenschaft eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d656f-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="d656f-118">Dieser Bezeichner ist das einzige Anlagenmerkmal, das garantiert gleich bleibt, nachdem die Nachricht geschlossen und erneut geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d656f-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="d656f-119">Der Speicheranbieter muss diese Eigenschaft sitzungsübergreifend beibehalten, um diese Garantie sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="d656f-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="d656f-120">Für Ordner enthält diese Eigenschaft einen Schlüssel, der in der Ordnerhierarchietabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d656f-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="d656f-121">In der Regel ist dies der gleiche Wert wie der wert, der von der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d656f-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d656f-122">Bei Nachrichtenspeichern ist diese Eigenschaft mit der **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) identisch.</span><span class="sxs-lookup"><span data-stu-id="d656f-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d656f-123">In einem Nachrichtenspeicherobjekt sollte diese Eigenschaft für alle Speicheranbieter eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d656f-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="d656f-124">Eine Möglichkeit besteht in der Kombination des Werts der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))-Eigenschaft für den Speicher (eindeutig für diesen Anbietertyp) mit einer [GUID-Struktur](guid.md) oder einem anderen wert, der für den bestimmten Nachrichtenspeicher eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="d656f-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="d656f-125">Diese Eigenschaft ist immer über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d656f-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="d656f-126">Einige Anbieter können sie unmittelbar nach der Instanziierung verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="d656f-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="d656f-127">Ein Client oder Dienstanbieter kann Werte aus dieser Eigenschaft mithilfe von memcmp vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d656f-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="d656f-128">Dies ist für Eintragsbezeichnerwerte nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="d656f-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="d656f-129">Diese Eigenschaft ist jedoch garantiert innerhalb desselben Nachrichtenspeichers oder Adressbuchcontainers eindeutig. Zwei Objekte aus unterschiedlichen Containern können denselben Wert dieser Eigenschaft haben.</span><span class="sxs-lookup"><span data-stu-id="d656f-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="d656f-130">Ein Unterschied zwischen dem Datensatz und den Suchtasten ist, dass der Datensatzschlüssel für das Objekt spezifisch ist, während der Suchschlüssel in andere Objekte kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d656f-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="d656f-131">Beispielsweise können zwei Kopien des Objekts denselben wert **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) haben, müssen jedoch unterschiedliche Werte für diese Eigenschaft haben.</span><span class="sxs-lookup"><span data-stu-id="d656f-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="d656f-132">In der folgenden Tabelle werden wichtige Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="d656f-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="d656f-133">**Merkmal**</span><span class="sxs-lookup"><span data-stu-id="d656f-133">**Characteristic**</span></span>|<span data-ttu-id="d656f-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="d656f-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="d656f-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="d656f-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="d656f-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="d656f-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d656f-137">Erforderlich für Anlagenobjekte</span><span class="sxs-lookup"><span data-stu-id="d656f-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="d656f-138">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-138">No</span></span>  <br/> |<span data-ttu-id="d656f-139">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-139">Yes</span></span>  <br/> |<span data-ttu-id="d656f-140">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-140">No</span></span>  <br/> |
|<span data-ttu-id="d656f-141">Erforderlich für Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="d656f-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="d656f-142">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-142">Yes</span></span>  <br/> |<span data-ttu-id="d656f-143">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-143">Yes</span></span>  <br/> |<span data-ttu-id="d656f-144">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-144">No</span></span>  <br/> |
|<span data-ttu-id="d656f-145">Erforderlich für Nachrichtenspeicherobjekte</span><span class="sxs-lookup"><span data-stu-id="d656f-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="d656f-146">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-146">Yes</span></span>  <br/> |<span data-ttu-id="d656f-147">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-147">Yes</span></span>  <br/> |<span data-ttu-id="d656f-148">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-148">No</span></span>  <br/> |
|<span data-ttu-id="d656f-149">Erforderlich für Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="d656f-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="d656f-150">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-150">Yes</span></span>  <br/> |<span data-ttu-id="d656f-151">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-151">No</span></span>  <br/> |<span data-ttu-id="d656f-152">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-152">No</span></span>  <br/> |
|<span data-ttu-id="d656f-153">Nach Client anknabel</span><span class="sxs-lookup"><span data-stu-id="d656f-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="d656f-154">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-154">No</span></span>  <br/> |<span data-ttu-id="d656f-155">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-155">No</span></span>  <br/> |<span data-ttu-id="d656f-156">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-156">Yes</span></span>  <br/> |
|<span data-ttu-id="d656f-157">Verfügbar vor einem Aufruf von **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="d656f-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="d656f-158">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="d656f-158">Maybe</span></span>  <br/> |<span data-ttu-id="d656f-159">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="d656f-159">Maybe</span></span>  <br/> |<span data-ttu-id="d656f-160">Nachrichten Ja Andere vielleicht</span><span class="sxs-lookup"><span data-stu-id="d656f-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="d656f-161">In einem Kopiervorgang geändert</span><span class="sxs-lookup"><span data-stu-id="d656f-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="d656f-162">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-162">Yes</span></span>  <br/> |<span data-ttu-id="d656f-163">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-163">Yes</span></span>  <br/> |<span data-ttu-id="d656f-164">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-164">No</span></span>  <br/> |
|<span data-ttu-id="d656f-165">Von einem Client nach einer Kopie ändernd</span><span class="sxs-lookup"><span data-stu-id="d656f-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="d656f-166">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-166">No</span></span>  <br/> |<span data-ttu-id="d656f-167">Nein</span><span class="sxs-lookup"><span data-stu-id="d656f-167">No</span></span>  <br/> |<span data-ttu-id="d656f-168">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-168">Yes</span></span>  <br/> |
|<span data-ttu-id="d656f-169">Eindeutig in ...</span><span class="sxs-lookup"><span data-stu-id="d656f-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="d656f-170">Gesamte Welt</span><span class="sxs-lookup"><span data-stu-id="d656f-170">Entire world</span></span>  <br/> |<span data-ttu-id="d656f-171">Anbieterinstanz</span><span class="sxs-lookup"><span data-stu-id="d656f-171">Provider instance</span></span>  <br/> |<span data-ttu-id="d656f-172">Gesamte Welt</span><span class="sxs-lookup"><span data-stu-id="d656f-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="d656f-173">Binär vergleichbar (wie bei memcmp)</span><span class="sxs-lookup"><span data-stu-id="d656f-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="d656f-174">Nein – Verwenden von **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="d656f-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="d656f-175">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-175">Yes</span></span>  <br/> |<span data-ttu-id="d656f-176">Ja</span><span class="sxs-lookup"><span data-stu-id="d656f-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d656f-177">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d656f-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d656f-178">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d656f-178">Protocol specifications</span></span>

<span data-ttu-id="d656f-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d656f-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d656f-180">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d656f-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d656f-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d656f-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d656f-182">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="d656f-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d656f-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d656f-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d656f-184">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="d656f-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d656f-185">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d656f-185">Header files</span></span>

<span data-ttu-id="d656f-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d656f-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="d656f-187">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d656f-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="d656f-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d656f-188">Mapitags.h</span></span>
  
> <span data-ttu-id="d656f-189">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d656f-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d656f-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d656f-190">See also</span></span>



[<span data-ttu-id="d656f-191">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d656f-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d656f-192">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d656f-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d656f-193">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d656f-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d656f-194">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d656f-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

