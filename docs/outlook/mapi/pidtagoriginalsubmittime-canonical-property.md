---
title: Kanonische PidTagOriginalSubmitTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 43d0387f1c25c5ac86168caaddddd9fb9171c827
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794723"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="52a2c-103">Kanonische PidTagOriginalSubmitTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52a2c-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="52a2c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52a2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52a2c-105">Die ursprünglichen Übermittlung-Datum und Uhrzeit der Nachricht in den Bericht enthält.</span><span class="sxs-lookup"><span data-stu-id="52a2c-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52a2c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52a2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52a2c-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="52a2c-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="52a2c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="52a2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52a2c-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="52a2c-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="52a2c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52a2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="52a2c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="52a2c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="52a2c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52a2c-112">Area:</span></span>  <br/> |<span data-ttu-id="52a2c-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="52a2c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52a2c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52a2c-114">Remarks</span></span>

<span data-ttu-id="52a2c-115">Am ersten Übermittlung einer Nachricht sollte eine Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52a2c-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="52a2c-116">Er wird nicht geändert, wenn die Nachricht weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="52a2c-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="52a2c-117">In nur-Berichten wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="52a2c-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52a2c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52a2c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52a2c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="52a2c-119">Protocol specifications</span></span>

<span data-ttu-id="52a2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2c-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="52a2c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52a2c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2c-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="52a2c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52a2c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="52a2c-124">Header files</span></span>

<span data-ttu-id="52a2c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52a2c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="52a2c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="52a2c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="52a2c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52a2c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="52a2c-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52a2c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52a2c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52a2c-129">See also</span></span>



[<span data-ttu-id="52a2c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52a2c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52a2c-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52a2c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52a2c-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52a2c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52a2c-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52a2c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
