---
title: PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409580"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="5a657-103">PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a657-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5a657-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a657-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a657-105">Enthält den Suchschlüssel des Autors der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="5a657-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a657-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5a657-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a657-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5a657-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5a657-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5a657-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a657-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="5a657-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="5a657-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5a657-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a657-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a657-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a657-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5a657-112">Area:</span></span>  <br/> |<span data-ttu-id="5a657-113">Server</span><span class="sxs-lookup"><span data-stu-id="5a657-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a657-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a657-114">Remarks</span></span>

<span data-ttu-id="5a657-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5a657-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="5a657-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey-Eigenschaft](pidtagsendersearchkey-canonical-property.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a657-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="5a657-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="5a657-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="5a657-118">Die ursprünglichen Autoreneigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messagingdomäne.</span><span class="sxs-lookup"><span data-stu-id="5a657-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="5a657-119">Wenn eine Nachricht von einer anderen Messagingdomäne, z. B. aus dem Internet, eintrifft, stellen diese Eigenschaften eine Möglichkeit zur Verfügung, um sicherzustellen, dass ursprüngliche Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="5a657-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a657-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a657-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a657-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5a657-121">Header files</span></span>

<span data-ttu-id="5a657-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a657-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a657-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5a657-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a657-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a657-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5a657-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5a657-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a657-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a657-126">See also</span></span>



[<span data-ttu-id="5a657-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a657-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a657-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5a657-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a657-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5a657-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a657-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5a657-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

