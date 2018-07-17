---
title: Kanonische PidTagReadReceiptRequested-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1d4d4404d175458d5b708948b11c93b734a8bd1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794865"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="69bf7-103">Kanonische PidTagReadReceiptRequested-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69bf7-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="69bf7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69bf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69bf7-105">Enthält True, wenn der Absender eine Nachricht möchte Nachrichtensystem einen lesen Bericht aus, wenn der Empfänger eine Nachricht gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="69bf7-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69bf7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="69bf7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69bf7-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="69bf7-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="69bf7-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="69bf7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69bf7-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="69bf7-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="69bf7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="69bf7-110">Data type:</span></span>  <br/> |<span data-ttu-id="69bf7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="69bf7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="69bf7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="69bf7-112">Area:</span></span>  <br/> |<span data-ttu-id="69bf7-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="69bf7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69bf7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="69bf7-114">Remarks</span></span>

<span data-ttu-id="69bf7-115">Diese Eigenschaft muss auf TRUE festgelegt sein, um die Werte in der **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) und **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) Eigenschaften zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="69bf7-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="69bf7-116">Wenn eine Nachricht mit **PR_READ_RECEIPT_REQUESTED** Set gelöscht oder abläuft, bevor Nachrichtensystem einen schreibgeschützten Bericht generiert werden kann, wird ein nonread Bericht generiert.</span><span class="sxs-lookup"><span data-stu-id="69bf7-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69bf7-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="69bf7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69bf7-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="69bf7-118">Protocol specifications</span></span>

<span data-ttu-id="69bf7-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69bf7-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69bf7-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="69bf7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69bf7-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69bf7-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69bf7-122">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="69bf7-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69bf7-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="69bf7-123">Header files</span></span>

<span data-ttu-id="69bf7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69bf7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="69bf7-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="69bf7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="69bf7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69bf7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="69bf7-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69bf7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69bf7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69bf7-128">See also</span></span>



[<span data-ttu-id="69bf7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69bf7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69bf7-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69bf7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69bf7-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="69bf7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69bf7-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="69bf7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
