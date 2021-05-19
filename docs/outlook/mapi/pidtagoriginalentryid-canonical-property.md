---
title: PidTagOriginalEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f3f4f42d91c4091943d6183508e2bc76c17197fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342721"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="439f6-103">PidTagOriginalEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="439f6-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="439f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="439f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="439f6-105">Enthält die ursprüngliche Eintrags-ID für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes schreibbares Adressbuch kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="439f6-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="439f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="439f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="439f6-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="439f6-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="439f6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="439f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="439f6-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="439f6-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="439f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="439f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="439f6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="439f6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="439f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="439f6-112">Area:</span></span>  <br/> |<span data-ttu-id="439f6-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="439f6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="439f6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="439f6-114">Remarks</span></span>

<span data-ttu-id="439f6-115">Diese Eigenschaft ist eine der Eigenschaften, die Informationen zur ursprünglichen Quelle eines kopierten Eintrags enthalten.</span><span class="sxs-lookup"><span data-stu-id="439f6-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="439f6-116">Für einen nicht gelesenen Bericht enthält diese Eigenschaft eine Kopie der Eintrags-ID des ursprünglichen Nachrichtenempfängers, für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="439f6-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="439f6-117">Wenn der ursprüngliche Empfänger Teil einer Verteilerliste ist, wird der Eintragsbezeichner der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="439f6-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="439f6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="439f6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="439f6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="439f6-119">Protocol specifications</span></span>

<span data-ttu-id="439f6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="439f6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="439f6-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="439f6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="439f6-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="439f6-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="439f6-123">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="439f6-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="439f6-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="439f6-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="439f6-125">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="439f6-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="439f6-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="439f6-126">Header files</span></span>

<span data-ttu-id="439f6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="439f6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="439f6-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="439f6-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="439f6-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="439f6-129">Mapitags.h</span></span>
  
> <span data-ttu-id="439f6-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="439f6-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="439f6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="439f6-131">See also</span></span>



[<span data-ttu-id="439f6-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="439f6-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="439f6-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="439f6-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="439f6-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="439f6-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="439f6-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="439f6-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

