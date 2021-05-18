---
title: PidTagAttachMimeTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327244"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="e3a52-103">PidTagAttachMimeTag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e3a52-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="e3a52-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3a52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3a52-105">Enthält Formatierungsinformationen zu einer Multipurpose Internet Mail Extensions (MIME)-Anlage.</span><span class="sxs-lookup"><span data-stu-id="e3a52-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3a52-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e3a52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3a52-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="e3a52-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="e3a52-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e3a52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3a52-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="e3a52-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="e3a52-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e3a52-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3a52-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e3a52-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e3a52-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e3a52-112">Area:</span></span>  <br/> |<span data-ttu-id="e3a52-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="e3a52-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3a52-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3a52-114">Remarks</span></span>

<span data-ttu-id="e3a52-115">Wenn die **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) den Wert **OID_MIMETAG** enthält, sollte der Transportanbieter diese Eigenschaften überprüfen, um zu bestimmen, wie die Anlage formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="e3a52-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="e3a52-116">Diese Eigenschaften werden aus dem Parameter Content-type des eingehenden MIME-Headers kopiert.</span><span class="sxs-lookup"><span data-stu-id="e3a52-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="e3a52-117">Die Zusammensetzung der Zeichenfolge wird im RFC 1521-Dokument definiert.</span><span class="sxs-lookup"><span data-stu-id="e3a52-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="e3a52-118">Das Format ist Typ/Untertyp, z. B. Application/Binary oder Text/Plain.</span><span class="sxs-lookup"><span data-stu-id="e3a52-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3a52-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3a52-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3a52-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e3a52-120">Protocol specifications</span></span>

<span data-ttu-id="e3a52-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3a52-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3a52-122">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e3a52-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e3a52-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3a52-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3a52-124">Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="e3a52-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3a52-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e3a52-125">Header files</span></span>

<span data-ttu-id="e3a52-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3a52-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3a52-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e3a52-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3a52-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3a52-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e3a52-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e3a52-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3a52-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3a52-130">See also</span></span>



[<span data-ttu-id="e3a52-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3a52-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3a52-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e3a52-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3a52-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e3a52-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3a52-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e3a52-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

