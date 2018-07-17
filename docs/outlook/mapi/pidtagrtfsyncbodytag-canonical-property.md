---
title: Kanonische PidTagRtfSyncBodyTag-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795024"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="b1868-103">Kanonische PidTagRtfSyncBodyTag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1868-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="b1868-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1868-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1868-105">Enthält wesentliche Zeichen, die am Anfang des den Nachrichtentext angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b1868-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1868-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1868-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1868-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="b1868-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="b1868-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b1868-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1868-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="b1868-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="b1868-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1868-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1868-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1868-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b1868-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1868-112">Area:</span></span>  <br/> |<span data-ttu-id="b1868-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b1868-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1868-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1868-114">Remarks</span></span>

<span data-ttu-id="b1868-115">Die [RTFSync](rtfsync.md) -Funktion verwendet die Tags für Text an den Anfang des Nachrichtentexts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1868-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="b1868-116">Wenn der Text geändert wird, wird das Tag verwendet, um den Anfang der vorherigen Text zu finden.</span><span class="sxs-lookup"><span data-stu-id="b1868-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="b1868-117">Diese Eigenschaften sind zusätzliche Eigenschaften von Rich-Text-Format.</span><span class="sxs-lookup"><span data-stu-id="b1868-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="b1868-118">Sie werden von der Funktion **RTFSync** verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1868-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1868-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1868-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1868-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1868-120">Protocol specifications</span></span>

<span data-ttu-id="b1868-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1868-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1868-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b1868-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1868-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1868-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1868-124">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="b1868-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1868-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b1868-125">Header files</span></span>

<span data-ttu-id="b1868-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1868-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1868-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b1868-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1868-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1868-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b1868-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b1868-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1868-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1868-130">See also</span></span>



[<span data-ttu-id="b1868-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1868-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1868-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1868-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1868-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1868-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1868-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1868-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
