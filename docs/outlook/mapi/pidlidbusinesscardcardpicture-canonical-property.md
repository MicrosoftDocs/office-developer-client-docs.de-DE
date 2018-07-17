---
title: Kanonische PidLidBusinessCardCardPicture-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8e241022504291ad70f45a3318a7901bbbba213f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793458"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="4a96a-103">Kanonische PidLidBusinessCardCardPicture-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4a96a-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="4a96a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a96a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a96a-105">Enthält das Bild, das auf einer Visitenkarte verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a96a-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a96a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a96a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a96a-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="4a96a-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="4a96a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4a96a-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a96a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="4a96a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="4a96a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4a96a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a96a-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="4a96a-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="4a96a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a96a-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a96a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a96a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a96a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a96a-114">Area:</span></span>  <br/> |<span data-ttu-id="4a96a-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="4a96a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a96a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a96a-116">Remarks</span></span>

<span data-ttu-id="4a96a-117">Der Wert dieser Eigenschaft muss entweder ein portable Network Graphics (PNG) oder JPEG-Stream.</span><span class="sxs-lookup"><span data-stu-id="4a96a-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="4a96a-118">Diese Eigenschaft sollte in Verbindung mit der **DispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md))-Eigenschaft wie folgt verwendet werden: **DispidBCCardPicture** sollte nicht vorhanden sein, auf einen Kontakt If ** DispidBCDisplayDefinition** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4a96a-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="4a96a-119">Diese Eigenschaft sollte auch nicht vorhanden sein, wenn die Daten in **DispidBCCardPicture** Bild einer Karte nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4a96a-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a96a-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a96a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a96a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4a96a-121">Protocol specifications</span></span>

<span data-ttu-id="4a96a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a96a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a96a-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4a96a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a96a-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a96a-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a96a-125">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4a96a-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a96a-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4a96a-126">Header files</span></span>

<span data-ttu-id="4a96a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a96a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a96a-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4a96a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a96a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a96a-129">See also</span></span>



[<span data-ttu-id="4a96a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a96a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a96a-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a96a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a96a-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a96a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a96a-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a96a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
