---
title: PidTagMessageSize (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355650"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="031f1-103">PidTagMessageSize (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="031f1-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="031f1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="031f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="031f1-105">Enthält die Summe aller Eigenschaften eines Nachrichtenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="031f1-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="031f1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="031f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="031f1-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="031f1-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="031f1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="031f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="031f1-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="031f1-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="031f1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="031f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="031f1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="031f1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="031f1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="031f1-112">Area:</span></span>  <br/> |<span data-ttu-id="031f1-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="031f1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="031f1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="031f1-114">Remarks</span></span>

<span data-ttu-id="031f1-115">Es wird empfohlen, dass Nachrichtenobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="031f1-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="031f1-116">Die Nachrichtengröße gibt die ungefähre Anzahl von Bytes an, die übertragen werden, wenn die Nachricht von einem Nachrichtenspeicher in einen anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="031f1-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="031f1-117">Da es sich um die Summe der Größen aller Eigenschaften des Message-Objekts handelt, ist sie in der Regel erheblich größer als der Nachrichtentext allein.</span><span class="sxs-lookup"><span data-stu-id="031f1-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="031f1-118">Die meisten Nachrichtenspeicheranbieter berechnen diese Eigenschaft für Nachrichten, die sie verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="031f1-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="031f1-119">Einige Nachrichtenspeicheranbieter unterstützen diese Eigenschaft jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="031f1-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="031f1-120">In jedem Fall ist diese Eigenschaft erst verfügbar, wenn die [IMAPIProp::SaveChanges-](imapiprop-savechanges.md) oder [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="031f1-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="031f1-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="031f1-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="031f1-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="031f1-122">Protocol specifications</span></span>

<span data-ttu-id="031f1-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="031f1-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="031f1-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="031f1-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="031f1-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="031f1-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="031f1-126">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="031f1-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="031f1-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="031f1-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="031f1-128">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="031f1-128">Handles folder operations.</span></span>
    
<span data-ttu-id="031f1-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="031f1-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="031f1-130">Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.</span><span class="sxs-lookup"><span data-stu-id="031f1-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="031f1-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="031f1-131">Header files</span></span>

<span data-ttu-id="031f1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="031f1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="031f1-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="031f1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="031f1-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="031f1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="031f1-135">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="031f1-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="031f1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031f1-136">See also</span></span>



[<span data-ttu-id="031f1-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="031f1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="031f1-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="031f1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="031f1-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="031f1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="031f1-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="031f1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

