---
title: Kanonische PidTagOriginalSearchKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26854b640669bbc6479ce90ba9cad18cdf4d9264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794720"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="a4e3d-103">Kanonische PidTagOriginalSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4e3d-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a4e3d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4e3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4e3d-105">Enthält den ursprünglichen Suche Schlüssel für einen Eintrag aus einem Adressbuch an ein persönliches Adressbuch oder anderen beschreibbaren Adressbuch kopiert.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4e3d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a4e3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4e3d-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a4e3d-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a4e3d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a4e3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4e3d-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="a4e3d-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="a4e3d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a4e3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4e3d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a4e3d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a4e3d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a4e3d-112">Area:</span></span>  <br/> |<span data-ttu-id="a4e3d-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="a4e3d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4e3d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4e3d-114">Remarks</span></span>

<span data-ttu-id="a4e3d-115">Diese Eigenschaft ist eine der Eigenschaften, die der ursprünglichen Quelle eines Eintrags kopierten Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="a4e3d-116">Bei einem Bericht nonread enthält diese Eigenschaft eine Kopie des Schlüssels "Suchen" von der ursprünglichen Empfänger der Nachricht für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="a4e3d-117">Wenn der ursprüngliche Empfänger einer Verteilerliste gehört, wird die suchen-Taste der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4e3d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a4e3d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a4e3d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a4e3d-119">Protocol specifications</span></span>

<span data-ttu-id="a4e3d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4e3d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4e3d-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a4e3d-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4e3d-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4e3d-123">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a4e3d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a4e3d-124">Header files</span></span>

<span data-ttu-id="a4e3d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4e3d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4e3d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4e3d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4e3d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a4e3d-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a4e3d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4e3d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4e3d-129">See also</span></span>



[<span data-ttu-id="a4e3d-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4e3d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4e3d-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4e3d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4e3d-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a4e3d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4e3d-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a4e3d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
