---
title: PidLidContacts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319460"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="bd8ec-103">PidLidContacts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd8ec-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="bd8ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd8ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd8ec-105">Enthält die Namen der Kontakte, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd8ec-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd8ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd8ec-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="bd8ec-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="bd8ec-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="bd8ec-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd8ec-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bd8ec-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bd8ec-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bd8ec-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd8ec-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="bd8ec-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="bd8ec-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd8ec-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd8ec-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd8ec-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bd8ec-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd8ec-114">Area:</span></span>  <br/> |<span data-ttu-id="bd8ec-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="bd8ec-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd8ec-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd8ec-116">Remarks</span></span>

<span data-ttu-id="bd8ec-117">Diese Eigenschaft enthält die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft jeder Adressbucheintrags-ID, auf die im Wert der **eigenschaft dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) verwiesen wird. </span><span class="sxs-lookup"><span data-stu-id="bd8ec-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="bd8ec-118">Sie kann Namen enthalten, auf die in **dispidContactLinkEntry nicht verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="bd8ec-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd8ec-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd8ec-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd8ec-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd8ec-120">Protocol specifications</span></span>

<span data-ttu-id="bd8ec-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd8ec-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd8ec-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd8ec-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd8ec-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd8ec-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bd8ec-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd8ec-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd8ec-126">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="bd8ec-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd8ec-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd8ec-128">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd8ec-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bd8ec-129">Header files</span></span>

<span data-ttu-id="bd8ec-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd8ec-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd8ec-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bd8ec-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd8ec-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd8ec-132">See also</span></span>



[<span data-ttu-id="bd8ec-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd8ec-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd8ec-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bd8ec-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd8ec-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd8ec-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd8ec-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd8ec-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

