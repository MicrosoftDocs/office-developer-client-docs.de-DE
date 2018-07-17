---
title: Kanonische PidTagOriginalDeliveryTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cd8c44923e64fcea4464f758389db05bb6b7e374
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794676"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="6eeaf-103">Kanonische PidTagOriginalDeliveryTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6eeaf-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="6eeaf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6eeaf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6eeaf-105">Eine Kopie der Originalnachricht Übermittlung Datum und Uhrzeit in einem Thread enthält.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6eeaf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6eeaf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6eeaf-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="6eeaf-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="6eeaf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6eeaf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6eeaf-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="6eeaf-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="6eeaf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6eeaf-110">Data type:</span></span>  <br/> |<span data-ttu-id="6eeaf-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6eeaf-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6eeaf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6eeaf-112">Area:</span></span>  <br/> |<span data-ttu-id="6eeaf-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="6eeaf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6eeaf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6eeaf-114">Remarks</span></span>

<span data-ttu-id="6eeaf-115">Diese Eigenschaft wird von der ursprünglichen **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))-Eigenschaft in den nachfolgenden Antworten oder Weiterleiten Vorgänge kopiert und in Lese- und nonread Berichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="6eeaf-116">Übermittlungsberichte verwenden Sie die Eigenschaft **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6eeaf-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6eeaf-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6eeaf-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6eeaf-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6eeaf-118">Protocol specifications</span></span>

<span data-ttu-id="6eeaf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eeaf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6eeaf-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6eeaf-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eeaf-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6eeaf-122">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6eeaf-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6eeaf-123">Header files</span></span>

<span data-ttu-id="6eeaf-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6eeaf-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6eeaf-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6eeaf-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6eeaf-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6eeaf-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6eeaf-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6eeaf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6eeaf-128">See also</span></span>



[<span data-ttu-id="6eeaf-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6eeaf-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6eeaf-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6eeaf-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6eeaf-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6eeaf-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6eeaf-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6eeaf-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
