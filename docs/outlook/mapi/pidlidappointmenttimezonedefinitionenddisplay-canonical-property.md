---
title: Kanonische PidLidAppointmentTimeZoneDefinitionEndDisplay-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 119cd7edc5b9b615a39cea6aa1c405c396ce2afa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793436"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="3a469-103">Kanonische PidLidAppointmentTimeZoneDefinitionEndDisplay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a469-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="3a469-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a469-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a469-105">Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn das Ende einer Einzelinstanz-Termin oder eine Besprechungsanfrage ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3a469-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a469-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3a469-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a469-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="3a469-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="3a469-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3a469-108">Property set:</span></span>  <br/> |<span data-ttu-id="3a469-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3a469-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3a469-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="3a469-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3a469-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="3a469-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="3a469-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3a469-112">Data type:</span></span>  <br/> |<span data-ttu-id="3a469-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3a469-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3a469-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a469-114">Area:</span></span>  <br/> |<span data-ttu-id="3a469-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="3a469-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a469-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a469-116">Remarks</span></span>

<span data-ttu-id="3a469-117">Microsoft Office Outlook 2003 oder früher und Lösungen, basieren auf Collaboration Data Objects (CDO) 1.2.1 und, die das Calendar Update-Tool nicht für Microsoft Outlook und Microsoft Exchange Server ausgeführt haben, Speichern der Start- und Endzeit der Einzel-Instanz Termine und Besprechungsanfragen in koordinierter Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="3a469-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3a469-118">Diese Clients speichern keine Informationen für die Zeitzone, in dem die Termin- oder Besprechungsanfragen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a469-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="3a469-119">Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und CDO 1.2.1-basierter Lösungen, die im Kalender von Outlook oder Exchange Server ausgeführt haben aktualisieren Tool verwenden **DispidApptTZDefEndDisplay** , um die Zeitzone für die Endzeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3a469-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="3a469-120">**DispidApptTZDefEndDisplay** zeigt Termin oder eine Besprechung in der ursprünglichen Zeitzone, die es geplant wurde, und legt fest, ob die Endzeit angepasst werden sollten, wenn die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="3a469-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="3a469-121">Wenn diese Eigenschaft nicht vorhanden ist, wird der Zeitzone angegeben, die von der **DispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md))-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a469-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="3a469-122">Wenn **DispidApptTZDefStartDisplay** fehlt oder ist ungültig ist, wird davon ausgegangen, dass die aktuellen Ortszeitzone.</span><span class="sxs-lookup"><span data-stu-id="3a469-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="3a469-123">**DispidApptTZDefEndDisplay** wird nur für die Anzeige verwendet und ist nicht in Serie Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a469-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="3a469-124">Ein Parser wird beim Lesen eines Streams von **DispidApptTZDefEndDisplay**abgerufen, oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefEndDisplay**Engagement **TZDEFINITION** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3a469-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="3a469-125">Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a469-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="3a469-126">**DispidApptTZDefEndDisplay** gibt die Informationen zur Zeitzone für die Eigenschaft **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a469-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="3a469-127">Das Format, Einschränkungen und Berechnung von **DispidApptTZDefEndDisplay** sind identisch mit der in der **DispidApptTZDefStartDisplay** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="3a469-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3a469-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3a469-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a469-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3a469-129">Protocol specifications</span></span>

<span data-ttu-id="3a469-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a469-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a469-131">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a469-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a469-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a469-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a469-133">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="3a469-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a469-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3a469-134">Header files</span></span>

<span data-ttu-id="3a469-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a469-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a469-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3a469-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a469-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a469-137">See also</span></span>



[<span data-ttu-id="3a469-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a469-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a469-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a469-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a469-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3a469-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a469-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3a469-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
