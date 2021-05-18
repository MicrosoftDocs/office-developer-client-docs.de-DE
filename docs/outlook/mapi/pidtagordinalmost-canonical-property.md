---
title: PidTagOrdinalMost (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329187"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="bd222-103">PidTagOrdinalMost (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd222-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="bd222-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd222-105">Enthält eine positive Zahl, deren negativer Wert kleiner oder gleich dem Wert der **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md))-Eigenschaft aller Vorgänge im Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="bd222-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd222-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd222-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd222-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="bd222-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="bd222-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bd222-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd222-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="bd222-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="bd222-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd222-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd222-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bd222-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bd222-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd222-112">Area:</span></span>  <br/> |<span data-ttu-id="bd222-113">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bd222-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd222-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd222-114">Remarks</span></span>

<span data-ttu-id="bd222-115">Diese Eigenschaft muss aktualisiert werden, um diese Bedingung zu erhalten, wenn sich die **dispidTaskOrdinal-Eigenschaft** eines Aufgabenobjekts im Ordner so ändert, dass die Bedingung verletzt würde.</span><span class="sxs-lookup"><span data-stu-id="bd222-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bd222-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd222-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd222-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd222-117">Protocol specifications</span></span>

<span data-ttu-id="bd222-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd222-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd222-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bd222-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd222-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd222-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd222-121">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bd222-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="bd222-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bd222-122">Header files</span></span>

<span data-ttu-id="bd222-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd222-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd222-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bd222-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd222-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd222-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bd222-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bd222-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd222-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd222-127">See also</span></span>



[<span data-ttu-id="bd222-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd222-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd222-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bd222-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd222-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd222-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd222-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd222-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

