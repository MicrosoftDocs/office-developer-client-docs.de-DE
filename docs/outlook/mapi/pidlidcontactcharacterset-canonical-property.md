---
title: Kanonische PidLidContactCharacterSet-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9706d1060347609708070140aae51d9dcadbb9c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793499"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="cea9b-103">Kanonische PidLidContactCharacterSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cea9b-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="cea9b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cea9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cea9b-105">Gibt den Zeichensatz für diesen Kontakt verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea9b-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cea9b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cea9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cea9b-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="cea9b-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="cea9b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cea9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="cea9b-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cea9b-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cea9b-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="cea9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cea9b-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="cea9b-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="cea9b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cea9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="cea9b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cea9b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cea9b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cea9b-114">Area:</span></span>  <br/> |<span data-ttu-id="cea9b-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="cea9b-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cea9b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cea9b-116">Remarks</span></span>

<span data-ttu-id="cea9b-117">Anwendungen können diese Eigenschaft verwenden, zur Unterstützung bei der eine Zeichensatz abhängige Liste der Optionen für die **DispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **DispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) und **DispidFileUnderId generieren **([PidLidFileUnderId](pidlidfileunderid-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cea9b-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="cea9b-118">Wenn der Wert der Eigenschaft "0 x 00000000" oder "0 x 00000001" ist, sollte Applications die-Eigenschaft behandelt, als nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cea9b-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cea9b-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cea9b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cea9b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cea9b-120">Protocol specifications</span></span>

<span data-ttu-id="cea9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cea9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cea9b-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cea9b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cea9b-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cea9b-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cea9b-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cea9b-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cea9b-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cea9b-125">Header files</span></span>

<span data-ttu-id="cea9b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cea9b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cea9b-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cea9b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cea9b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cea9b-128">See also</span></span>



[<span data-ttu-id="cea9b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cea9b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cea9b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cea9b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cea9b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cea9b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cea9b-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cea9b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
