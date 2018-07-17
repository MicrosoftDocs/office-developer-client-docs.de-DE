---
title: Kanonische PidLidBusyStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793456"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="ab2cc-103">Kanonische PidLidBusyStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ab2cc-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ab2cc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab2cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab2cc-105">Die Verfügbarkeit des Benutzers für einen Termin darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab2cc-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab2cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab2cc-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="ab2cc-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="ab2cc-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ab2cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="ab2cc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ab2cc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ab2cc-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="ab2cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ab2cc-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="ab2cc-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="ab2cc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab2cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="ab2cc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab2cc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab2cc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab2cc-114">Area:</span></span>  <br/> |<span data-ttu-id="ab2cc-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="ab2cc-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab2cc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab2cc-116">Remarks</span></span>

<span data-ttu-id="ab2cc-117">Diese Eigenschaft gibt die Verfügbarkeit eines Benutzers für das Ereignis, das durch das Objekt beschrieben und muss einer der unten angegebenen Werte.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="ab2cc-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ab2cc-118">**Value**</span></span>|<span data-ttu-id="ab2cc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab2cc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab2cc-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab2cc-120">0x00000000</span></span>  <br/> |<span data-ttu-id="ab2cc-121">Der Benutzer ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="ab2cc-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ab2cc-122">0x00000001</span></span>  <br/> |<span data-ttu-id="ab2cc-123">Der Benutzer hat ein mit Vorbehalt Ereignis geplant.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="ab2cc-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ab2cc-124">0x00000002</span></span>  <br/> |<span data-ttu-id="ab2cc-125">Der Benutzer ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="ab2cc-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="ab2cc-126">0x00000003</span></span>  <br/> |<span data-ttu-id="ab2cc-127">Der Benutzer befindet sich nicht im Büro.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ab2cc-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab2cc-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab2cc-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab2cc-129">Protocol specifications</span></span>

<span data-ttu-id="ab2cc-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab2cc-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab2cc-131">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab2cc-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab2cc-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab2cc-133">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab2cc-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab2cc-134">Header files</span></span>

<span data-ttu-id="ab2cc-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab2cc-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab2cc-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab2cc-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab2cc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab2cc-137">See also</span></span>



[<span data-ttu-id="ab2cc-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab2cc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab2cc-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab2cc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab2cc-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab2cc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab2cc-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab2cc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
