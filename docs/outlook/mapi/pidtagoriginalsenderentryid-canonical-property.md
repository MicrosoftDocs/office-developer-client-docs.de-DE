---
title: Kanonische PidTagOriginalSenderEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f18587e28c6a3954b86dd58f0167e826d3086c51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794705"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="c7371-103">Kanonische PidTagOriginalSenderEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c7371-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c7371-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7371-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7371-105">Enthält die Eintrags-ID des Absenders einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird die erste Version.</span><span class="sxs-lookup"><span data-stu-id="c7371-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7371-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c7371-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7371-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c7371-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c7371-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c7371-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7371-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="c7371-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="c7371-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c7371-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7371-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c7371-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c7371-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c7371-112">Area:</span></span>  <br/> |<span data-ttu-id="c7371-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="c7371-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7371-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7371-114">Remarks</span></span>

<span data-ttu-id="c7371-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c7371-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="c7371-116">Am ersten-Übermittlung der Nachricht sollte eine Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7371-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="c7371-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="c7371-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7371-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7371-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7371-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c7371-119">Protocol specifications</span></span>

<span data-ttu-id="c7371-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7371-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7371-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c7371-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7371-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7371-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7371-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c7371-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7371-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c7371-124">Header files</span></span>

<span data-ttu-id="c7371-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7371-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7371-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c7371-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7371-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7371-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c7371-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c7371-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7371-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7371-129">See also</span></span>



[<span data-ttu-id="c7371-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7371-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7371-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7371-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7371-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c7371-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7371-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c7371-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
