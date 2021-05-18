---
title: PidTagStoreRecordKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278729"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="21867-103">PidTagStoreRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="21867-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="21867-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21867-105">Enthält den eindeutigen binär-vergleichbaren Bezeichner (Datensatzschlüssel) des Nachrichtenspeichers, in dem sich ein Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="21867-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21867-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="21867-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21867-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="21867-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="21867-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="21867-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21867-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="21867-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="21867-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="21867-110">Data type:</span></span>  <br/> |<span data-ttu-id="21867-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21867-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21867-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="21867-112">Area:</span></span>  <br/> |<span data-ttu-id="21867-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21867-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21867-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21867-114">Remarks</span></span>

<span data-ttu-id="21867-115">Für einen Nachrichtenspeicher ist diese Eigenschaft mit der eigenen PR_RECORD_KEY **(** [PidTagRecordKey](pidtagrecordkey-canonical-property.md)) identisch.</span><span class="sxs-lookup"><span data-stu-id="21867-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="21867-116">Die Beziehung zwischen dieser Eigenschaft und **PR_RECORD_KEY** ist identisch mit der Beziehung zwischen **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) und **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="21867-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21867-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="21867-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21867-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="21867-118">Protocol specifications</span></span>

<span data-ttu-id="21867-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21867-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21867-120">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="21867-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="21867-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21867-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21867-122">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="21867-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21867-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="21867-123">Header files</span></span>

<span data-ttu-id="21867-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21867-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="21867-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="21867-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="21867-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21867-126">Mapitags.h</span></span>
  
> <span data-ttu-id="21867-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="21867-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21867-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21867-128">See also</span></span>



[<span data-ttu-id="21867-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21867-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21867-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="21867-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21867-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="21867-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21867-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="21867-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

