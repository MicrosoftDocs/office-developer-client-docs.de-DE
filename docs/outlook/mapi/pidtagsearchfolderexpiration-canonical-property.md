---
title: Kanonische PidTagSearchFolderExpiration-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bd70d18242fadee964ad96305728e63617a0276f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795113"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="e9cf9-103">Kanonische PidTagSearchFolderExpiration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9cf9-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="e9cf9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9cf9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9cf9-105">Enthält die Uhrzeit, an dem der Suche Ordnercontainer veraltete werden, und aktualisiert oder neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9cf9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e9cf9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9cf9-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="e9cf9-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="e9cf9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e9cf9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9cf9-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="e9cf9-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="e9cf9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e9cf9-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9cf9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e9cf9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e9cf9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e9cf9-112">Area:</span></span>  <br/> |<span data-ttu-id="e9cf9-113">Suchen</span><span class="sxs-lookup"><span data-stu-id="e9cf9-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9cf9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9cf9-114">Remarks</span></span>

<span data-ttu-id="e9cf9-115">Diese Eigenschaft muss als die Anzahl der Minuten seit Mitternacht (Coordinated Universal Time, UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9cf9-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9cf9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9cf9-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e9cf9-117">Protocol specifications</span></span>

<span data-ttu-id="e9cf9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9cf9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9cf9-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9cf9-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9cf9-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9cf9-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9cf9-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e9cf9-122">Header files</span></span>

<span data-ttu-id="e9cf9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9cf9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9cf9-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9cf9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9cf9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e9cf9-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e9cf9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9cf9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9cf9-127">See also</span></span>



[<span data-ttu-id="e9cf9-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9cf9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9cf9-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9cf9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9cf9-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e9cf9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9cf9-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e9cf9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
