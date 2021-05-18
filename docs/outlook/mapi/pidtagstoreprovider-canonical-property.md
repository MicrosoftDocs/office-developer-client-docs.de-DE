---
title: PidTagStoreProvider (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412051"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="7f7bc-103">PidTagStoreProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7f7bc-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="7f7bc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f7bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f7bc-105">Enthält eine vom Anbieter definierte [MAPIUID-Struktur,](mapiuid.md) die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7bc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7f7bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f7bc-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="7f7bc-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="7f7bc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7f7bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f7bc-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="7f7bc-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="7f7bc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7f7bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f7bc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f7bc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f7bc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7f7bc-112">Area:</span></span>  <br/> |<span data-ttu-id="7f7bc-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f7bc-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f7bc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f7bc-114">Remarks</span></span>

<span data-ttu-id="7f7bc-115">Die [MAPIUID-Struktur](mapiuid.md) identifiziert den Typ des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="7f7bc-116">Der Wert wird von Nachrichtenspeicheranbietern für Nachrichtenspeicherobjekte berechnet und ist für jeden Anbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="7f7bc-117">Es wird in der Regel zum Durchsuchen der Tabelle des Nachrichtenspeichers verwendet, um einen Speicher des gewünschten Typs zu finden, z. B. öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="7f7bc-118">Diese Eigenschaft entspricht der PR_AB_PROVIDER_ID **(** [PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) -Eigenschaft für Adressbücher.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f7bc-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f7bc-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f7bc-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7f7bc-120">Header files</span></span>

<span data-ttu-id="7f7bc-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f7bc-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f7bc-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f7bc-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f7bc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7f7bc-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7f7bc-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f7bc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f7bc-125">See also</span></span>



[<span data-ttu-id="7f7bc-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f7bc-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f7bc-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7bc-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f7bc-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7f7bc-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f7bc-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7f7bc-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

