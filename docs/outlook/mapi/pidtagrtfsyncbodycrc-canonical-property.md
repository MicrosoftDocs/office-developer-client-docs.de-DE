---
title: Kanonische PidTagRtfSyncBodyCrc-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa144ca93e8fad9b9b5a5da1ee457e5cc3bbd841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795021"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="55c39-103">Kanonische PidTagRtfSyncBodyCrc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55c39-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="55c39-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55c39-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55c39-105">Enthält das Kontrollkästchen zyklischer Redundanz (CRC) für den Nachrichtentext berechnet.</span><span class="sxs-lookup"><span data-stu-id="55c39-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c39-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="55c39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55c39-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="55c39-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="55c39-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="55c39-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55c39-109">0 x 1006</span><span class="sxs-lookup"><span data-stu-id="55c39-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="55c39-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="55c39-110">Data type:</span></span>  <br/> |<span data-ttu-id="55c39-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55c39-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55c39-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="55c39-112">Area:</span></span>  <br/> |<span data-ttu-id="55c39-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="55c39-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c39-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55c39-114">Remarks</span></span>

<span data-ttu-id="55c39-115">Die Funktion [RTFSync](rtfsync.md) berechnet das CRC mithilfe von nur die Zeichen, die sie für die Nachricht erzielt werden hält.</span><span class="sxs-lookup"><span data-stu-id="55c39-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="55c39-116">Beispielsweise sind einige Leerzeichen und Sonderzeichen ignoriert CRC ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="55c39-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="55c39-117">Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55c39-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="55c39-118">Diese Eigenschaften werden von der Funktion **RTFSync** verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55c39-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55c39-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55c39-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55c39-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="55c39-120">Protocol specifications</span></span>

<span data-ttu-id="55c39-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c39-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c39-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="55c39-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55c39-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c39-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c39-124">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="55c39-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55c39-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="55c39-125">Header files</span></span>

<span data-ttu-id="55c39-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55c39-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="55c39-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="55c39-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="55c39-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55c39-128">Mapitags.h</span></span>
  
> <span data-ttu-id="55c39-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="55c39-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55c39-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c39-130">See also</span></span>



[<span data-ttu-id="55c39-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55c39-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55c39-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55c39-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55c39-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="55c39-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55c39-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="55c39-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
