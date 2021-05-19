---
title: PidTagOriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355608"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="9f401-103">PidTagOriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9f401-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9f401-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f401-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f401-105">Enthält den ursprünglichen Anzeigenamen für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f401-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f401-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9f401-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f401-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9f401-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9f401-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9f401-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f401-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="9f401-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="9f401-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9f401-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f401-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f401-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9f401-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9f401-112">Area:</span></span>  <br/> |<span data-ttu-id="9f401-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="9f401-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f401-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f401-114">Remarks</span></span>

<span data-ttu-id="9f401-115">Diese Eigenschaften enthalten Informationen zur ursprünglichen Quelle eines kopierten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="9f401-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="9f401-116">Für einen nicht gelesenen Bericht enthalten diese Eigenschaften eine Kopie des Anzeigenamens des ursprünglichen Nachrichtenempfängers, für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9f401-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="9f401-117">Wenn der ursprüngliche Empfänger Teil einer Verteilerliste ist, wird der Anzeigename der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9f401-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="9f401-118">Eine Clientanwendung kann diese Eigenschaften verwenden, um Änderungen oder "Spoofing" von Einträgen zu verhindern, indem eine unveränderte Kopie des Anzeigenamens zum Vergleich zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="9f401-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f401-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9f401-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f401-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9f401-120">Protocol specifications</span></span>

<span data-ttu-id="9f401-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f401-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f401-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9f401-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f401-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f401-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f401-124">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="9f401-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f401-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9f401-125">Header files</span></span>

<span data-ttu-id="9f401-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f401-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f401-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9f401-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f401-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f401-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9f401-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9f401-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f401-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f401-130">See also</span></span>



[<span data-ttu-id="9f401-131">PidTagTransmittableDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9f401-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="9f401-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f401-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f401-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9f401-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f401-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9f401-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f401-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9f401-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

