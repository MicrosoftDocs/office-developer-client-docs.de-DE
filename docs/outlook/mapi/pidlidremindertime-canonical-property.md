---
title: Kanonische PidLidReminderTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e74dbb1f8e0e64feb2c86eb04e146e201089a4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793761"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="736d7-103">Kanonische PidLidReminderTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="736d7-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="736d7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="736d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="736d7-105">Gibt die anfängliche Signal Zeit für eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="736d7-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="736d7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="736d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="736d7-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="736d7-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="736d7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="736d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="736d7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="736d7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="736d7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="736d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="736d7-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="736d7-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="736d7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="736d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="736d7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="736d7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="736d7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="736d7-114">Area:</span></span>  <br/> |<span data-ttu-id="736d7-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="736d7-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="736d7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="736d7-116">Remarks</span></span>

<span data-ttu-id="736d7-117">Für Calendar-Objekten stellt diese Eigenschaft der Zeit, wenn der Benutzer spät werden, also die Anfangszeit des Termins.</span><span class="sxs-lookup"><span data-stu-id="736d7-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="736d7-118">Clients müssen der Wert in koordinierter Weltzeit (UTC) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="736d7-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="736d7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="736d7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="736d7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="736d7-120">Protocol specifications</span></span>

<span data-ttu-id="736d7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="736d7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="736d7-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="736d7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="736d7-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="736d7-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="736d7-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="736d7-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="736d7-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="736d7-125">Header files</span></span>

<span data-ttu-id="736d7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="736d7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="736d7-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="736d7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="736d7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="736d7-128">See also</span></span>



[<span data-ttu-id="736d7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="736d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="736d7-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="736d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="736d7-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="736d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="736d7-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="736d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
