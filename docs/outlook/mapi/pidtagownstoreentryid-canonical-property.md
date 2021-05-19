---
title: PidTagOwnStoreEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427374"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="8d277-103">PidTagOwnStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8d277-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8d277-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d277-105">Enthält die Eintrags-ID des eng gekoppelten Nachrichtenspeichers eines Transports.</span><span class="sxs-lookup"><span data-stu-id="8d277-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d277-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8d277-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d277-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8d277-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8d277-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8d277-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d277-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="8d277-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="8d277-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8d277-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d277-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d277-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d277-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8d277-112">Area:</span></span>  <br/> |<span data-ttu-id="8d277-113">Nachrichten-Store-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d277-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d277-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d277-114">Remarks</span></span>

<span data-ttu-id="8d277-115">Diese Eigenschaft gibt die Eintrags-ID für den eng gekoppelten Speicher an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8d277-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="8d277-116">Beispielsweise kann ein Transportanbieter den Eintragsbezeichner für den privaten Ordnerspeicher angeben, damit der MAPI-Spooler den Transportanbieter mit dem Speicher verbinden kann.</span><span class="sxs-lookup"><span data-stu-id="8d277-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d277-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d277-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8d277-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8d277-118">Header files</span></span>

<span data-ttu-id="8d277-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d277-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d277-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8d277-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d277-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d277-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8d277-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8d277-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d277-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d277-123">See also</span></span>



[<span data-ttu-id="8d277-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d277-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d277-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8d277-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d277-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8d277-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d277-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8d277-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

