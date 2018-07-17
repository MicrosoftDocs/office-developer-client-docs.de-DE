---
title: Kanonische PidLidTaskMode-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f8eef7863cec565403d41dae26687b75f078e0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793856"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="7db6c-103">Kanonische PidLidTaskMode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7db6c-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="7db6c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7db6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7db6c-105">Gibt den Zuordnungsstatus des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7db6c-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7db6c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7db6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7db6c-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="7db6c-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="7db6c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7db6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="7db6c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7db6c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7db6c-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7db6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7db6c-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="7db6c-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="7db6c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7db6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="7db6c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7db6c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7db6c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7db6c-114">Area:</span></span>  <br/> |<span data-ttu-id="7db6c-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7db6c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7db6c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7db6c-116">Remarks</span></span>

<span data-ttu-id="7db6c-117">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="7db6c-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="7db6c-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7db6c-118">**Value**</span></span>|<span data-ttu-id="7db6c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7db6c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7db6c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db6c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="7db6c-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7db6c-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="7db6c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7db6c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="7db6c-123">Die Aufgabe ist in eine Aufgabenanfrage eingebettet.</span><span class="sxs-lookup"><span data-stu-id="7db6c-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="7db6c-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7db6c-124">0x00000002</span></span>  <br/> |<span data-ttu-id="7db6c-125">Die Aufgabe wurde vom Beauftragte für die Aufgabe angenommen.</span><span class="sxs-lookup"><span data-stu-id="7db6c-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="7db6c-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="7db6c-126">0x00000003</span></span>  <br/> |<span data-ttu-id="7db6c-127">Die Aufgabe wurde vom Beauftragte für die Aufgabe abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="7db6c-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="7db6c-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="7db6c-128">0x00000004</span></span>  <br/> |<span data-ttu-id="7db6c-129">Die Aufgabe ist in einem Update Aufgabe eingebettet.</span><span class="sxs-lookup"><span data-stu-id="7db6c-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="7db6c-130">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="7db6c-130">0x00000005</span></span>  <br/> |<span data-ttu-id="7db6c-131">Die Aufgabe wurde die Aufgabe delegierende Person zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7db6c-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7db6c-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7db6c-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7db6c-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7db6c-133">Protocol specifications</span></span>

<span data-ttu-id="7db6c-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7db6c-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7db6c-135">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7db6c-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7db6c-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7db6c-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7db6c-137">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="7db6c-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7db6c-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7db6c-138">Header files</span></span>

<span data-ttu-id="7db6c-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7db6c-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="7db6c-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7db6c-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7db6c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7db6c-141">See also</span></span>



[<span data-ttu-id="7db6c-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7db6c-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7db6c-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7db6c-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7db6c-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7db6c-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7db6c-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7db6c-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
