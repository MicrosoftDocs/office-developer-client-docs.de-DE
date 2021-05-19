---
title: PidLidAppointmentReplyTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ba79498569c544d1b0ee22e968477d5b68812c09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331787"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="17589-103">PidLidAppointmentReplyTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="17589-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="17589-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17589-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17589-105">Gibt das Datum und die Uhrzeit an, zu der der Teilnehmer auf eine empfangene Besprechungsanfrage oder Besprechungsaktualisierung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="17589-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17589-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="17589-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17589-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="17589-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="17589-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="17589-108">Property set:</span></span>  <br/> |<span data-ttu-id="17589-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="17589-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="17589-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="17589-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="17589-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="17589-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="17589-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="17589-112">Data type:</span></span>  <br/> |<span data-ttu-id="17589-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="17589-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="17589-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="17589-114">Area:</span></span>  <br/> |<span data-ttu-id="17589-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="17589-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17589-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17589-116">Remarks</span></span>

<span data-ttu-id="17589-117">Der Wert muss in koordinierter Weltzeit (Coordinated Universal Time, UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17589-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17589-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17589-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17589-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="17589-119">Protocol specifications</span></span>

<span data-ttu-id="17589-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17589-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17589-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="17589-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17589-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17589-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17589-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="17589-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17589-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="17589-124">Header files</span></span>

<span data-ttu-id="17589-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17589-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="17589-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="17589-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17589-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17589-127">See also</span></span>



[<span data-ttu-id="17589-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17589-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17589-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="17589-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17589-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="17589-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17589-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="17589-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

