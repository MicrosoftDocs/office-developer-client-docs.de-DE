---
title: Kanonische PidTagIcon-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0aa5873d98b7ae9dea1bdaffc37f7996262b6062
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794455"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="762af-103">Kanonische PidTagIcon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="762af-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="762af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="762af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="762af-105">Eine Bitmap mit einer Gesamtgröße Symbol für ein Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="762af-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="762af-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="762af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="762af-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="762af-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="762af-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="762af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="762af-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="762af-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="762af-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="762af-110">Data type:</span></span>  <br/> |<span data-ttu-id="762af-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="762af-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="762af-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="762af-112">Area:</span></span>  <br/> |<span data-ttu-id="762af-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="762af-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="762af-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="762af-114">Remarks</span></span>

<span data-ttu-id="762af-115">Diese Eigenschaft enthält ein Bild mit 32 x 32 Pixeln eines Symbols, identisch mit den Inhalt ein. ICO-Datei.</span><span class="sxs-lookup"><span data-stu-id="762af-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="762af-116">Diese Eigenschaft wird normalerweise übernommen aus der. ICO-Datei in der LargeIcon-Zeile der entsprechenden Abschnitt der Konfigurationsdatei Formular [Beschreibung] angegeben.</span><span class="sxs-lookup"><span data-stu-id="762af-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="762af-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="762af-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="762af-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="762af-118">Protocol specifications</span></span>

<span data-ttu-id="762af-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="762af-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="762af-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="762af-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="762af-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="762af-121">Header files</span></span>

<span data-ttu-id="762af-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="762af-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="762af-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="762af-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="762af-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="762af-124">Mapitags.h</span></span>
  
> <span data-ttu-id="762af-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="762af-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="762af-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="762af-126">See also</span></span>



[<span data-ttu-id="762af-127">Kanonische PidTagMiniIcon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="762af-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="762af-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="762af-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="762af-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="762af-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="762af-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="762af-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="762af-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="762af-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
