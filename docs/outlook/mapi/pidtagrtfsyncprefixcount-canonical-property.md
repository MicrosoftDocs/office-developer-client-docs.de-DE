---
title: Kanonische PidTagRtfSyncPrefixCount-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c9a62365b46e85cc8f5d22fd31de3b5c6bd3f76a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795010"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="220a6-103">Kanonische PidTagRtfSyncPrefixCount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="220a6-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="220a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="220a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="220a6-105">Enthält eine Anzahl von Zeichen, die vor der signifikanten Zeichen der Nachricht angezeigt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="220a6-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="220a6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="220a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="220a6-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="220a6-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="220a6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="220a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="220a6-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="220a6-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="220a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="220a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="220a6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="220a6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="220a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="220a6-112">Area:</span></span>  <br/> |<span data-ttu-id="220a6-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="220a6-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="220a6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="220a6-114">Remarks</span></span>

<span data-ttu-id="220a6-115">Die Anzahl der Anfangszeichen enthält keine Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="220a6-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="220a6-116">Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="220a6-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="220a6-117">RTF-Hilfs-Eigenschaften werden von der Funktion [RTFSync](rtfsync.md) verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="220a6-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="220a6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="220a6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="220a6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="220a6-119">Protocol specifications</span></span>

<span data-ttu-id="220a6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="220a6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="220a6-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="220a6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="220a6-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="220a6-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="220a6-123">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="220a6-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="220a6-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="220a6-124">Header files</span></span>

<span data-ttu-id="220a6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="220a6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="220a6-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="220a6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="220a6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="220a6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="220a6-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="220a6-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="220a6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="220a6-129">See also</span></span>



[<span data-ttu-id="220a6-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="220a6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="220a6-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="220a6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="220a6-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="220a6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="220a6-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="220a6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
