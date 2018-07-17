---
title: Kanonische PidTagOriginalSenderAddressType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5cac96287db9638f699b75e0c387e003beb5e197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794707"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="363ca-103">Kanonische PidTagOriginalSenderAddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="363ca-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="363ca-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="363ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="363ca-105">Enthält den Adresstyp des Absenders einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird die erste Version.</span><span class="sxs-lookup"><span data-stu-id="363ca-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="363ca-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="363ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="363ca-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="363ca-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="363ca-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="363ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="363ca-109">0 x 0066</span><span class="sxs-lookup"><span data-stu-id="363ca-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="363ca-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="363ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="363ca-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="363ca-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="363ca-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="363ca-112">Area:</span></span>  <br/> |<span data-ttu-id="363ca-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="363ca-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="363ca-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="363ca-114">Remarks</span></span>

<span data-ttu-id="363ca-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="363ca-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="363ca-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="363ca-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="363ca-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="363ca-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="363ca-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="363ca-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="363ca-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="363ca-119">Protocol specifications</span></span>

<span data-ttu-id="363ca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="363ca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="363ca-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="363ca-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="363ca-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="363ca-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="363ca-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="363ca-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="363ca-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="363ca-124">Header files</span></span>

<span data-ttu-id="363ca-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="363ca-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="363ca-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="363ca-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="363ca-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="363ca-127">Mapitags.h</span></span>
  
> <span data-ttu-id="363ca-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="363ca-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="363ca-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="363ca-129">See also</span></span>



[<span data-ttu-id="363ca-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="363ca-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="363ca-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="363ca-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="363ca-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="363ca-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="363ca-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="363ca-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
