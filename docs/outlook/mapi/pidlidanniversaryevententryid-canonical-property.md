---
title: PidLidAnniversaryEventEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335574"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="fef7f-103">PidLidAnniversaryEventEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fef7f-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fef7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fef7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fef7f-105">Gibt die Eintrags-ID des Termins an, der den Jahrestag des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="fef7f-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fef7f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fef7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fef7f-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="fef7f-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="fef7f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="fef7f-108">Property set:</span></span>  <br/> |<span data-ttu-id="fef7f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="fef7f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="fef7f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fef7f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fef7f-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="fef7f-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="fef7f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fef7f-112">Data type:</span></span>  <br/> |<span data-ttu-id="fef7f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fef7f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fef7f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fef7f-114">Area:</span></span>  <br/> |<span data-ttu-id="fef7f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="fef7f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fef7f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fef7f-116">Remarks</span></span>

<span data-ttu-id="fef7f-117">Der von der **dispidAnniversaryEventEID-Eigenschaft** angegebene Termin muss mit diesem Kontakt mithilfe der **Eigenschaften dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) und **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) verknüpft werden, wie in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)detailliert.</span><span class="sxs-lookup"><span data-stu-id="fef7f-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fef7f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fef7f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fef7f-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fef7f-119">Protocol specifications</span></span>

<span data-ttu-id="fef7f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fef7f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fef7f-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fef7f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fef7f-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fef7f-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fef7f-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fef7f-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fef7f-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="fef7f-124">Header files</span></span>

<span data-ttu-id="fef7f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fef7f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fef7f-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fef7f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fef7f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fef7f-127">See also</span></span>



[<span data-ttu-id="fef7f-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fef7f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fef7f-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="fef7f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fef7f-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fef7f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fef7f-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fef7f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

