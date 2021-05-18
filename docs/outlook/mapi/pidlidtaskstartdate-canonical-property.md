---
title: PidLidTaskStartDate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316681"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="d388f-103">PidLidTaskStartDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d388f-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="d388f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d388f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d388f-105">Das Datum, an dem der Benutzer mit dem Vorgang beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="d388f-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d388f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d388f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d388f-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="d388f-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="d388f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="d388f-108">Property set:</span></span>  <br/> |<span data-ttu-id="d388f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d388f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d388f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d388f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d388f-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="d388f-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="d388f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d388f-112">Data type:</span></span>  <br/> |<span data-ttu-id="d388f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d388f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d388f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d388f-114">Area:</span></span>  <br/> |<span data-ttu-id="d388f-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d388f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d388f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d388f-116">Remarks</span></span>

<span data-ttu-id="d388f-117">Wenn dieser Eigenschaftswert nichtet bleibt, hat der Vorgang kein Startdatum.</span><span class="sxs-lookup"><span data-stu-id="d388f-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="d388f-118">Der Wert "0x5AE980E0" (1.525.252.320) bedeutet auch, dass der Vorgang kein Startdatum hat.</span><span class="sxs-lookup"><span data-stu-id="d388f-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="d388f-119">Wenn der Vorgang ein Startdatum hat, muss der Wert eine Zeitkomponente von Mitternacht aufweisen, und die **Eigenschaften dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) und **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) müssen ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d388f-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="d388f-120">Diese Eigenschaft wird von der Informational Flagging Protocol Specification und Task-Related Object Protocol Specification in [[MS-OXOTASK] gemeinsam verwendet.](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d388f-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d388f-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d388f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d388f-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d388f-122">Protocol specifications</span></span>

<span data-ttu-id="d388f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d388f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d388f-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d388f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d388f-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d388f-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d388f-126">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d388f-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d388f-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d388f-127">Header files</span></span>

<span data-ttu-id="d388f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d388f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d388f-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d388f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d388f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d388f-130">See also</span></span>



[<span data-ttu-id="d388f-131">Kanonische PidLidTaskDueDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d388f-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="d388f-132">Kanonische PidLidCommonStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d388f-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="d388f-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d388f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d388f-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d388f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d388f-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d388f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d388f-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d388f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

