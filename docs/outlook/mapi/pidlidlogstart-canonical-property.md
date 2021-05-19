---
title: PidLidLogStart (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337016"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="3613d-103">PidLidLogStart (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3613d-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="3613d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3613d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3613d-105">Represents the start date and time for the journal message.</span><span class="sxs-lookup"><span data-stu-id="3613d-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3613d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3613d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3613d-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="3613d-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="3613d-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="3613d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3613d-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="3613d-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="3613d-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3613d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3613d-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="3613d-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="3613d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3613d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3613d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3613d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3613d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3613d-114">Area:</span></span>  <br/> |<span data-ttu-id="3613d-115">Journal</span><span class="sxs-lookup"><span data-stu-id="3613d-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3613d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3613d-116">Remarks</span></span>

<span data-ttu-id="3613d-117">Die Zeit in koordinierter Weltzeit (Coordinated Universal Time, UTC), zu der die Aktivität gestartet wurde, muss gleich der **eigenschaft dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="3613d-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3613d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3613d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3613d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3613d-119">Protocol specifications</span></span>

<span data-ttu-id="3613d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3613d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3613d-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3613d-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3613d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3613d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3613d-123">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3613d-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3613d-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="3613d-124">Header files</span></span>

<span data-ttu-id="3613d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3613d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3613d-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3613d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3613d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3613d-127">See also</span></span>



[<span data-ttu-id="3613d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3613d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3613d-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="3613d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3613d-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3613d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3613d-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3613d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

