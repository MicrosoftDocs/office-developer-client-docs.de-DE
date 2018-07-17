---
title: Kanonische PidTagSearchFolderTag-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5e2f158607496a8cee9f9c731f2d7d6e185a2851
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795109"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a><span data-ttu-id="11599-103">Kanonische PidTagSearchFolderTag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="11599-103">PidTagSearchFolderTag Canonical Property</span></span>

  
  
<span data-ttu-id="11599-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11599-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11599-105">Enthält den Wert, mit dem diese Definition-Nachricht mit dem entsprechenden Container der Suche Ordner synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="11599-105">Contains the value used to synchronize this definition message with the matching search folder container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11599-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="11599-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11599-107">PR_WB_SF_TAG</span><span class="sxs-lookup"><span data-stu-id="11599-107">PR_WB_SF_TAG</span></span>  <br/> |
|<span data-ttu-id="11599-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="11599-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11599-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="11599-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="11599-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="11599-110">Data type:</span></span>  <br/> |<span data-ttu-id="11599-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="11599-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="11599-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="11599-112">Area:</span></span>  <br/> |<span data-ttu-id="11599-113">Suchen</span><span class="sxs-lookup"><span data-stu-id="11599-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11599-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11599-114">Remarks</span></span>

<span data-ttu-id="11599-115">Diese Eigenschaft wird geändert, wenn die Nachricht Definition geändert wird.</span><span class="sxs-lookup"><span data-stu-id="11599-115">This property is changed when the definition message is changed.</span></span> <span data-ttu-id="11599-116">Es muss jede Iteration ändern, aber möglicherweise nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="11599-116">It must change each iteration, but it may not be unique.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11599-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11599-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11599-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="11599-118">Protocol specifications</span></span>

<span data-ttu-id="11599-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11599-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11599-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="11599-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11599-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11599-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11599-122">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="11599-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11599-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="11599-123">Header files</span></span>

<span data-ttu-id="11599-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11599-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="11599-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="11599-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="11599-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11599-126">Mapitags.h</span></span>
  
> <span data-ttu-id="11599-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="11599-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11599-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11599-128">See also</span></span>



[<span data-ttu-id="11599-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11599-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11599-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11599-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11599-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="11599-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11599-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="11599-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
