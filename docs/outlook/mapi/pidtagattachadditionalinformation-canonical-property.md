---
title: PidTagAttachAdditionalInformation (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339872"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="aa890-103">PidTagAttachAdditionalInformation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aa890-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="aa890-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa890-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa890-105">Stellt Dateitypinformationen für eine Nicht-Windows-Anlage zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aa890-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa890-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aa890-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa890-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="aa890-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="aa890-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aa890-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa890-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="aa890-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="aa890-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aa890-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa890-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aa890-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aa890-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aa890-112">Area:</span></span>  <br/> |<span data-ttu-id="aa890-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="aa890-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa890-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa890-114">Remarks</span></span>

<span data-ttu-id="aa890-115">Diese Eigenschaft stellt Metadaten zu einer bestimmten Anlage basierend auf der Codierung der Anlage bereit.</span><span class="sxs-lookup"><span data-stu-id="aa890-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="aa890-116">Wenn beispielsweise die **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))-Eigenschaft MacBinary enthält, enthält **PR_ATTACH_ADDITIONAL_INFO** eine Zeichenfolge, die den #A0 und -Dateityp darstellt, formatiert als ":CREA:TYPE" für die codierte Macintosh-Datei.</span><span class="sxs-lookup"><span data-stu-id="aa890-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aa890-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa890-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa890-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aa890-118">Protocol specifications</span></span>

<span data-ttu-id="aa890-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa890-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa890-120">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="aa890-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa890-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="aa890-121">Header files</span></span>

<span data-ttu-id="aa890-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa890-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa890-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aa890-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa890-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa890-124">Mapitags.h</span></span>
  
> <span data-ttu-id="aa890-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="aa890-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa890-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa890-126">See also</span></span>



[<span data-ttu-id="aa890-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa890-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa890-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="aa890-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa890-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aa890-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa890-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aa890-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

