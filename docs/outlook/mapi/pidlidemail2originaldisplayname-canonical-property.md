---
title: Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2b3f59633fcea0b895cd024dbbbc106c8d492bf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793504"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="c637f-103">Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c637f-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="c637f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c637f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c637f-105">Gibt den zweiten Anzeigenamen, der die die e-Mail-Adresse für den Kontakt entspricht.</span><span class="sxs-lookup"><span data-stu-id="c637f-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c637f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c637f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c637f-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="c637f-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="c637f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c637f-108">Property set:</span></span>  <br/> |<span data-ttu-id="c637f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c637f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c637f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="c637f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c637f-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="c637f-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="c637f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c637f-112">Data type:</span></span>  <br/> |<span data-ttu-id="c637f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c637f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c637f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c637f-114">Area:</span></span>  <br/> |<span data-ttu-id="c637f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c637f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c637f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c637f-116">Remarks</span></span>

<span data-ttu-id="c637f-117">Wenn der Wert der Eigenschaft **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) "SMTP" ist, sollte der Wert der jeweiligen **PidLidEmail2OriginalDisplayName** -Eigenschaft den Wert der jeweiligen **entsprechen. dispidEmail2EmailAddress** -Eigenschaft ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c637f-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="c637f-118">Der Zweck dieser Eigenschaft wird eine alternative benutzerfreundliche Adresse angezeigt, die in der **dispidEmail2EmailAddress**entspricht.</span><span class="sxs-lookup"><span data-stu-id="c637f-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c637f-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c637f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c637f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c637f-120">Protocol specifications</span></span>

<span data-ttu-id="c637f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c637f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c637f-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c637f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c637f-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c637f-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c637f-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c637f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c637f-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c637f-125">Header files</span></span>

<span data-ttu-id="c637f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c637f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c637f-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c637f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c637f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c637f-128">See also</span></span>



[<span data-ttu-id="c637f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c637f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c637f-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c637f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c637f-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c637f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c637f-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c637f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
