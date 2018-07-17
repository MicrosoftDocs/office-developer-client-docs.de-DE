---
title: Kanonische PidLidTaskDateCompleted-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9737b5f940f95c88c2d3c5c6e98fc885daf64219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793798"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="11833-103">Kanonische PidLidTaskDateCompleted-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="11833-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="11833-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11833-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11833-105">Gibt das Datum an, wenn der Benutzer die Aufgabe abschließt.</span><span class="sxs-lookup"><span data-stu-id="11833-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11833-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="11833-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11833-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="11833-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="11833-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="11833-108">Property set:</span></span>  <br/> |<span data-ttu-id="11833-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="11833-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="11833-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="11833-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="11833-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="11833-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="11833-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="11833-112">Data type:</span></span>  <br/> |<span data-ttu-id="11833-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="11833-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="11833-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="11833-114">Area:</span></span>  <br/> |<span data-ttu-id="11833-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="11833-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11833-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11833-116">Remarks</span></span>

<span data-ttu-id="11833-117">Wenn festgelegt, diese Eigenschaft Zeitkomponente Mitternacht in der lokalen Zeitzone vorhanden sein muss (Coordinated Universal Time, UTC) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="11833-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11833-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11833-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11833-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="11833-119">Protocol specifications</span></span>

<span data-ttu-id="11833-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11833-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11833-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="11833-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11833-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11833-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11833-123">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="11833-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="11833-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="11833-124">Header files</span></span>

<span data-ttu-id="11833-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11833-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="11833-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="11833-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11833-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11833-127">See also</span></span>



[<span data-ttu-id="11833-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11833-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11833-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11833-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11833-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="11833-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11833-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="11833-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
