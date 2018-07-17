---
title: Kanonische PidLidBirthdayEventEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4a8cf9ac24f275d8b9cdbe03b5a90477771a2ab4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793454"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="cd0b2-103">Kanonische PidLidBirthdayEventEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd0b2-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cd0b2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd0b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd0b2-105">Gibt die **EntryId** des Termins optional, die das Geburtsdatum des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd0b2-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd0b2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cd0b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd0b2-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="cd0b2-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="cd0b2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cd0b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="cd0b2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cd0b2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cd0b2-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="cd0b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cd0b2-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="cd0b2-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="cd0b2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cd0b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="cd0b2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cd0b2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cd0b2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cd0b2-114">Area:</span></span>  <br/> |<span data-ttu-id="cd0b2-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="cd0b2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd0b2-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd0b2-116">Remarks</span></span>

<span data-ttu-id="cd0b2-117">Des Termins werden dies von dieser Eigenschaft angegeben wird muss mit diesem Kontakt verknüpft werden, mithilfe der **DispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **DispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) und ** DispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) Eigenschaften, die im angegebenen [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cd0b2-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd0b2-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd0b2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd0b2-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cd0b2-119">Protocol specifications</span></span>

<span data-ttu-id="cd0b2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd0b2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd0b2-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cd0b2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd0b2-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd0b2-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd0b2-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cd0b2-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd0b2-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cd0b2-124">Header files</span></span>

<span data-ttu-id="cd0b2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd0b2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd0b2-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cd0b2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd0b2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd0b2-127">See also</span></span>



[<span data-ttu-id="cd0b2-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd0b2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd0b2-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd0b2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd0b2-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cd0b2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd0b2-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cd0b2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
