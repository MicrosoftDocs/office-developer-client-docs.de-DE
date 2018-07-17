---
title: Kanonische PidTagSearchAttachments-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795107"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="a22e2-103">Kanonische PidTagSearchAttachments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a22e2-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="a22e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a22e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a22e2-105">Enthält eine Unicodezeichenfolge, die im Anlageninhalt für den Speicher abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a22e2-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="a22e2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a22e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a22e2-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="a22e2-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="a22e2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a22e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a22e2-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="a22e2-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="a22e2-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="a22e2-110">Property type:</span></span>  <br/> |<span data-ttu-id="a22e2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a22e2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a22e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a22e2-112">Area:</span></span>  <br/> |<span data-ttu-id="a22e2-113">Suchen</span><span class="sxs-lookup"><span data-stu-id="a22e2-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a22e2-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a22e2-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="a22e2-115">Diese MAPI-Einschränkung Tag verwendet bei der Suche für Anlageninhalt, möglicherweise nicht in der Headerdatei zum Herunterladen definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="a22e2-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="a22e2-116">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="a22e2-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="a22e2-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a22e2-117">Protocol specifications</span></span>

<span data-ttu-id="a22e2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a22e2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a22e2-119">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="a22e2-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a22e2-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a22e2-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a22e2-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="a22e2-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a22e2-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a22e2-122">Header files</span></span>

<span data-ttu-id="a22e2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a22e2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a22e2-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a22e2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a22e2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a22e2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a22e2-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a22e2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a22e2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22e2-127">See also</span></span>



[<span data-ttu-id="a22e2-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a22e2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a22e2-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a22e2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a22e2-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a22e2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a22e2-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a22e2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
